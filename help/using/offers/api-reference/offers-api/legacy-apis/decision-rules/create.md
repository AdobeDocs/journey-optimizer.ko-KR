---
title: 의사 결정 규칙 만들기
description: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 12c49f4c-a1b5-4841-ab98-663b4c771fb6
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 11%

---

# 의사 결정 규칙 만들기 {#create-decision-rule}

의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제약 조건입니다.

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표는 다음을 구성하는 유효한 값을 보여줍니다. *Content-Type* 및 *Accept* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 결정 규칙이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "xdm:name": "Sales rule",
    "description": "Decisioning rule for sales",
    "xdm:condition": {
        "xdm:type": "PQL",
        "xdm:format": "pql/text",
        "xdm:value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "xdm:definedOn": {
        "profile": {
            "xdm:schema": {
                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "xdm:referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**응답**

성공적인 응답은 고유한 인스턴스 ID 및 배치를 포함하여 새로 생성된 의사 결정 규칙에 대한 정보를 반환합니다 `@id`. 이후 단계에서 인스턴스 ID를 사용하여 의사 결정 규칙을 업데이트하거나 삭제할 수 있습니다. 고유한 결정 규칙을 사용할 수 있습니다 `@id` 개인화된 오퍼를 만드는 데 사용하는 이후 튜토리얼의 옵션입니다.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
