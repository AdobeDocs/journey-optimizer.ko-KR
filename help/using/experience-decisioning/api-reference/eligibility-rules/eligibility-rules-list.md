---
title: 목록 자격 규칙
description: 자격 규칙을 사용하면 프로필 속성 및 대상과 같이 타깃팅하려는 항목을 기반으로 적격 후보를 정의할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 4%

---

# 목록 자격 규칙 {#list-eligibilit-rules}

자격 규칙은 자격 조건을 정의하는 방법을 정의하는 PQL 규칙 표현식으로 구성됩니다.

오퍼 라이브러리 API에 대한 단일 GET 요청을 수행하여 모든 자격 규칙 목록을 볼 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdRule입니다. | `property=exdRule%3D%3Dtrue` |

## 쿼리 매개 변수 사용 {#using-query-parameters}

쿼리 매개 변수를 사용하여 리소스를 나열할 때 결과를 페이지로 지정하고 필터링할 수 있습니다.

### 페이징 {#paging}

페이징에 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `property` | 선택적 속성 필터: <ul><li>속성은 AND 작업별로 그룹화됩니다.</li><li>매개 변수는 다음과 같이 반복될 수 있습니다. property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}..] 또는 property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}..]</li><li>속성 표현식이 `[!]field[op]value` 형식이며 `[==,!=,<=,>=,<,>,~]`에 `op`이(가) 있어 정규 표현식을 지원합니다.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 이름 앞에 - 를 추가하면 (orderby=-name) 내림차순 (Z-A)으로 이름별로 항목이 정렬됩니다. 경로 표현식은 점으로 구분된 경로 형식입니다. 이 매개 변수는 다음과 같이 반복될 수 있습니다. `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 반환되는 엔티티 수를 제한합니다. | `limit=5` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?property=exdRule%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 액세스 권한이 있는 자격 규칙 목록을 반환합니다.

```json
{
    "results": [
        {
            "created": "2024-10-28T01:18:08.506Z",
            "modified": "2024-10-28T01:18:08.506Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19af09a9ae45a8d3",
            "name": "dasdsa",
            "description": "",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "dasdsa",
                "namespace": "ups"
            }
        },
        {
            "created": "2024-10-27T04:01:29.343Z",
            "modified": "2024-10-27T04:33:44.781Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19ade575cf95e584",
            "name": "nick test pes",
            "description": "dasdsad",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "dasdsad",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "nick test pes",
                "namespace": "ups",
                "estimates": [
                    {
                        "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                        "addressabilityText": "Of total",
                        "color": "#12805c",
                        "estimateData": {
                            "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                            "estimatedSize": 0,
                            "totalRows": 62088,
                            "percent": 0,
                            "standardError": 0,
                            "confidenceInterval": "95%",
                            "state": "RESULT_READY",
                            "profilesReadSoFar": 62088,
                            "numRowsToRead": 62088
                        },
                        "state": "RESULT_READY"
                    }
                ]
            }
        }
    ],
    "count": 2,
    "total": 229,
    "_links": {
        "self": {
            "href": "/offer-rules?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?orderby=-modified&limit=2&start=2024-10-27T01:24:51.785Z",
            "type": "application/json"
        }
    }
}
```
