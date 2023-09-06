---
title: 컬렉션 수식어 목록 만들기
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 6%

---

# 컬렉션 수식어 목록 만들기 {#list-tags}

컬렉션 한정자(이전의 &quot;태그&quot;라고 함)를 사용하면 오퍼를 보다 효율적으로 구성하고 정렬할 수 있습니다. 예를 들어 블랙 프라이데이 오퍼에 &quot;블랙 프라이데이&quot; 컬렉션 한정자를 사용하여 레이블을 지정할 수 있습니다. 그런 다음 오퍼 라이브러리의 검색 기능을 사용하여 해당 컬렉션 한정자를 사용하는 모든 오퍼를 쉽게 찾을 수 있습니다.

컬렉션 한정자를 사용하여 오퍼를 컬렉션으로 함께 그룹화할 수도 있습니다. 자세한 내용은 다음 자습서를 참조하십시오. [컬렉션 만들기](../../../offer-library/creating-collections.md).

에 대한 단일 GET 요청을 수행하여 모든 컬렉션 한정자 목록을 볼 수 있습니다. [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 결과를 필터링 기준으로 사용할 선택적 쿼리 매개 변수입니다. | `limit=2` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
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
| `property` | 선택적 속성 필터: <br> <ul> - 속성은 AND 작업별로 그룹화됩니다. <br><br> - 매개 변수는 다음과 같이 반복될 수 있습니다. property=<property-expr>[&amp;속성=<property-expr2>...] 또는 속성=<property-expr1>[,<property-expr2>...] <br><br> - 속성 표현식이 형식입니다. [!]필드[op]값, 옵트인 [==!=,&lt;=,>=,&lt;,>,~], 정규 표현식 지원 | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 엔티티 수를 제한합니다. | `limit=5` |

**응답**

성공적인 응답은 존재하는 컬렉션 한정자 목록을 반환합니다.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
