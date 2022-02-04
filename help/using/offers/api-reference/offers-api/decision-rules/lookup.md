---
title: 의사 결정 규칙 조회
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제한입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 54368710-1021-43c0-87b7-5176cc6c72f7
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# 의사 결정 규칙 조회 {#lookup-decision-rule}

에 GET 요청을 수행하여 특정 의사 결정 규칙을 조회할 수 있습니다 [!DNL Offer Library] 결정 규칙을 포함하는 API `@id` 또는 요청 경로에 있는 의사 결정 규칙의 이름입니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정 규칙이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | 의사 결정 규칙과 연관된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `id` | 와 일치하는 `@id` 엔티티의 속성입니다. 문자열이 정확히 일치합니다. 매개 변수 s `id` 및 `name` 함께 사용할 수 없습니다. | `xcore:eligibility-rule:124e0faf5b8ee89b` |
| `name` | 엔티티의 xdm:name 속성과 일치하는 데 사용되는 문자열입니다. 문자열이 정확히 일치하고 대문자와 일치하지만 와일드카드 문자를 사용할 수 있습니다. 매개 변수 `id` 및 `name` 함께 사용할 수 없습니다. | `Sales rule` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유한 결정 규칙에 대한 정보를 포함하여 조회한 특정 결정 규칙의 세부 사항을 반환합니다 `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2020-10-21T20:14:08.153670Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-21T20:13:43.048666Z",
                "repo:lastModifiedDate": "2020-10-21T20:13:43.048666Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales rule",
                    "description": "Decisioning rule for sales",
                    "xdm:definedOn": {
                        "profile": {
                            "xdm:schema": {
                                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                                "version": "1"
                            },
                            "xdm:referencePaths": [
                                "person.name.firstName"
                            ]
                        }
                    },
                    "condition": {
                        "format": "pql/text",
                        "type": "PQL",
                        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
                    },
                    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
