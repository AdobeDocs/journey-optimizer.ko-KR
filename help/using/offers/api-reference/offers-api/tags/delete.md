---
title: 태그 삭제
description: 태그를 사용하면 오퍼를 보다 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 태그 삭제 {#delete-tag}

경우에 따라 태그를 제거(DELETE)해야 할 수 있습니다. 테넌트 컨테이너에서 만든 태그만 삭제할 수 있습니다. 이 작업은 DELETE 요청을 [!DNL Offer Library] 삭제할 태그의 $id를 사용하는 API입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 태그가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 업데이트할 태그의 인스턴스 ID입니다. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 202(컨텐츠 없음) 및 빈 본문을 반환합니다.

태그에 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 요청에 Accept 헤더를 포함해야 하지만 태그가 컨테이너에서 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 받아야 합니다.
