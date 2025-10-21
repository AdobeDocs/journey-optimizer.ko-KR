---
title: 결정 삭제
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# 의사 결정 삭제 {#delete-decision}

결정을 제거(DELETE)해야 하는 경우가 있습니다. 이 작업은 삭제할 결정의 [!DNL Offer Library]을(를) 사용하여 `id` API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `offerDecision1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

결정에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 결정이 제거되었으므로 HTTP 상태 404(찾을 수 없음)를 받아야 합니다.
