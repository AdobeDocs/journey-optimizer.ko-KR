---
title: Exd 배치 업데이트
description: 배치 확장은 오퍼를 결정하는 제한 및 등급 방법과 연관된 컬렉션으로 구성됩니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 6%

---

# exd 배치 업데이트 {#update-exd-placement}

오퍼 라이브러리 API에 PUT 요청을 하여 배치를 수정하거나 업데이트할 수 있습니다.

사용 가능한 작업을 포함하여 JSON PUT에 대한 자세한 내용은 공식 JSON PUT 설명서를 참조하십시오.

**Accept 및 Content-Type 헤더**

다음 표는 요청 헤더의 콘텐츠 유형 필드를 구성하는 유효한 값을 보여 줍니다.

| 매개변수 | 설명 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API 형식**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `placement1234` |

**요청**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `value` | 매개 변수를 업데이트할 새 값입니다. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업은 `add`, `replace`, `remove`, `copy` 및 `test`입니다. |

**응답**

성공적인 응답은 ID를 포함하여 exd 배치에 대한 업데이트된 세부 정보를 반환합니다.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
