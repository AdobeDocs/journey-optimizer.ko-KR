---
title: 컬렉션 조회
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 오퍼의 하위 집합입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 컬렉션 조회 {#look-up-collection}

컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 오퍼의 하위 집합입니다.

에 GET 요청을 작성하여 특정 컬렉션을 조회할 수 있습니다 [!DNL Offer Library] 컬렉션을 포함하는 API `@id` 또는 요청 경로에 있는 컬렉션의 이름입니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 컬렉션이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | 컬렉션과 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `id` | 와 일치하는 `@id` 엔티티의 속성입니다. 문자열이 정확히 일치합니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없습니다. | `xcore:offer-filter:124bd44648f17ec1` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열입니다. 문자열이 정확히 일치하고 대문자와 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없습니다. | `Mobile demo` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유 컬렉션에 대한 정보를 포함한 배치 세부 사항을 반환합니다 `@id`.

```json
{
    "containerId": "ab574eca-f7a9-38d0-b3d9-297376ca9ee2",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2020-10-21T21:29:27.329070Z",
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
                "_score": 0,
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
                        "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
