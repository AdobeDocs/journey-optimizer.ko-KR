---
title: 의사 결정 마이그레이션 API
description: Decisioning Migration Service API를 사용하여 자동화된 종속성 해결 및 롤백 지원을 통해 샌드박스 간에 의사 결정 관리 개체를 마이그레이션하는 방법에 대해 알아봅니다.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 398d4c2ab3a2312a0af5b8ac835f7d1f49a61b5b
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 3%

---


# 의사 결정 마이그레이션 API {#decisioning-migration-api}

Decisioning 마이그레이션 서비스 API를 사용하면 의사 결정 관리 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션할 수 있습니다. 마이그레이션 프로세스는 종속성 분석, 실행 및 선택적 롤백 기능을 포함하는 비동기 워크플로우로 실행됩니다.

이 API를 사용하면 데이터 무결성과 관계를 유지하면서 환경 간(예: 개발에서 스테이징으로, 또는 스테이징에서 프로덕션으로) 의사 결정 콘텐츠를 원활하게 전환할 수 있습니다.

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

마이그레이션을 실행하기 전에 대상 샌드박스가 올바르게 구성되었는지 확인하십시오.

* **특성** - 필요한 프로필 특성과 컨텍스트 특성이 대상 샌드박스에 있는지 확인하거나 매핑을 준비합니다.
* **세그먼트** - 필요한 세그먼트가 대상 샌드박스에 있는지 확인하거나 네임스페이스와 ID를 사용하여 매핑할 계획입니다.
* **데이터 집합** - 마이그레이션에 사용할 데이터 집합 이름을 식별합니다(`dependency.datasetName`).
* **데이터스트림** - 마이그레이션에서 데이터스트림(`createDataStream`)을 만들지 여부를 결정합니다.

샌드박스 관리에 대한 자세한 내용은 [샌드박스 사용 및 할당](../administration/sandboxes.md)을 참조하세요.

## API 기본 사항 {#api-basics}

### 기본 URL {#base-urls}

환경에 따라 다음 기본 URL을 사용합니다.

* **프로덕션**: `https://platform.adobe.io`
* **스테이징**: `https://platform-stage.adobe.io`

### 인증 {#authentication}

모든 API 요청에는 다음 헤더가 필요합니다.

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

인증 설정에 대한 자세한 지침은 [Journey Optimizer 인증 안내서](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}를 참조하세요.

### 워크플로 모델 {#workflow-model}

각 API 호출은 워크플로우 리소스를 만들거나 검색합니다. 워크플로우는 마이그레이션 작업의 진행 상황과 결과를 추적하는 비동기 작업입니다.

워크플로에는 다음과 같은 속성이 있습니다.

* `id` - 고유한 워크플로우 식별자(UUID)
* `status` - 현재 워크플로 상태: `New`, `Running`, `Completed`, `Failed` 또는 `Cancelled`
* `result` - 완료 시 워크플로 출력(마이그레이션 결과 및 경고 포함)
* `errors` - 실패 시 구조적 오류 세부 정보
* `_etag` - 삭제 작업에 사용되는 버전 식별자(서비스 사용자만 해당)
* `_links.self` - 상태를 검색하기 위한 워크플로 URL

## 마이그레이션 워크플로 {#migration-workflow}

마이그레이션 프로세스는 종속성 분석과 마이그레이션 실행의 두 가지 주요 단계로 구성됩니다. 마이그레이션을 성공적으로 수행하려면 다음 단계를 따르십시오.

### 1단계: 종속성 분석 {#analyze-dependencies}

마이그레이션하기 전에 종속성 워크플로우를 사용하여 대상 샌드박스에서 의사 결정 관리에서 의사 결정에 매핑해야 하는 항목을 식별합니다. 이러한 분석은 객체 간의 관계를 이해하고 필요한 매핑을 준비하는 데 도움이 됩니다.

#### 종속성 워크플로우 만들기 {#create-dependency-workflow}

다음 API 호출을 사용하여 종속성 분석 워크플로우를 만듭니다.

**API 형식**

```http
POST /migration/service/dependency
```

**샌드박스 수준 종속성(먼저 권장됨)**

샌드박스 수준 분석으로 시작하여 모든 종속성에 대한 전체 보기를 확인합니다.

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**오퍼 수준 종속성**

특정 오퍼에 대한 종속성만 분석하려면 `requestLevel: "offer"`을(를) 설정하고 분석할 오퍼 ID가 있는 `offersList` 배열을 제공하십시오.

**의사 결정 수준 종속성**

특정 결정에 대해서만 종속성을 분석하려면 `requestLevel: "decision"`을(를) 설정하고 분석할 결정 ID가 있는 `decisionsList` 배열을 제공하십시오.

#### 종속성 워크플로 상태 확인 {#poll-dependency-status}

종속성 워크플로우를 폴링하여 분석이 완료되면 확인합니다.

**API 형식**

```http
GET /migration/service/dependency/{id}
```

**요청**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

`status` 필드에 `Completed`이(가) 표시되면 종속성 분석이 준비되었습니다. 워크플로우 출력을 사용하여 마이그레이션 종속성 매핑을 빌드합니다.

* **profileAttributeDependency** - 소스 프로필 특성을 대상 프로필 특성에 매핑합니다.
* **contextAttributeDependency** - 소스 컨텍스트 특성을 대상 컨텍스트 특성에 매핑합니다.
* **segmentsDependency** - 소스 세그먼트 키를 대상 세그먼트 식별자(`{segmentNamespace, segmentId}`)에 매핑합니다.
* **datasetName** - 마이그레이션의 대상 데이터 세트 이름을 지정합니다.

### 2단계: 마이그레이션 실행 {#execute-migration}

종속성을 분석하고 매핑을 준비하면 마이그레이션을 실행할 수 있습니다.

#### 마이그레이션 워크플로우 만들기 {#create-migration-workflow}

1단계의 종속성 매핑을 사용하여 마이그레이션을 구성하고 실행합니다.

**API 형식**

```http
POST /migration/service/migrations
```

**샌드박스 수준 마이그레이션**

모든 의사 결정 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션하려면 다음을 수행하십시오.

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
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
GET /migration/service/migrations/{id}
```

**요청**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
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
POST /migration/service/rollbacks/{migrationWorkflowId}
```

`{migrationWorkflowId}`을(를) 롤백하려는 마이그레이션 워크플로의 ID로 바꾸십시오.

**요청**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### 롤백 상태 모니터링 {#poll-rollback-status}

롤백 워크플로우를 폴링하여 진행 상황을 추적합니다.

**API 형식**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**요청**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
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
| Campaign | 캠페인 *(기본 콘텐츠만)* |
| 배치 | 표면 + 채널 구성 |
| 태그 | 통합 태그 |

## 워크플로우 정리 {#cleanup}

워크플로우 리소스는 서비스 사용자만 삭제할 수 있습니다. 삭제 작업에는 워크플로우의 `If-Match` 값이 있는 `_etag` 헤더가 필요합니다.

**사용 가능한 삭제 작업:**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>워크플로우 삭제는 적절한 권한이 있는 서비스 계정에만 사용할 수 있습니다. 워크플로우 리소스를 삭제해야 하는 경우 시스템 관리자에게 문의하십시오.

## 관련 항목 {#related-topics}

* [의사 결정 관리에서 의사 결정으로 마이그레이션](migrate-to-decisioning.md) - 의사 결정 마이그레이션의 이점 및 기능 이해
* [의사 결정 시작](gs-experience-decisioning.md)
* [보호 및 제한 사항 결정](decisioning-guardrails.md)
* [API 결정하기 시작](api-reference/getting-started.md)
