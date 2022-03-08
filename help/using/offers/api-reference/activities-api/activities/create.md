---
title: 의사 결정 만들기
description: 결정에는 오퍼의 선택을 알리는 논리가 포함되어 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 553501b0-30a9-4795-9a9d-f42df5f4f2ea
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 11%

---

# 의사 결정 만들기 {#create-decision}

에 POST 요청을 수행하여 결정을 만들 수 있습니다 [!DNL Offer Library] API, 컨테이너 ID를 제공하는 동안

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표에서는 *컨텐츠 유형* 및 *수락* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
      "_instance": {
          "xdm:name": "Test API",
          "xdm:startDate": "2022-01-20T16:00:00Z",
          "xdm:endDate": "2022-01-27T16:00:00Z",
          "xdm:status": "live",
          "xdm:criteria": [
              {
                  "xdm:placements": [
                      "xcore:offer-placement:1457f9322f005194"
                  ],
                  "xdm:optionSelection": {
                      "xdm:filter": "xcore:offer-filter:1457f93227d0b6f0"
                  }
              }
          ],
          "xdm:fallback": "xcore:fallback-offer:13c259399d8bf013"
      },
      "_links": {}
  }'
```

**응답**

성공적인 응답은 고유한 인스턴스 ID 및 배치를 포함하여 새로 생성된 결정에 대한 정보를 반환합니다 `@id`. 이후 단계에서 인스턴스 ID를 사용하여 결정을 업데이트하거나 삭제할 수 있습니다.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
