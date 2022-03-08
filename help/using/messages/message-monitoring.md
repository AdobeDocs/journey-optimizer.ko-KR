---
title: 메시지 실행 모니터링
description: 모니터링 지침 학습
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 950f8186-07f6-4cc1-936c-d0984fb0f988
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# 메시지 모니터링 {#monitor-message-execution}

메시지가 성공적으로 실행, 전송 및 전달되는지 확인하려면, [!DNL Journey Optimizer] 은 현재 게시되고 트리거된 메시지를 모니터링하는 기능을 제공합니다. 여정 간에 메시지가 어떻게 작동하는지 확인할 수 있습니다 <!--and APIs--> 실시간으로 **[!UICONTROL Executions]** 목록.

이 목록에 액세스하려면 **[!DNL Journey Optimizer]** 홈 페이지, 선택 **[!UICONTROL Messages]**&#x200B;를 클릭하고 를 클릭한 다음 **[!UICONTROL Executions]** 탭.

이 탭에서는 두 가지 보기를 사용할 수 있습니다. **[!UICONTROL Live view]** 및 **[!UICONTROL Global view]**.

* 다음 **[!UICONTROL Live view]** 탭에서 다음을 제공합니다. **실행된 모든 메시지의 실시간 개요** 하나 이상의 [여정](../building-journeys/journey.md) **지난 24시간 동안에만**.

   ![](assets/message-execution-tab-live.png)

   이 목록은 60초마다 자동으로 새로 고쳐집니다. 지난 24시간 동안 특정 메시지에 대한 실행이 발생하지 않으면, 모든 열에 해당 메시지에 대한 null 값(0)이 표시됩니다.

* 다음 **[!UICONTROL Global view]** 탭에는 **실행된 모든 메시지 개요** 하나 이상의 [여정](../building-journeys/journey.md) **메시지 시작 날짜 이후**.

   ![](assets/message-execution-tab-global.png)

   이 목록은 90분마다 자동으로 새로 고침됩니다. 데이터는 각 메시지 시작 날짜 이후 시간에 따라 집계됩니다.

메시지가 게시되었지만 여정에 의해 아직 트리거되지 않은 경우, 탭 중 하나에 나열되지 않습니다. 다음 요소만 나열됩니다.
* 트리거되었지만 아직 시작되지 않은 메시지(보류 중)
* 트리거되었으며 현재 실행 중인 메시지(진행 중)

>[!NOTE]
>
>여러 여정에서 메시지가 사용된 경우, 각 실행에 대해 여정 당 하나의 행이 표시됩니다.

기본적으로 메시지는 가장 최근 실행 날짜부터 표시됩니다. 을(를) 클릭합니다. **[!UICONTROL Filters]** 아이콘을 사용하여 채널, 시작 날짜 및/또는 종료 날짜에 따라 메시지를 검색할 수 있습니다. 또한 테스트 이벤트를 **실행 목록**.

![](assets/message-execution-tab-filters.png)

다음 <!--**[!UICONTROL Quick action]**-->두 번째 열에서 해당 [메시지](create-message.md) 및 [라이브 보고서](../reports/live-report.md) 만약 **[!UICONTROL Live view]**&#x200B;또는 [글로벌 보고서](../reports/global-report.md) 만약 **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

각 메시지 실행에 대해 많은 표시기가 표시됩니다.

* **[!UICONTROL Message label]**: 정의한 메시지 제목 [메시지 만들기](create-message.md). 자동으로 생성된 실행 ID는 괄호로 표시됩니다.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: 메시지, 여정 버전 및 여정의 메시지를 활용하는 작업의 레이블을 활용하는 여정의 이름입니다.

* **[!UICONTROL Status]**: 메시지 실행 상태.

* **[!UICONTROL Start date]**: 여정에서 메시지가 실행된 날짜 및 시간입니다.

* **[!UICONTROL Targeted]**: 각 메시지 실행에 대한 타겟팅된 프로필 수입니다.

* **[!UICONTROL Excluded]**: 제외 규칙으로 인해 초기 대상에서 제외된 프로필 수입니다.

* **[!UICONTROL Sent]**: 전송된 메시지 수입니다.

* **[!UICONTROL Delivered]**: 바운스 또는 다른 배달 오류를 생성하지 않고 수신자의 사서함(전자 메일) 또는 장치(푸시)에서 성공적으로 전달된 메시지 수입니다.

* **[!UICONTROL Bounces]**: 게재 오류로 인해 배달할 수 없는 메시지 수입니다. [바운스에 대해 자세히 알아보기](suppression-list.md).

* **[!UICONTROL Opens]**: 열린 메시지 수입니다.

* **[!UICONTROL Clicks]**: 이메일에 있는 링크에 대한 클릭 수입니다.

   >[!NOTE]
   >
   >푸시 알림에 대한 클릭 수가 없습니다. 사용자가 푸시 알림을 클릭하면 앱이 열립니다. 이 앱은 열려 있는 것으로 간주할 수 있습니다.

* **[!UICONTROL Errors]**: 기술 오류로 인해 보낼 수 없는 메시지 수입니다.

* **[!UICONTROL Spam complaints]**: 수신자가 스팸으로 표시한 메시지 수입니다. 의 불만 사항에 대해 자세히 알아보십시오 [게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

테이블에 표시할 열을 선택할 수 있습니다. 이렇게 하려면 **[!UICONTROL Customize table]** 아이콘을 클릭하고 표시할 열을 선택합니다.

![](assets/message-execution-customize-table.png)

in **전역 보기** 데이터만 숫자, 백분율 또는 둘 다로 표시할 것인지 선택할 수 있습니다. 을(를) 클릭합니다. **데이터 형식** 드롭다운 목록에서 세 옵션 간을 전환합니다.

![](assets/message-execution-data-format.png)

각 하이퍼링크를 클릭하면 해당 메시지 요약 보기가 열립니다. [메시지에 대해 자세히 알아보기](create-message.md).
