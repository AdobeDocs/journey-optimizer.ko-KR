---
title: 대체 오퍼 삭제
description: 다른 오퍼에 적합하지 않은 경우 고객에게 대체 오퍼가 전송됩니다
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 10%

---


# 대체 오퍼 삭제 {#delete-fallback-offer}

대체 오퍼를 제거(DELETE)해야 하는 경우가 있습니다. 이 작업은 다음에 대한 DELETE 요청을 수행함으로써 수행됩니다. [!DNL Offer Library] 삭제하려는 대체 오퍼의 ID를 사용하는 API입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `fallbackOffer1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

오퍼에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있으며, 대체 오퍼가 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
