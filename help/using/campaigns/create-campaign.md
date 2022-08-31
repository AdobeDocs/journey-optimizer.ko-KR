---
title: 캠페인 만들기
description: 에서 캠페인을 만드는 방법을 알아봅니다 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 11%

---

# 캠페인 만들기 {#create-campaign}

>[!NOTE]
>
>새 캠페인을 만들기 전에 표면 채널(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 준비가 되었는지 확인하십시오. 자세한 내용은 다음 섹션을 참조하십시오.
>
>* [채널 표면 생성](../configuration/channel-surfaces.md)
>* [세그먼트 시작](../segment/about-segments.md)


## 첫 번째 캠페인 만들기 {#create}

1. 액세스 권한 **[!UICONTROL Campaigns]** 메뉴를 클릭한 다음 **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >기존 라이브 캠페인을 복제하여 새 라이브 캠페인을 만들 수도 있습니다. [자세히 보기](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. 에서 **[!UICONTROL Actions]** 섹션에서 메시지를 보내는 데 사용할 채널과 채널 표면을 선택한 다음 **[!UICONTROL Create]**.

   표면은 [시스템 관리자](../start/path/administrator.md)에 의해 정의된 구성입니다. 여기에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >마케팅 캠페인 유형과 호환되는 채널 표면만 드롭다운 목록에 나열됩니다.

<!--Only channel surfaces compatible with the campaign type (marketing or transactional) are listed in the drop-down list.-->

1. 캠페인의 제목과 설명을 지정합니다.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 에서 **[!UICONTROL Actions]** 섹션에서 캠페인과 함께 전송할 메시지를 구성합니다.

   1. 을(를) 클릭합니다. **[!UICONTROL Edit content]** 버튼을 클릭한 다음 메시지 콘텐츠를 구성하고 디자인합니다. [메시지에 대해 자세히 알아보기](../messages/get-started-content.md).

      다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 배웁니다.

      * [이메일 만들기](../messages/create-email.md)
      * [푸시 알림 만들기](../messages/create-push.md)
      * [SMS 메시지 만들기](../messages/create-sms.md)
   1. 컨텐츠가 정의되면 **[!UICONTROL Simulate content]** 테스트 프로필로 컨텐츠를 미리 보고 테스트할 수 있습니다. [자세히 알아보기](../design/preview.md).

   1. 화살표를 클릭하여 캠페인 만들기 화면으로 돌아갑니다.

      ![](assets/create-campaign-design.png)

   1. 에서 **[!UICONTROL Actions tracking]** 섹션에서 수신자가 게재에 어떻게 반응하는지를 추적할지 지정합니다. 클릭 및/또는 열기를 추적할 수 있습니다.

      캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report.md)


1. 타겟팅할 대상을 정의합니다. 이렇게 하려면 **[!UICONTROL Select audience]** 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시하는 단추. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   에서 **[!UICONTROL Identity namespace]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 캠페인에서 타겟팅되지 않습니다.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. 특정 날짜 또는 반복 빈도로 캠페인을 실행하려면 를 구성합니다 **[!UICONTROL Schedule]** 섹션을 참조하십시오. [캠페인을 예약하는 방법 알아보기](#schedule)

캠페인이 준비되면 검토하고 게시할 수 있습니다. [자세히 보기](#review-activate)

## 캠페인 검토 및 활성화 {#review-activate}

캠페인이 구성되면 활성화하기 전에 매개 변수와 콘텐츠를 검토해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. campaign 구성 화면에서 를 클릭합니다. **[!UICONTROL Review to activate]** 캠페인 요약을 표시합니다.

   요약에서는 필요한 경우 캠페인을 수정하고 매개 변수가 잘못되었거나 누락되었는지 확인할 수 있습니다.

   >[!IMPORTANT]
   >
   >오류의 경우 캠페인을 활성화할 수 없습니다. 계속하기 전에 오류를 해결하십시오.

   ![](assets/create-campaign-alerts.png)

1. 캠페인이 올바르게 구성되었는지 확인하고 를 클릭합니다. **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. 이제 캠페인이 활성화됩니다. 상태는 입니다. **[!UICONTROL Live]**, 또는 **[!UICONTROL Scheduled]** 시작 일자를 입력한 경우 [캠페인 상태에 대해 자세히 알아보기](get-started-with-campaigns.md#statuses).

   캠페인에 구성된 메시지가 즉시 또는 지정된 날짜에 전송됩니다.

   >[!NOTE]
   >
   >다음 **[!UICONTROL Completed]** 상태는 활성화한 후 3일 후 캠페인에 자동으로 할당되거나, 반복 실행이 있는 경우 캠페인의 종료 날짜에 할당됩니다.
   >
   >종료 날짜가 지정되지 않은 경우 캠페인은 **[!UICONTROL Live]** 상태. 변경하려면 캠페인을 수동으로 중지해야 합니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md)

1. 캠페인이 활성화되면 언제든지 해당 정보를 열어 확인할 수 있습니다. 요약에서는 타겟팅된 프로필 및 배달되고 실패한 작업 수에 대한 통계를 가져올 수 있습니다.

   전용 보고서에서 **[!UICONTROL Reports]** 버튼을 클릭합니다. [자세히 보기](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

## 캠페인 예약 {#schedule}

기본적으로 캠페인은 수동으로 활성화되면 시작되고 메시지가 한 번 전송되면 종료됩니다.

캠페인의 메시지를 보낼 빈도를 정의할 수 있습니다. 이렇게 하려면 **[!UICONTROL Action triggers]** 캠페인 만들기 화면의 옵션 을 사용하여 캠페인을 매일, 주별 또는 월별 중 어떤 것으로 실행해야 하는지를 지정합니다.

활성화 직후 캠페인을 실행하지 않으려면 를 사용하여 메시지를 보낼 날짜와 시간을 지정할 수 있습니다 **[!UICONTROL Campaign start]** 선택 사항입니다. 다음  **[!UICONTROL Campaign end]** 옵션을 사용하면 반복 캠페인의 실행을 중지할 시기를 지정할 수 있습니다.

![](assets/create-campaign-schedule.png)
