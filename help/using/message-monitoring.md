---
title: 메시지 실행 모니터링
description: 모니터링 지침 학습
source-git-commit: 3f02a5debbc870915175d2802eb30ff567a3c159
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# 메시지 모니터링 {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

메시지가 성공적으로 실행, 전송 및 전달되는지 확인하기 위해 [!DNL Journey Optimizer]은(는) 현재 게시되고 트리거되는 메시지를 모니터링하는 기능을 제공합니다. **[!UICONTROL Executions]** 목록에서 여정 <!--and APIs--> 간에 메시지가 실시간으로 어떻게 수행되는지 확인할 수 있습니다.

이 목록에 액세스하려면 **[!DNL Journey Optimizer]** 홈 페이지에서 **[!UICONTROL Messages]** 을 선택하고 **[!UICONTROL Executions]** 탭을 클릭하십시오.

이 탭에서는 두 가지 보기를 사용할 수 있습니다.**[!UICONTROL Live view]** 및 **[!UICONTROL Global view]**

* **[!UICONTROL Live view]** 탭에서는 지난 24시간 동안 하나 이상의 [여정](building-journeys/journey.md) **에 의해 트리거된 모든 실행된 메시지의**&#x200B;실시간 개요를 제공합니다&#x200B;**.**

   ![](assets/message-execution-tab-live.png)

   이 목록은 60초마다 자동으로 새로 고쳐집니다. 지난 24시간 동안 특정 메시지에 대한 실행이 발생하지 않으면, 모든 열에 해당 메시지에 대한 null 값(0)이 표시됩니다.

* **[!UICONTROL Global view]** 탭에서는 메시지 시작 날짜&#x200B;**이후 하나 이상의 [여정](building-journeys/journey.md)**&#x200B;에 의해 트리거되는 모든 실행된 메시지의 **개요를 제공합니다.**

   ![](assets/message-execution-tab-global.png)

   이 목록은 90분마다 자동으로 새로 고침됩니다. 데이터는 각 메시지 시작 날짜 이후 시간에 따라 집계됩니다.

메시지가 게시되었지만 여정에 의해 아직 트리거되지 않은 경우, 탭 중 하나에 나열되지 않습니다. 다음 요소만 나열됩니다.
* 트리거되었지만 아직 시작되지 않은 메시지(보류 중)
* 트리거되었으며 현재 실행 중인 메시지(진행 중)

<!--For multichannel messages, one row per channel is displayed for each message. STILL VALID? looks like NOT-->

>[!NOTE]
>
>여러 여정에서 메시지가 사용된 경우, 각 실행에 대해 여정 당 하나의 행이 표시됩니다.

<!--![](assets/message-execution-multichannel.png)-->

<!--If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.-->

기본적으로 메시지는 가장 최근 실행 날짜부터 표시됩니다. 채널, 시작 날짜 및/또는 종료 날짜에 따라 메시지를 검색하려면 **[!UICONTROL Filters]** 아이콘을 클릭하십시오.

![](assets/message-execution-tab-filters.png)

<!--**[!UICONTROL Quick action]**-->두 번째 열은 [메시지](create-message.md)를 열고 **[!UICONTROL Live view]**&#x200B;에 있는 경우 [라이브 보고서](reports/live-report.md)에 액세스하거나 **[!UICONTROL Global view]**&#x200B;에 있는 경우 [전역 보고서](reports/global-report.md)에 액세스할 수 있도록 합니다.

![](assets/message-execution-open-live-report.png)

각 메시지 실행에 대해 많은 표시기가 표시됩니다.

* **[!UICONTROL Message label]**:메시지를 만들 때 정의한 메시지  [제목입니다](create-message.md). 자동으로 생성된 실행 ID는 괄호로 표시됩니다.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**:메시지, 여정 버전 및 여정의 메시지를 활용하는 작업의 레이블을 활용하는 여정의 이름입니다.

* **[!UICONTROL Status]**:메시지 실행 상태.  <!--List all the possible statuses? For now only Live status? The user cannot stop or cancel the execution. TBC by Fred-->

* **[!UICONTROL Start date]**:여정에서 메시지가 실행된 날짜 및 시간입니다.

   <!--Targeted: Number of targeted profiles for each message execution. To come?-->

* **[!UICONTROL Excluded]**:제외 규칙으로 인해 초기 대상에서 제외된 프로필 수입니다.

* **[!UICONTROL Sent]**:전송된 메시지 수입니다.

* **[!UICONTROL Delivered]**:바운스 또는 다른 배달 오류를 생성하지 않고 수신자의 사서함(전자 메일) 또는 장치(푸시)에서 성공적으로 전달된 메시지 수입니다.

* **[!UICONTROL Bounces]**:게재 오류로 인해 배달할 수 없는 메시지 수입니다. [바운스에 대해 자세히 알아보십시오](suppression-list.md).

* **[!UICONTROL Opens]**:열린 메시지 수입니다.

* **[!UICONTROL Clicks]**:이메일에 있는 링크에 대한 클릭 수입니다.

   >[!NOTE]
   >
   >푸시 알림에 대한 클릭 수가 없습니다.사용자가 푸시 알림을 클릭하면 앱이 열립니다. 이 앱은 열려 있는 것으로 간주할 수 있습니다.

* **[!UICONTROL Errors]**:기술 오류로 인해 보낼 수 없는 메시지 수입니다.

* **[!UICONTROL Spam complaints]**:수신자가 스팸으로 표시한 메시지 수입니다. [불만 사항에 대해 자세히 알아보십시오](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability).

각 하이퍼링크를 클릭하면 해당 메시지 요약 보기가 열립니다. [메시지에 대해 자세히 알아보기](create-message.md).
