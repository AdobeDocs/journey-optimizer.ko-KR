---
title: 등급 수식 업데이트
description: 등급 수식 을 사용하면 항목의 등급을 매기는 데 사용되는 점수 함수를 정의할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 6%

---

# 순위 공식 업데이트 {#update-ranking-formula}

오퍼 라이브러리 API에 PUT 요청을 하여 등급 공식을 수정하거나 업데이트할 수 있습니다.

사용 가능한 작업을 포함하여 JSON PUT에 대한 자세한 내용은 공식 [JSON PUT 설명서](http://jsonpatch.com/)를 참조하십시오.

**Accept 및 Content-Type 헤더**

다음 표는 요청 헤더의 콘텐츠 유형 필드를 구성하는 유효한 값을 보여 줍니다.

| 헤더 이름 | 값 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API 형식**

```http
PUT /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `rankingFormula1234` |

**요청**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Ranking Function DPS",
    "description": "Ranking  function description",
    "isPure": true,
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `value` | 매개 변수를 업데이트할 새 값입니다. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업은 `add`, `replace`, `remove`, `copy` 및 `test`입니다. |

**응답**

성공적인 응답은 ID를 포함하여 순위 공식의 업데이트된 세부 정보를 반환합니다.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
