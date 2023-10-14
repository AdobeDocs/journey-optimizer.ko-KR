---
title: 컬렉션 조회
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.
feature: Offers, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# 컬렉션 조회 {#look-up-collection}

컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.

에 GET 요청을 하여 특정 컬렉션을 조회할 수 있습니다. [!DNL Offer Library] 컬렉션을 포함하는 API `id` 요청 경로에서.

**API 형식**

```http
GET /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 지속성 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 조회할 엔티티의 ID입니다. | `offerCollection1234` |

**요청**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 고유 컬렉션에 대한 정보를 포함하여 컬렉션 세부 정보를 반환합니다 `id`.

```json
{
        "created": "2022-09-16T18:59:23.063+00:00",
    "modified": "2022-09-16T18:59:23.063+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerCollection1234",
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}
```
