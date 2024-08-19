---
title: 항목 컬렉션 삭제
description: 컬렉션을 사용하면 환경 설정에 따라 결정 항목을 분류하고 그룹화할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
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
