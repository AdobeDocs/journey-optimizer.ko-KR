---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 배치 조회
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: db337b5c-426a-4695-81e8-3a1b041791f2
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 24%

---

# 배치 조회 {#look-up-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../experience-decisioning/gs-experience-decisioning.md)


배치 [!DNL Offer Library]을(를) 포함하는 `id` API에 대한 GET 요청을 수행하여 특정 배치를 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/placements/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `offerPlacement1234` |

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

응답이 성공하면 고유한 배치 `id`에 대한 정보를 포함하여 배치 세부 정보가 반환됩니다.

```json
{
     "created": "2023-05-15T11:22:50.031+00:00",
    "modified": "2023-05-15T11:22:50.031+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerPlacement1234",
    "name": "Placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/web",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": false,
    "returnMetaData": {
        "decisionName": true,
        "offerName": true,
        "offerAttributes": true,
        "offerPriority": true,
        "placementName": true,
        "channelType": true,
        "contentType": true
    }
}
```
