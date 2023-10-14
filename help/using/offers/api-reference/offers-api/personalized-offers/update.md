---
title: 개인화된 오퍼 업데이트
description: 맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 8%

---

# 개인화된 오퍼 업데이트 {#update-personalized-offer}

에 PATCH 요청을 하여 개인화된 오퍼를 수정하거나 업데이트할 수 있습니다. [!DNL Offer Library] API

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 다음을 참조하십시오. [JSON 패치 설명서](https://jsonpatch.com/).

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `personalizedOffer1234` |

**요청**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업에는 다음이 포함됩니다. `add`, `replace`, `remove`, `copy` 및 `test`. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `value` | 매개 변수를 업데이트할 새 값입니다. |

**응답**

성공적인 응답은 배치 ID를 포함하여 업데이트된 배치 세부 정보를 반환합니다.

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
