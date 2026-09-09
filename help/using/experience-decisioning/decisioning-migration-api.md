---
title: 의사 결정 마이그레이션 API
description: Decisioning Migration Service API를 사용하여 자동화된 종속성 해결 및 롤백 지원을 통해 샌드박스 간에 의사 결정 관리 개체를 마이그레이션하는 방법에 대해 알아봅니다.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: bf147566ac63bce11f4413a2450b55d436f01d7a
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 2%

---

# 의사 결정 마이그레이션 API {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**이 페이지에서:** Decisioning 마이그레이션 서비스 API를 사용하여 자동화된 종속성 분석과 롤백 지원을 통해 샌드박스 간에 의사 결정 관리 개체를 이동하므로 데이터 무결성을 유지하면서 환경 간에 의사 결정 콘텐츠를 전환할 수 있습니다.

>[!ENDSHADEBOX]

Decisioning 마이그레이션 서비스 API를 사용하면 의사 결정 관리 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션할 수 있습니다. 마이그레이션 프로세스는 종속성 분석, 실행 및 선택적 롤백 기능을 포함하는 비동기 워크플로우로 실행됩니다.

이 API를 사용하면 데이터 무결성과 관계를 유지하면서 <!--(e.g., from development to staging, or staging to production) --> 환경 간에 의사 결정 콘텐츠를 원활하게 전환할 수 있습니다.

의사 결정 관리와 비교하여 Decisioning의 장점과 기능에 대해 알아보려면 [이 페이지](migrate-to-decisioning.md)를 참조하세요.

## 기능 {#capabilities}

Decisioning 마이그레이션 서비스 API는 다음 기능을 제공합니다.

* **종속성 분석** - 특성, 세그먼트, 데이터 세트 요구 사항을 포함하여 원본 샌드박스와 대상 샌드박스 간에 필요한 모든 종속성을 식별합니다.
* **유연한 마이그레이션 범위** - 필요에 따라 샌드박스, 오퍼 또는 의사 결정 수준에서 마이그레이션을 실행합니다.
* **롤백 지원** - 유효성 검사 중에 문제가 발견된 경우 완료된 마이그레이션을 되돌립니다.

## 사전 요구 사항 {#prerequisites}

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

>[!NOTE]
>
>대상 샌드박스는 소스 샌드박스와 동일할 수 있습니다. 마이그레이션 프로세스는 이러한 시나리오를 처리하며, 오브젝트가 동일한 샌드박스 내에서 마이그레이션되든 다른 샌드박스로 마이그레이션되든 관계없이 데이터 무결성을 보장합니다.

### 샌드박스 간 마이그레이션 사전 요구 사항 {#cross-sandbox-prerequisites}

소스 샌드박스가 타겟 샌드박스를 ≠ 때 다음 항목이 필요합니다.

* **프로필 특성** - 대상 샌드박스에 있거나 미리 정의된 매핑이 있어야 합니다.
* **세그먼트 ID** - 이전→새 ID 매핑을 사용하여 대상 샌드박스에서 미리 만들어야 합니다.
* **ID 매핑** - 일관된 ID 확인을 위해 구성해야 합니다.

## API 기본 사항 {#api-basics}

### 기본 URL {#base-url}

다음 기본 URL을 사용하십시오.

* **프로덕션**: `https://decisioning-migration.adobe.io`

### 인증 {#authentication}

모든 API 요청에는 다음 헤더가 필요합니다.

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

인증 설정에 대한 자세한 지침은 [Journey Optimizer 인증 안내서](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}를 참조하세요.

## 마이그레이션 워크플로 {#migration-workflow}

마이그레이션 프로세스는 종속성 분석과 마이그레이션 실행의 두 가지 주요 단계로 구성됩니다. 마이그레이션을 성공적으로 수행하려면 다음 단계를 따르십시오.

### 1단계: 종속성 분석 {#analyze-dependencies}

마이그레이션하기 전에 종속성 워크플로우를 사용하여 대상 샌드박스에서 의사 결정 관리에서 의사 결정에 매핑해야 하는 항목을 식별합니다. 이러한 분석은 객체 간의 관계를 이해하고 필요한 매핑을 준비하는 데 도움이 됩니다.

#### 종속성 워크플로우 만들기 {#create-dependency-workflow}

다음 API 호출을 사용하여 종속성 분석 워크플로우를 만듭니다.

**API 형식**

```http
POST /workflows/generate-dependencies
```

**샌드박스 수준 종속성(먼저 권장됨)**

샌드박스 수준 분석으로 시작하여 모든 종속성에 대한 전체 보기를 확인합니다.

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**오퍼 수준 종속성**

특정 오퍼에 대한 종속성만 분석하려면 쿼리 문자열에서 `request-level=offer`을(를) 사용하여 동일한 끝점을 호출하고 본문에서 분석할 오퍼 ID를 사용하여 `offersList` 배열을 제공하십시오.

**의사 결정 수준 종속성**

특정 의사 결정에 대한 종속성만 분석하려면 쿼리 문자열에서 `request-level=decision`을(를) 사용하고 본문에서 분석할 의사 결정 ID를 포함하는 `decisionsList` 배열을 제공하십시오.

#### 종속성 워크플로 상태 확인 {#poll-dependency-status}

종속성 워크플로우를 폴링하여 분석이 완료되면 확인합니다.

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

`status` 필드에 `Completed`이(가) 표시되면 종속성 분석이 준비되었습니다. 워크플로우 출력을 사용하여 마이그레이션 종속성 매핑을 빌드합니다.

* **profileAttributes** - 소스 프로필 특성을 대상 프로필 특성에 매핑합니다.
* **contextAttributes** - 소스 컨텍스트 특성을 대상 컨텍스트 특성에 매핑합니다.
* **세그먼트** - 각 소스 세그먼트 키를 대상 세그먼트 식별자(`{namespace, id}`)에 매핑합니다.
* **datasetName** - 마이그레이션에 사용되는 대상 경험 이벤트 데이터 세트입니다. Journey Optimizer Edge(Web SDK) 호출에 대해 활성화된 데이터 스트림에 연결해야 합니다. 해당 스키마를 사용하여 마이그레이션된 컨텍스트 속성을 추가합니다.

2단계에서 마이그레이션 요청의 `dependency` 개체에 이러한 매핑을 제공합니다.

### 2단계: 마이그레이션 실행 {#execute-migration}

종속성을 분석하고 매핑을 준비하면 마이그레이션을 실행할 수 있습니다.

#### 마이그레이션 워크플로우 만들기 {#create-migration-workflow}

1단계의 종속성 매핑을 사용하여 마이그레이션을 구성하고 실행합니다.

**API 형식**

```http
POST /workflows/migration
```

**샌드박스 수준 마이그레이션**

모든 의사 결정 개체를 한 샌드박스에서 다른 샌드박스로 마이그레이션하려면 다음을 수행하십시오.

```shell
curl --request POST \
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
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
    }
  }'
```

**오퍼 수준 마이그레이션**

특정 오퍼만 마이그레이션하려면 쿼리 문자열에서 `request-level=offer`을(를) 사용하고 본문에 `offersList` 배열을 추가하십시오.

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**의사 결정 수준 마이그레이션**

특정 결정만 마이그레이션하려면 쿼리 문자열에서 `request-level=decision`을(를) 사용하고 본문에 `decisionsList` 배열을 추가하십시오.

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**요청 필드**

* **요청 수준**(쿼리) - 마이그레이션 범위: `sandbox`, `offer` 또는 `decision`.
* **imsOrgId**(필수) - IMS 조직 ID.
* **sourceSandboxDetails.sandboxName**(필수) - 의사 결정 관리 엔티티를 포함하는 Source 샌드박스.
* **targetSandboxDetails.sandboxName**(필수) - Decisioning 엔터티가 만들어지는 대상 샌드박스.
* **dependency.datasetName**(필수) - 대상 경험 이벤트 데이터 세트입니다. Journey Optimizer Edge(웹 SDK) 호출에 대해 활성화된 데이터 스트림에 연결해야 합니다. 해당 스키마를 사용하여 마이그레이션된 컨텍스트 속성을 추가합니다.
* **createDataStream** - `true`에서 새 Journey Optimizer 사용 데이터 스트림을 만듭니다. `false`은(는) `dependency.datasetName`의 데이터 세트에 이미 첨부된 데이터 스트림을 다시 사용합니다.
* **dependency.profileAttributes** - 소스 → 대상 프로필 특성 맵입니다.
* **dependency.contextAttributes** - 소스 → 대상 컨텍스트 특성 맵입니다.
* **dependency.segments** - 소스 세그먼트 키→ 대상 세그먼트(`{namespace, id}`)의 맵입니다.
* **offersList[]** / **decisionsList[]** - 마이그레이션할 오퍼 또는 의사 결정 ID입니다. `request-level`이(가) 각각 `offer` 또는 `decision`일 때 필요합니다.

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

모든 워크플로우(종속성, 마이그레이션 및 롤백)는 동일한 리소스 필드를 반환합니다.

* **id** - 워크플로 식별자(UUID); 일치하는 `GET /{id}`을(를) 사용하여 상태를 폴링합니다.
* **상태** - 주기 상태: `New`, `Running`, `Completed` 또는 `Failed`.
* **결과** - `Completed`에 있음; 워크플로 출력(예: 마이그레이션된 개체의 매핑 및 경고).
* **오류[]** - `Failed`에 있음, 구조적 오류 세부 정보(`result.error` 참조).
* **_links.self** - 워크플로 리소스의 URL입니다.

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

## 마이그레이션 범위 및 범위 {#migration-scope}

마이그레이션 범위를 이해하면 의사 결정 관리에서 의사 결정으로의 전환을 계획하고 확인하는 데 도움이 됩니다. 이 섹션에서는 마이그레이션 프로세스에 대해 설명하고 수동 작업을 필요로 하는 사항을 간략하게 설명합니다.

### 범위 내: 적용 대상 {#in-scope}

마이그레이션 API는 다음 항목과 기능을 처리합니다.

* **사용 사례** - 인바운드/Edge 의사 결정 사용 사례만 범위에 있습니다. Journey Optimizer 이메일 채널 마이그레이션의 아웃바운드 또는 OD가 지원되지만 수동 업데이트가 필요합니다.
* **코드 기반 경험 캠페인** - 마이그레이션 중에 자동으로 만들어지며, 대상 샌드박스의 마이그레이션된 결정 범위당 하나의 캠페인입니다.
* **채널 구성/표면** - 의사 결정 관리 배치별로 만들어진 채널 구성/표면으로, 의사 결정 응답의 적절한 라우팅을 보장합니다.
* **오퍼 콘텐츠 형식** - 오퍼는 해당 콘텐츠 형식이 JSON 또는 텍스트인 경우에만 마이그레이션됩니다. 다른 콘텐츠 유형은 수동 재생성이 필요합니다.
* **오퍼 특성** - 사용자 지정 메타데이터를 유지하면서 &quot;개인화된 오퍼 항목 - Experience Decisioning&quot; 스키마의 `offer_item_custom_attributes` 필드 그룹에 보존됩니다.
* **컨텍스트 특성** - 추적 및 개인화를 위해 `custom_context_attributes` 필드 그룹의 경험 이벤트 스키마에 추가되었습니다.
* **결정 범위** - 하나의 결정 관리 결정 범위가 하나의 선택 전략 + 하나의 결정 정책 + 하나의 의사 결정 캠페인에 매핑되어 적절한 엔터티 계층 구조를 유지합니다.
* **API 전용 자격 규칙** - API만을 통해 만들어진 자격 규칙(의사 결정 관리 UI에서는 아님)은 마이그레이션되고 의사 결정에서 API 전용으로 유지됩니다. UI에서 만든 규칙도 마이그레이션됩니다.

### 범위 외: 다루지 않거나 수동 작업이 필요한 사항 {#out-of-scope}

다음 항목은 수동 작업이 필요하거나 마이그레이션 도구에서 지원되지 않습니다.

* **의사 결정 배치** - 마이그레이션 도구로 만들어진 배치가 없습니다. 아키텍처를 기반으로 마이그레이션 전이나 후에 의사 결정에서 수동으로 만들어야 합니다.
* **배치 수준 한도** - 배치 수준 빈도 한도가 마이그레이션되지 않았습니다.
* **JSON/텍스트가 아닌 오퍼 콘텐츠** - JSON 또는 텍스트 이외의 콘텐츠 형식(예: HTML, 이미지)이 있는 오퍼는 마이그레이션되지 않으며 Decisioning에서 수동으로 다시 만들어야 합니다.
* **프로필 특성 및 세그먼트** - 프로필 특성 및 세그먼트 멤버십은 마이그레이션 도구로 만들거나 편집하지 않습니다. 마이그레이션을 실행하기 전에 타겟 샌드박스에 이미 존재해야 합니다.
* **세그먼트 ID 매핑** - 세그먼트 ID는 대상 샌드박스에서 미리 만들어야 합니다. 세그먼트 해결을 위해 마이그레이션 API 요청에 이전→새 ID 매핑을 제공해야 합니다.
* **데이터 수집 코드 변경** - 클라이언트측 및 서버측 이벤트 추적 코드 변경 내용은 자동화되지 않습니다. 구현 팀이 Decisioning 요청/응답 형식 및 Decisioning 이벤트 스키마를 사용하도록 이벤트 컬렉션을 업데이트해야 합니다.

## 엔티티 매핑 참조 {#entity-mapping}

Decision management에서 Decisioning으로 마이그레이션할 때 엔티티는 다음 표에 따라 매핑됩니다. 매핑에는 기본 의사 결정 엔티티와 마이그레이션 중에 만들어지거나 사용되는 추가 관련 엔티티가 포함됩니다.

### 의사 결정 관리 - 의사 결정 엔티티 매핑

| 의사 결정 관리 엔티티 | 의사 결정 엔티티 | 추가 엔티티 |
|-----------|--------------|-------------------|
| 결정 | 선택 전략 | 품목 수집, 자격 규칙, 순위 공식 |
| | 의사 결정 정책 | 항목 수, 선택 전략, 대체 오퍼 항목 |
| | 코드 기반 경험 캠페인 | 의사 결정 정책, 컨텐츠, 채널 구성, Journey Optimizer 조각 |
| 배치 | 채널 구성 | — |
| 컬렉션 | 항목 컬렉션 | 통합 태그, 오퍼 항목 |
| 컬렉션 한정자 | 통합 태그 | — |
| 규칙 | 의사 결정 규칙 | — |
| 순위 공식 | 의사 결정 순위 공식 | — |
| 오퍼 | 오퍼 항목 | 자격 규칙, Journey Optimizer 조각, 통합 태그, 빈도 제한 |
| | 오퍼 항목 스키마 | — |
| | Journey Optimizer 조각 | — |

### 이름 지정 규칙

마이그레이션 프로세스는 일관성을 보장하고 이름 충돌을 방지하기 위해 `ExD_` 접두사를 사용하는 이름 지정 규칙을 적용합니다.

| Source 개체 | 의사 결정 관리 이름 패턴 | 의사 결정 이름 패턴 |
|---------------|-----------------|-------------------|
| 오퍼 | `<offerName>` | `ExD_<offerName>` |
| 자격 규칙 | `<ruleName>` | `ExD_<ruleName>` |
| 순위 공식 | `<formulaName>` | `ExD_<formulaName>` |
| 컬렉션 | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| 의사 결정 → 선택 전략 | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| 의사 결정 → 결정 정책 | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Journey Optimizer 조각 | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| 배치 → 서피스 | `<placementName>` | `ExD_<placementName>` *(밑줄로 변환된 공백/점)* |
| 통합 태그 | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| CBE 캠페인 | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### 추가 속성

| Source 속성 | 대상 위치 |
|-----------------|-----------------|
| 오퍼 속성 | 개인화된 오퍼 항목 스키마의 &quot;migratedofferattributes&quot; 필드 |
| 컨텍스트 속성 | 마이그레이션 중에 제공된 데이터 세트에 첨부된 스키마의 &quot;migratedcontextattributes&quot; 필드 |

## 요청 및 응답 모델 {#request-response-model}

Decision Management에서 Decisioning으로 마이그레이션할 때 새 요청 및 응답 형식을 사용하도록 애플리케이션 코드를 업데이트해야 합니다. 두 시스템 모두 Edge Network 끝점을 사용하지만 페이로드 구조와 필드 이름이 다릅니다.

### 의사 결정 관리 Edge 요청(현재) {#dm-request}

현재 의사 결정 관리 Edge 요청은 다음 구조를 따릅니다.

**끝점:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**머리글:**
&#x200B;- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
&#x200B;- `x-api-key: <API_KEY>`(Developer Console)
&#x200B;- `x-gw-ims-org-id: <IMS_ORG_ID>`(형식: `{ORG_ID}@AdobeOrg`)
&#x200B;- `x-request-id: <UNIQUE_REQUEST_ID>`(추적 및 중복 제거용)
&#x200B;- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
&#x200B;- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
&#x200B;- `x-sandbox-name: <SANDBOX_NAME>`(예: prod, dev)

**요청 본문 매개 변수:**
&#x200B;- `xdm:dryRun`(true/false) - 보고를 오염시키지 않고 요청 테스트
&#x200B;- `xdm:propositionRequests[]` - 결정 요청 배열:
  &#x200B;- `activityId` - 결정 활동 식별자
  &#x200B;- `placementId` - 배치 식별자
  &#x200B;- `itemCount` - 반환할 최대 오퍼 수
&#x200B;- `xdm:profiles[].xdm:identityMap` - ID 매핑(전자 메일, ECID 등)
&#x200B;- `xdm:validateContextData` - 엄격한 컨텍스트 데이터 유효성 검사 플래그
&#x200B;- `xdm:responseFormat.xdm:includeContent` - 실제 콘텐츠와 ID만 포함

**예제 요청 본문:**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>OD(Full Decision Management) 요청/응답 참조에 대해서는 [Edge Decisioning API](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api)&#x200B;(base64 인코딩 `decisionScopes`을 사용하여 `activityId` 및 `placementId`을(를) 포함하는 웹 SDK/Edge 변형)을 참조하십시오.

### Decisioning Edge 요청(마이그레이션 후) {#decisioning-request}

마이그레이션 후에는 동일한 Edge Network 엔드포인트를 통해 Decisioning 요청 형식을 사용합니다.

**끝점:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**키 요청 필드:**
&#x200B;- `query.identity.fetch` - 확인할 ID 유형 배열(예: `["ECID"]`)
&#x200B;- `event.xdm.environment.type` - 환경 유형: `"browser"`, `"app"` 또는 `"server"`
&#x200B;- `event.xdm.environment.browserDetails` - 브라우저 메타데이터(`viewportWidth`, `viewportHeight`, `userAgent`)
&#x200B;- `event.xdm.identityMap` - 결정 관리와 동일한 ID 매핑
&#x200B;- `event.xdm.timestamp` - ISO 8601 타임스탬프
&#x200B;- `query.personalization.surfaces` - 대상 표면 배열(예: `["web://site.com/homepage"]`) — `decisionScope`을(를) 대체합니다.
&#x200B;- `query.personalization.schemas` - 반환할 콘텐츠 스키마(예: `["json-content-item", "html-content-item"]`)
&#x200B;- `data.__adobe.ajo.allowDuplicateDecisionItems` - 중복 제거 제어(기본값: `true`, 여러 표면에 적합한 항목이 한 번만 반환되도록 `false`을(를) 설정하고 다른 표면은 대체/빈 항목을 받습니다). 결정 관리 `allowDuplicatePropositions`을(를) 바꿉니다.
&#x200B;- `data.__adobe.ajo.dryRun` - 테스트 플래그. 보고 및 최대 가용량 카운터 모두에 대한 피드백 이벤트를 억제합니다. 결정 관리 `xdm:dryRun`을(를) 바꿉니다. 프로덕션 전에 제거합니다.

**예제 요청 본문(서버측):**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>전체 Journey Optimizer Decisioning Web SDK/Edge 참조에 대해서는 [코드 기반 경험: Decisioning 구현](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)을 참조하십시오.

### Decisioning Edge 응답 {#decisioning-response}

Decisioning 응답에 문제 유형 `personalization:decisions`(오퍼), `locationHint:result` 및 `state:store`(유지할 쿠키)별로 구성된 여러 핸들이 포함되어 있습니다.

**응답 구조:**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**주요 응답 필드:**
&#x200B;- `handle[].type` - 핸들 형식(`personalization:decisions`, `locationHint:result`, `state:store`)
&#x200B;- `payload[].id` - 고유한 제안 인스턴스 ID — 다시 표시/상호 작용 이벤트로 에코
&#x200B;- `payload[].scope` - 제안이 해결된 표면 URI
&#x200B;- `payload[].scopeDetails.decisionProvider` - 엔진이 `AJO`인지 확인
&#x200B;- `payload[].scopeDetails.correlationID` - 결정 인스턴스를 서비스 중인 이벤트에 연결합니다.
&#x200B;- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` - 제안에 대한 순위 및 캠페인/액션 메타데이터
&#x200B;- `payload[].scopeDetails.characteristics.eventToken` - 메시지 수준 추적 토큰
&#x200B;- `payload[].scopeDetails.characteristics.subPropositions` - Base64로 인코딩된 **결정 항목의 배열**; 각 항목은 항목당 고유한 `token`을(를) 전달합니다. 표시/상호 작용 이벤트에서 `propositionAction.tokens`에 전달하는 항목별 토큰입니다.
&#x200B;- `payload[].items[].schema` / `payload[].items[].data.content` - 렌더링할 콘텐츠 스키마 및 실제 오퍼 콘텐츠(JSON/HTML)
&#x200B;- `state:store` 페이로드 - 후속 요청(서버측)에서 유지 및 전달할 ID 및 클러스터 쿠키

`characteristics.subPropositions` 문자열 base64는 항목당 `token`이(가) 있는 제공된 항목의 배열로 디코딩합니다.

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## 구현 패턴 {#implementation-patterns}

Decisioning 은 세 가지 구현 접근 방식을 지원합니다.

### 클라이언트측 구현(웹 SDK/모바일 SDK) {#client-side}

웹 SDK 또는 모바일 SDK은 모든 요청 및 쿠키 관리를 자동으로 처리합니다. SDK은 각 요청과 함께 ID 및 클러스터 쿠키를 저장하고 전달합니다.

**쿠키 처리:** 자동 — Web SDK에서 `kndctr_<OrgId>_identity` 및 `kndctr_<OrgId>_cluster` 쿠키를 관리합니다.

### 서버측 구현(Edge Network API) {#server-side}

애플리케이션 서버는 Edge Network에 직접 POST를 진행하며 수동으로 쿠키 전달을 관리해야 합니다. 서버가 들어오는 요청에서 브라우저 쿠키를 추출하여 `meta.state.entries[]`을(를) 통해 Edge Network으로 전달한 다음 응답에서 쿠키를 반환합니다.

**쿠키 처리:** 수동 — 앱 서버는 브라우저 요청에서 쿠키를 추출하여 요청 본문의 Edge Network으로 전달하고 응답으로 설정해야 합니다. ID 일관성을 위해 쿠키를 `meta.state.entries`에서 명시적으로 전달해야 합니다.

### 하이브리드 구현 {#hybrid}

서버측 렌더링(초기 페이지 로드)과 클라이언트측 SDK(후속 상호 작용)을 결합합니다. 서버는 Edge Network을 통해 초기 콘텐츠를 렌더링한 다음 Web SDK이 후속 개인화 요청을 처리합니다.

**쿠키 처리:** 혼합 — Server Side는 Edge Network으로 수동 쿠키 전달이 필요하며 Web SDK에서 자동으로 클라이언트측을 처리합니다. 일관된 ID 확인을 위해 서버측 렌더링의 ID 토큰을 클라이언트측 SDK에서 사용할 수 있는지 확인합니다.

## 이벤트 추적 및 데이터 수집 {#event-tracking}

의사 결정 결과를 적절하게 특성화하고, 빈도 제한 기능을 활성화하고, AI 기반 순위 최적화를 활용하려면 의사 결정 이벤트 스키마를 사용하여 이벤트 추적을 구현해야 합니다.

### 필수 이벤트 필드 {#event-fields}

`eventType`과(와) `_experience.decisioning.propositionEventType`은(는) 모두 필요합니다. 둘 중 하나가 누락된 경우 해당 디스플레이/상호 작용 카운터는 증가하지 않습니다.

* **`eventType`** - 이벤트 범주를 지정합니다.
  &#x200B;- `decisioning.propositionDisplay` — 노출 이벤트(사용자에게 표시되는 오퍼)
  &#x200B;- `decisioning.propositionInteract` — 상호 작용 이벤트(사용자가 오퍼를 클릭하거나 오퍼에 참여)

* **`_experience.decisioning.propositionEventType`** - 이벤트 하위 유형에 플래그를 지정합니다. `1`(각 값은 `1` 또는 `0`임)로 설정된 **정확히 하나의** 이벤트 유형 키 포함(동일한 개체에서 여러 이벤트 유형을 `1`(으)로 설정하지 않음):
  &#x200B;- `{ "display": 1 }` — 노출 이벤트
  &#x200B;- `{ "interact": 1 }` — 상호 작용 이벤트
  &#x200B;- `display`/`interact`/`dismiss`이(가) 모두 `0`이거나 `eventType`이(가) `decisioning.proposition<Display|Interact|Dismiss>` 이외의 값인 경우 이벤트가 **사용자 지정 이벤트**(으)로 처리됩니다.

* **`_experience.decisioning.propositionAction.tokens[]`** - 카운터를 증가시킬 제공된 항목을 식별하는 항목별 토큰:
  &#x200B;- 디코딩된 `subPropositions` 배열 — **not** `scopeDetails.characteristics.eventToken`에서 각 항목의 `token`을(를) 복사합니다. 이 배열은 다른 메시지 수준 토큰입니다.
  &#x200B;- 토큰을 받은 그대로, 수정되지 않은 상태로 전달합니다.
  &#x200B;- **상호 작용 이벤트:**&#x200B;은(는) **정확히 하나의** 토큰(클릭한 항목)을 제공합니다.
  &#x200B;- **이벤트 표시:** 선택 사항 - 토큰을 입력하여 특정 항목을 늘리거나, **생략** `tokens`을(를) 입력하여 `subPropositions`에서 **모든** 항목에 대한 카운터를 늘리십시오.

* **`_experience.decisioning.propositions[]`** - `id`, `scope` 및 응답에서 전체 `scopeDetails`을(를) 포함하여 제공된 제안을 다시 에코합니다(`characteristics.subPropositions`을(를) 전달하며 `decisionProvider`이(가) 필요). 명시적 `items[]` 배열을 만들 필요가 없습니다.

### 스키마 요구 사항 {#schema-requirements}

마이그레이션 전에 Decisioning 필드 그룹을 이벤트 데이터 세트 스키마에 연결합니다.

1. Experience Platform에서 이벤트 데이터 세트 스키마를 엽니다.
2. `Experience Event - Proposition Details` 필드 그룹 추가
3. 다음 필드가 매핑되었는지 확인합니다.
   &#x200B;- `_experience.decisioning.*`개 필드
   &#x200B;- `_experience.decisioning.propositionAction.tokens`
   &#x200B;- `_experience.decisioning.propositionEventType`

### 추적 토큰 처리 {#tracking-token}

추적 토큰은 다음 요구 사항에 따라 처리되어야 합니다.

* **항목별 토큰은 카운터를 구동합니다** — `propositionAction.tokens`의 값은 메시지 수준 `characteristics.eventToken`이(가) 아닌 `subPropositions`에서 제공된 각 항목의 `token`입니다.
* **이벤트 상호 작용** — 정확히 하나의 토큰(클릭한 항목)을 제공합니다.
* **이벤트 표시** — 토큰은 선택 사항입니다. `subPropositions`에서 모든 항목을 증가시키려면 생략하거나 해당 항목만 증가시키려면 특정 토큰을 제공하십시오.
* **토큰을 수정하지 마십시오** — 받은 그대로 값을 전달합니다. 인코딩, 구문 분석 또는 변경하지 마십시오.

## Decisioning 이벤트 예 {#event-examples}

각 예제는 제공된 제안(`characteristics.subPropositions`을 포함하는 `scopeDetails` 포함)을 되메아리며 `eventType`과(와) `propositionEventType`을(를) 모두 설정합니다. 카운터는 `subPropositions`의 항목에 대해 증가합니다. `propositionAction.tokens`은(는) 항목을 선택합니다.

### 이벤트 표시

오퍼가 사용자에게 표시되면 이벤트를 표시하여 의사 결정에 알립니다. 표시된 항목의 토큰을 제공하거나 `tokens`을(를) 생략하여 `subPropositions`의 모든 항목에 대한 표시 카운터를 증가시키십시오.

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### 상호 작용(클릭) 이벤트

상호 작용 이벤트는 사용자가 표시된 오퍼를 클릭하거나 참여하는 시점을 추적합니다. **은(는) 클릭한 항목을 식별하는**&#x200B;정확히 하나&#x200B;**토큰을 제공해야 합니다**.

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### 사용자 지정 이벤트

사용자 지정 이벤트는 고객 정의 `eventType`(`decisioning.proposition<Display|Interact|Dismiss>` 이외의 모든 값)을(를) 사용하고 `propositionEventType`의 모든 `display`/`interact`/`dismiss`을(를) `0`(`OTHER`(으)로 분류)로 설정합니다. 사용자 지정 이벤트는 `subPropositions`에 대해 디스플레이 이벤트(다중 토큰 필터링)처럼 디코딩되고 구성된 PQL을 통해 평가됩니다.

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

이러한 이벤트를 통해 의사 결정에서 빈도 제한, 기본 보고 및 AI 기반 순위 최적화를 사용할 수 있습니다. 웹 SDK을 사용하여 제안 이벤트를 보내는 방법은 [코드 기반 경험: 의사 결정 구현](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)을 참조하십시오.

## 엔드 투 엔드 마이그레이션 프로세스 {#migration-process}

1. 사전 요구 사항 유효성 검사 — 마이그레이션을 시작하기 전에 Target 샌드박스가 준비되었고 모든 사전 요구 사항 종속성이 식별되고 준비되었는지 확인합니다(프로필 속성, 세그먼트 ID, ID 매핑).

1. 마이그레이션 API 호출 — 마이그레이션 API를 실행하여 사전 요구 사항 및 매핑을 사용하여 의사 결정 관리 객체를 의사 결정으로 마이그레이션합니다.

1. 초안 의사 결정 엔티티 생성 — 툴링은 엔티티 매핑당 초안 상태에서 캠페인, 의사 결정 정책, 선택 전략, 오퍼 항목 등을 생성합니다. 대상 샌드박스에서 생성된 모든 Decisioning 개체를 검토합니다. 이름 지정, 엔티티 유형 및 참조의 유효성을 검사합니다. 고객이 직면한 문제는 아직 없습니다. 의사 결정 관리에서 라이브 트래픽을 계속 처리합니다.

1. 클라이언트 및 서버 코드 업데이트 — 새 Decisioning 요청/응답 형식을 사용하는 데 필요한 코드 변경 사항을 구현하고 필수 필드를 사용하여 이벤트 추적을 구현합니다.

1. 활성화 및 전환 — 의사 결정 객체(전략, 정책, 캠페인, 표면)를 활성화하고 자체 타임라인에서 의사 결정 관리에서 벗어나 트래픽을 전환합니다.

## 관련 항목 {#related-topics}

* [의사 결정 관리에서 의사 결정으로 마이그레이션](migrate-to-decisioning.md) - 의사 결정 마이그레이션의 이점 및 기능 이해
* [의사 결정 시작](gs-experience-decisioning.md)
* [보호 및 제한 사항 결정](decisioning-guardrails.md)
* [API 결정하기 시작](api-reference/getting-started.md)