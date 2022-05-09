---
title: 제외 목록
description: Learn what the suppression list is, its purpose and what is included in it.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 3%

---

# 제외 목록 {#suppression-list}

A suppression list consists of email addresses that you want to exclude from your deliveries, because sending to these contacts could hurt your sending reputation and delivery rates.

[!DNL Journey Optimizer]

It gathers email addresses and domains that are suppressed across all mailings in a single client environment, meaning specific to an organization ID associated with a sandbox ID.

## Why a suppression list? {#why-suppression-list}

To control the email messages that are received by their inbox owners and ensure they only receive those they want, Internet service providers (ISPs) and commercial spam filters have their proprietary algorithms to track the overall reputation of email senders based on the IP addresses and sending domain(s) they use.

If you do not take their feedback (such as spam complaints, bounces, etc.) into account, they will rate your reputation down. The suppression list helps you with honoring the ISPs&#39; feedback.

The recipients whose email addresses are suppressed are automatically excluded from message delivery. 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다.

## What&#39;s on the suppression list? {#what-s-on-suppression-list}

Email addresses are added to the suppression list as follows:

* ********

* **** [](../configuration/retries.md)

* [****](../configuration/manage-suppression-list.md#add-addresses-and-domains)

[](#delivery-failures)

>[!NOTE]
>
>[!DNL Journey Optimizer] Their choice is handled at the Experience Platform level. [](../messages/consent.md)

For each address, the basic reason for being suppressed and the suppression category (soft, hard, etc.) are displayed in the suppression list. [](../configuration/manage-suppression-list.md)

>[!NOTE]
>
>**[!UICONTROL Suppressed]** ****[](../building-journeys/read-segment.md)[](../building-journeys/journeys-message.md)******[!UICONTROL Sent]**
>
>[](../reports/live-report.md)[](../reports/global-report.md) [](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html)

### 게재 실패 {#delivery-failures}

There are two types of errors when a delivery fails:

* **** A hard bounce indicates an invalid email address (i.e. an email address that does not exist). This involves a bounce message from the receiving email server that explicitly states that the address is invalid.
* **** This is a temporary email bounce that occurred for a valid email address.

****

****<!--or an **ignored** error--> [](../configuration/retries.md)

If you continue sending to these addresses, it may affect your delivery rates, because it tells ISPs that you may not be following email address list maintenance best practices, and therefore may not be a trustworthy sender.

### Spam complaints {#spam-complaints}

The suppression list collects email addresses that mark your message as spam. For example, if someone writes to a customer service requesting to never receive mail again from you, the email address of that person will be suppressed across your instance and you won&#39;t be able to deliver to that address anymore.

Sending to recipients after they submit a spam complaint may have a huge impact on your sending reputation, because it informs ISPs that you may send unwanted emails and may not listen to your recipients.

This could lead to your IP address or sending domain being blocked, which can be avoided with these addresses being on the suppression list.
