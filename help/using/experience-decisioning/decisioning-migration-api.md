---
title: 의사 결정 마이그레이션 API
description: Decisioning Migration Service API를 사용하여 자동화된 종속성 해결 및 롤백 지원을 통해 샌드박스 간에 의사 결정 관리 개체를 마이그레이션하는 방법에 대해 알아봅니다.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 3%

---

# 의사 결정 마이그레이션 API {#decisioning-migration-api}

Decisioning 마이그레이션 서비스 API를 사용하면 의사 결정 관리 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션할 수 있습니다. 마이그레이션 프로세스는 종속성 분석, 실행 및 선택적 롤백 기능을 포함하는 비동기 워크플로우로 실행됩니다.

이 API를 사용하면 데이터 무결성과 관계를 유지하면서 <!--(e.g., from development to staging, or staging to production) --> 환경 간에 의사 결정 콘텐츠를 원활하게 전환할 수 있습니다.

의사 결정 관리와 비교하여 Decisioning의 장점과 기능에 대해 알아보려면 [이 페이지](migrate-to-decisioning.md)를 참조하세요.

## 기능 {#capabilities}

Decisioning 마이그레이션 서비스 API는 다음 기능을 제공합니다.

* **종속성 분석** - 특성, 세그먼트, 데이터 세트 요구 사항을 포함하여 원본 샌드박스와 대상 샌드박스 간에 필요한 모든 종속성을 식별합니다.
* **유연한 마이그레이션 범위** - 필요에 따라 샌드박스, 오퍼 또는 의사 결정 수준에서 마이그레이션을 실행합니다.
* **롤백 지원** - 유효성 검사 중에 문제가 발견된 경우 완료된 마이그레이션을 되돌립니다.

## 전제 조건 {#prerequisites}

### 필요한 권한 {#permissions}

마이그레이션 API를 사용하려면 소스 및 타겟 샌드박스 모두에서 적절한 권한이 필요합니다.

**Source 샌드박스** - 의사 결정 관리 개체에 대한 읽기 액세스 권한

**Target 샌드박스** - Decisioning 개체에 대한 액세스 만들기 및 편집

일반적인 권한은 다음과 같습니다.

* 의사 결정 관리 / 보기
* 의사 결정 관리/보기
* 오퍼 관리
* 순위 전략 관리
* 캠페인 관리(캠페인 관련 아티팩트를 마이그레이션하는 경우)
* 데이터스트림 관리/보기(데이터스트림을 생성하는 경우)
* 스키마 관리/보기

>[!NOTE]
>
>[이 섹션](gs-experience-decisioning.md#steps)에서 Decisioning 권한을 할당하는 방법을 알아봅니다. 전체 사용 권한 목록은 [기본 제공 사용 권한](../administration/ootb-permissions.md#ootb-permissions) 페이지를 참조하세요.

### Target 샌드박스 준비 {#target-sandbox-preparation}

Before running a migration, ensure your target sandbox is properly configured:

* **Attributes** - Verify that required profile attributes and context attributes exist in the target sandbox, or prepare mappings for them.
* **Segments** - Ensure required segments exist in the target sandbox, or plan to map them using namespace and ID.
* **Dataset** - Identify a dataset name to use for the migration (`dependency.datasetName`).
* **Datastream** - Decide whether the migration should create a datastream (`createDataStream`).

For more information about sandbox management, refer to [Use and assign sandboxes](../administration/sandboxes.md).

## API 기본 사항 {#api-basics}

### 기본 URL {#base-url}

Use the following base URL:

* **Production**: `https://decisioning-migration.adobe.io`
  <!--* **Staging**: `https://decisioning-migration-stage.adobe.io`-->

### 인증 {#authentication}

All API requests require the following headers:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

For detailed instructions on setting up authentication, refer to the [Journey Optimizer authentication guide](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

### Workflow model {#workflow-model}

Each API call creates or retrieves a workflow resource. Workflows are asynchronous operations that track the progress and results of migration tasks.

A workflow has the following properties:

* `id` - Unique workflow identifier (UUID)
* `status` - Current workflow status: `New`, `Running`, `Completed`, or `Failed`
* `result` - Workflow output when completed (includes migration results and warnings)
* `errors` - Structured error details when failed
* `_links.self` - Workflow URL for retrieving status
  <!--* `_etag` - Version identifier used for delete operations (service users only)-->

## Migration workflow {#migration-workflow}

The migration process consists of two main steps: analyzing dependencies and executing the migration. Follow these steps to ensure a successful migration.

### Step 1: Analyze dependencies {#analyze-dependencies}

Before migrating, use the dependency workflow to identify what needs to be mapped from Decision management to Decisioning in your target sandbox. This analysis helps you understand the relationships between objects and prepare the necessary mappings.

#### Create a dependency workflow {#create-dependency-workflow}

Use the following API call to create a dependency analysis workflow.

**API 형식**

```http
POST /workflows/generate-dependencies
```

**Sandbox-level dependency (recommended first)**

Start with a sandbox-level analysis to get a complete view of all dependencies:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Offer-level dependency**

To analyze dependencies for specific offers only, set `requestLevel: "offer"` and provide an `offersList` array with the offer IDs you want to analyze.

**Decision-level dependency**

To analyze dependencies for specific decisions only, set `requestLevel: "decision"` and provide a `decisionsList` array with the decision IDs you want to analyze.

#### Check dependency workflow status {#poll-dependency-status}

Poll the dependency workflow to check when the analysis is complete.

**API 형식**

```http
GET /workflows/generate-dependencies/{id}
```

**요청**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

When the `status` field shows `Completed`, the dependency analysis is ready. Use the workflow output to build your migration dependency mappings:

* **profileAttributes** - Maps source profile attributes to target profile attributes
* **contextAttributes** - Maps source context attributes to target context attributes
* **segments** - Maps source segment keys to target segment identifiers (`{namespace, id}`)
* **datasetName** - Specifies the target dataset name for the migration

### Step 2: Execute the migration {#execute-migration}

Once you have analyzed the dependencies and prepared your mappings, you can execute the migration.

#### Create a migration workflow {#create-migration-workflow}

Use the dependency mappings from Step 1 to configure and execute your migration.

**API 형식**

```http
POST /workflows/migration
```

**Sandbox-level migration**

모든 의사 결정 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션하려면 다음을 수행하십시오.

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/migration" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**오퍼 수준 마이그레이션**

특정 오퍼만 마이그레이션하려면 `requestLevel: "offer"`을(를) 사용하고 `offersList` 배열을 추가하십시오.

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**의사 결정 수준 마이그레이션**

특정 결정만 마이그레이션하려면 `requestLevel: "decision"`을(를) 사용하고 `decisionsList` 배열을 추가하십시오.

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### 마이그레이션 상태 모니터링 {#poll-migration-status}

마이그레이션 워크플로우를 폴링하여 진행 상황을 추적합니다.

**API 형식**

```http
GET /workflows/migration/{id}
```

**요청**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**마이그레이션 결과**

`status` 필드에 `Completed`이(가) 표시되면 마이그레이션이 성공한 것입니다. `result` 워크플로에는 다음이 포함됩니다.
* 마이그레이션된 개체의 매핑
* 마이그레이션 도중 발생한 모든 경고

`status` 필드에 `Failed`이(가) 표시되면 `errors[]` 배열 및 `result.error` 필드에서 무엇이 잘못되었는지 자세히 검토합니다.

## 마이그레이션 유효성 검사 {#validate-migration}

마이그레이션이 성공적으로 완료되면 모든 개체가 올바르게 마이그레이션되었는지 확인합니다.

### 유효성 검사 목록 {#validation-checklist}

1. **세그먼트** - 참조된 모든 세그먼트가 매핑에 따라 대상 샌드박스에서 올바르게 확인되는지 확인합니다.
2. **특성** - 모든 프로필 특성 및 컨텍스트 특성이 대상 샌드박스에 있으며 올바르게 매핑되었는지 확인합니다.
3. **Decisioning 개체** - Journey Optimizer 사용자 인터페이스에서 마이그레이션된 개체를 검토합니다.
   * 오퍼(의사 결정 항목)
   * 자격 규칙
   * 순위 공식
   * 선택 전략
   * 의사 결정 정책
4. **데이터스트림 테스트** - 데이터스트림이 만들어진 경우 Edge Interact API를 사용하여 런타임 배달을 테스트합니다.

### 예 {#test-runtime-delivery}

마이그레이션이 데이터 스트림을 생성한 경우 다음 예를 사용하여 오퍼 게재를 테스트할 수 있습니다.

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## 마이그레이션 롤백 {#rollback}

유효성 검사 중에 문제가 발견되면 완료된 마이그레이션을 롤백하여 대상 샌드박스를 이전 상태로 복원할 수 있습니다.

### 롤백 워크플로우 만들기 {#create-rollback-workflow}

되돌릴 마이그레이션을 참조하는 롤백 워크플로우를 생성하여 롤백을 시작합니다.

**API 형식**

```http
POST /workflows/rollback
```

**요청**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

`<MIGRATION_WORKFLOW_ID>`을(를) 롤백하려는 마이그레이션 워크플로의 ID로 바꾸십시오.

### 롤백 상태 모니터링 {#poll-rollback-status}

롤백 워크플로우를 폴링하여 진행 상황을 추적합니다.

**API 형식**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**요청**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## 동시 작업 흐름 처리 {#handle-concurrency}

마이그레이션 API를 사용하면 조직당 한 번에 하나의 워크플로우만 실행할 수 있습니다. 다른 워크플로우가 진행 중일 때 새 워크플로우를 만들려고 하면 **409 충돌** 오류 응답을 받게 됩니다(&quot;워크플로우가 이미 진행 중입니다..&quot;).

이 경우 진행 중인 워크플로우가 완료될 때까지 기다리거나 워크플로우 ID를 검색하고 상태를 폴링합니다. 현재 워크플로우가 완료되면 새 워크플로우를 만들 수 있습니다.

## 엔티티 매핑 참조 {#entity-mapping}

Decision management에서 Decisioning으로 마이그레이션할 때 엔티티는 다음과 같이 매핑됩니다.

| 의사 결정 관리 | 결정 |
|-------------------|-------------|
| 오퍼 | 결정 항목 |
| 오퍼 컬렉션 | 항목 컬렉션 |
| 자격 규칙 | 자격 규칙 |
| 순위 공식 | 순위 공식 |
| 결정 | 선택 전략 + 결정 정책 |
| 캠페인 | 캠페인 *(기본 콘텐츠만)* |
| 배치 | 표면 + 채널 구성 |
| 태그 | 통합 태그 |
| 오퍼 속성 | 개인화된 오퍼 항목 스키마의 `migratedofferattributes` 필드 |
| 컨텍스트 속성 | 마이그레이션 중에 제공된 데이터 세트에 연결된 스키마의 `migratedcontextattributes` 필드 |

## 워크플로우 정리 {#cleanup}

<!--
Workflow resources can be deleted by service users only. Delete operations require an `If-Match` header with the workflow's `_etag` value.

**Available delete operations:**

* `DELETE /workflows/generate-dependencies/{id}`
* `DELETE /workflows/migration/{id}`
* `DELETE /workflows/rollback/{id}`
-->

워크플로우 삭제는 공개적으로 사용할 수 없습니다. 워크플로우 리소스를 삭제해야 하는 경우 시스템 관리자에게 문의하십시오.

## 관련 항목 {#related-topics}

* [의사 결정 관리에서 의사 결정으로 마이그레이션](migrate-to-decisioning.md) - 의사 결정 마이그레이션의 이점 및 기능 이해
* [의사 결정 시작](gs-experience-decisioning.md)
* [보호 및 제한 사항 결정](decisioning-guardrails.md)
* [API 결정하기 시작](api-reference/getting-started.md)
