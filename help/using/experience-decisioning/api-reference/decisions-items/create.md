---
title: 의사 결정 항목 만들기
description: 오퍼 라이브러리 API를 사용하여 의사 결정 항목을 만드는 방법을 알아봅니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e60b0eec-29bc-4411-9eab-08eaf738fc79
source-git-commit: 8463b2f98806b009e7af4a9d28dac9015108d1c6
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# 의사 결정 항목 만들기 {#create-decision-items}

오퍼 라이브러리 API에 POST 요청을 하여 의사 결정 항목을 만들 수 있습니다.

**API 형식**

```http
POST /{ENDPOINT_PATH}/offer-items 
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |

**요청**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-items' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '{
    "_experience": {
        "decisioning": {
            "offeritem": {
                "lifecycleStatus": "approved"
            },
            "decisionitem": {
                "itemCalendarConstraints": {
                    "endDate": "2030-12-31T08:00:00.000Z",
                    "startDate": "2024-06-10T04:00:00.000Z"
                },
                "itemCatalogID": "itemCatalong1234",
                "itemConstraints": {
                    "eligibilityRule": "rule1234",
                    "profileConstraintType": "eligibilityRule"
                },
                "itemDescription": "Offer item description",
                "itemName": "Offer Item One",
                "itemPriority": 1
            }
        }
    },
    "_<imsOrg>": {
        "foo": "bar"
    }
}'
```

**응답**

성공적인 응답은 ID를 포함하여 새로 생성된 결정 항목의 세부 사항을 반환합니다. 이후 단계에서 이 ID를 사용하여 결정 항목을 업데이트하거나 삭제할 수 있습니다.

```json
{
    "etag": 1,
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

