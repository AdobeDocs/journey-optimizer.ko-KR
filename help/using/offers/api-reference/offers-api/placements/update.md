---
title: 배치 업데이트
description: 배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 8%

---

# 배치 업데이트 {#update-placement}

에 PATCH 요청을 하여 컨테이너의 배치를 수정하거나 업데이트할 수 있습니다. [!DNL Offer Library] API.

사용 가능한 작업을 포함하여 JSON 패치에 대한 자세한 내용은 다음을 참조하십시오. [JSON 패치 설명서](http://jsonpatch.com/).

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 및 *Accept* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 배치가 위치한 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 업데이트하려는 배치의 인스턴스 ID입니다. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**요청**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Sales and Promotions Placement"
        },
        {
            "op": "replace",
            "path": "/_instance/xdm:description",
            "value": "A test placement to contain offers of sales and discounts"
        }
    ]'
```

| 매개변수 | 설명 |
| --------- | ----------- |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업에는 다음이 포함됩니다. `add`, `replace`, 및 `remove`. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `value` | 매개 변수를 업데이트할 새 값입니다. |

**응답**

성공적인 응답은 고유한 인스턴스 ID와 배치를 포함하여 업데이트된 배치 세부 정보를 반환합니다 `@id`.

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2020-10-21T19:59:10.700149Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
