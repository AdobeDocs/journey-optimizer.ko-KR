---
title: 제안 전달
description: 의사 결정 관리는 마케터가 비즈니스 논리 및 의사 결정 규칙을 사용하여 채널 및 애플리케이션 전반에 걸쳐 최종 사용자 맞춤형 제안 경험을 제작하여 제공할 수 있는 서비스 및 UI 프로그램의 집합입니다.
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 3%

---

# 결정 API를 사용하여 오퍼 제공

의사 결정 관리 기능을 사용하면 비즈니스 논리 및 의사 결정 규칙을 사용하여 채널 및 애플리케이션 전반에 개인화된 제안 경험을 제작하여 제공할 수 있습니다. 오퍼는 오퍼를 볼 자격이 있는 사람을 지정하는 규칙과 연관된 규칙이 있을 수 있는 마케팅 메시지입니다.

[!DNL Decisions] API에 POST 요청을 하여 오퍼를 만들고 제공할 수 있습니다.

이 자습서에서는 의사 결정 관리와 관련하여 API에 대한 작업 이해를 필요로 합니다. 자세한 내용은 [의사 결정 관리 API 개발자 안내서](../getting-started.md)를 참조하십시오. 또한 이 자습서를 사용하려면 고유한 배치 ID 및 결정 ID 값을 사용할 수 있어야 합니다. 이러한 값을 취득하지 않은 경우 [배치](../offers-api/placements/create.md) 만들기 및 [결정](../activities-api/activities/create.md)에 대한 자습서를 참조하십시오.

![](../../../assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

## 머리글 수락 및 내용 유형

다음 표는 요청 헤더의 *Content-Type* 및 *Accept* 필드를 구성하는 유효한 값을 보여 줍니다.

| 헤더 이름 | 값 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**API 형식**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | 결정이 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**요청**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
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
| `xdm:propositionRequests` | 이 개체에는 배치 및 결정 식별자가 들어 있습니다. |
| `xdm:propositionRequests.xdm:placementId` | 고유한 배치 식별자입니다. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 고유 의사 결정 식별자입니다. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 반환할 오퍼 수입니다. 최대 수는 30입니다. | `"xdm:itemCount": 2` |
| `xdm:profiles` | 이 개체에는 의사 결정을 요청한 프로필에 대한 정보가 들어 있습니다. API 요청의 경우 여기에는 하나의 프로필이 포함됩니다. |
| `xdm:profiles.xdm:identityMap` | 이 개체는 ID의 네임스페이스 통합 코드를 기반으로 최종 사용자 ID 집합을 보유합니다. ID 맵은 각 네임스페이스의 ID를 두 개 이상 포함할 수 있습니다. 네임스페이스에 대한 자세한 내용은 [ID 네임스페이스 개요](https://docs.adobe.com/content/help/ko-KR/experience-platform/identity/namespaces.html)를 참조하십시오. | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 프로필 결정 요청을 고유하게 식별하는 데 사용할 수 있는 클라이언트가 생성한 ID. 이 ID는 응답에서 다시 반복되며 결정 결과에 영향을 주지 않습니다. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | 이 객체는 중복 제거 규칙의 제어 구조를 나타냅니다. 특정 차원에 대해 동일한 옵션을 제안할 수 있는지 여부를 나타내는 일련의 플래그. true로 설정된 플래그는 중복이 허용되고 플래그로 지정된 카테고리에서 제거되어서는 안 된다는 것을 의미합니다. false로 설정된 플래그는 의사 결정 엔진이 차원 전체에서 동일한 제안을 해서는 안 되며, 대신 하위 결정 중 하나에 대해 다음 우수 옵션을 선택해야 함을 의미합니다. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | true로 설정된 경우 동일한 옵션을 여러 결정으로 지정할 수 있습니다. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | true로 설정된 경우 동일한 옵션을 여러 배치에 할당할 수 있습니다. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 프로필 액세스 서비스에서 반환한 데이터를 제어하는 병합 정책을 식별합니다. 요청에 지정되지 않은 경우 의사 결정 관리에서 프로필 액세스 서비스를 전달하지 않고 호출자가 제공한 id를 전달합니다. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 응답 컨텐츠를 포맷하는 플래그 세트입니다. |
| `xdm:responseFormat.xdm:includeContent` | `true`으로 설정된 경우 응답에 대한 내용을 포함하는 부울 값입니다. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 추가 메타데이터가 반환되는 내용을 지정하는 데 사용되는 객체입니다. 이 속성이 포함되지 않으면 기본적으로 `xdm:id` 및 `repo:etag`이 반환됩니다. | `name` |
| `xdm:responseFormat.xdm:activity` | 이 플래그는 `xdm:activity`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name` |
| `xdm:responseFormat.xdm:option` | 이 플래그는 `xdm:option`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | 이 플래그는 `xdm:placement`에 대해 반환된 특정 메타데이터 정보를 식별합니다. | `name`, `channel`, `componentType` |

**응답**

성공적인 응답으로 고유한 `xdm:propositionId`을 포함하여 제안에 대한 정보를 반환합니다.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
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
| `xdm:propositionId` | XDM DecisionEvent와 연결된 제안 엔티티에 대한 고유 식별자입니다. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 이 개체에는 하나의 결정 제안이 있습니다. 결정에 대해 여러 옵션을 반환할 수 있습니다. 옵션을 찾을 수 없으면 결정 폴백 오퍼가 반환됩니다. 단일 결정 프로세스에는 항상 `options` 속성 또는 `fallback` 속성이 포함됩니다. 이 경우 `options` 속성은 비워 둘 수 없습니다. |
| `xdm:propositions.xdm:activity` | 이 개체에는 의사 결정에 대한 고유 식별자가 들어 있습니다. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 이 객체에는 오퍼 배치에 대한 고유 식별자가 포함됩니다. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 이 개체에는 고유 식별자를 포함한 단일 옵션이 있습니다. 이 개체가 있으면 이 개체를 비워 둘 수 없습니다. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 구성 요소의 유형을 정의합니다. `@type` 클라이언트의 처리 계약 역할을 수행합니다. 경험이 어셈블되면 작성자는 특정 유형의 구성 요소를 찾습니다. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 응답 컨텐츠의 형식입니다. | 응답 컨텐츠는 다음과 같습니다.`text`, `html block` 또는 `image link` |
| `xdm:score` | 옵션 또는 결정과 연결된 등급 함수의 결과로 계산되는 옵션에 대한 점수입니다. 등급 함수가 등급 중 오퍼의 점수를 결정하는 데 관여하는 경우 이 필드는 API에서 반환됩니다. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 이 개체에는 고유 식별자를 포함한 단일 폴백 오퍼가 포함됩니다. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 리소스의 실제 또는 디지털 표현입니다. 일반적으로 형식에는 리소스의 미디어 유형이 포함되어야 합니다. 이 포맷은 리소스를 표시 또는 운영하는 데 필요한 소프트웨어, 하드웨어 또는 기타 장비를 결정하는 데 사용할 수 있습니다. 컴퓨터 미디어 형식을 정의하는 [인터넷 미디어 유형](http://www.iana.org/assignments/media-types/) 목록 등 제어된 어휘에서 값을 선택하는 것이 좋습니다. | `"dc:format": "image/png"` 또는 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 콘텐츠 전달 네트워크 또는 서비스 끝점에서 자산을 읽을 수 있는 선택적 URL입니다. 이 URL은 사용자 에이전트가 공개적으로 자산을 액세스하는 데 사용됩니다. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 의사 결정 응답 메시지를 만든 시간입니다. 이것은 획기적인 시기로 표현된다. | `"ode:createDate": 1566497582038` |

## 자습서 비디오 {#video}

다음 비디오는 의사 결정 관리의 구성 요소에 대한 이해를 지원하기 위한 것입니다.

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform 기반으로 구축된 Offer decisioning 응용 프로그램 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하기 위한 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## 다음 단계

이 API 가이드를 따르면 [!DNL Decisions] API를 사용하여 오퍼를 만들고 제공했습니다. 자세한 내용은 의사 결정 관리](../../../offers/get-started/starting-offer-decisioning.md)에 대한 [개요를 참조하십시오.
