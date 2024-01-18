---
title: 컬렉션 한정자 삭제
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 컬렉션 수식어 삭제 {#delete-tag}

컬렉션 한정자(이전에는 &quot;태그&quot;라고 함)를 제거(DELETE)해야 하는 경우가 있습니다. 이 작업은 삭제하려는 컬렉션 한정자의 ID를 사용하여 오퍼 라이브러리 API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `tag1234` |

**요청**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 200과 빈 본문을 반환합니다.

컬렉션 한정자에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 컬렉션 한정자가 제거되었으므로 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.