---
title: 컬렉션 한정자 조회
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 컬렉션 한정자 조회 {#look-up-tag}

에 GET 요청을 하여 특정 컬렉션 한정자(이전의 &quot;태그&quot;라고 함)를 조회할 수 있습니다. [!DNL Offer Library] 컬렉션 한정자를 포함하는 API `@id` 또는 요청 경로에 있는 컬렉션 한정자의 이름입니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 컬렉션 한정자가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | 컬렉션 한정자와 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `id` | 를 일치시키는 데 사용되는 문자열 `@id` 엔티티의 속성입니다. 문자열이 정확하게 일치합니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없습니다. | `xcore:tag:124e147572cd7866` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열. 문자열은 대소문자를 사용하여 정확히 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없음 | `Holiday sales and promotions` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유 컬렉션 구분자에 대한 정보를 포함하여 컬렉션 구분자의 세부 정보를 반환합니다 `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:35:28.233975Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-21T20:34:34.486296Z",
                "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Holiday sales and promotions",
                    "@id": "xcore:tag:124e147572cd7866"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#d48fd160-13dc-11eb-bc55-c11be7252432",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
