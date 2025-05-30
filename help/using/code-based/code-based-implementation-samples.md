---
title: 코드 기반 구현 샘플
description: 이 페이지에서는 Journey Optimizer 코드 기반 기능에 대한 구현 방법 샘플을 보여 줍니다
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 2%

---

# 코드 기반 구현 방법 샘플 {#implementation-samples}

코드 기반 경험은 모든 유형의 고객 구현을 지원합니다. 이 페이지에서는 각 구현 방법에 대한 샘플을 찾을 수 있습니다.

* [클라이언트측](#client-side-implementation)
* [서버측](#server-side-implementation)
* [하이브리드](#hybrid-implementation)

>[!IMPORTANT]
>
>[이 링크](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}를 팔로우하여 다양한 개인화 및 실험 사용 사례에 대한 샘플 구현을 찾으십시오. 필요한 구현 단계와 전체적인 개인화 흐름이 작동하는 방식을 더 잘 이해하기 위해 이러한 단계를 확인하고 실행합니다.

## 클라이언트측 구현 {#client-side-implementation}

클라이언트측 구현이 있는 경우 AEP 클라이언트 SDK 중 하나인 AEP Web SDK 또는 AEP Mobile SDK 를 사용할 수 있습니다.

* [아래](#client-side-how) 단계에서는 샘플 **Web SDK** 구현의 코드 기반 경험 여정 및 캠페인이 Edge에 게시한 콘텐츠를 가져오고 개인화된 콘텐츠를 표시하는 프로세스를 설명합니다.

* **Mobile SDK**&#x200B;를 사용하여 코드 기반 채널을 구현하는 단계는 [이 자습서](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}에 설명되어 있습니다.

  >[!NOTE]
  >
  >모바일 사용 사례에 대한 샘플 구현은 [iOS 앱](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 및 [Android 앱](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}에서 사용할 수 있습니다.

### 작동 방법 - 웹 SDK {#client-side-how}

1. [웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko){target="_blank"}이(가) 페이지에 포함되어 있습니다.

1. 개인화 콘텐츠를 가져오려면 `sendEvent` 명령을 사용하고 [표면 URI](code-based-surface.md)<!--( or location/path)-->를 지정해야 합니다.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. 결정에 따라 DOM을 업데이트하려면 구현 코드([`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} 메서드 사용)에서 코드 기반 경험 항목을 수동으로 적용해야 합니다.

1. 코드 기반 경험 여정 및 캠페인의 경우 콘텐츠가 표시된 시기를 나타내기 위해 표시 이벤트를 수동으로 보내야 합니다. 이 작업은 `sendEvent` 명령을 통해 수행됩니다.

   ```javascript
   function sendDisplayEvent(decision) {
     const { id, scope, scopeDetails = {} } = decision;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionDisplay",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
           },
         },
       },
     });
   }
   ```

1. 코드 기반 경험 여정 및 캠페인의 경우 사용자가 콘텐츠와 상호 작용한 시기를 나타내기 위해 상호 작용 이벤트를 수동으로 전송해야 합니다. 이 작업은 `sendEvent` 명령을 통해 수행됩니다.

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               label: label
             },
           },
         },
       },
     });
   }
   ```

### 주요 관찰

**쿠키**

쿠키는 사용자 ID 및 클러스터 정보를 유지하는 데 사용됩니다. 클라이언트측 구현을 사용하는 경우 Web SDK는 요청 라이프사이클 동안 이러한 쿠키의 저장 및 전송을 자동으로 처리합니다.

| Cookie | 용도 | 저장 주체 | 보낸 사람 |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | 사용자 ID 세부 정보 포함 | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | 요청을 이행하는 데 사용해야 하는 경험 에지 클러스터를 나타냅니다. | Web SDK | Web SDK |

**배치 요청**

제안을 가져오고 디스플레이 알림을 보내려면 Adobe Experience Platform API에 대한 요청이 필요합니다. 클라이언트측 구현을 사용하는 경우 `sendEvent` 명령이 사용될 때 Web SDK에서 이러한 요청을 수행합니다.

| 요청 | 만든 사람 |
| ---------------------------------------------- | ----------------------------------- |
| 제안 가져오기를 위한 요청 상호 작용 | sendEvent 명령을 사용하는 웹 SDK |
| 디스플레이 알림 전송을 위한 상호 작용 요청 | sendEvent 명령을 사용하는 웹 SDK |

**흐름 다이어그램**

![](assets/code-based-client-side-implementation.png)

## 서버측 구현 {#server-side-implementation}

서버측 구현이 있는 경우 AEP Edge Network API 중 하나를 사용할 수 있습니다.

아래 단계에서는 웹 페이지에 대한 샘플 Edge Network API 구현에서 코드 기반 경험 여정 및 캠페인에 의해 에지에 게시된 콘텐츠를 가져오고 개인화된 콘텐츠를 표시하는 프로세스를 설명합니다.

### 작동 방식

1. 웹 페이지가 요청되고 브라우저에서 이전에 저장한 쿠키(`kndctr_` 접두사)가 포함됩니다.
1. 앱 서버에서 페이지를 요청하면 [대화형 데이터 수집 끝점](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=ko)으로 이벤트를 전송하여 개인화 콘텐츠를 가져옵니다. 이 샘플 앱은 몇 가지 도우미 메서드를 사용하여 API에 대한 요청 빌드 및 전송을 단순화합니다([aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"} 참조). 하지만 이 요청은 이벤트 및 쿼리가 포함된 페이로드가 있는 `POST`입니다. 이전 단계의 쿠키(사용 가능한 경우)는 `meta>state>entries` 배열의 요청에 포함됩니다.

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. 코드 기반 경험 여정 및 캠페인의 JSON 경험은 응답에서 읽히고 HTML 응답을 생성할 때 사용됩니다.

1. 코드 기반 경험 여정 및 캠페인의 경우 여정 또는 캠페인 컨텐츠가 표시된 시기를 나타내기 위해 표시 이벤트를 구현에서 수동으로 보내야 합니다. 이 예에서 알림은 요청 라이프사이클 동안 서버측에서 전송됩니다.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. HTML 응답이 반환되면 ID 및 클러스터 쿠키가 애플리케이션 서버에 의한 응답에 설정됩니다.

### 주요 관찰

**쿠키**

쿠키는 사용자 ID 및 클러스터 정보를 유지하는 데 사용됩니다. 서버측 구현을 사용하는 경우 애플리케이션 서버는 요청 라이프사이클 동안 이러한 쿠키의 저장 및 전송을 처리해야 합니다.

| Cookie | 용도 | 저장 주체 | 보낸 사람 |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | 사용자 ID 세부 정보 포함 | 응용 프로그램 서버 | 응용 프로그램 서버 |
| kndctr_AdobeOrg_cluster | 요청을 이행하는 데 사용해야 하는 경험 에지 클러스터를 나타냅니다. | 응용 프로그램 서버 | 응용 프로그램 서버 |

**배치 요청**

제안을 가져오고 디스플레이 알림을 보내려면 Adobe Experience Platform API에 대한 요청이 필요합니다. 클라이언트측 구현을 사용하는 경우 `sendEvent` 명령이 사용될 때 Web SDK에서 이러한 요청을 수행합니다.

| 요청 | 만든 사람 |
| ---------------------------------------------- | ------------------------------------------------------------ |
| 제안 가져오기를 위한 요청 상호 작용 | Adobe Experience Platform API를 호출하는 애플리케이션 서버 |
| 디스플레이 알림 전송을 위한 상호 작용 요청 | Adobe Experience Platform API를 호출하는 애플리케이션 서버 |

**흐름 다이어그램**

![](assets/code-based-server-side-implementation.png)

## 하이브리드 구현 {#hybrid-implementation}

하이브리드 구현이 있는 경우 아래 링크를 확인하십시오.

* Adobe 기술 블로그: [Adobe Experience Platform Web SDK의 하이브리드 Personalization](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* SDK 설명서: [Web SDK 및 Edge Network 서버 API를 사용한 하이브리드 개인화](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html?lang=ko){target="_blank"}
