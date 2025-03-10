---
title: 목록 등급 수식
description: 등급 수식 을 사용하면 항목의 등급을 매기는 데 사용되는 점수 함수를 정의할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 4%

---

# 목록 등급 수식 {#list-ranking-formulas}

순위 공식은 순위를 매기는 방법을 정의하는 순위 함수로 구성됩니다.

오퍼 라이브러리 API에 대한 단일 GET 요청을 수행하여 모든 등급 수식 목록을 볼 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/ranking-formulas?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdFunction. | `property=exdFunction%3D%3Dtrue` |

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
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas?property=exdFunction%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 등급 수식 목록을 반환합니다.

```json
{
    "results": [
        {
            "created": "2024-08-08T23:45:15.380Z",
            "modified": "2024-10-22T18:15:05.909Z",
            "etag": 36,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/ranking-function"
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps:ranking-function:1947f5372cc4ed74",
            "name": "[Do not delete] - Cypress e2e - edit",
            "description": "some description",
            "returnType": {
                "type": "INTEGER"
            },
            "exdFunction": true,
            "expression": {
                "type": "PQL",
                "format": "pql/text",
                "value": "42 = 11"
            }
        },
        {
            "created": "2024-05-03T13:06:22.361Z",
            "modified": "2024-10-18T22:47:35.396Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/ranking-function;version=0.3"
            ],
            "createdBy": "FD62391F5B44DF970A494124@AdobeID",
            "lastModifiedBy": "6F8A6FF05F4011C40A494005@AdobeID",
            "id": "xcore:ranking-function:18ca80c5b15c5e11",
            "name": "doc test exd",
            "description": "",
            "returnType": {
                "type": "INTEGER"
            },
            "exdFunction": true,
            "expression": {
                "type": "PQL",
                "format": "pql/text",
                "value": "false"
            }
        }
    ],
    "count": 2,
    "total": 50,
    "_links": {
        "self": {
            "href": "/ranking-formulas?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/ranking-formulas?orderby=-modified&limit=2&start=2024-10-18T22:22:35.048Z",
            "type": "application/json"
        }
    }
}
```
