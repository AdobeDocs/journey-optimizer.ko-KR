---
title: 캠페인 만들기
description: 에서 캠페인을 만드는 방법을 알아봅니다 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 4%

---

# 캠페인 만들기 {#create-campaign}

>[!NOTE]
>
>새 캠페인을 만들기 전에 표면 채널(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 준비가 되었는지 확인하십시오. 자세한 내용은 다음 섹션을 참조하십시오.
>
>* [채널 표면 생성](../configuration/channel-surfaces.md)
>* [세그먼트 시작](../segment/about-segments.md)


## 캠페인 구성 {#configure}

캠페인을 만드는 단계는 다음과 같습니다.

1. 액세스 권한 **[!UICONTROL Campaigns]** 메뉴를 클릭한 다음 **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

   >[!NOTE]
   >
   >기존 라이브 캠페인을 복제하여 새 라이브 캠페인을 만들 수도 있습니다.[자세히 알아보기](modify-stop-campaign.md#duplicate) <!-- check if only live campaigns-->

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. 에서 **[!UICONTROL Actions]** 섹션에서 메시지를 보내는 데 사용할 채널과 채널 표면을 선택한 다음 **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >캠페인 유형(마케팅 또는 트랜잭션)과 호환되는 채널 표면만 드롭다운 목록에 나열됩니다.

1. 캠페인의 제목과 설명을 지정합니다.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 에서 **[!UICONTROL Actions]** 섹션에서 캠페인과 함께 전송할 메시지를 구성합니다.

   1. 을(를) 클릭합니다. **[!UICONTROL Edit content]** 버튼을 클릭한 다음 메시지 콘텐츠를 구성하고 디자인합니다. [메시지에 대해 자세히 알아보기](../messages/get-started-content.md)

      >[!NOTE]
      >
      >다음 **[!UICONTROL Simulate content]** 단추를 사용하면 테스트 프로필을 사용하여 콘텐츠를 미리 보고 테스트할 수 있습니다. [자세히 보기](../design/preview.md)

   1. 콘텐츠가 준비되면 화살표를 클릭하여 캠페인 만들기 화면으로 돌아갑니다.

      ![](assets/create-campaign-design.png)

   1. 에서 **[!UICONTROL Actions tracking]** 섹션에서 수신자가 게재에 어떻게 반응하는지를 추적할지 지정합니다.

      캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report.md)

1. 타겟팅할 대상을 정의합니다. 이렇게 하려면 **[!UICONTROL Select audience]** 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시하는 단추. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   에서 **[!UICONTROL Identity namespace]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 캠페인에서 타겟팅되지 않습니다.

1. 캠페인의 시작 및 종료 날짜를 구성합니다. 기본적으로 캠페인은 수동으로 활성화되면 시작되고, 메시지가 한 번 전송되면 종료되도록 구성됩니다.

1. 또한 캠페인에 구성된 작업 실행 빈도를 지정할 수 있습니다.

   <!-- NOTE For API-triggered campaigns, scheduling at a specific date and time with recurrence is not available as action is triggered via API. However, start and end date are relevant to ensure that, if an API call is made prior of after the window, then those get errored.-->

   ![](assets/create-campaign-schedule.png)

<!--1. If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

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

1. 이제 캠페인이 활성화되고 이(가) 있습니다 **[!UICONTROL Live]** 상태(또는 **[!UICONTROL Scheduled]**  시작 날짜를 지정한 경우). [캠페인 상태에 대해 자세히 알아보기](get-started-with-campaigns.md#statuses). 캠페인에 구성된 메시지가 즉시 또는 지정된 날짜에 실행됩니다.

   >[!NOTE]
   >
   >다음 **[!UICONTROL Completed]** 상태는 활성화한 후 3일 후 캠페인에 자동으로 할당되거나, 반복 실행이 있는 경우 캠페인의 종료 날짜에 할당됩니다.
   >
   >종료 날짜를 지정하지 않은 경우 캠페인이 &quot;라이브&quot; 상태를 유지합니다. 변경하려면 캠페인을 수동으로 중지해야 합니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md)

1. 캠페인이 활성화되면 언제든지 해당 정보를 열어 확인할 수 있습니다. 요약에서는 타겟팅된 프로필 및 배달되고 실패한 작업 수에 대한 통계를 가져올 수 있습니다.

   전용 보고서에서 **[!UICONTROL Reports]** 버튼을 클릭합니다. [자세히 보기](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
