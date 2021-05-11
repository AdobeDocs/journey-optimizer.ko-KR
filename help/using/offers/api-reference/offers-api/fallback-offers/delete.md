---
title: 대체 오퍼 삭제
description: 다른 오퍼에 대한 자격이 없는 경우 고객에게 대체 오퍼가 전송됩니다.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 8%

---

# 대체 오퍼 삭제

경우에 따라 대체 오퍼를 제거(DELETE)해야 할 수 있습니다. 테넌트 컨테이너에서 만든 폴백 오퍼만 삭제할 수 있습니다. 삭제하려는 폴백 오퍼의 $id를 사용하여 [!DNL Offer Library] API에 DELETE 요청을 수행하여 수행됩니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 폴백 오퍼가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 폴백 오퍼의 인스턴스 ID입니다. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 202(콘텐츠 없음) 및 빈 본문을 반환합니다.

대체 오퍼에 대한 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 요청에 수락 헤더를 포함해야 하지만, 대체 오퍼가 컨테이너에서 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 받아야 합니다.
