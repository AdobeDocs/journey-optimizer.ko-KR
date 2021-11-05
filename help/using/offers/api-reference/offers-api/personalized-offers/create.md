---
title: 개인화된 오퍼 만들기
description: 개인화된 오퍼는 자격 규칙 및 제한을 기반으로 사용자 정의 가능한 마케팅 메시지입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 701b8a46b5f22c31bee479ddfb63f8e399cee4a1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 9%

---

# 개인화된 오퍼 만들기

개인화된 오퍼는 자격 규칙 및 제한을 기반으로 사용자 정의 가능한 마케팅 메시지입니다.

에 POST 요청을 작성하여 개인화된 오퍼를 생성할 수 있습니다 [!DNL Offer Library] API, 컨테이너 ID를 제공하는 동안

## Accept 및 Content-Type 헤더

다음 표에서는 *컨텐츠 유형* 및 *수락* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API 형식**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 개인화된 오퍼가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2020-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
        },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
        },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**응답**

성공적인 응답은 고유한 인스턴스 ID 및 배치를 포함하여 새로 만든 개인화된 오퍼에 대한 정보를 반환합니다 `@id`. 이후 단계에서 인스턴스 ID를 사용하여 개인화된 오퍼를 업데이트하거나 삭제할 수 있습니다.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## 제한 사항 {#limitations}

일부 오퍼 제약 조건은 현재 모바일에서 지원되지 않습니다 [!DNL Experience Edge] 워크플로우(예: `Capping`. 다음 `Capping` 필드 값은 모든 사용자에게 오퍼를 제공할 수 있는 횟수를 지정합니다. 자세한 내용은 [오퍼 자격 규칙 및 제한 설명서](../../../offer-library/creating-personalized-offers.md).