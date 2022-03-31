---
title: Batch Decisioning API
description: Batch Decisioning API를 사용하여 사전 정의된 의사 결정 범위 내에서 세그먼트화된 프로필에 대한 최상의 오퍼를 선택하는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 817a77c5717804ccae36db3dd8920008ab127684
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# 을 사용하여 오퍼 게재 [!DNL Batch Decisioning] API

다음 [!DNL Batch Decisioning] API를 사용하면 한 번의 호출로 주어진 세그먼트의 모든 프로필에 offer decisioning 기능을 사용할 수 있습니다. 세그먼트의 각 프로필에 대한 오퍼 콘텐츠는 사용자 지정 일괄 처리 워크플로우에 사용할 수 있는 Adobe Experience Platform 데이터 세트에 배치됩니다.

사용 [!DNL Batch Decisioning] API를 사용하면 결정 범위에 대해 Adobe Experience Platform 세그먼트의 모든 프로필에 대한 최상의 오퍼로 데이터 세트를 채울 수 있습니다. 예를 들어, 조직은 메시지 게재 공급업체에 오퍼를 보낼 수 있도록 배치 결정을 실행하려고 할 수 있습니다. 그런 다음 이러한 오퍼는 동일한 사용자 세그먼트에 대한 배치 메시지 전달을 위해 전송되는 콘텐츠로 사용됩니다.

이를 수행하려면 조직에서 다음을 수행합니다.

* 를 실행합니다. [!DNL Batch Decisioning] API - 두 개의 요청을 포함합니다.

   1. A **배치 GET 요청** 배치 작업 로드 상태를 가져오려면

   2. A **배치 POST 요청** 작업 로드를 시작하여 배치 처리 오퍼 선택을 시작하려면 다음을 수행합니다.

* 데이터 세트를 메시지 배달 공급업체 API로 내보냅니다.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## 시작하기 {#getting-started}

이 API를 사용하기 전에 다음 전제 조건 단계를 완료했는지 확인하십시오.

### 결정 준비

결정을 준비하려면 아래 절차를 따르십시오.

* 결정 결과를 내보내려면 &quot;ODE Decision Events&quot; 스키마를 사용하여 데이터 세트를 만듭니다.

* 평가된 다음 업데이트해야 하는 Platform 세그먼트를 만듭니다. 자세한 내용은 [세분화 설명서](http://www.adobe.com/go/segmentation-overview-en) 세그먼트 멤버십 평가를 업데이트하는 방법에 대해 자세히 알아보십시오.

* Adobe Journey Optimizer에서 결정 ID와 배치 ID로 구성된 결정 범위가 있는 결정을 만듭니다. 자세한 내용은 [결정 범위 정의 섹션](../../offer-activities/create-offer-activities.md) 추가 정보를 얻기 위한 의사 결정에 대한 안내서를 참조하십시오.

### API 요구 사항

모든 Batch Decisioning 요청에는 다음과 같은 추가 헤더가 필요합니다.

* `Content-Type`: `application/json`
* `x-request-id`: 요청을 식별하는 고유한 문자열입니다.
* `x-sandbox-name`: 샌드박스 이름입니다.
* `x-sandbox-id`: 샌드박스 ID입니다.

## 배치 결정에 대한 정보 검색 {#retrieve-information-on-a-batch-decision}

특정 결정에 대한 정보를 검색하려면 `/workloads/decisions` 결정에 해당하는 작업 로드 ID 값을 제공하는 중 끝점입니다.

**API 형식**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 결정이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | 단일 작업 로드를 식별하는 Offer decisioning에 의해 생성된 UUID입니다. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}'
```

**응답**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| 속성 | 설명 | 예 |
| -------- | ----------- | ------- |
| `@id` | 단일 작업 로드를 식별하는 Offer decisioning에 의해 생성된 UUID입니다. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | IMS 조직 ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 컨테이너 ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 의사 결정 작업 로드 요청을 만든 시간입니다. | `1648076994405` |
| `ode:status` | 작업 로드 상태는 &quot;QUEUED&quot;로 시작되고 &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; 또는 &quot;ERROR&quot;로 변경됩니다. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 상태가 &quot;PROCESSING&quot; 또는 &quot;INGESTING&quot;인 경우 sparkJobId 및 batchID와 같은 자세한 정보가 표시됩니다. 상태가 &quot;오류&quot;인 경우 오류 세부 정보가 표시됩니다. |  |

## 배치 프로세스 시작 {#start-a-batch-process}

작업 로드를 배치 프로세스 결정에 시작하려면 `/workloads/decisions` 엔드포인트.

**API 형식**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 결정이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| 속성 | 설명 | 예 |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | 세그먼트의 고유 식별자입니다. 하나의 값만 포함할 수 있습니다. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 결정 이벤트를 기록할 수 있는 출력 데이터입니다. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | placementId 및 activityId가 포함된 래퍼 |  |
| `xdm:activityId` | 결정의 고유 식별자입니다. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 고유 배치 식별자입니다. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 의사결정 범위에 대해 요청한 옵션 등의 항목 수를 보여주는 선택적 필드입니다. 기본적으로 API는 범위당 하나의 옵션을 반환하지만 이 필드를 지정하여 더 많은 옵션을 명시적으로 요청할 수 있습니다. 범위 당 최소 1개 및 최대 30개의 옵션을 요청할 수 있습니다. | `1` |
| `xdm:includeContent` | 선택적 필드이며 `false` 기본적으로 제공됩니다. If `true`에는 오퍼 콘텐츠가 데이터 집합의 의사 결정 이벤트에 포함되어 있습니다. | `false` |

자세한 내용은 [의사 결정 관리 설명서](../../get-started/starting-offer-decisioning.md) 를 참조하십시오.

**응답**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| 속성 | 설명 | 예 |
| -------- | ----------- | ------- |
| `@id` | 단일 작업 로드를 식별하는 Offer decisioning에 의해 생성된 UUID입니다. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | IMS 조직의 ID입니다. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 컨테이너 ID입니다. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 의사 결정 작업 로드 요청을 만든 시간입니다. | `1648078924834` |
| `ode:status` | 작업 로드 상태입니다. | `ode:status: "QUEUED"` |

## 서비스 수준 {#service-levels}

모든 일괄 처리 결정에 대한 종단 시간은 작업 로드를 생성한 시점부터 출력 데이터 세트에 사용할 수 있는 결정 결과까지의 기간입니다. POST 요청 페이로드의 세그먼트 크기는 종단 간 배치 결정 시간에 영향을 주는 주요 요소입니다. 다음은 다양한 세그먼트 크기에 대한 몇 가지 관찰입니다.

* 세그먼트 크기 &lt;= 10K: 6분
* 세그먼트 크기 &lt;= 1M: 10분
* 세그먼트 크기 &lt;= 15M: 75분

## 제한 사항 {#limitations}

다음의 제한 사항은 다음과 같습니다 [!DNL Batch Decisioning] API:

* **단일 배치 작업**: 현재 한 번에 데이터 세트당 하나의 일괄 처리 작업만 실행할 수 있습니다. 다른 모든 요청은 HTTP 429(요청이 너무 많음)로 응답합니다.
* **빈도 제한**: 하루에 한 번 발생하는 프로필 스냅샷에서 일괄 처리가 실행됩니다. 다음 [!DNL Batch Decisioning] API는 빈도를 제한하고 항상 최신 스냅샷의 프로필을 로드합니다.

## 다음 단계 {#next-steps}

이 API 가이드에 따라 를 사용하여 작업 로드 상태 및 전달된 오퍼를 확인했습니다 [!DNL Batch Decisioning] API. 자세한 내용은 [의사 결정 관리 개요](../../get-started/starting-offer-decisioning.md).
