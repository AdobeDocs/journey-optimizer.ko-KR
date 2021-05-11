---
title: 배치 검색
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# 배치 검색

배치 `@id` 또는 요청 경로의 배치 이름을 포함하는 [!DNL Offer Library] API에 GET 요청을 하여 특정 배치를 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 배치가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | 배치와 연관된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `id` | 엔티티의 `@id` 속성과 일치시키는 데 사용되는 문자열입니다. 문자열이 정확히 일치합니다. 매개 변수 `id` 및 `name`은(는) 함께 사용할 수 없습니다. | `xcore:offer-placement:124541309805b7e8` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열입니다. 이 문자열은 대문자화로 정확히 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name`은(는) 함께 사용할 수 없습니다. | `Sales and Promotions Placement` |

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유한 배치 `@id`에 대한 정보를 포함한 배치 세부 정보를 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T20:04:53.656503Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-21T19:57:09.837456Z",
                "repo:lastModifiedDate": "2020-10-21T19:59:10.700149Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales and Promotions Placement",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "A test placement to contain offers of sales and discounts",
                    "@id": "xcore:offer-placement:124e0be5699743d3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
