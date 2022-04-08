---
title: Add constraints to an offer
description: Learn how to define the conditions for an offer to be displayed
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 5ea04ea9f8ed76b616db1038b917f2d37dea003c
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 3%

---

# Add constraints to an offer {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="About offer constraints"
>abstract="With constraints, you can specify how the offer is prioritized and presented to the user compared to other offers."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="About offer priority"
>abstract="In this field, you can specify priority settings for the offer. Priority is a number used to rank offers that meet all constraints such as eligibility, dates, and capping."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="우선 순위"
>abstract="The priority helps define the priority of the offer compared to other ones if the user qualifies for more than one offer. The higher an offer&#39;s priority will be, the higher its priority will be compared to other offers."

Constraints allow you to define the conditions under which an offer will be displayed.

1. **[!UICONTROL Offer eligibility]** [자세히 알아보기](#eligibility)

   ![](../assets/offer-eligibility.png)

1. **[!UICONTROL Priority]** The higher an offer&#39;s priority will be, the higher its priority will be compared to other offers.

   ![](../assets/offer-priority.png)

1. **[!UICONTROL Capping]** [자세히 알아보기](#capping)

   ![](../assets/offer-capping.png)

1. **[!UICONTROL Next]**

For example, if you set the following constraints:

![](../assets/offer-constraints-example.png)

* The offer will be considered for users that match the &quot;Gold Loyalty Customers&quot; decision rule only.
* The offer&#39;s priority is set to &quot;50&quot;, meaning the offer will be presented before offers with a priority between 1 and 49, and after the ones with a priority of at least 51.
* The offer will be presented only once per user accross all placements.

## Eligibility {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Eligibility"
>abstract="Offer eligibility allows you to restrict the offer to specific profiles that you define using segments or decision rules."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="About offer eligibility"
>abstract="In this section, you can use decision rules to determine which users are eligible to the offer."
>additional-url="https://video.tv.adobe.com/v/329373" text="데모 비디오 시청"

**[!UICONTROL Offer eligibility]**

>[!NOTE]
>
>********[](#segments-vs-decision-rules)

* **[!UICONTROL All visitors]**

   ![](../assets/offer-eligibility-default.png)

* [](../../segment/about-segments.md)

   **[!UICONTROL Visitors who fall into one or multiple segments]****[!UICONTROL And]****[!UICONTROL Or]**

   ![](../assets/offer-eligibility-segment.png)

* [](../offer-library/creating-decision-rules.md)**[!UICONTROL By defined decision rule]****[!UICONTROL Decision rule]**

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >[!DNL Journey Optimizer] [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events)

### Using segments vs decision rules {#segments-vs-decision-rules}

********

Basically, the output of a segment is a list of profiles, whereas a decision rule is a function executed on demand against a single profile during the decisioning process. The difference between those two usages are detailed below.

* **세그먼트**

   On one hand, segments are a group of Adobe Experience Platform profiles that match a certain logic based on profile attributes and experience events. However, Offer Management does not recompute the segment, which may not be up-to-date when presenting the offer.

   [](../../segment/about-segments.md)

* **의사 결정 규칙**

   On the other hand, a decision rule is based on data available in Adobe Experience Platform and determines to whom an offer can be shown. Once selected in an offer or a decision for a given placement, the rule is executed every single time a decision is made, which ensures that each profile gets the latest and the best offer.

   [](creating-decision-rules.md)

## Frequency capping {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="About offer capping"
>abstract="In this field, you can specify how many times the offer can be presented."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Capping"
>abstract="Capping is used as a constraint to define the maximum number of times an offer can be presented."

Capping is used as a constraint to define the maximum number of times an offer can be presented.

Limiting the number of times users get specific offers allows you to avoid over-solicitating your customers and thus to optimize each touchpoint with the best offer.

To set capping, follow the steps below.

1. Define the number of times the offer can be presented.

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >The number must be greater than 0.

1. Specify if you want the capping to be applied accross all users or to one specific profile:

   ![](../assets/offer-capping-total.png)

   * **[!UICONTROL In total]**

      For example, if you are an electronics retailer having a &#39;TV doorbuster deal&#39;, you want the offer to be only returned 200 times across all profiles.

   * **[!UICONTROL Per profile]**

      For example, if you are a bank with a &#39;Platinum credit card&#39; offer, you don&#39;t want this offer to be shown more than 5 times per profile. Indeed, you believe that if the user has seen the offer 5 times and not acted on it, they have a higher chance to act on the next best offer.

1. [](#representations)**[!UICONTROL All placements]****[!UICONTROL Per placement]**

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL All placements]**

      ************

   * **[!UICONTROL Per placement]**

      ************

1. Once saved and approved, if the offer has been presented the number of times you have specified in this field according to the criteria you defined, its delivery will stop.

The number of times an offer is proposed is calculated at email preparation time. 예를 들어, 많은 수의 오퍼가 포함된 이메일을 준비하는 경우 해당 숫자는 이메일 전송 여부와 관계없이 최대 상한에 포함됩니다.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>Capping counters will reset when the offer expires or 2 years after the offer start date, whichever comes first. [](creating-personalized-offers.md#create-offer)

### Impact of changing dates on capping {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="Changing the date may have an impact on capping"
>abstract="If capping is applied to this offer, it may be impacted when you change the start or end date."

You must proceed with care when changing the date of an offer, because this can have an impact on capping if the following conditions are met:

* [](#review)
* [](#capping)
* Capping is defined per profile.

>[!NOTE]
>
>[](creating-personalized-offers.md#create-offer)

Frequency capping per profile stores the capping counts on each profile. When you change the start and end date of an approved offer, the capping count for some profiles could be impacted according to the different scenarios described below.

![](../assets/offer-capping-change-date.png)

****

| <br> | <br> | Possible impact on the capping count |
|--- |--- |--- |
| ... the offer start date is updated before the original offer start date has begun, | ... the capping count will begin on the new start date. | 아니요 |
| ... the new start date is before the current end date, | ... the capping will continue with a new start date and the previous capping count for each profile will carry forward. | 아니요 |
| ... the new start date is after the current end date, | ... the current capping will expire and the new capping count will start again from 0 for all profiles on the new start date. | 예 |

****

| <br> | <br> | Possible impact on the capping count |
|--- |--- |--- |
| ... a decisioning request occurs before the original offer end date, | ... the capping count will be updated and the previous capping count for each profile will carry forward. | 아니요 |
| ... no decisioning request occurs before the original end date, | ... the capping count will reset on the original end date for each profile. The new capping count will then start again from 0 for any new decisioning requests that will occur after the original end date. | 예 |

**예**

********

1. Profiles X, Y and Z are presented the offer.
1. ********
1. ****

   * ********
   * ********

![](../assets/offer-capping-change-date-ex.png)
