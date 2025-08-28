---
title: 결정 조회
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 99159704-fa39-47ff-b445-0cd6b325007d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# 결정 조회 {#look-up-decision}

결정 [!DNL Offer Library] 또는 요청 경로에 결정 이름이 포함된 `@id` API에 대한 GET 요청을 수행하여 특정 결정을 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정이 위치한 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | 의사 결정과 연관된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `id` | 엔터티의 `@id` 속성과 일치하는 데 사용되는 문자열입니다. 문자열이 정확하게 일치합니다. `id` 및 `name` 매개 변수는 함께 사용할 수 없습니다. | `xcore:offer-activity:124527ab00b2ebbc` |
| `name` | 엔터티의 xdm:name 속성과 일치하는 데 사용되는 문자열입니다. 문자열은 대소문자를 사용하여 정확히 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 &quot;id&quot;와 &quot;name&quot;은 함께 사용할 수 없습니다. | `LBAR` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유 결정 `@id`에 대한 정보를 포함하여 배치 세부 정보를 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2023-10-19T19:50:08.047489Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
    "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
    ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2023-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2023-10-14T07:00:00.000Z",
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
        "total": 1,
        "count": 1
            },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
            }   
        }
}
```
