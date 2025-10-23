---
title: Edge Decisioning API를 사용하여 오퍼 게재
description: Adobe Experience Platform 웹 SDK을 사용하면 API 또는 오퍼 라이브러리를 사용하여 만든 개인화된 오퍼를 검색하고 렌더링할 수 있습니다.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Edge Decisioning API를 사용하여 오퍼 게재 {#edge-decisioning-api}

## 시작하기 및 사전 요구 사항 {#edge-overview-and-prerequisites}

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview)은(는) Adobe Experience Cloud 고객이 Experience Platform Edge Network을 통해 Experience Cloud에서 다양한 서비스와 상호 작용할 수 있도록 하는 클라이언트측 JavaScript 라이브러리입니다.

Experience Platform 웹 SDK은 의사 결정 관리를 포함하여 Adobe에서 개인화 솔루션 쿼리를 지원하므로 API 또는 오퍼 라이브러리를 사용하여 만든 개인화된 오퍼를 검색하고 렌더링할 수 있습니다. 자세한 지침은 [오퍼 만들기](../../get-started/starting-offer-decisioning.md)에 대한 설명서를 참조하세요.

[Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview)를 사용하여 의사 결정 관리를 구현하는 방법에는 두 가지가 있습니다. 한 가지 방법은 개발자에 맞춰져 있고 웹 사이트와 프로그래밍에 대한 지식이 필요합니다. 또 다른 방법은 Adobe Experience Platform 사용자 인터페이스를 사용하여 HTML 페이지의 헤더에서 작은 스크립트만 참조하도록 하는 오퍼를 설정하는 것입니다.

Adobe Experience Platform Web SDK을 사용하여 개인화된 오퍼를 제공하는 방법에 대한 자세한 내용은 [의사 결정 관리](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html#enabling-offer-decisioning)의 Adobe Experience Platform 설명서를 참조하십시오.

## Adobe Experience Platform 웹 SDK {#aep-web-sdk}

Platform Web SDK은 다음 SDK를 대체합니다.

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK은 이러한 라이브러리를 결합하지 않았으며 처음부터 새로운 구현입니다. 이를 사용하려면 먼저 다음 단계를 수행해야 합니다.

1. 조직에 SDK을 사용할 수 있는 적절한 권한이 있고 권한을 올바르게 구성했는지 확인하십시오.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. Adobe Experience Cloud 계정의 데이터 수집 탭에서 [데이터 스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html)합니다.

1. SDK을 설치합니다. 이렇게 하는 방법에는 여러 가지가 있습니다. 이 방법은 [SDK 페이지 설치](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html)에 나와 있습니다. 이 페이지는 서로 다른 각 구현 방법을 사용하여 계속됩니다.

SDK을 사용하려면 [스키마](../../../data/get-started-schemas.md)와 [데이터스트림](../../../data/get-started-datasets.md)이 정의되어 있어야 합니다.

<!-- ****TODO - Configure schema**** -->

오퍼를 개인화하려면 개인화/프로필을 별도로 구성해야 합니다.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

의사 결정 관리에 사용할 SDK을 구성하려면 아래 두 단계 중 하나를 수행합니다.

## 옵션 1 - Launch를 사용하여 Tag 확장 및 구현 설치

이 옵션은 코딩 경험이 적을 수 있는 사용자에게 보다 편리합니다.

1. [태그 속성 만들기](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html)

1. [포함 코드 추가](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html)

1. &quot;데이터스트림&quot; 드롭다운에서 구성을 선택하여 생성한 데이터스트림으로 Adobe Experience Platform Web SDK 확장을 설치하고 구성합니다. [확장](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html)에 대한 설명서를 참조하세요.

   ![Adobe Experience Platform 웹 SDK](../../assets/installed-catalog-web-sdk.png)

   ![확장 구성](../../assets/configure-sdk-extension.png)

1. 필요한 [데이터 요소](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html)를 만듭니다. 최소한 Platform Web SDK ID 맵 및 Platform Web SDK XDM 개체 데이터 요소를 만들어야 합니다.

   ![ID 맵](../../assets/sdk-identity-map.png)

   ![XDM 개체](../../assets/xdm-object.png)

1. [규칙](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) 만들기:

   Platform Web SDK 이벤트 보내기 작업을 추가하고 해당 작업의 구성에 관련 decisionScope를 추가합니다

   ![오퍼 렌더링](../../assets/rule-render-offer.png)

   ![오퍼 요청](../../assets/rule-request-offer.png)

1. 구성한 모든 관련 규칙, 데이터 요소 및 확장이 포함된 라이브러리를 [만들고 게시](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html)합니다.

## 옵션 2 - 사전 설치된 독립 실행형 버전을 사용하여 수동으로 구현

다음은 웹 SDK의 사전 설치된 독립 실행형 설치를 사용하여 의사 결정 관리를 사용하는 데 필요한 단계입니다. 이 안내서에서는 SDK을 처음 구현하는 단계이므로 모든 단계를 적용할 수 없다고 가정합니다. 이 안내서에서는 일부 개발 경험도 가정합니다.

옵션 2의 JavaScript 코드 조각(예: HTML 페이지의 [ 섹션에 ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html)이 페이지`<head>`에 미리 빌드된 독립 실행형 버전)을 포함하십시오.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

SDK 구성을 설정하려면 Adobe 계정 내에서 edgeConfigId와 orgId라는 두 개의 ID가 필요합니다. edgeConfigId는 사전 요구 사항에 구성해야 하는 데이터 스트림 ID와 동일합니다.

edgeConfigID/데이터스트림 ID를 찾으려면 데이터 수집으로 이동하여 데이터스트림을 선택합니다. 조직 ID를 찾으려면 프로필로 이동합니다.

이 페이지의 지침에 따라 JavaScript에서 SDK을 구성합니다. 항상 구성 함수에서 edgeConfigId와 orgId를 사용합니다. 이 설명서에서는 구성에 존재하는 선택적 매개 변수에 대해서도 설명합니다. 최종 구성은 다음과 같이 표시될 수 있습니다.

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

디버깅에 사용할 디버거 Chrome 확장을 설치합니다. 다음 위치에서 찾을 수 있음: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

그런 다음 디버거 내에서 계정에 로그인합니다. 그런 다음 로그로 이동하여 올바른 작업 영역에 연결되어 있는지 확인하십시오. 이제 오퍼에서 의사 결정 범위의 base64 인코딩 버전을 복사합니다.

웹 사이트를 편집할 때 결정 범위를 Adobe으로 보낼 수 있도록 구성 및 `sendEvent` 함수가 포함된 스크립트를 포함하십시오.

**예**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

응답을 처리하는 방법에 대한 예는 다음을 참조하십시오.

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

디버거를 사용하여 Edge 네트워크에 성공적으로 연결했는지 확인할 수 있습니다.

>[!NOTE]
>
>로그에 에지에 대한 연결이 보이지 않는 경우 광고 차단기를 비활성화해야 할 수 있습니다.

오퍼를 만든 방법과 사용된 형식을 다시 참조하십시오. 오퍼는 결정에서 충족된 기준에 따라 Adobe Experience Platform 내에서 만들 때 지정한 정보가 포함된 오퍼가 반환됩니다.

이 예제에서 반환되는 JSON은 다음과 같습니다.

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

응답 개체를 처리하고 필요한 데이터를 구문 분석합니다. 한 번의 `sendEvent` 호출로 여러 결정 범위를 보낼 수 있으므로 응답이 약간 다르게 보일 수 있습니다.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

이 예제에서 웹 페이지에서 오퍼 관련 세부 정보를 처리하고 사용하는 데 필요한 경로는 `result['decisions'][0]['items'][0]['data']['content']`입니다.

JS 변수를 설정하려면 다음을 수행하십시오.

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

<!--## Limitations

Some offer constraints are currently not supported with the mobile Experience Edge workflows, for example Capping. The Capping field value specifies the number of times an offer can be presented across all users. For more details, see [Add constraints to an offer](../../offer-library/add-constraints.md#capping).-->
