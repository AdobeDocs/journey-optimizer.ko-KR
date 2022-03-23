---
title: 태그 만들기
description: 태그를 사용하면 오퍼를 보다 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 10%

---

# 태그 만들기 {#create-tag}

에 POST 요청을 작성하여 태그를 만들 수 있습니다 [!DNL Offer Library] API, 컨테이너 ID를 제공하는 동안

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표에서는 *컨텐츠 유형* 및 *수락* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 태그가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**응답**

성공적인 응답은 고유한 인스턴스 ID 및 배치를 포함하여 새로 만든 태그에 대한 정보를 반환합니다 `@id`. 이후 단계에서 인스턴스 ID를 사용하여 태그를 업데이트하거나 삭제할 수 있습니다. 고유한 태그를 사용할 수 있습니다 `@id` 을 사용하여 컬렉션과 개인화된 오퍼를 만들 수 있습니다.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
