---
title: 개인화된 오퍼 삭제
description: 맞춤형 오퍼는 자격 규칙 및 제한에 따라 사용자 정의 가능한 마케팅 메시지입니다.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 7%

---

# 개인화된 오퍼 삭제 {#delete-personalized-offer}

개인화된 오퍼를 제거(DELETE)해야 하는 경우가 있습니다. 이 작업은 삭제하려는 개인화된 오퍼의 ID를 사용하여 [!DNL Offer Library] API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `personalizedOffer1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

개인화된 오퍼에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있으며, 개인화된 오퍼가 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
