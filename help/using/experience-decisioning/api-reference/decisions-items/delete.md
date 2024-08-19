---
title: 결정 항목 삭제
description: 의사 결정 항목은 만들고 컬렉션 및 카탈로그로 구성할 수 있는 마케팅 오퍼입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---


# 결정 항목 삭제 {#delete-decision-item}

의사 결정 항목을 제거하려면 삭제할 의사 결정 항목의 ID를 사용하여 오퍼 라이브러리 API에 대한 DELETE 요청을 수행합니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `offerItem1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

결정 항목에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 결정 항목이 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
