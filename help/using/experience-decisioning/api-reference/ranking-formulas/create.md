---
title: 등급 수식 만들기
description: 등급 수식 을 사용하면 항목의 등급을 매기는 데 사용되는 점수 함수를 정의할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# 등급 수식 만들기 {#create-ranking-formula}

오퍼 라이브러리 API에 POST 요청을 하여 등급 공식을 만들 수 있습니다.

**Accept 및 Content-Type 헤더**

다음 표는 요청 헤더의 콘텐츠 유형 필드를 구성하는 유효한 값을 보여 줍니다.

| 헤더 이름 | 값 |
| --------- | ----------- | 
| Content-Type | application/json |

**API 형식**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |

**요청**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
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

**응답**

응답이 성공하면 `id`을(를) 포함하여 새로 만든 순위 수식의 세부 정보가 반환됩니다. 이후 단계에서 `id`을(를) 사용하여 순위 공식을 업데이트하거나 삭제할 수 있습니다.

```json
{
    "etag": 1,
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
