---
title: 의사 결정 규칙 삭제
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제한입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 5%

---

# 의사 결정 규칙 삭제

의사 결정 규칙을 제거(DELETE)해야 하는 경우가 있습니다. 테넌트 컨테이너에서 만든 의사 결정 규칙만 삭제할 수 있습니다. 이 작업은 DELETE 요청을 [!DNL Offer Library] 삭제할 의사 결정 규칙의 인스턴스 ID를 사용하는 API입니다.

**API 형식**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정 규칙이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 업데이트할 의사 결정 규칙의 인스턴스 ID입니다. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**요청**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 HTTP 상태 202(컨텐츠 없음) 및 빈 본문을 반환합니다.

의사 결정 규칙에 조회(GET) 요청을 시도하여 삭제를 확인할 수 있습니다. 요청에 Accept 헤더를 포함해야 하지만 결정 규칙이 컨테이너에서 제거되었기 때문에 HTTP 상태 404(찾을 수 없음)를 받아야 합니다.
