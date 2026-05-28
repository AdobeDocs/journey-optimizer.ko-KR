---
title: 의사 결정 항목 업데이트
description: 의사 결정 항목은 만들고 컬렉션 및 카탈로그로 구성할 수 있는 마케팅 오퍼입니다.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/5hMZmGEl--fCOFYxhy-wRRFh4JG7o-CHWDMKfA7rD78
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 5%

---

# 의사 결정 항목 업데이트 {#update-decision-items}

오퍼 라이브러리 API에 PATCH 요청을 하여 의사 결정 항목을 수정하거나 업데이트할 수 있습니다.

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 공식 [JSON 패치 설명서](https://jsonpatch.com/)를 참조하세요.

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `offerItem1234` |

**요청**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `value` | 매개 변수를 업데이트할 새 값입니다. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `op` | 수행할 작업의 유형입니다. 작업은 `add`, `replace`, `remove`, `copy` 및 `test`입니다. |

**응답**

성공적인 응답은 ID를 포함하여 업데이트된 항목의 세부 정보를 반환합니다. 이후 단계에서 이 ID를 사용하여 결정 항목을 업데이트하거나 삭제할 수 있습니다.

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
