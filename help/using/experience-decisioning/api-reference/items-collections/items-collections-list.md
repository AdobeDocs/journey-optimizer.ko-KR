---
title: 목록 항목 컬렉션
description: 컬렉션을 사용하면 환경 설정에 따라 결정 항목을 분류하고 그룹화할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 10%

---


# 목록 항목 컬렉션 {#list-decision-items}

항목 컬렉션이라고도 하는 컬렉션을 사용하면 환경 설정에 따라 결정 항목을 분류하고 그룹화할 수 있습니다. 이러한 범주는 결정 항목의 속성을 활용하는 규칙을 작성하여 생성됩니다.

오퍼 라이브러리 API에 대한 단일 GET 요청을 수행하여 모든 항목 컬렉션의 목록을 볼 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/item-collections?{QUERY_PARAMS}
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
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}..] 또는 property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}..]</li><li>속성 표현식이 `[!]field[op]value` 형식이며 `[==,!=,<=,>=,<,>,~]`에 `op`이(가) 있어 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복될 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 엔티티 수를 제한합니다. | `limit=5` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 항목 컬렉션 목록을 반환합니다.

```json
{
    "results": [
        {
            "created": "2024-01-31T18:28:52.888Z",
            "modified": "2024-06-28T19:44:13.112Z",
            "etag": 7,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection1234",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
                }
            ],
            "tags": []
        },
        {
            "created": "2024-06-10T16:02:57.878Z",
            "modified": "2024-06-10T16:02:57.878Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection5678",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"greater than\",\"value\":{\"left\":\"_<imsOrg>.some_integer\",\"right\":100}}"
                }
            ],
            "tags": []
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/item-collections?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/item-collections?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
