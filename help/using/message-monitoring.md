---
title: 메시지 실행 모니터링
description: 모니터링 지침 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 메시지 모니터링 {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

메시지가 성공적으로 실행, 전송 및 전달되었는지 확인하기 위해 [!DNL Journey Optimizer]은 현재 게시되고 트리거된 메시지를 모니터링할 수 있는 기능을 제공합니다. **[!UICONTROL Executions]** 목록에서 실시간으로 여정 <!--and APIs--> 간에 메시지가 어떻게 작동하는지 확인할 수 있습니다.

이 목록에 액세스하려면 **[!DNL Journey Optimizer]** 홈 페이지에서 **[!UICONTROL Messages]**&#x200B;을 선택하고 **[!UICONTROL Executions]** 탭을 클릭합니다.

이 탭에서는 두 가지 보기를 제공합니다.**[!UICONTROL Live view]** 및 **[!UICONTROL Global view]**.

* **[!UICONTROL Live view]** 탭은 지난 24시간 동안 하나 이상의 [여정](building-journeys/journey.md) **에 의해 트리거된 모든 실행 메시지**&#x200B;에 대한 **실시간 개요를 제공합니다.**.

   ![](assets/message-execution-tab-live.png)

   이 목록은 60초마다 자동으로 새로 고침됩니다. 특정 메시지에 대해 지난 24시간 동안 아무 실행도 발생하지 않으면 모든 열에 해당 메시지에 대한 null 값(0)이 표시됩니다.

* **[!UICONTROL Global view]** 탭은 메시지 시작 날짜&#x200B;**이후 하나 이상의 [여정](building-journeys/journey.md)**&#x200B;에 의해 트리거된 모든 실행 메시지&#x200B;**의**&#x200B;개요를 제공합니다.

   ![](assets/message-execution-tab-global.png)

   이 목록은 90분마다 자동으로 새로 고쳐집니다. 데이터는 각 메시지 시작 날짜 이후 시간에 따라 집계됩니다.

메시지가 게시되었지만 여정에 의해 아직 트리거되지 않은 경우 어느 탭에도 나열되지 않습니다. 다음 요소만 나열됩니다.
* 트리거되었지만 아직 시작하지 않은 메시지(보류 중).
* 트리거되었고 현재 실행 중인 메시지(진행 중).

다중 채널 메시지의 경우 각 메시지에 대해 채널당 하나의 행이 표시됩니다.

![](assets/message-execution-multichannel.png)

메시지가 여러 여정에서 사용된 경우 **[!UICONTROL Source]** 열에는 **[!UICONTROL Multiple]**&#x200B;이 표시됩니다.

기본적으로 메시지는 가장 최근 실행 날짜부터 시작됩니다. 채널, 시작 날짜 및/또는 종료 날짜에 따라 메시지를 검색하려면 **[!UICONTROL Filters]** 아이콘을 클릭합니다.

![](assets/message-execution-tab-filters.png)

두 번째 열을 사용하여 해당 [메시지](create-message.md)를 열고 **[!UICONTROL Live view]**&#x200B;에 있는 경우 [라이브 보고서](reports/live-report.md)에 액세스하거나 **[!UICONTROL Global view]**&#x200B;에 있는 경우 [글로벌 보고서](reports/global-report.md)에 액세스할 수 있습니다.

![](assets/message-execution-open-live-report.png)

각 메시지 실행에 대해 여러 표시기가 표시됩니다.

* **[!UICONTROL Message label]**:메시지를 만들 때 정의한 메시지  [제목입니다](create-message.md).
* **[!UICONTROL Execution ID]**:자동으로 생성된 식별자.
* **[!UICONTROL Source]**:해당 메시지를 활용하는 여정 이름입니다.
* **[!UICONTROL Start date]**:여정에서 메시지를 실행한 날짜 및 시간입니다.
* **[!UICONTROL Excluded]**:제외 규칙으로 인해 초기 대상에서 제외된 프로필 수입니다.
* **[!UICONTROL Sent]**:전송된 메시지 수입니다.
* **[!UICONTROL Delivered]**:바운스 또는 다른 배달 오류를 생성하지 않고 받는 사람의 사서함(이메일) 또는 장치(푸시)에서 전달된 메시지 수입니다.
* **[!UICONTROL Bounces]**:배달 오류로 인해 배달할 수 없는 메시지 수입니다. [바운스에 대한 자세한 내용을 살펴보십시오](suppression-lists.md#delivery-failures).
* **[!UICONTROL Opens]**:열린 메시지 수입니다.
* **[!UICONTROL Clicks]**:이메일에 있는 링크에 대한 클릭 수.

   >[!NOTE]
   >
   >푸시 알림에 대한 클릭 수가 없습니다.사용자가 푸시 알림을 클릭하면 앱이 열리고, 이 앱은 열린 상태로만 간주될 수 있습니다.

* **[!UICONTROL Errors]**:기술적 오류로 인해 보낼 수 없는 메시지 수입니다.

각 하이퍼링크를 클릭하면 해당 메시지 요약 보기가 열립니다. [메시지에 대한 자세한 내용을 살펴보십시오](create-message.md).
