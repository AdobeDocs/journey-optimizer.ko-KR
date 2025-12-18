---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 개인화된 오퍼 조회
description: 맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 2e30b155-688b-432b-a703-d09de12ebdfd
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 19%

---

# 개인화된 오퍼 조회 {#look-up-personalized-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../../../experience-decisioning/gs-experience-decisioning.md)


맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.

요청 경로에 개인화된 오퍼 ID가 포함된 [!DNL Offer Library] API에 대한 GET 요청을 수행하면 개인화된 특정 오퍼를 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `personalizedOffer1234` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

응답이 성공하면 고유한 맞춤형 오퍼 `id`에 대한 정보를 포함하여 맞춤형 오퍼의 세부 정보가 반환됩니다.

```json
{
    "created": "2023-05-15T14:35:16.781+00:00",
    "modified": "2023-05-15T14:38:26.691+00:00",
    "etag": 2,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "personalizedOffer1234",
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}
```
