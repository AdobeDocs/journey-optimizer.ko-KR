---
title: 랜딩 페이지 사용 사례
description: Journey Optimizer에서 랜딩 페이지를 사용하는 가장 일반적인 사용 사례를 알아봅니다
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 21%

---

# 랜딩 페이지 사용 사례

다음은 사용 가능한 방법의 예입니다 [!DNL Journey Optimizer] 고객이 일부 또는 모든 통신 수신을 옵트인하거나 옵트아웃하도록 하는 랜딩 페이지.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## 서비스 구독 {#subscription-to-a-service}

수신자가 서비스를 구독하도록 하는 주요 단계는 아래에 나와 있습니다.

![](../assets/lp_subscription-uc.png)

예를 들어, 다음 달에 이벤트를 구성하고, 해당 이벤트에 관심이 있는 고객을 계속 유지하기 위해 이벤트 등록 캠페인을 시작한다고 가정합니다.

1. 이벤트 등록의 구독 목록을 만듭니다. 추가 정보 [구독 목록](subscription-list.md)

1. [랜딩 페이지 만들기](create-lp.md): 수신자가 이벤트에 등록할 수 있도록 해줍니다.

1. 구독 목록에 대한 링크를 포함하여 등록 랜딩 페이지를 구성하고 디자인합니다. 빌드에 대해 자세히 알아보기 [기본 랜딩 페이지](create-lp.md#configure-primary-page)

1. 수신자가 등록 양식을 제출하면 표시되는 감사 인사 페이지를 만듭니다. 추가 정보 [랜딩 하위 페이지](create-lp.md#configure-subpages)

1. 이메일 메시지를 만듭니다. 추가 정보 [메시지 만들기](../create-message.md)

1. [링크 삽입](../message-tracking.md#insert-links) 메시지를 표시합니다. 선택 **[!UICONTROL Landing page]** 로서의 **[!UICONTROL Link type]** 그리고 [랜딩 페이지](create-lp.md#configure-primary-page) 등록용으로 만들 수 있습니다.

   ![](../assets/lp_subscription-uc-link.png)

1. 콘텐츠를 저장하고 [메시지를 게시합니다](../publish-manage-message.md).

1. 을(를) 통해 메시지 보내기 [여정](../building-journeys/journey.md) 이제 이벤트 및 등록 랜딩 페이지로 트래픽을 유도하기 위해 등록 알림을 사용할 수 있습니다.

   전자 메일이 수신되면 수신자가 랜딩 페이지에 대한 링크를 클릭하면 감사 페이지로 이동하며 구독 목록에 추가됩니다.

1. 이벤트에 등록한 수신자에게 확인 이메일을 보낼 수 있습니다. 이렇게 하려면 를 사용하여 다른 여정을 통해 보냅니다 **[!UICONTROL Segment qualification]** 이벤트를 선택하고 세그먼트로 만든 구독 목록을 선택합니다.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 옵트 아웃 {#opt-out}

수신자가 통신에서 구독을 해지하도록 하려면 옵트아웃 랜딩 페이지에 대한 링크를 전자 메일에 포함할 수 있습니다.

수신자의 동의 관리 및 수신자가 [이 섹션](../consent.md).

### 옵트아웃 관리 {#opt-out-management}

수신자가 브랜드로부터 커뮤니케이션 수신을 거부할 수 있는 기능을 제공하는 것은 법적 요구사항입니다. 에서 해당 법률에 대해 자세히 알아보십시오 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

따라서 수신자에게 보내는 모든 이메일에 항상 **구독 취소 링크**&#x200B;를 포함해야 합니다.

* 이 링크를 클릭하면 수신자는 옵트아웃을 확인하는 버튼이 포함된 랜딩 페이지로 이동됩니다.
* 옵트아웃 단추를 클릭하면 프로필 데이터가 이 정보로 업데이트됩니다.

### 옵트아웃 구성 {#configure-opt-out}

메시지 수신자가 랜딩 페이지를 통해 커뮤니케이션에서 가입을 해지할 수 있도록 하려면 아래 단계를 따르십시오.

1. 빌드 [랜딩 페이지](create-lp.md). 랜딩 페이지별 사용 **[!UICONTROL Form]** 구성 요소, 정의 **[!UICONTROL Opt-out]** 확인란을 선택하고 업데이트하도록 선택합니다. **[!UICONTROL Channel (email)]**: 랜딩 페이지에서 옵트아웃 상자를 체크하는 프로필은 모든 통신에서 옵트아웃됩니다. [자세히 알아보기](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [메시지를 ](../create-message.md)[!DNL Journey Optimizer]에 만듭니다.

1. 콘텐츠에서 텍스트를 선택하고 [링크 삽입](../message-tracking.md#insert-links) 상황별 도구 모음 사용. 단추에 대한 링크를 사용할 수도 있습니다.

   ![](../assets/lp_opt-out-insert-link.png)

1. **[!UICONTROL Link type]** 드롭다운 목록에서 **[!UICONTROL Landing page]**&#x200B;을(를) 선택합니다.

1. 을(를) 선택합니다 [랜딩 페이지](create-lp.md#configure-primary-page) 옵트아웃을 위해 만든

   ![](../assets/lp_opt-out-landing-page.png)

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 콘텐츠를 저장하고 [메시지를 게시합니다](../publish-manage-message.md).

1. 을(를) 통해 메시지 보내기 [여정](../building-journeys/journey.md).

1. 메시지가 수신되면 수신자가 구독 취소 링크를 클릭하면 랜딩 페이지가 표시됩니다.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. 수신자가 랜딩 페이지에서 옵트아웃 링크를 클릭하면 프로필 데이터가 업데이트되며, 다시 구독하지 않으면 브랜드로부터 커뮤니케이션을 받지 않습니다.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

해당 프로필의 선택 사항이 업데이트되었는지 확인하려면 Experience Platform으로 이동하여 ID 네임스페이스 및 해당 ID 값을 선택하여 프로필에 액세스합니다. 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

**[!UICONTROL Attributes]** 탭에서 **[!UICONTROL choice]**&#x200B;에 대한 값이 **[!UICONTROL no]**&#x200B;로 변경되었음을 확인할 수 있습니다.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->