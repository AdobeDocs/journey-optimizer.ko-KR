---
title: 의사 결정 규칙 나열
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제한입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 5%

---

# 의사 결정 규칙 나열 {#list-decision-rules}

의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제한입니다. 컨테이너에서 단일 GET 요청을 수행하여 기존 의사 결정 규칙 목록을 볼 수 있습니다 [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정 규칙이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | 의사 결정 규칙과 연관된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `{QUERY_PARAMS}` | 결과를 기준으로 필터링할 선택적 쿼리 매개 변수입니다. | `limit=1` |

## 쿼리 매개 변수 사용 {#using-query-parameters}

리소스를 나열할 때 쿼리 매개 변수를 사용하여 결과를 페이지 및 필터링할 수 있습니다.

### 페이징 {#paging}

페이징의 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `q` | 선택한 필드에서 검색할 선택적 쿼리 문자열입니다. 쿼리 문자열은 소문자여야 하며 큰따옴표로 묶어서 토큰화되지 않도록 하고 특수 문자를 이스케이프 처리할 수 있습니다. 문자 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 에는 특별한 의미가 있으며 쿼리 문자열에 나타나면 백슬래시로 이스케이프해야 합니다. | `default` |
| `qop` | q 쿼리 문자열 매개 변수의 값에 AND 또는 OR 연산자를 적용합니다. | `AND` / `OR` |
| `field` | 검색을 다음으로 제한할 필드 선택 사항입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. field=field1[,field=field2,..] 및 (경로 표현식은 _instance.xdm:name과 같이 점으로 구분된 경로의 형식입니다.) | `_instance.xdm:name` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 추가 `-` 이전 제목 (`orderby=-title`)은 제목별로 항목을 내림차순으로 정렬합니다(Z-A). | `-repo:createdDate` |
| `limit` | 반환된 의사 결정 규칙 수를 제한합니다. | `limit=5` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 컨테이너 내에 있는 의사 결정 규칙 목록을 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2020-10-22T04:14:12.676802Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "36693c30-0377-11eb-9dd8-d781cc064407",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-30T23:46:51.379003Z",
                "repo:lastModifiedDate": "2020-10-02T05:06:36.780806Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Qualified for mortgage products",
                    "offerui:segmentModel": {
                        "name": "Qualified for mortgage products",
                        "canHaveFolder": true,
                        "isMissingAnsibleModel": false,
                        "description": "",
                        "deprecated": {
                            "reason": "",
                            "status": false
                        },
                        "schema": {
                            "name": "_xdm.context.profile",
                            "id": "some id"
                        },
                        "schemaName": "",
                        "expression": {
                            "xEventAttributesContainer": {
                                "itemType": "eventTypeCardContainer",
                                "logicalOperator": "then",
                                "exclude": false,
                                "items": []
                            },
                            "logicalOperator": "and",
                            "isValid": true,
                            "profileAttributesContainer": {
                                "itemType": "segmentContainer",
                                "logicalOperator": "and",
                                "exclude": false,
                                "items": [
                                    {
                                        "component": {
                                            "__entity__": true,
                                            "id": "profile._xcoree2etesting.productCategory",
                                            "type": "n"
                                        },
                                        "isPlaceholder": false,
                                        "comparisonType": "equals",
                                        "value": [
                                            "mortgage"
                                        ]
                                    }
                                ]
                            }
                        },
                        "mergePolicyId": "3558157a-19cb-40b4-ba13-a5f5ce31b011",
                        "namespace": "ups"
                    },
                    "xdm:condition": {
                        "xdm:format": "pql/text",
                        "xdm:type": "PQL",
                        "xdm:value": "_xcoree2etesting.productCategory.equals(\"mortgage\", false)"
                    },
                    "xdm:definedOn": {},
                    "xdm:description": "",
                    "@id": "xcore:eligibility-rule:12333714edbf49e6"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#36693c30-0377-11eb-9dd8-d781cc064407",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/36693c30-0377-11eb-9dd8-d781cc064407",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=36693c30-0377-11eb-9dd8-d781cc064407&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
