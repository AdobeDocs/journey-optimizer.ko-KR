---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 대체 오퍼 업데이트
description: 다른 오퍼에 적합하지 않은 경우 고객에게 대체 오퍼가 전송됩니다
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 20%

---

# 대체 오퍼 업데이트 {#update-fallback-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../../../experience-decisioning/gs-experience-decisioning.md)


[!DNL Offer Library] API에 대한 PATCH 요청을 통해 컨테이너에서 대체 오퍼를 수정하거나 업데이트할 수 있습니다.

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 공식 [JSON 패치 설명서](https://jsonpatch.com/)를 참조하세요.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 요청 헤더의 *Content-Type* 및 *Accept* 필드를 구성하는 올바른 값을 보여 줍니다.

| 헤더 이름 | 값 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `fallbackOffer1234` |

**요청**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업은 `add`, `replace`, `remove`, `copy` 및 `test`입니다. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `value` | 매개 변수를 업데이트할 새 값입니다. |

**응답**

응답이 성공하면 `id`을(를) 포함하여 대체 오퍼에 대한 업데이트된 세부 정보가 반환됩니다.

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
