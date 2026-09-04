---
title: 웹 SDK에서 받은 편지함 지원 구성
description: Adobe Experience Platform Web SDK에서 컨텐츠 카드 및 받은 편지함 캠페인을 사용하여 Adobe Journey Optimizer에서 영구 메시지 받은 편지함을 작성하는 방법을 알아봅니다.
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 1ee6fd3ed3523635ea7dbe46dbae0e2403246818
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# Web SDK에서 받은 편지함 지원 구성 {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**이 페이지에서:** 웹 사이트에서 지속적인 알림 받은 편지함을 제공할 수 있도록 Content Card 캠페인과 받은 편지함 캠페인을 결합한 샘플을 설정하고 실행합니다.

>[!ENDSHADEBOX]

메시지 받은 편지함은 동일한 표면을 타겟팅하는 두 개의 Adobe Journey Optimizer 캠페인에 의해 구동되는 영구 알림 받은 편지함입니다.

* 개별 알림 항목을 받은 편지함으로 배달하는 **콘텐츠 카드 캠페인**.
* 제목, 빈 상태 복사본 및 레이아웃과 같은 구성을 제공하는 **받은 편지함 캠페인**&#x200B;입니다.


## Adobe Journey Optimizer 구성 {#ajo-setup}

웹 SDK을 구현하기 전에 받은 편지함에 콘텐츠를 전달하는 Journey Optimizer의 데이터 스트림, 채널 및 캠페인을 설정하십시오.

1. **Adobe Experience Platform**&#x200B;이(가) 활성화되고 **이벤트 데이터 세트**&#x200B;이(가) 선택된 상태로 **Journey Optimizer**&#x200B;을(를) 서비스로 사용하여 구성된 **데이터 스트림**&#x200B;을(를) 구성합니다.

1. 같은 표면을 공유하는 두 개의 채널 구성을 만듭니다. 한 개의 **콘텐츠 카드** 채널과 한 개의 **받은 편지함** 채널. [콘텐츠 카드 채널을 구성하는 방법을 알아보세요](../content-card/content-card-configuration.md) 및 [받은 편지함 채널을 구성하는 방법을 알아보세요](inbox-configuration.md).

   두 채널의 **페이지 URL** 및 **페이지의 위치**&#x200B;를 필수 구성 요소에서 정의한 표면으로 설정합니다. 이 위치는 웹 SDK 코드에서 쿼리하는 표면과 일치해야 합니다.

1. [콘텐츠 카드 구성에 콘텐츠 카드 채널을 사용하는 콘텐츠 카드 캠페인을 만듭니다](../content-card/create-content-card.md).

   웹 페이지의 사용자 작업에 따라 배달해야 하는 메시지의 경우 관련 작업에 대해 **추가 배달 규칙**&#x200B;을(를) 사용하도록 설정하고 메시지가 표시되는 시기를 결정하는 이벤트 및 값 조건을 설정하십시오. 받은 편지함에서 수신해야 하는 각 알림 유형에 대해 이 작업을 반복합니다.

1. 받은 편지함 채널을 사용하는 [받은 편지함 캠페인을 만듭니다](inbox-create.md). 이 캠페인은 받은 편지함 셸 자체를 구성하는 메타데이터를 제공합니다.

   동일한 사용자에 대해 동시에 활성화되도록 받은 편지함 캠페인의 대상자 및 예약 설정을 콘텐츠 카드 캠페인과 일치시키십시오.

1. 두 캠페인을 모두 활성화합니다.

## 웹 SDK 구현 {#web-sdk-implementation}

받은 편지함은 다음 두 가지 웹 SDK 명령을 사용합니다.

* `subscribeRulesetItems`은(는) 표시 변경에 적합한 제안이 변경될 때마다 실행되는 콜백을 등록합니다.

* `sendEvent`이(가) 해당 제안을 가져옵니다. 나중에 추가 이벤트를 전송하여 표시할 메시지를 업데이트할 수 있습니다.

1. 컨텐츠 카드 및 받은 편지함 스키마, AJO 채널 구성과 일치하는 표면을 정의합니다.

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. 데이터스트림으로 웹 SDK을 구성합니다.

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. 표면 및 스키마에 대한 규칙 세트 항목을 구독하고 콘텐츠 카드 제안이 변경될 때 처리하는 콜백을 제공합니다.

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. 사용자가 애플리케이션과 상호 작용할 때 이벤트를 전송하여 표시되는 콘텐츠 카드 제안을 업데이트하십시오.

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. `subscribeRulesetItems` 콜백에서 제공하는 `collectEvent` 함수를 사용하여 상호 작용을 AJO에 다시 보고합니다. 이렇게 하면 캠페인 보고가 정확하게 수행됩니다.

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. 추가 게재 규칙이 있는 카드(예: `action = deposit-funds`)의 경우 `sendEvent`에만 표시되지 않으므로 일치하는 `decisionContext`을(를) 사용하여 `evaluateRulesets`을(를) 호출하여 트리거하십시오.

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   `subscribeRulesetItems` 콜백은 기존 카드와 함께 포함된 모든 새로 자격을 갖춘 카드로 다시 실행됩니다.

1. 종속성을 설치하고 샘플 서버를 시작합니다.

   ```bash
   npm install
   npm start
   ```

1. 브라우저에서 `https://localhost`을(를) 엽니다.

1. 테스트하기 전에 AJO 환경을 가리키도록 `src/app/page.js`에서 `datastreamId`, `orgId` 및 `SURFACE` 상수를 업데이트하십시오.

{{$include /help/_includes/do-not-localize/inbox/ai-augmented-inbox-configuration-sdk.md}}
