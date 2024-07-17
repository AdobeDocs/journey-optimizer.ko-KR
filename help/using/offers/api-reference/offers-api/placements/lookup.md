---
title: 배치 조회
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: db337b5c-426a-4695-81e8-3a1b041791f2
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# 배치 조회 {#look-up-placement}

`id` 배치를 포함하는 [!DNL Offer Library] API에 대한 GET 요청을 수행하여 특정 배치를 조회할 수 있습니다.

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
