---
title: 캠페인 만들기
description: 에서 캠페인을 만드는 방법을 알아봅니다 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 3%

---


# 캠페인 만들기 {#create-campaign}

>[!NOTE]
>
>새 캠페인을 만들기 전에 메시지 사전 설정과 Adobe Experience Platform 세그먼트를 사용할 수 있는지 확인하십시오. 자세한 내용은 다음 섹션을 참조하십시오.
>
>* [메시지 사전 설정 만들기](../configuration/message-presets.md)
>* [세그먼트 시작](../segment/about-segments.md)


## 캠페인 구성 {#configure}

캠페인을 만드는 단계는 다음과 같습니다.

1. 액세스 권한 **[!UICONTROL Campaigns]** 메뉴를 클릭한 다음 **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date,
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. In this case, profiles to be targeted and triggers for actions need to be set via the API call.-->

1. 에서 **[!UICONTROL Actions]** 섹션에서 메시지를 보내는 데 사용할 채널과 메시지 표면(즉, 메시지 사전 설정)을 선택합니다.

   ![](assets/create-campaign-action.png)

1. 캠페인의 제목과 설명을 지정합니다.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

   ![](assets/create-campaign-properties.png)

1. 에서 **[!UICONTROL Actions]** 섹션에서 캠페인과 함께 전송할 메시지를 구성합니다.

   1. 을(를) 클릭합니다. **[!UICONTROL Edit content]** 버튼을 클릭한 다음 메시지를 구성하고 디자인합니다. [메시지 구성 방법 알아보기](../messages/get-started-content.md).

      콘텐츠가 준비되면 화살표를 클릭하여 캠페인 만들기 화면으로 돌아갑니다.

      ![](assets/create-campaign-design.png)

   1. 에서 **[!UICONTROL Actions tracking]** 섹션에서 수신자가 게재에 어떻게 반응하는지를 추적할지 지정합니다.

      캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](campaign-global-report.md)

      ![](assets/create-campaign-action-properties.png)

1. 타겟팅할 대상을 정의합니다. 이렇게 하려면 **[!UICONTROL Select audience]** 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시하는 단추. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

   ![](assets/create-campaign-audience.png)

   <!--By default, the targeted audience for in-app messages includes all the users of the selected mobile application.-->

   에서 **[!UICONTROL Identity namespace]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 캠페인에서 타겟팅되지 않습니다. <!--info vue dans section journeys, read segment-->

   <!--If you are creating a campaign to send an in-app message, you can choose how and when the message will be shown to the audience using existing mobile app triggers.-->
   <!-- where are triggers configured?-->

1. 캠페인의 시작 및 종료 날짜를 구성합니다.

   기본적으로 캠페인은 수동으로 활성화되면 시작되고, 메시지가 한 번 전송되면 종료되도록 구성됩니다.

1. 또한 캠페인에 구성된 작업을 실행할 빈도를 구성할 수 있습니다.

   ![](assets/create-campaign-schedule.png)

캠페인이 준비되면 검토하고 게시할 수 있습니다( [캠페인 검토 및 활성화](#review-activate)).

## 캠페인 검토 및 활성화 {#review-activate}

캠페인이 구성되면 활성화하기 전에 매개 변수와 콘텐츠를 검토해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. campaign 구성 화면에서 를 클릭합니다. **[!UICONTROL Review to activate]** 캠페인 요약을 표시합니다.

   요약에서는 필요한 경우 캠페인을 수정하고 매개 변수가 잘못되었거나 누락되었는지 확인할 수 있습니다.

   >[!IMPORTANT]
   >
   >오류가 발생하면 캠페인을 활성화할 수 없습니다. 계속하기 전에 오류를 해결하십시오.

   ![](assets/create-campaign-alerts.png)

1. 캠페인이 올바르게 구성되었는지 확인하고 를 클릭합니다. **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. 이제 캠페인이 활성화되고 이(가) 있습니다 **[!UICONTROL Live]** 상태(또는 **[!UICONTROL Scheduled]**  시작 날짜를 지정한 경우). [캠페인 상태에 대해 자세히 알아보기](get-started-with-campaigns.md#statuses)

   캠페인에 구성된 메시지가 즉시 또는 지정된 날짜에 실행됩니다.

   >[!NOTE]
   >
   >캠페인이 활성화되면 메시지가 실행된 후에도 &quot;라이브&quot; 상태를 유지합니다. 상태를 변경하려면 수동으로 중지해야 합니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md)

1. 캠페인이 활성화되면 언제든지 해당 정보를 열어 확인할 수 있습니다. 요약에서는 타겟팅된 프로필 및 배달되고 실패한 작업 수에 대한 통계를 가져올 수 있습니다.

   전용 보고서에서 **[!UICONTROL Reports]** 버튼을 클릭합니다. [자세히 보기](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >캠페인에서 생성된 메시지는 [!DNL Journey Optimizer] campaign 기능을 사용할 수 있습니다. 만든 후에 캠페인에서만 액세스할 수 있고, 에는 표시되지 않습니다. **[!UICONTROL Messages]** 메뉴 아래의 제품에서 사용할 수 있습니다.