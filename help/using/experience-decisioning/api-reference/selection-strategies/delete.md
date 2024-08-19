---
title: 선택 전략 삭제
description: 선택 전략은 오퍼를 결정하기 위한 제약 조건 및 등급 방법과 연관된 컬렉션으로 구성됩니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---


# 선택 전략 삭제 {#delete-selection-strategy}

경우에 따라 선택 전략을 제거(DELETE)해야 할 수 있습니다. 이 작업은 삭제하려는 선택 전략의 ID를 사용하여 오퍼 라이브러리 API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `selectionStrategy1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

선택 전략에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 선택 전략이 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
