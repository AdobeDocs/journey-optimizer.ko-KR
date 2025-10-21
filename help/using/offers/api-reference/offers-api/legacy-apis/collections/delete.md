---
title: 컬렉션 삭제
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 351d1f44-f3dc-49f9-bc3d-c775dad3cad4
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 7%

---

# 컬렉션 삭제 {#delete-collection}

경우에 따라 컬렉션을 제거(DELETE)해야 할 수 있습니다. 테넌트 컨테이너에서 만드는 컬렉션만 삭제할 수 있습니다. 이 작업은 삭제하려는 컬렉션의 $id를 사용하여 [!DNL Offer Library] API에 대한 DELETE 요청을 수행함으로써 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 컬렉션이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 업데이트하려는 컬렉션의 인스턴스 ID입니다. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 202(콘텐츠 없음) 및 빈 본문을 반환합니다.

컬렉션에 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 요청에 Accept 헤더를 포함해야 하지만 컬렉션이 컨테이너에서 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 수신해야 합니다.
