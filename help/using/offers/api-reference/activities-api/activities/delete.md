---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 결정 삭제
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 22%

---

# 의사 결정 삭제 {#delete-decision}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../../../experience-decisioning/gs-experience-decisioning.md)


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
