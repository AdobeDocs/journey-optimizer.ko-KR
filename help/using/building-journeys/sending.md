---
title: 여정 실행 시작
description: 여정을 시작하고 메시지를 보내는 방법 학습
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 2%

---


# 여정 실행 {#message-execution}

![](../assets/do-not-localize/badge.png)

## 여정 테스트

테스트 프로필을 사용하여 여정을 테스트할 수 있습니다. 이 단계는 설정 및 메시지의 유효성을 확인하는 데 권장됩니다.

이 [섹션](testing-the-journey.md)에서 자세히 알아보십시오.

## 여정 활성화

여정을 게시하여 활성화해야 합니다.

![](../assets/jo-journeyuc2_32bis.png)

이 [섹션](publishing-the-journey.md)에서 자세히 알아보십시오.


게시한 후에는 전용 보고 도구를 사용하여 여정을 모니터링하여 여정의 효과를 측정할 수 있습니다.

![](../assets/jo-dynamic_report_journey_12.png)

[보고서에 대한 자세한 내용](../reports/live-report.md)

## 메시지 보내기 {#send-messages}

메시지에 정의된 내용이 있고 게시되면 [여정](journey.md)을 통해 메시지를 보낼 준비가 되었습니다.

>[!NOTE]
>
>초안 모드에 있는 메시지를 여정에 추가할 수 있지만 여정을 게시하기 전에 메시지가 게시되었는지 확인합니다.

메시지가 전송되면 여러 표시기를 통해 메시지 실행을 모니터링할 수 있습니다. [메시지 실행 모니터링에 대해 자세히 알아보십시오](../message-monitoring.md).

## 메시지 예약 {#schedule-messages}

메시지는 [여정](journey.md)에서 **[!UICONTROL Read segment]** 활동을 통해 예약할 수 있습니다. 세그먼트가 여정에 들어올 시기를 지정할 수 있습니다. [세그먼트 읽기 활동에 대해 자세히 알아보십시오](read-segment.md).

이렇게 하려면 아래 단계를 수행합니다:

1. 여정을 편집하고 **[!UICONTROL Read segment]** 활동을 드래그 앤 드롭한 다음 구성을 시작합니다. [세그먼트 읽기 활동 구성에 대해 자세히 알아보십시오](read-segment.md#configuring-segment-trigger-activity).

1. 여정 속성에 액세스하려면 **[!UICONTROL Edit journey schedule]** 링크를 클릭합니다.

   ![](../assets/message-read-segment-schedule.png)

1. **[!UICONTROL Scheduler type]** 필드를 구성합니다.목록에서 원하는 값을 선택하여 세그먼트가 특정 날짜/시간 또는 반복 기준으로 여정을 입력하도록 합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]** 섹션은 **[!UICONTROL Read Segment]** 활동이 캔버스로 드롭된 경우에만 사용할 수 있습니다.

   ![](../assets/message-read-segment-scheduler.png)

1. **[!UICONTROL Once]**&#x200B;을 선택하는 경우 세그먼트가 여정에 들어갈 특정 날짜와 시간을 정의합니다.

   ![](../assets/message-read-segment-scheduler-once.png)

1. 반복 방법을 선택하는 경우 시작 날짜와 시간을 편집합니다. 종료 날짜 및 시간을 선택적으로 정의할 수도 있습니다.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >기본적으로 세그먼트는 여정이 게시된 후 1시간을 의미하는 여정 **[!UICONTROL As soon as possible]**&#x200B;을 입력합니다.

1. **[!UICONTROL OK]**&#x200B;을 클릭하여 변경 내용을 저장합니다.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
