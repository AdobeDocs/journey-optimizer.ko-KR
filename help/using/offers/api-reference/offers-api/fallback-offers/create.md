---
title: 대체 오퍼 만들기
description: 다른 오퍼에 적합하지 않은 경우 고객에게 대체 오퍼가 전송됩니다
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 12%

---

# 대체 오퍼 만들기 {#create-fallback-offer}

에 대한 POST 요청을 하여 대체 오퍼를 만들 수 있습니다. [!DNL Offer Library] API.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
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

**응답**

성공적인 응답은 고유한 대체 오퍼를 포함하여 새로 생성된 대체 오퍼에 대한 정보를 반환합니다 `id`. 다음을 사용할 수 있습니다. `id` 이후 단계에서는 대체 오퍼를 업데이트 또는 삭제하거나 이후 튜토리얼에서 의사 결정을 만듭니다.


```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
