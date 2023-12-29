---
title: 컬렉션 삭제
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 9%

---

# 컬렉션 삭제 {#delete-collection}

경우에 따라 컬렉션을 제거(DELETE)해야 할 수 있습니다. 이 작업은 다음에 대한 DELETE 요청을 수행함으로써 수행됩니다. [!DNL Offer Library] 를 사용하는 API `id` 을(를) 삭제하려는 컬렉션입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 삭제하려는 엔티티의 ID입니다. | `offerCollection1234` |

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

컬렉션에 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 컬렉션이 제거되었으므로 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
