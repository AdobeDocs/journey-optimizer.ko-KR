---
title: 대체 오퍼 나열
description: 다른 오퍼에 대한 자격이 없는 경우 고객에게 대체 오퍼가 전송됩니다.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 4%

---

# 대체 오퍼 나열

다른 오퍼에 대한 자격이 없는 경우 고객에게 대체 오퍼가 전송됩니다. 대체 오퍼를 만드는 단계는 오퍼를 만들 때와 같이 하나 이상의 표현을 만드는 데 포함됩니다.

[!DNL Offer Library] API에 대한 단일 GET 요청을 수행하여 컨테이너 내의 모든 폴백 오퍼의 목록을 볼 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FALLBACK_OFFER}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 폴백 오퍼가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FALLBACK_OFFER}` | 폴백 오퍼와 연관된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1` |
| `{QUERY_PARAMS}` | 결과를 필터링하는 선택적 쿼리 매개 변수입니다. | `limit=1` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 쿼리 매개 변수 사용

쿼리 매개 변수를 사용하여 리소스를 나열할 때 결과를 페이지 및 필터링할 수 있습니다.

### 페이징

페이징 시 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `q` | 선택한 필드에서 검색할 선택적 쿼리 문자열. 쿼리 문자열은 소문자를 구분해야 하며 큰 따옴표로 묶어서 토큰화되지 않도록 하고 특수 문자를 escape할 수 있습니다. `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 문자는 특별한 의미를 가지며 쿼리 문자열에 나타날 때 백슬래시로 이스케이프해야 합니다. | `default` |
| `qop` | q 쿼리 문자열 매개 변수의 값에 AND 또는 OR 연산자를 적용합니다. | `AND` / `OR` |
| `field` | 검색을 제한할 선택적 필드 목록입니다. 다음과 같이 이 매개 변수를 반복할 수 있습니다.field=field1[,field=field2,..] 및 (경로 표현식은 _instance.xdm:name과 같은 점으로 구분된 경로의 형태임) | `_instance.xdm:name` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 제목(`orderby=-title`) 앞에 `-`을 추가하면 제목별로 내림차순(Z-A)으로 항목이 정렬됩니다. | `-repo:createdDate` |
| `limit` | 반환된 폴백 오퍼 수를 제한합니다. | `limit=5` |

**응답**

성공적인 응답은 액세스할 수 있는 컨테이너 내에 있는 폴백 오퍼 목록을 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1",
    "requestTime": "2020-10-22T07:12:30.923768Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-17T15:18:20.657299Z",
                "repo:lastModifiedDate": "2020-10-02T02:34:48.034583Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "F1: Web fallback ",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "xdm:content": "aaa",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json",
                                    "repo:name": "aa"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201b2150d98c2"
                        },
                        {
                            "xdm:components": [
                                {
                                    "xdm:content": "bb",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                                    "dc:format": "text/html",
                                    "repo:name": "bb"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201c34354a2b4"
                        },
                        {
                            "xdm:components": [
                                {
                                    "xdm:deliveryURL": "https://mysite.com",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "dc:format": "image/png",
                                    "repo:name": "ll"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122207eddb05205a"
                        }
                    ],
                    "xdm:status": "approved",
                    "xdm:tags": [],
                    "@id": "xcore:fallback-offer:122206064e0d98df"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5#053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 5,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=053bc610-f8f9-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
