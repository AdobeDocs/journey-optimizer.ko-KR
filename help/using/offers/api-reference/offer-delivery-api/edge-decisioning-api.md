---
title: Deliver offers using the Edge Decisioning API
description: The Adobe Experience Platform Web SDK allows you to retrieve and render personalized offers that you have created using APIs or the Offer Library.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 2%

---

# Deliver offers using the Edge Decisioning API {#edge-decisioning-api}

## Getting started &amp; prerequisites {#edge-overview-and-prerequisites}

[](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview)

The Experience Platform Web SDK supports querying the personalization solutions at Adobe, including Decision Management, allowing you to retrieve and render personalized offers that you have created using APIs or the Offer Library. [](../../get-started/starting-offer-decisioning.md)

[](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) One way is geared towards developers and requires knowledge of websites and programming. The other way is using the Adobe Experience Platform user interface to set up offers which only requires a small script to be referenced in the header of the HTML page.

[](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning)

>[!NOTE]
>
>The use of Decision Management in Adobe Experience Platform Web SDK is currently available in early access to select users. This functionality is not available to all organizations.

## Adobe Experience Platform 웹 SDK {#aep-web-sdk}

Platform Web SDK replaces the following SDKs:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

The SDK did not combine these libraries and is a new implementation from the ground up. To use it, you must first follow these steps:

1. Ensure your organization has the appropriate permissions to use the SDK and you have configured the permissions correctly.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en)

1. Install the SDK. [](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) This page will continue with each different method of implementation.

[](../../../start/get-started-schemas.md)[](../../../start/get-started-datasets.md)

<!-- ****TODO - Configure schema**** -->

To personalize offers, you must separately configure your personalization/profiles.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

To configure the SDK for Offer Decisioning, follow either of two steps below:

## Option 1 - Install the Tag extension and implementation using Launch

This option is more user-friendly for people who may have less coding experience.

1. [](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Install and configure the Platform Web SDK extension with the Datastream you created by selecting the configuration from the “Datastream” dropdown. [](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en)

   ![Adobe Experience Platform 웹 SDK](../../assets/installed-catalog-web-sdk.png)

   ![](../../assets/configure-sdk-extension.png)

1. [](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en) At the bare minimum, you must create a Platform Web SDK Identity Map and a Platform Web SDK XDM Object data element.

   ![ID 맵](../../assets/sdk-identity-map.png)

   ![XDM 개체](../../assets/xdm-object.png)

1. [](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en)

   Add a Platform Web SDK Send Event action and add the relevant decisionScopes to that action’s configuration

   ![](../../assets/rule-render-offer.png)

   ![](../../assets/rule-request-offer.png)

1. [](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en)

## Option 2 - Manually implement using the pre-built stand  alone version

Here are the steps needed to use Offer Decisioning using the prebuilt standalone installation of the web SDK. This guide assumes this is your first time implementing the SDK, so all of the steps may not be applicable to you. This guide also assumes some development experience.

[](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en)`<head>`

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

You will need two IDs from within your Adobe account to set up the SDK configuration - your edgeConfigId and your orgId. The edgeConfigId is the same as your Datastream ID, which you should have configured in the Prerequisites.

To find your edgeConfigID/datastream ID, go to Data Collection and select your Datastream. To find your orgId, go to your profile.

Configure the SDK in JavaScript following the instructions on this page. You will always use your edgeConfigId and orgId in the configuration function. The documentation also describes what optional parameters exist for your configuration. Your final configuration might end up looking something like this:

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

Install the Debugger Chrome extension to use with debugging. <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Next, log into your account within the debugger. Then, go to Logs and make sure you are connected to the correct workspace. Now, copy the base64 encoded version of the decision scope from your offer.

`sendEvent`

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

See the following for an example on how to handle the response:

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

You can use the debugger to verify that you have successfully connected to the Edge network.

>[!NOTE]
>
>If you are not seeing a connection to the edge in the logs, you might need to disable your ad blocker.

Refer back to how you created your offer and the formatting used. Based on the criteria met in the decision, an offer will be returned to you containing the information you specified when creating it within the Adobe Experience Platform.

In this example, the JSON to be returned is:

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Handle the response object and parse the data you need. `sendEvent`

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

`result['decisions'][0]['items'][0]['data']['content']`

To set the JS variables:

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## 제한 사항

Some offer constraints are currently not supported with the mobile Experience Edge workflows, for example Capping. The Capping field value specifies the number of times an offer can be presented across all users. [](../../offer-library/add-constraints.md#capping)
