---
title: 컬렉션 만들기
description: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ea79add2-1ea7-4c5c-ba67-f99d10975c4f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# 컬렉션 만들기 {#create-collection}

컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 하는 오퍼의 하위 집합입니다.

POST ID를 제공하는 동안 [!DNL Offer Library] API에 대한 컨테이너를 요청하여 컬렉션을 만들 수 있습니다.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 요청 헤더의 *Content-Type* 및 *Accept* 필드를 구성하는 올바른 값을 보여 줍니다.

| 헤더 이름 | 값 |
| ----------- | ----- |
| 수락 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 컬렉션이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**응답**

응답이 성공하면 고유한 인스턴스 ID와 배치 `@id`을(를) 포함하여 새로 만든 컬렉션에 대한 정보가 반환됩니다. 이후 단계에서 인스턴스 ID를 사용하여 컬렉션을 업데이트하거나 삭제할 수 있습니다. 이후 자습서에서 고유한 컬렉션 `@id`을(를) 사용하여 결정을 만들 수 있습니다.

```json
{
   "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2023-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
