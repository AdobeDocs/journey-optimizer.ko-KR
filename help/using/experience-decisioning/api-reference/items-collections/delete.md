---
title: 항목 컬렉션 삭제
description: 그룹 결정을 컬렉션으로 분류하는 방법을 알아봅니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---


# 항목 컬렉션 삭제 {#delete-decision-item}

경우에 따라 항목 컬렉션을 제거(DELETE)해야 할 수 있습니다. 이 작업은 삭제하려는 항목 컬렉션의 ID를 사용하여 오퍼 라이브러리 API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `itemCollections1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

항목 컬렉션에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 항목 컬렉션이 제거되었으므로 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
