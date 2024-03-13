---
title: 배치 만들기
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c7301f6-95d3-4720-81fe-5f2602cd30ec
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# 배치 만들기 {#create-placement}

에 POST 요청을 하여 배치를 생성할 수 있습니다. [!DNL Offer Library] 컨테이너 ID를 제공하는 동안 API.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 및 *Accept* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| 수락 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 배치가 위치한 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sales Placement",
        "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
        "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
        "xdm:description": "A test placement to contain offers"
}'
```

**응답**

성공적인 응답은 고유한 인스턴스 ID와 배치를 포함하여 새로 생성된 배치의 세부 정보를 반환합니다 `@id`. 이후 단계에서 인스턴스 ID를 사용하여 배치를 업데이트하거나 삭제할 수 있습니다. 고유한 배치를 사용할 수 있습니다 `@id` 의사 결정, 의사 결정 규칙 및 대체 오퍼를 만드는 데 사용할 수 있는 나중 튜토리얼에서.

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2023-10-21T19:57:09.837456Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
