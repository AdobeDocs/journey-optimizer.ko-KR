---
title: 여정 실행 시작
description: 여정을 시작하고 메시지를 보내는 방법을 알아봅니다
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%

---


# 여정 실행 {#message-execution}

## 여정 테스트

테스트 프로필을 사용하여 여정을 테스트할 수 있습니다. 이 단계는 설정 및 메시지의 유효성을 검사하는 것이 좋습니다.

자세한 내용 [섹션](testing-the-journey.md).

## 여정 활성화

여정을 활성화하려면 게시해야 합니다.

![](../assets/jo-journeyuc2_32bis.png)

자세한 내용 [섹션](publishing-the-journey.md).


게시되면 전용 보고 도구를 사용하여 여정을 모니터링하여 여정의 효과를 측정할 수 있습니다.

![](../assets/jo-dynamic_report_journey_12.png)

[보고서에 대해 자세히 알아보기](../reports/live-report.md)

## 메시지 보내기 {#send-messages}

메시지에 정의된 컨텐츠가 있고 게시되면 을(를) 통해 보낼 준비가 되었습니다. [여정](journey.md).

>[!NOTE]
>
>초안 모드에 있는 메시지를 여정에 추가할 수 있지만, 여정을 게시하기 전에 메시지가 게시되었는지 확인할 수 있습니다.

메시지가 전송되면 여러 표시기를 통해 실행을 모니터링할 수 있습니다. [메시지 실행 모니터링에 대해 자세히 알아보기](../message-monitoring.md).

## 메시지 예약 {#schedule-messages}

메시지는 **[!UICONTROL Read Segment]** 의 활동 [여정](journey.md). 세그먼트가 여정을 입력할 시기를 지정할 수 있습니다. [세그먼트 읽기 활동에 대해 자세히 알아보십시오](read-segment.md).

이렇게 하려면 아래 단계를 수행합니다:

1. 여정 편집, 끌어서 놓기 **[!UICONTROL Read Segment]** 활동을 시작하고 구성을 시작합니다. [세그먼트 읽기 활동 구성에 대한 자세한 내용을 알아봅니다](read-segment.md#configuring-segment-trigger-activity).

1. 을(를) 클릭합니다. **[!UICONTROL Edit journey schedule]** 링크를 클릭하여 여정 속성에 액세스합니다.

   ![](../assets/message-read-segment-schedule.png)

1. 구성 **[!UICONTROL Scheduler type]** 필드: 목록에서 원하는 값을 선택하여 세그먼트가 특정 날짜/시간 또는 반복으로 여정을 입력하도록 합니다.

   >[!NOTE]
   >
   >다음 **[!UICONTROL Schedule]** 섹션은 **[!UICONTROL Read Segment]** 활동이 캔버스에 삭제되었습니다.

   ![](../assets/message-read-segment-scheduler.png)

1. 선택하는 경우 **[!UICONTROL Once]**&#x200B;을(를) 통해 세그먼트가 여정을 입력할 특정 날짜 및 시간을 정의합니다.

   ![](../assets/message-read-segment-scheduler-once.png)

1. 반복 방법을 선택하는 경우 시작 날짜 및 시간을 편집합니다. 종료 날짜 및 시간 옵션을 정의할 수도 있습니다.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >기본적으로 세그먼트는 여정을 입력합니다 **[!UICONTROL As soon as possible]**: 여정이 게시된 후 1시간을 의미합니다.

1. 클릭 **[!UICONTROL OK]** 변경 사항을 저장하려면 을 클릭합니다.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
