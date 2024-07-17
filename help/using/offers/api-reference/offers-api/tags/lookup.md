---
title: 컬렉션 한정자 조회
description: 컬렉션 한정자를 사용하면 오퍼를 더 잘 구성하고 정렬할 수 있습니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# 컬렉션 한정자 조회 {#look-up-tag}

요청 경로에 컬렉션 한정자 ID를 포함하는 오퍼 라이브러리 API에 GET 요청을 하여 특정 컬렉션 한정자(이전의 &quot;태그&quot;라고 함)를 조회할 수 있습니다.

**API 형식**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
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

성공적인 응답은 컨테이너 ID, 인스턴스 ID 및 고유한 컬렉션 한정자 `@id`에 대한 정보를 포함하여 컬렉션 한정자의 세부 정보를 반환합니다.

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
