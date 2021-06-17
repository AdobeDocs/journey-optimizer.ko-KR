---
title: 여정 실행 시작
description: 여정을 시작하고 메시지를 보내는 방법을 알아봅니다
source-git-commit: 9e152f50c2360010d83ffccbe536380879ffb5da
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%

---


# 여정 실행 {#message-execution}

## 여정 테스트

테스트 프로필을 사용하여 여정을 테스트할 수 있습니다. 이 단계는 설정 및 메시지의 유효성을 검사하는 것이 좋습니다.

자세한 내용은 이 [섹션](testing-the-journey.md)을 참조하십시오.

## 여정 활성화

여정을 활성화하려면 게시해야 합니다.

![](../assets/jo-journeyuc2_32bis.png)

자세한 내용은 이 [섹션](publishing-the-journey.md)을 참조하십시오.


게시되면 전용 보고 도구를 사용하여 여정을 모니터링하여 여정의 효과를 측정할 수 있습니다.

![](../assets/jo-dynamic_report_journey_12.png)

[보고서에 대해 자세히 알아보기](../reports/live-report.md)

## 메시지 보내기 {#send-messages}

메시지에 정의된 컨텐츠가 있고 게시되면 [여정](journey.md)을 통해 전송할 준비가 되었습니다.

>[!NOTE]
>
>초안 모드에 있는 메시지를 여정에 추가할 수 있지만, 여정을 게시하기 전에 메시지가 게시되었는지 확인할 수 있습니다.

메시지가 전송되면 여러 표시기를 통해 실행을 모니터링할 수 있습니다. [메시지 실행 모니터링에 대해 자세히 알아보십시오](../message-monitoring.md).

## 메시지 예약 {#schedule-messages}

메시지는 [여정](journey.md)에서 **[!UICONTROL Read Segment]** 활동을 통해 예약할 수 있습니다. 세그먼트가 여정을 입력할 시기를 지정할 수 있습니다. [세그먼트 읽기 활동에 대해 자세히 알아보십시오](read-segment.md).

이렇게 하려면 아래 단계를 수행합니다:

1. 여정을 편집하고 **[!UICONTROL Read Segment]** 활동을 끌어다 놓고 구성을 시작합니다. [세그먼트 읽기 활동 구성에 대해 자세히 알아보십시오](read-segment.md#configuring-segment-trigger-activity).

1. 여정 속성에 액세스하려면 **[!UICONTROL Edit journey schedule]** 링크를 클릭하십시오.

   ![](../assets/message-read-segment-schedule.png)

1. **[!UICONTROL Scheduler type]** 필드를 구성합니다.목록에서 원하는 값을 선택하여 세그먼트가 특정 날짜/시간 또는 반복으로 여정을 입력하도록 합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]** 섹션은 **[!UICONTROL Read Segment]** 활동이 캔버스에 드롭된 경우에만 사용할 수 있습니다.

   ![](../assets/message-read-segment-scheduler.png)

1. **[!UICONTROL Once]** 을 선택하는 경우 세그먼트가 여정을 입력할 특정 날짜와 시간을 정의합니다.

   ![](../assets/message-read-segment-scheduler-once.png)

1. 반복 방법을 선택하는 경우 시작 날짜 및 시간을 편집합니다. 종료 날짜 및 시간 옵션을 정의할 수도 있습니다.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >기본적으로 세그먼트는 여정 **[!UICONTROL As soon as possible]** 을 입력합니다. 이는 여정이 게시되고 1시간이 지난 후에 의미합니다.

1. **[!UICONTROL OK]** 을 클릭하여 변경 내용을 저장합니다.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
