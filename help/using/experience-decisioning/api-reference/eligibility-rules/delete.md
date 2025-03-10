---
title: 자격 규칙 삭제
description: 자격 규칙을 사용하면 프로필 속성 및 대상과 같이 타깃팅하려는 항목을 기반으로 적격 후보를 정의할 수 있습니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# 자격 규칙 삭제 {#delete-eligibility-rule}

경우에 따라 자격 규칙을 제거(DELETE)해야 할 수 있습니다. 이 작업은 삭제하려는 자격 규칙의 ID를 사용하여 오퍼 라이브러리 API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `rule1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

규칙에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 규칙이 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
