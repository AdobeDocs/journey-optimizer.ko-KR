---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 대체 오퍼 삭제
description: 다른 오퍼에 적합하지 않은 경우 고객에게 대체 오퍼가 전송됩니다
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 22%

---


# 대체 오퍼 삭제 {#delete-fallback-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../experience-decisioning/gs-experience-decisioning.md)


대체 오퍼를 제거(DELETE)해야 하는 경우가 있습니다. 이 작업은 삭제하려는 대체 오퍼의 ID를 사용하여 [!DNL Offer Library] API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

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
