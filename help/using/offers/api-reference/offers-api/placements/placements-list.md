---
title: 배치 나열
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: f7d2666c88dd2cfb1237fbab34c1ec3b141260b4
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 16%

---

# 배치 나열 {#list-placements}

배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다. 배치는 올바른 오퍼 콘텐츠가 메시지 내의 올바른 위치에 표시되도록 하는 데 도움이 됩니다. 오퍼에 컨텐츠를 추가할 때 해당 컨텐츠가 표시될 수 있는 배치를 선택하라는 메시지가 표시됩니다.

에 대한 단일 GET 요청을 수행하여 모든 배치 목록을 볼 수 있습니다. [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/placements?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |

## 쿼리 매개 변수 사용 {#using-query-parameters}

쿼리 매개 변수를 사용하여 리소스를 나열할 때 결과를 페이지로 지정하고 필터링할 수 있습니다.

### 페이징 {#paging}

페이징에 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] 또는 속성={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>속성 표현식이 형식입니다. `[!]field[op]value`, 포함 `op` 위치: `[==,!=,<=,>=,<,>,~]`, 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 존재하는 배치 목록과 액세스 권한이 있는 배치 목록을 반환합니다.

```json
{
    "results": [
        {
            "created": "2023-05-15T11:22:50.031+00:00",
            "modified": "2023-05-15T11:22:50.031+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement5678",
            "name": "Placement one",
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
        },
        {
            "created": "2023-05-19T08:29:15.875+00:00",
            "modified": "2023-05-19T08:29:15.875+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement1234",
            "name": "Placement two",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
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
    ],
    "count": 2,
    "total": 4,
    "_links": {
        "self": {
            "href": "/placements?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/placements?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
