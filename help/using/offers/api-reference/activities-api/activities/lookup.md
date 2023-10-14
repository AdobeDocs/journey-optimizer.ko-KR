---
title: 결정 조회
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ee242f0f-f331-4f41-9418-938b4ca1dda3
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---

# 결정 조회 {#look-up-decision}

에 GET 요청을 하여 특정 결정을 조회할 수 있습니다. [!DNL Offer Library] 의사 결정을 포함하는 API `id` 요청 경로에서.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `offerDecision1234` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 고유 의사 결정에 대한 정보를 포함하여 의사 결정 세부 사항을 반환합니다 `id`.

```json
{
    "created": "2022-11-15T16:35:06.873+00:00",
    "modified": "2023-05-15T15:00:27.641+00:00",
    "etag": 3,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerDecision1234",
    "name": "Test Decision One",
    "status": "draft",
    "startDate": "2021-08-23T07:00:00.000+00:00",
    "endDate": "2021-08-25T07:00:00.000+00:00",
    "fallback": "fallbackOffer1234",
    "criteria": [
        {
            "placements": [
                "offerPlacement1234",
                "offerPlacement5678"
            ],
            "rank": {
                "priority": 0,
                "order": {
                    "orderEvaluationType": "ranking-strategy",
                    "rankingStrategy": "123456789123"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            },
            "optionSelection": {
                "filter": "offerCollection1234"
            }
        }
    ]
}
```
