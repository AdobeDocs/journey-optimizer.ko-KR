---
title: 의사 결정 항목 업데이트
description: 의사 결정 항목은 만들고 컬렉션 및 카탈로그로 구성할 수 있는 마케팅 오퍼입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# 의사 결정 항목 업데이트 {#update-decision-items}

오퍼 라이브러리 API에 PATCH 요청을 하여 의사 결정 항목을 수정하거나 업데이트할 수 있습니다.

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 공식 [JSON 패치 설명서](http://jsonpatch.com/)를 참조하세요.

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
