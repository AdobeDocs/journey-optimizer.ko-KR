---
title: 개인화된 오퍼 업데이트
description: 개인화된 오퍼는 자격 규칙 및 제한을 기반으로 사용자 정의 가능한 마케팅 메시지입니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 8%

---

# 개인화된 오퍼 업데이트 {#update-personalized-offer}

에 PATCH 요청을 작성하여 개인화된 오퍼를 수정하거나 업데이트할 수 있습니다 [!DNL Offer Library] API

사용 가능한 작업을 포함한 JSON 패치에 대한 자세한 내용은 공식 문서를 참조하십시오 [JSON 패치 설명서](http://jsonpatch.com/).

## Accept 및 Content-Type 헤더 {#accept-and-content-type-headers}

다음 표에서는 *컨텐츠 유형* 및 *수락* 요청 헤더의 필드:

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API 형식**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 개인화된 오퍼가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "add",
            "path": "/_instance/xdm:representations/-",
            "value": {
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3",
                "xdm:components": [
                    {
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-text",
                        "dc:format": "text/plain",
                        "dc:language": ["en"],
                        "xdm:content": "Here is your first sale offer!"
                    }
                ]
            }
        }
    ]'
```

| 매개 변수 | 설명 |
| --------- | ----------- |
| `op` | 연결을 업데이트하는 데 필요한 작업을 정의하는 데 사용되는 작업 호출입니다. 작업은 다음과 같습니다. `add`, `replace`, 및 `remove`. |
| `path` | 업데이트할 매개 변수의 경로입니다. |
| `value` | 매개 변수를 업데이트할 새 값입니다. |

**응답**

성공적인 응답은 고유 인스턴스 ID 및 개인화된 오퍼를 포함하여 개인화된 오퍼의 업데이트된 세부 사항을 반환합니다 `@id`.

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
