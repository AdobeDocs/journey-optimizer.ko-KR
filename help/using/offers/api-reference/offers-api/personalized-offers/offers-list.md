---
title: 개인화된 오퍼 나열
description: 맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# 개인화된 오퍼 나열 {#list-personalized-offers}

맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.

에 대한 단일 GET 요청을 수행하여 모든 개인화된 오퍼 목록을 볼 수 있습니다. [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=personalized&{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 결과를 필터링 기준으로 사용할 선택적 쿼리 매개 변수입니다. | `limit=2` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 쿼리 매개 변수 사용 {#using-query-parameters}

쿼리 매개 변수를 사용하여 리소스를 나열할 때 결과를 페이지로 지정하고 필터링할 수 있습니다.

### 페이징 {#paging}

페이징에 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] 또는 속성={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>속성 표현식이 형식입니다. `[!]field[op]value`, 포함 `op` 위치: `[==,!=,<=,>=,<,>,~]`, 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 배치 수를 제한합니다. | `limit=5` |

**응답**

성공적인 응답은 액세스 권한이 있는 오퍼와 함께 있는 개인화된 오퍼 목록을 반환합니다.

```json
{
    "results": [
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
    ],
    "count": 1,
    "total": 1,
    "_links": {
        "self": {
            "href": "/offers?offer-type=personalized&href={SELF_HREF}",
            "type": "application/json"
        }
    }
}
```
