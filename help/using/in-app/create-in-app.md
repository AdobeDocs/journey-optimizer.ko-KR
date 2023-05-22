---
title: 인앱 알림 만들기
description: Journey Optimizer에서 인앱 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 9bebcde9edde40a0fadba34d8b40757036a6436d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 6%

---

# 인앱 메시지 만들기  {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. 액세스 **[!UICONTROL 캠페인]** 메뉴를 선택한 다음 **[!UICONTROL 캠페인 만들기]**.

1. 다음에서 **[!UICONTROL 속성]** 섹션에서 캠페인 실행 유형(예약됨 또는 API 트리거됨)이 실행되는 시점을 선택합니다. 에서 캠페인 유형에 대해 자세히 알아보기 [이 페이지](../campaigns/create-campaign.md#campaigntype).

1. 다음에서 **[!UICONTROL 작업]** 섹션에서 다음을 선택합니다. **[!UICONTROL 인앱 메시지]** 및 **[!UICONTROL 앱 표면]** 인앱 메시지에 대해 이전에 구성되었습니다. 그런 다음 을 클릭합니다. **[!UICONTROL 만들기]**.

   에서 인앱 구성에 대해 자세히 알아보기 [이 페이지](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 다음에서 **[!UICONTROL 속성]** 섹션에서 다음을 입력합니다. **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]** 설명.

1. 인앱 메시지에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다. **[!UICONTROL 액세스 관리]**. [자세히 알아보기](../administration/object-based-access.md).

1. 다음을 클릭합니다. **[!UICONTROL 대상자 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 버튼입니다. [자세히 알아보기](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. 다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. 클릭 **[!UICONTROL 트리거 편집]** 메시지를 트리거할 이벤트 및 기준을 선택하려면 다음을 수행하십시오.

   1. 클릭 **조건 추가** 트리거에서 여러 이벤트 또는 기준을 고려하도록 하려는 경우.
   1. 이벤트가 연결되는 방식을 선택합니다(예: 선택). **[!UICONTROL 및]** 원한다면 **모두** 메시지를 표시하거나 선택하려면 트리거가 true여야 합니다. **[!UICONTROL 또는]** 메시지를 표시하려면 다음을 수행합니다. **다음 중 하나** 이 트리거를 true로 설정합니다.
   1. 클릭 **[!UICONTROL 그룹 만들기]** 트리거를 함께 그룹화합니다.

   ![](assets/in_app_create_3.png)

1. 인앱 메시지가 활성 상태일 때 트리거 빈도를 선택합니다. 다음 옵션을 사용할 수 있습니다.

   * **[!UICONTROL 항상]**: 다음에서 이벤트가 선택될 때 항상 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 한 번]**: 다음에서 이벤트를 처음 선택할 때만 이 메시지 표시 **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 클릭스루할 때까지]**: 다음에서 이벤트를 선택하면 이 메시지 표시: **[!UICONTROL 모바일 앱 트리거]** 드롭다운은 SDK에서 &quot;클릭됨&quot; 동작을 사용하여 상호 작용 이벤트를 전송할 때까지 발생합니다.
   * **[!UICONTROL X 회]**: 이 메시지를 X회 표시합니다.

1. 필요한 경우 다음 중 하나를 선택합니다 **[!UICONTROL 요일]** 또는 **[!UICONTROL 하루 중 시간]** 인앱 메시지가 표시됩니다.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 의 내 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 이제 를 사용하여 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [자세히 알아보기](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## 방법 비디오{#video}

아래 비디오에서는 캠페인에서 인앱 메시지를 만들고, 구성하고, 게시하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)