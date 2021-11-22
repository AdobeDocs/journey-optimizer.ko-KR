---
title: 결정 삭제
description: 결정에는 오퍼의 선택을 알리는 논리가 포함되어 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 5%

---

# 의사 결정 삭제

간혹 결정(DELETE 활동)을 제거(오퍼 활동)해야 할 수도 있습니다. 테넌트 컨테이너에서 생성하는 결정만 삭제할 수 있습니다. 이 작업은 DELETE 요청을 [!DNL Offer Library] 삭제할 대체 오퍼의 $id를 사용하는 API입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 결정의 인스턴스 ID입니다. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 202(컨텐츠 없음) 및 빈 본문을 반환합니다.

결정에 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 요청에 Accept 헤더를 포함해야 하지만 결정이 컨테이너에서 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 받아야 합니다.
