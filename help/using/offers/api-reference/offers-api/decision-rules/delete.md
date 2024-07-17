---
title: 결정 규칙 삭제
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# 의사 결정 규칙 삭제 {#delete-decision-rule}

때때로 결정 규칙을 제거(DELETE)해야 할 수 있습니다. 이 작업은 삭제할 결정 규칙의 `id`을(를) 사용하여 [!DNL Offer Library] API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `offerRule1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

결정 규칙에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있으며 결정 규칙이 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
