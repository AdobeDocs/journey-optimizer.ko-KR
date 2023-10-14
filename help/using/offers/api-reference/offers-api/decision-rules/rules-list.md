---
title: 의사 결정 규칙 나열
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---

# 의사 결정 규칙 나열 {#list-decision-rules}

의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다. 에 대한 단일 GET 요청을 수행하여 컨테이너 내의 기존 의사 결정 규칙 목록을 볼 수 있습니다. [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
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
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] 또는 속성={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>속성 표현식이 형식입니다. `[!]field[op]value`, 포함 `op` 위치: `[==,!=,<=,>=,<,>,~]`, 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 엔티티 수를 제한합니다. | `limit=5` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 의사 결정 규칙 목록을 반환합니다.

```json
{
     "results": [
        {
            "created": "2022-09-16T18:59:53.651+00:00",
            "modified": "2022-09-16T18:59:53.651+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule1234",
            "name": "Californians with one or more purchases greater than $1000",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
                 }
        },
        {
            "created": "2023-03-06T15:11:42.178+00:00",
            "modified": "2023-03-06T15:11:42.178+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule5678",
            "name": "People born after 1981",
            "description": "Persons with the birth date after 1981",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "person.birthDate occurs after date(1981, 1, 1)"
            }
        }
    ],
    "count": 2,
    "total": 25,
    "_links": {
        "self": {
            "href": "/offer-rules?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
