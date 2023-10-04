---
title: 컬렉션 수식어 만들기
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 12%

---


# 컬렉션 수식어 만들기 {#create-tag}

에 POST 요청을 하여 컬렉션 한정자(이전에는 &quot;태그&quot;라고 함)를 만들 수 있습니다. [!DNL Offer Library] API.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/tags
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |

**요청**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**응답**

성공적인 응답은 새로 생성된 컬렉션 한정자에 대한 정보를 반환합니다(예: `id`. 이후 단계에서 컬렉션 한정자를 업데이트하거나 삭제할 수 있습니다. 고유한 컬렉션 한정자를 사용할 수 있습니다. `id` 컬렉션 및 개인화된 오퍼를 만드는 데 도움이 되는 나중 튜토리얼에 추가했습니다.

```json
{
    "etag": 1,
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
