---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지 사용 사례
description: Journey Optimizer에서 랜딩 페이지를 사용하는 가장 일반적인 사용 사례를 알아봅니다
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 16%

---

# 랜딩 페이지 사용 사례 {#lp-use-cases}

다음은 사용 가능한 방법의 몇 가지 예입니다 [!DNL Journey Optimizer] 고객이 일부 또는 모든 통신 수신을 옵트인하거나 옵트아웃하도록 하는 랜딩 페이지.

## 서비스 구독 {#subscription-to-a-service}

가장 일반적인 사용 사례 중 하나는 고객을 [서비스 구독](subscription-list.md) (예: 뉴스레터 또는 이벤트) 를 랜딩 페이지로 이동할 수 있습니다. 주요 단계는 아래 그래프에 나와 있습니다.

![](assets/lp_subscription-uc.png)

예를 들어 다음 달에 이벤트를 구성하고 이벤트 등록 캠페인을 시작한다고 가정합니다<!--to keep your customers that are interested updated on that event-->. 이렇게 하려면 수신자가 이 이벤트에 등록할 수 있도록 랜딩 페이지에 대한 링크가 포함된 이메일을 보냅니다. 등록하는 사용자는 이 목적으로 만든 구독 목록에 추가됩니다.

### 랜딩 페이지 설정 {#set-up-lp}

1. 등록된 사용자를 저장할 이벤트 등록의 구독 목록을 만듭니다. 구독 목록을 만드는 방법을 알아봅니다 [여기](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [랜딩 페이지 만들기](create-lp.md) 을 클릭하여 수신자가 이벤트에 등록할 수 있도록 합니다.

   ![](assets/lp_create-lp-details.png)

1. 등록 구성 [기본 랜딩 페이지](create-lp.md#configure-primary-page).

1. 디자인 시 [랜딩 페이지 콘텐츠](design-lp.md)에서 만든 구독 목록을 선택하여 등록 확인란을 선택하는 프로필로 업데이트합니다.

   ![](assets/lp_subscription-uc-lp-list.png)

1. 수신자가 등록 양식을 제출하면 사용자에게 표시될 &#39;감사 인사&#39; 페이지를 만듭니다. 랜딩 하위 페이지를 구성하는 방법 알아보기 [여기](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [게시](create-lp.md#publish) 랜딩 페이지.

1. 다음 [여정](../building-journeys/journey.md), 추가 **이메일** 활동을 통해 트래픽을 등록 랜딩 페이지로 유도할 수 있습니다.

   ![](assets/lp_subscription-uc-journey.png)

1. [이메일 디자인](../messages/get-started-content.md) 이제 해당 이벤트에 대한 등록이 열려 있음을 알려주십시오.

1. [링크 삽입](../design/message-tracking.md#insert-links) 메시지 콘텐츠에 삽입하십시오. 선택 **[!UICONTROL 랜딩 페이지]** 로서의 **[!UICONTROL 링크 유형]** 그리고 [랜딩 페이지](create-lp.md#configure-primary-page) 등록용으로 만들 수 있습니다.

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >메시지를 보내려면 선택한 랜딩 페이지가 아직 만료되지 않았는지 확인하십시오. 만료 날짜를 업데이트하는 방법 알아보기 [이 섹션](create-lp.md#configure-primary-page).

   전자 메일이 수신되면 수신자가 랜딩 페이지에 대한 링크를 클릭하면 &#39;감사 인사&#39; 페이지로 이동하며 구독 목록에 추가됩니다.

### 확인 이메일 보내기 {#send-confirmation-email}

또한 이벤트에 등록한 수신자에게 확인 이메일을 보낼 수 있습니다. 이렇게 하려면 아래 절차를 따르십시오.

1. 다른 만들기 [여정](../building-journeys/journey.md). 을(를) 클릭하여 랜딩 페이지에서 직접 수행할 수 있습니다 **[!UICONTROL 여정 만들기]** 버튼을 클릭합니다. [여기](create-lp.md#configure-primary-page)에서 추가 정보를 확인하십시오

   ![](assets/lp_subscription-uc-create-journey.png)

1. 을(를) 펼칩니다. **[!UICONTROL 이벤트]** 카테고리 및 삭제 **[!UICONTROL 세그먼트 자격]** 활동을 캔버스로 이동합니다. [여기](../building-journeys/segment-qualification-events.md)에서 추가 정보를 확인하십시오

1. 을(를) 클릭합니다. **[!UICONTROL 세그먼트]** 필드를 작성하고 만든 구독 목록을 선택합니다.

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. 선택한 확인 이메일을 추가하고 여정을 통해 보냅니다.

   ![](assets/lp_subscription-uc-confirm-email.png)

이벤트에 등록한 모든 사용자는 확인 이메일을 받게 됩니다.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 옵트 아웃 {#opt-out}

수신자가 통신에서 구독을 해지하도록 하려면 옵트아웃 랜딩 페이지에 대한 링크를 전자 메일에 포함할 수 있습니다.

수신자의 동의 관리 및 수신자가 [이 섹션](../privacy/opt-out.md).

### 옵트아웃 관리 {#opt-out-management}

수신자가 브랜드로부터 커뮤니케이션 수신을 거부할 수 있는 기능을 제공하는 것은 법적 요구사항입니다. [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=ko#regulations){target=&quot;_blank&quot;}에서 해당 법률에 대해 자세히 알아보세요.

따라서 수신자에게 보내는 모든 이메일에 항상 **구독 취소 링크**&#x200B;를 포함해야 합니다.

* 이 링크를 클릭하면 수신자는 옵트아웃을 확인하는 버튼이 포함된 랜딩 페이지로 이동됩니다.
* 옵트아웃 단추를 클릭하면 프로필 데이터가 이 정보로 업데이트됩니다.

### 옵트아웃 구성 {#configure-opt-out}

이메일 수신자가 랜딩 페이지를 통해 커뮤니케이션에서 가입을 해지할 수 있도록 하려면 아래 단계를 따르십시오.

1. 랜딩 페이지를 만듭니다. [자세히 보기](create-lp.md)

1. 기본 페이지를 정의합니다. [자세히 보기](create-lp.md#configure-primary-page)

1. [디자인](design-lp.md) 기본 페이지 컨텐츠: 랜딩 페이지별 사용 **[!UICONTROL 양식]** 구성 요소, 정의 **[!UICONTROL 옵트아웃]** 확인란을 선택하고 업데이트하도록 선택합니다. **[!UICONTROL 채널(이메일)]**: 랜딩 페이지에서 옵트아웃 상자를 체크하는 프로필은 모든 통신에서 옵트아웃됩니다.

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. 확인 추가 [하위 페이지](create-lp.md#configure-subpages) 양식을 제출하는 사용자에게 표시됩니다.

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >기본 페이지의 **[!UICONTROL 클릭유도문안]** 섹션 **[!UICONTROL 양식]** 구성 요소. [자세히 보기](design-lp.md)

1. 페이지의 콘텐츠를 구성하고 정의했으면, [게시](create-lp.md#publish) 랜딩 페이지.

   ![](assets/lp_opt-out-publish.png)

1. [이메일 메시지 만들기](../messages/get-started-content.md) 여정에 있을 때 사용됩니다.

1. 콘텐츠에서 텍스트를 선택하고 상황별 도구 모음을 사용하여 [링크를 삽입합니다. ](../design/message-tracking.md#insert-links) 단추에 대한 링크를 사용할 수도 있습니다.

   ![](assets/lp_opt-out-insert-link.png)

1. 선택 **[!UICONTROL 랜딩 페이지]** 에서 **[!UICONTROL 링크 유형]** 드롭다운 목록을 선택하고 [랜딩 페이지](create-lp.md#configure-primary-page) 옵트아웃을 위해 만든

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >메시지를 보내려면 선택한 랜딩 페이지가 아직 만료되지 않았는지 확인하십시오. 만료 날짜를 업데이트하는 방법 알아보기 [이 섹션](create-lp.md#configure-primary-page).

1. 여정을 게시하고 실행합니다. [자세히 알아보기](../building-journeys/journey.md).

1. 메시지가 수신되면 수신자가 이메일에서 가입 해지 링크를 클릭하면 랜딩 페이지가 표시됩니다.

   ![](assets/lp_opt-out-submit-form.png)

   수신자가 상자를 선택하고 양식을 제출하는 경우:

   * 옵트아웃 수신자는 확인 메시지 화면으로 리디렉션됩니다.

   * 프로필 데이터가 업데이트되며, 다시 구독하지 않으면 브랜드로부터 커뮤니케이션을 받지 않습니다.

해당 프로필의 선택 사항이 업데이트되었는지 확인하려면 Experience Platform으로 이동하여 ID 네임스페이스 및 해당 ID 값을 선택하여 프로필에 액세스합니다. [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target=&quot;_blank&quot;}에서 자세한 내용을 알아보세요.

![](assets/lp_opt-out-profile-choice.png)

에서 **[!UICONTROL 속성]** 탭에서 **[!UICONTROL 선택]** 이(가) **[!UICONTROL 아니요]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../privacy/opt-out.md#unsubscribe-header)

////////


## Leverage landing page submission event {#leverage-lp-event}

You can use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.

To do this, you need to create an event containing the landing page submission information and use it in a journey. Follow the steps below.

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**, and in the **[!UICONTROL Events]** section, select **[!UICONTROL Manage]**.

    ![](assets/lp_subscription-uc-configurations.png)

1. The list of events displays. Select **[!UICONTROL Create Event]**.

    ![](assets/lp_subscription-uc-create-event.png)

1. The event configuration pane opens on the right side of the screen. Configure a rule-based unitary event. [Learn more](../event/about-creating.md)

1. Define the schema: select **[!UICONTROL AJO Email Tracking Experience Event Schema v.1]** (available by default in [!DNL Journey Optimizer]).

    ![](assets/lp_subscription-uc-event-schema.png)

1. In the **[!UICONTROL Fields]** section, select the following elements:

    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Interaction Type]**
    
    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Landing Page Details]** > **[!UICONTROL Landing Page ID]**

    ![](assets/lp_subscription-uc-event-fields.png)

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple expression editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/segment-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
