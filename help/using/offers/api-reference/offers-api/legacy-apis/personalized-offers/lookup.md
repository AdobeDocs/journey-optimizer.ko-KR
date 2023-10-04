---
title: 개인화된 오퍼 조회
description: 맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2e30b155-688b-432b-a703-d09de12ebdfd
source-git-commit: a8bb58489c708f444d1fad193c8dc70d7e1a97de
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# 개인화된 오퍼 조회 {#look-up-personalized-offer}

맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.

에 GET 요청을 하여 개인화된 특정 오퍼를 조회할 수 있습니다. **오퍼 라이브러리** 개인화된 오퍼를 포함하는 API `@id` 또는 요청 경로에 있는 개인화된 오퍼의 이름입니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 개인화된 오퍼가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | 개인화된 오퍼와 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | 를 일치시키는 데 사용되는 문자열 `@id` 엔티티의 속성입니다. 문자열이 정확하게 일치합니다. 매개 변수 &quot;id&quot;와 &quot;name&quot;은 함께 사용할 수 없습니다. | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열. 문자열은 대소문자를 사용하여 정확히 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없음 | `Discount offer` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유한 개인화된 오퍼에 대한 정보를 포함하여 배치 세부 정보를 반환합니다 `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2020-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2020-10-20T20:01:02.927874Z",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2020-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                }
            }
        ],
        "total": 1,
        "count": 1
    }
}
```
