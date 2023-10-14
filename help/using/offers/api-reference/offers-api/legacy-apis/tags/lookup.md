---
title: 컬렉션 한정자 조회
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---

# 컬렉션 한정자 조회 {#look-up-tag}

에 GET 요청을 하여 특정 컬렉션 한정자(이전의 &quot;태그&quot;라고 함)를 조회할 수 있습니다. [!DNL Offer Library] 컬렉션 한정자를 포함하는 API `id` 요청 경로에서.

**API 형식**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `tag1234` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 고유한 수집 구분자에 대한 정보를 포함하여 수집 구분자의 상세내역을 반환합니다 `id`.

```json
{
       "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
