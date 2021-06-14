---
title: 태그 조회
description: 태그를 사용하면 오퍼를 보다 잘 구성하고 정렬할 수 있습니다.
feature: 오퍼
topic: 통합
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 4%

---

# 태그 조회

`@id` 태그 또는 요청 경로에 있는 태그의 이름을 포함하는 [!DNL Offer Library] API에 GET 요청을 하여 특정 태그를 찾을 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 태그가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | 태그와 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `id` | 엔티티의 `@id` 속성과 일치하는 데 사용되는 문자열입니다. 문자열이 정확히 일치합니다. 매개 변수 `id` 및 `name`은(는) 함께 사용할 수 없습니다. | `xcore:tag:124e147572cd7866` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열입니다. 문자열이 정확히 일치하고 대문자와 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name`은(는) 함께 사용할 수 없습니다 | `Holiday sales and promotions` |

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

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유한 태그 `@id`에 대한 정보를 포함하는 태그의 세부 사항을 반환합니다.

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
