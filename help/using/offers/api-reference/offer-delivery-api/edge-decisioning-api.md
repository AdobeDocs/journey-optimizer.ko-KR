---
title: Edge Decisioning API를 사용하여 오퍼 게재
description: The Adobe Experience Platform Web SDK allows you to retrieve and render personalized offers that you have created using APIs or the Offer Library.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: b02981f2c0cf74c8dba657570157709bc422d94c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 3%

---


# Deliver offers using the Edge Decisioning API {#edge-decisioning-api}

## Getting started &amp; prerequisites {#aep-web-sdk-overview-and-prerequisites}

The [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) is a client-side JavaScript library that allows Adobe Experience Cloud customers to interact with the various services in the Experience Cloud through the Experience Platform Edge Network.

The Experience Platform Web SDK supports querying the personalization solutions at Adobe, including Decision Management, allowing you to retrieve and render personalized offers that you have created using APIs or the Offer Library. 자세한 지침은 [오퍼 만들기](../../get-started/starting-offer-decisioning.md).

를 사용하여 Offer decisioning을 구현하는 방법에는 두 가지가 있습니다 [Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 한 가지 방법은 개발자를 위한 것이고 웹 사이트와 프로그래밍에 대한 지식이 필요합니다. 다른 방법은 Adobe Experience Platform 사용자 인터페이스를 사용하여 HTML 페이지의 헤더에서 작은 스크립트만 참조하도록 하는 오퍼를 설정하는 것입니다.

다음 문서를 참조하십시오. [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) platform Web SDK를 사용하여 개인화된 오퍼를 제공하는 방법에 대한 자세한 정보.

>[!NOTE]
>
>Adobe Experience Platform Web SDK에서 의사 결정 관리 를 사용하는 경우 현재 사용자를 선택하기 위해 일찍 액세스할 수 있습니다. 모든 IMS 조직에서는 이 기능을 사용할 수 없습니다.

## Adobe Experience Platform 웹 SDK  {#aep-web-sdk-overview-and-prerequisites}

Platform Web SDK replaces the following SDKs:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

The SDK did not combine these libraries and is a new implementation from the ground up. 사용하려면 먼저 다음 단계를 수행해야 합니다.

1. 조직에 SDK를 사용할 수 있는 적절한 권한이 있고 권한이 올바르게 구성되었는지 확인합니다.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) ( Adobe Experience Cloud에서 계정의 데이터 수집 탭 내).

1. SDK를 설치합니다. There are multiple methods of doing so, which are covered on the [Install the SDK page](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). 이 페이지는 각 서로 다른 구현 방법으로 계속 진행됩니다.

In order to use the SDK, you must have a [schema](../../../start/get-started-schemas.md) and a [datastream](../../../start/get-started-datasets.md) defined.

<!-- ****TODO - Configure schema**** -->

오퍼를 개인화하려면 개인화/프로필을 별도로 구성해야 합니다.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

To configure the SDK for Offer Decisioning, follow either of two steps below:

## Option 1 - Install the Tag extension and implementation using Launch

This option is more user-friendly for people who may have less coding experience.

1. [태그 속성 만들기](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [Add the embed code](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Install and configure the Platform Web SDK extension with the Datastream you created by selecting the configuration from the “Datastream” dropdown. 다음 문서를 참조하십시오. [확장](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform 웹 SDK](../../assets/installed-catalog-web-sdk.png)

   ![확장 구성](../../assets/configure-sdk-extension.png)

1. 필요한 만들기 [데이터 요소](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). At the bare minimum, you must create a Platform Web SDK Identity Map and a Platform Web SDK XDM Object data element.

   ![ID 맵](../../assets/sdk-identity-map.png)

   ![XDM 개체](../../assets/xdm-object.png)

1. 만들기 [규칙](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Add a Platform Web SDK Send Event action and add the relevant decisionScopes to that action’s configuration

   ![오퍼 렌더링](../../assets/rule-render-offer.png)

   ![오퍼 요청](../../assets/rule-request-offer.png)

1. [Create and publish](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) a library containing all the relevant Rules, Data Elements, and Extensions you have configured.

## Option 2 - Manually implement using the pre-built stand  alone version

Here are the steps needed to use Offer Decisioning using the prebuilt standalone installation of the web SDK. This guide assumes this is your first time implementing the SDK, so all of the steps may not be applicable to you. 이 안내서에서는 일부 개발 경험도 가정합니다.

옵션 2에서 다음 JavaScript 코드 조각을 포함합니다. 사전 빌드된 독립형 버전 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 에서 `<head>` 섹션에 있는 마지막 항목이 될 필요가 없습니다.


## 제한 사항

일부 오퍼 제한 사항은 현재 모바일 Experience Edge 워크플로우에서 지원되지 않습니다(예: 최대 가용량). The Capping field value specifies the number of times an offer can be presented across all users. 자세한 내용은 [오퍼에 제한 추가](../../offer-library/add-constraints.md#capping).
