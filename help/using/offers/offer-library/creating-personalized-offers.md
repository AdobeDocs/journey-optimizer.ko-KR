---
title: 개인화된 오퍼 만들기
description: Learn how to create, configure and manage your offers
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 5ea04ea9f8ed76b616db1038b917f2d37dea003c
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 3%

---

# 개인화된 오퍼 만들기 {#create-personalized-offers}

Before creating an offer, make sure that you created:

* **** [](../offer-library/creating-placements.md)
* **** [](../offer-library/creating-decision-rules.md)
* **** [](../offer-library/creating-tags.md)

➡️ [비디오에서 이 기능 살펴보기](#video)

**[!UICONTROL Offers]**

![](../assets/offers_list.png)

## 오퍼 만들기 {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="About offer attributes"
>abstract="With offer attributes, you can associate key value pairs with the offer for reporting and analysis purposes."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="Offer attributes"
>abstract="With offer attributes, you can associate key value pairs with the offer for reporting and analysis purposes."

****

1. **[!UICONTROL Create offer]****[!UICONTROL Personalized offer]**

   ![](../assets/create_offer.png)

1. Specify the offer&#39;s name as well as its start and end date and time. Outside of these dates, the offer won’t be selected by the Decisioning engine.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >Updating the start/end dates can have an impact on capping. [자세히 알아보기](add-constraints.md#capping-change-date)

1. **[!UICONTROL tags]** [자세히 알아보기](creating-tags.md).

1. **[!UICONTROL Offer attributes]**

1. Add representations to define where your offer will display in the message. [자세히 알아보기](add-representations.md)

   ![](../assets/channel-placement.png)

1. Add constraints to set the conditions for the offer to be displayed. [자세히 알아보기](add-constraints.md)

   ![](../assets/offer-constraints-example.png)

1. Review and save the offer. [자세히 알아보기](#review)

## Review the offer {#review}

Once eligibility rules and constraints have been defined, a summary of the offer properties displays.

1. Make sure everything is configured properly.

1. **[!UICONTROL Finish]**

1. **[!UICONTROL Save and approve]**&#x200B;를 선택합니다.

   ![](../assets/offer_review.png)

   You can also save the offer as a draft, in order to edit and approve it later on.

**[!UICONTROL Approved]****[!UICONTROL Draft]**

It is now ready to be delivered to users.

![](../assets/offer_created.png)

## Manage offers {#offer-list}

From the offer list, you can select the offer to display its properties. ************

![](../assets/offer_created.png)

**[!UICONTROL Edit]**[](#create-offer)[](#representations)[](#eligibility)

**[!UICONTROL Undo approve]****[!UICONTROL Draft]**

**[!UICONTROL Approved]**

![](../assets/offer_approve.png)

**[!UICONTROL More actions]**

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]** **[!UICONTROL Draft]**
* **[!UICONTROL Delete]**

   >[!CAUTION]
   >
   >The offer and its content will not be accessible anymore. This action cannot be undone.
   >
   >If the offer is used in a collection or a decision, it cannot be deleted. You must remove the offer from any objects first.

* **[!UICONTROL Archive]****[!UICONTROL Archived]** **[!UICONTROL Draft]****[!UICONTROL Approved]** You can only duplicate or delete it.

You can also delete or change the status of multiple offers at the same time by selecting the corresponding checkboxes.

![](../assets/offer_multiple-selection.png)

If you want to change the status of several offers whith different statuses, only the relevant statuses will be changed.

![](../assets/offer_change-status.png)

Once an offer has been created, you can click its name from the list.

![](../assets/offer_click-name.png)

This enables you to access detailed information for that offer. **[!UICONTROL Change log]**[](../get-started/user-interface.md#monitoring-changes)

![](../assets/offer_information.png)

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
