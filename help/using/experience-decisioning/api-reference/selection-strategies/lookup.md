---
title: 선택 전략 조회
description: 선택 전략은 오퍼를 결정하기 위한 제약 조건 및 등급 방법과 연관된 컬렉션으로 구성됩니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dcff8803404228bbed40e998d802bb6c0f4ac67e
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---


# 선택 전략 조회 {#list-selection-strategy}

요청 경로에 ID가 포함된 GET 라이브러리 API에 대한 오퍼 요청을 수행하여 특정 선택 전략을 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `selectionStrategy1234` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공한 응답은 선택 전략의 세부 정보를 반환합니다.

```json
{
    "created": "2024-02-08T03:01:50.924Z",
    "modified": "2024-02-16T23:03:03.019Z",
    "etag": 4,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "selectionStrategy1234",
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}
```
