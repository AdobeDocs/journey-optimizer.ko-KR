---
title: 오퍼 제공
description: 의사 결정 관리는 비즈니스 로직 및 의사 결정 규칙을 사용하여 마케터가 채널 및 애플리케이션에서 최종 사용자에게 개인화된 오퍼 경험을 만들어 제공할 수 있는 서비스 및 UI 프로그램의 컬렉션입니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: 30fed481bb02fd25f1833e76ae94330aa51d153b
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 2%

---

# Decisioning API를 사용하여 오퍼 게재 {#decisioning-api}

의사 결정 관리를 사용하면 비즈니스 논리 및 의사 결정 규칙을 사용하여 채널 및 애플리케이션 전반에 개인화된 오퍼 경험을 제작하여 제공할 수 있습니다. 오퍼는 오퍼를 볼 자격이 있는 사람을 지정하는 규칙과 관련된 마케팅 메시지입니다.

[!DNL Decisioning] API에 대한 POST 요청을 통해 오퍼를 만들고 게재할 수 있습니다.

이 자습서에서는 특히 의사 결정 관리에 대해 API를 이해하고 있어야 합니다. 자세한 내용은 [의사 결정 관리 API 개발자 안내서](../getting-started.md)를 참조하십시오. 또한 이 자습서에서는 고유한 배치 ID와 의사 결정 ID 값을 사용할 수 있어야 합니다. 이 값을 획득하지 않은 경우 [배치 만들기](../offers-api/placements/create.md) 및 [의사 결정 만들기](../activities-api/activities/create.md)에 대한 튜토리얼을 참조하십시오.

## 필수 헤더 {#required-headers}

다음 표는 요청 헤더의 *Content-Type* 및 *Accept* 필드를 구성하는 올바른 값을 보여 줍니다.

| 헤더 이름 | 값 |
| ----------- | ----- |
| 수락 | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Authorization | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* 페이로드(POST, PUT, PATCH)가 포함된 모든 요청에는 콘텐츠 유형 헤더가 필요합니다


>[!NOTE]
>
>권한 확인은 개별 샌드박스에 적용되지 않습니다. 호출자가 유효한 토큰을 제시한 경우 게재 API가 통과합니다.

## API 요청 {#request}

### API 형식

```https
POST /{ENDPOINT_PATH}/decisions
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/ods` |

### 요청

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}' 
```

| 속성 | 설명 | 예 |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | 이 개체에는 배치 및 의사 결정 식별자가 포함되어 있습니다. |
| `xdm:propositionRequests.xdm:placementId` | 고유 배치 식별자. | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 고유 의사 결정 식별자. | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | 반환할 오퍼 수입니다. 최대 숫자는 30입니다. | `"xdm:itemCount": 2` |
| `xdm:profiles` | 이 개체에는 결정이 요청된 프로필에 대한 정보가 들어 있습니다. API 요청의 경우 하나의 프로필이 포함됩니다. |
| `xdm:profiles.xdm:identityMap` | 이 개체에는 ID의 네임스페이스 통합 코드를 기반으로 하는 최종 사용자 ID 세트가 들어 있습니다. ID 맵에는 각 네임스페이스의 ID가 두 개 이상 포함될 수 있습니다. 네임스페이스에 대한 자세한 내용은 [이 페이지](../../../audience/get-started-identity.md)를 참조하세요. | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 프로필 결정 요청을 고유하게 식별하는 데 사용될 수 있는 클라이언트가 생성한 ID입니다. 이 ID는 응답에서 다시 에코백되며 결정 결과에 영향을 주지 않습니다. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | 이 객체는 데이터 중복 제거 규칙의 제어 구조를 의미합니다. 이는 특정 차원에 대해 동일한 옵션을 제안할 수 있는지 여부를 나타내는 일련의 플래그로 구성됩니다. true로 설정된 플래그는 복제가 허용되고 플래그가 지정한 범주 내에서 제거되어서는 안 됨을 의미합니다. false로 설정된 플래그는 의사 결정 엔진이 차원에서 동일한 제안을 하지 않고 대신 하위 의사 결정 중 하나에 대해 다음 최적 옵션을 선택해야 함을 의미합니다. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | true로 설정하면 여러 개의 결정에 동일한 옵션이 할당될 수 있습니다. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | true로 설정하면 여러 배치에 동일한 옵션이 할당될 수 있습니다. | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | CSV 대상자를 타깃팅하는 경우 이 매개 변수를 추가하고 &quot;true&quot;로 설정합니다. | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | 프로필 액세스 서비스에서 반환한 데이터를 제어하는 병합 정책을 식별합니다. 요청에 ID가 지정되지 않은 경우 의사 결정 관리 는 프로필 액세스 서비스를 전달하지 않고 호출자가 제공한 ID를 전달합니다. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 응답 콘텐츠의 형식을 지정하는 플래그 세트입니다. |
| `xdm:responseFormat.xdm:includeContent` | `true`(으)로 설정된 경우 응답에 콘텐츠를 포함하는 부울 값. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 반환되는 추가 메타데이터를 지정하는 데 사용되는 개체입니다. 이 속성이 포함되지 않으면 기본적으로 `xdm:id` 및 `repo:etag`이(가) 반환됩니다. | `name` |
| `xdm:responseFormat.xdm:activity` | 이 플래그는 `xdm:activity`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name` |
| `xdm:responseFormat.xdm:option` | 이 플래그는 `xdm:option`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | 이 플래그는 `xdm:placement`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name`, `channel`, `componentType` |

### 응답

성공적인 응답이 고유한 `xdm:propositionId`을(를) 포함하여 제안에 대한 정보를 반환합니다.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| 속성 | 설명 | 예 |
| -------- | ----------- | ------- |
| `xdm:propositionId` | XDM DecisionEvent와 연계된 제안 엔티티에 대한 고유 식별자. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 이 대상은 단일 결정 제안을 포함합니다. 결정을 위해 여러 옵션이 반환될 수 있습니다. 옵션을 찾을 수 없으면 의사 결정의 대체 오퍼가 반환됩니다. 단일 결정 제안에 항상 `options` 속성 또는 `fallback` 속성이 포함됩니다. 존재하는 경우 `options` 속성은 비워 둘 수 없습니다. |
| `xdm:propositions.xdm:activity` | 이 개체에는 의사 결정에 대한 고유 식별자가 들어 있습니다. | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 이 개체에는 오퍼 배치에 대한 고유 식별자가 들어 있습니다. | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 이 개체에는 고유 식별자를 포함한 단일 옵션이 있습니다. 존재하는 경우 해당 객체는 비워둘 수 없습니다. | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 구성 요소의 유형을 정의합니다. `@type`은(는) 클라이언트의 처리 계약 역할을 합니다. 경험이 어셈블되면 작성기는 특정 유형의 구성 요소를 찾습니다. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 응답 콘텐츠의 형식입니다. | 응답 콘텐츠는 `text`, `html block` 또는 `image link`일 수 있습니다. |
| `xdm:score` | 옵션 또는 결정과 연관된 순위 함수의 결과로 계산되는 옵션에 대한 점수입니다. 순위 지정 중에 오퍼의 점수를 결정하는 데 순위 지정 기능이 관련된 경우 API에서 이 필드를 반환합니다. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 이 개체에는 고유 식별자를 포함한 단일 대체 오퍼가 포함되어 있습니다. | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 리소스의 물리적 또는 디지털 표현입니다. 일반적으로 형식에는 리소스의 미디어 유형이 포함되어야 합니다. 포맷은 리소스를 표시하거나 운영하기 위해 필요한 소프트웨어, 하드웨어 또는 기타 장비를 결정하는 데 사용될 수 있다. 컴퓨터 미디어 형식을 정의하는 [인터넷 미디어 유형](https://www.iana.org/assignments/media-types/) 목록과 같은 통제 어휘에서 값을 선택하는 것이 좋습니다. | `"dc:format": "image/png"` 또는 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 컨텐츠 전달 네트워크 또는 서비스 끝점에서 자산을 읽는 선택적 URL입니다. 이 URL은 사용자 에이전트에서 공개적으로 자산에 액세스하는 데 사용됩니다. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 의사 결정 응답 메시지를 만든 시간입니다. 이는 획기적인 시간으로 표현됩니다. | `"ode:createDate": 1566497582038` |

**응답 코드**

아래 표에는 응답에서 반환할 수 있는 모든 코드가 나열되어 있습니다.

| 코드 | 설명 |
|  ---  |  ---  |
| 200 | 성공. 해당 활동에 대해 결정됨 |
| 400 | 잘못된 요청 매개변수. 잘못된 구문 때문에 서버에서 요청을 이해할 수 없습니다. |
| 403 | 사용할 수 없음. 권한이 충분하지 않음. |
| 422 | 처리할 수 없는 엔티티. 요청 구문은 올바르지만 의미 체계 오류로 인해 처리할 수 없습니다. |
| 429 | 요청이 너무 많습니다. 사용자가 지정된 시간 내에 너무 많은 요청을 보냈습니다. |
| 500 | 내부 서버 오류. 서버에서 예기치 않은 상태가 발생하여 요청을 수행할 수 없습니다. |
| 503 | 서버 오버로드로 인해 서비스를 사용할 수 없습니다. 현재 일시적인 오버로드로 인해 서버에서 요청을 처리할 수 없습니다. |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/342832/?quality=12&captions=kor) -->

## 다음 단계 {#next-steps}

이 API 안내서를 따라 [!DNL Decisions] API를 사용하여 오퍼를 만들고 전달했습니다. 자세한 내용은 [의사 결정 관리에 대한 개요](../../../offers/get-started/starting-offer-decisioning.md)를 참조하십시오.
