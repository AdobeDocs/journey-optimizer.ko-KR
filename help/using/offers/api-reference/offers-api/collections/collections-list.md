---
title: 컬렉션 나열
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 오퍼의 하위 집합입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 컬렉션 나열 {#list-collections}

컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 오퍼의 하위 집합입니다.

에 대한 단일 GET 요청을 수행하여 컨테이너 내의 모든 컬렉션 목록을 볼 수 있습니다 [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 컬렉션이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | 컬렉션과 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `{QUERY_PARAMS}` | 결과를 기준으로 필터링할 선택적 쿼리 매개 변수입니다. | `limit=1` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 쿼리 매개 변수 사용 {#using-query-parameters}

리소스를 나열할 때 쿼리 매개 변수를 사용하여 결과를 페이지 및 필터링할 수 있습니다.

### 페이징 {#paging}

페이징의 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `q` | 선택한 필드에서 검색할 선택적 쿼리 문자열입니다. 쿼리 문자열은 소문자여야 하며 큰따옴표로 묶어서 토큰화되지 않도록 하고 특수 문자를 이스케이프 처리할 수 있습니다. 문자 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 에는 특별한 의미가 있으며 쿼리 문자열에 나타나면 백슬래시로 이스케이프해야 합니다. | `demo collection` |
| `qop` | q 쿼리 문자열 매개 변수의 값에 AND 또는 OR 연산자를 적용합니다. | `AND` / `OR` |
| `field` | 검색을 다음으로 제한할 필드 선택 사항입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. field=field1[,field=field2,..] 및 (경로 표현식은 _instance.xdm:name과 같이 점으로 구분된 경로의 형식입니다.) | `_instance.xdm:name` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 추가 `-` 이전 제목 (`orderby=-title`)은 제목별로 항목을 내림차순으로 정렬합니다(Z-A). | `-repo:createdDate` |
| `limit` | 반환된 컬렉션 수를 제한합니다. | `limit=5` |

**응답**

성공적으로 응답하면 액세스 권한이 있는 컨테이너 내에 있는 컬렉션 목록이 반환됩니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2020-10-21T21:14:19.282175Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2020-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:tag:124bd3de7f598dd8"
                    ],
                    "xdm:name": "Mobile Demo",
                    "xdm:filterType": "anyTags",
                    "@id": "xcore:offer-filter:124bd44648f17ec1"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:36:29.272451Z",
                "repo:lastModifiedDate": "2020-09-17T14:36:29.272451Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:personalized-offer:1221fbedfa4d98b0"
                    ],
                    "xdm:name": "demo collection",
                    "xdm:filterType": "offers",
                    "@id": "xcore:offer-filter:1221fc71c74d98b4"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
