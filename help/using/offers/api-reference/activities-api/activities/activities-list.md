---
title: 의사 결정 나열
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 7%

---

# 의사 결정 나열 {#list-decisions}

결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.

에 대한 단일 GET 요청을 수행하여 모든 의사 결정 목록을 볼 수 있습니다. [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-decisions?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 결과를 필터링 기준으로 사용할 선택적 쿼리 매개 변수입니다. | `limit=2` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions?limit=2' \
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

성공적인 응답은 액세스 권한이 있는 결정 목록을 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2020-10-21T22:38:32.838180Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "286f6f80-026b-11eb-9439-ad36e372cbf1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 5,
                "repo:createdDate": "2020-09-29T15:48:02.808677Z",
                "repo:lastModifiedDate": "2020-10-15T15:49:26.673560Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "A2: Cross Channel Activity",
                    "xdm:endDate": "2020-10-09T07:00:00.000Z",
                    "xdm:startDate": "2020-09-29T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        },
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122201b2150d98c2"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:1222058c3f0d98de"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:12317fe6aeec9330"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2020-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2020-10-14T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:124527ab00b2ebbc"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 7,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=4e0206d0-0e6a-11eb-884a-c1a1104e3d7d&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
