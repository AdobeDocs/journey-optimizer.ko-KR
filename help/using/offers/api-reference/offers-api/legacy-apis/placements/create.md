---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 배치 만들기
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Decision Management, API
badge: label="레거시" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c7301f6-95d3-4720-81fe-5f2602cd30ec
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 22%

---

# 배치 만들기 {#create-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../../../../experience-decisioning/gs-experience-decisioning.md)


컨테이너 ID를 제공하는 동안 [!DNL Offer Library] API에 대한 POST 요청을 수행하여 배치를 만들 수 있습니다.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 요청 헤더의 *Content-Type* 및 *Accept* 필드를 구성하는 올바른 값을 보여 줍니다.

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

성공한 응답은 고유한 인스턴스 ID와 배치 `@id`을(를) 포함하여 새로 만든 배치의 세부 정보를 반환합니다. 이후 단계에서 인스턴스 ID를 사용하여 배치를 업데이트하거나 삭제할 수 있습니다. 나중 자습서에서 고유한 배치 `@id`을(를) 사용하여 의사 결정, 의사 결정 규칙 및 대체 오퍼를 만들 수 있습니다.

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
