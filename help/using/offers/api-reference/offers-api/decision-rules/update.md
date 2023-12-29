---
title: 의사 결정 규칙 업데이트
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 42c531fd-0dc9-492d-8827-2e1460454064
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 7%

---

# 의사 결정 규칙 업데이트 {#update-decision-rule}

에 PATCH 요청을 하여 의사 결정 규칙을 수정하거나 업데이트할 수 있습니다. [!DNL Offer Library] API.

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 다음을 참조하십시오. [JSON 패치 설명서](https://jsonpatch.com/).

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 업데이트하려는 엔티티의 ID입니다. | `offerRule1234` |

**요청**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated decision rule"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated decision rule description"
    }
]'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업에는 다음이 포함됩니다. `add`, `replace`, `remove`, `copy` 및 `test`. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `value` | 매개 변수를 업데이트할 새 값입니다. |

**응답**

성공적인 응답은 고유한 결정 규칙을 포함하여 결정 규칙의 업데이트된 세부 사항을 반환합니다 `id`.

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
