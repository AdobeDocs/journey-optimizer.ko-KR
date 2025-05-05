---
title: 의사 결정 항목 나열
description: 의사 결정 항목은 만들고 컬렉션 및 카탈로그로 구성할 수 있는 마케팅 오퍼입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 12%

---


# 의사 결정 항목 나열 {#list-decision-items}

Journey Optimizer를 사용하면 결정 항목이라고 하는 마케팅 오퍼를 생성하여 중앙 집중식 카탈로그 및 컬렉션으로 구성할 수 있습니다. 요구 사항에 맞게 정확하게 조정할 수 있도록 설계된 표준 및 사용자 지정 속성으로 구성됩니다. 또한 의사 결정 항목을 표시할 대상을 정의할 수 있는 프로필 제약 조건을 통합합니다.

오퍼 라이브러리 API에 대한 단일 GET 요청을 수행하여 모든 의사 결정 항목의 목록을 볼 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-items?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 결과를 필터링 기준으로 사용할 선택적 쿼리 매개 변수입니다. | `limit=2` |

## 쿼리 매개 변수 사용 {#using-query-parameters}

쿼리 매개 변수를 사용하여 리소스를 나열할 때 결과를 페이지로 지정하고 필터링할 수 있습니다.

### 페이징 {#paging}

페이징에 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}..] 또는 property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}..]</li><li>속성 표현식이 `[ !]field[op]value` 형식이며 `[==,!=,<=,>=,<,>,~]`에 `op`이(가) 있어 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복될 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 엔티티 수를 제한합니다. | `limit=5` |

**요청**

```shell
curl -X GET '<https://platform.adobe.io/data/core/dps/offer-items?limit=2>' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 오퍼 항목 목록을 반환합니다. `_<imsOrg>` 노드에는 사용자 지정 결정 항목 특성이 있습니다.

```json
{
    "results": [
        {
            "created": "2024-06-10T16:00:34.014Z",
            "modified": "2024-07-09T22:59:21.507Z",
            "etag": 1,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem5678",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "draft"
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
                        "itemID": "offerItem5678",
                        "itemLabels": [],
                        "itemName": "Offer Item One",
                        "itemPriority": 1,
                        "itemTags": []
                    }
                }
            },
            "_<imsOrg>": {
                "some_field": "some value"
            }
        },
        {
            "created": "2024-06-04T17:51:52.849Z",
            "modified": "2024-06-28T18:29:27.951Z",
            "etag": 5,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem1234",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "frequencyCappingConstraints": [],
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "approved"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-01T07:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "profileConstraintType": "none"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem1234",
                        "itemLabels": [],
                        "itemName": "Offer Item Two",
                        "itemPriority": 2,
                        "itemTags": []
                    }
                }
            },
            "YOUR_CUSTOM_ATTRIBUTES": {
                "some_field": "some value",
                "some_boolean_field": true
            }
        }
    ],
    "count": 2,
    "total": 844,
    "_links": {
        "self": {
            "href": "/offer-items?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-items?orderby=-modified&limit=2&start=2024-06-28T03:44:15.630Z",
            "type": "application/json"
        }
    }
}
```
