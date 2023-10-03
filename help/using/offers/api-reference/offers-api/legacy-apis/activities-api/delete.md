---
title: 결정 삭제
description: 결정에는 오퍼의 선택을 알려주는 논리가 포함되어 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: ef22b6183c7646cca8636f4a7e4dd87c8f88e8ce
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 8%

---


# 의사 결정 삭제 {#delete-decision}

결정을 제거(DELETE)해야 하는 경우도 있습니다. 테넌트 컨테이너에서 만드는 의사 결정만 삭제할 수 있습니다. 이 작업은 다음에 대한 DELETE 요청을 수행함으로써 수행됩니다. [!DNL Offer Library] 삭제하려는 대체 오퍼의 $id를 사용하는 API입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정이 위치한 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 결정의 인스턴스 ID입니다. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
	@@ -37,6 +35,6 @@ curl -X DELETE \

**Response**

A successful response returns HTTP status 202 (No Content) and a blank body.

You can confirm the deletion by attempting a lookup (GET) request to the decision. You will need to include an Accept header in the request, but should receive an HTTP status 404 (Not Found) because the decision has been removed from the container.

