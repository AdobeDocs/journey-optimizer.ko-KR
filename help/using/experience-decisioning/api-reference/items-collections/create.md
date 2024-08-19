---
title: 항목 컬렉션 만들기
description: 컬렉션을 사용하면 환경 설정에 따라 결정 항목을 분류하고 그룹화할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---


# 항목 컬렉션 만들기 {#create-decision-items}

오퍼 라이브러리 API에 POST 요청을 하여 항목 컬렉션을 만들 수 있습니다.

**API 형식**

```http
POST /{ENDPOINT_PATH}/item-collections
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |

**요청**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/item-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{     
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
}'
```

**응답**

성공적인 응답은 ID를 포함하여 새로 생성된 결정 항목의 세부 사항을 반환합니다. 이후 단계에서 이 ID를 사용하여 결정 항목을 업데이트하거나 삭제할 수 있습니다.

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
