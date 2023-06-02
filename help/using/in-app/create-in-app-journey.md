---
title: 여정에서 인앱 알림 만들기
description: Journey Optimizer에서 인앱 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informative"
source-git-commit: 9994bc6076f55128f5aa2c316433986eeff714b3
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 4%

---

# 여정의 인앱 메시지 만들기 {#create-in-app-journey}

1. 여정을 연 다음 **[!UICONTROL 인앱]** 의 활동 **[!UICONTROL 작업]** 팔레트의 섹션입니다.

   프로필이 여정 끝에 도달하면 표시되는 모든 인앱 메시지가 자동으로 만료됩니다. 이러한 이유로, 적절한 타이밍을 보장하기 위해 인앱 활동 후에 대기 활동이 자동으로 추가됩니다.

   ![](assets/in_app_journey_1.png)

1. 입력 **[!UICONTROL 레이블]** 및 **[!UICONTROL 설명]** 메시지를 표시합니다.

1. 다음을 선택합니다. [인앱 표면](inapp-configuration.md) 사용할 수 있습니다.

   ![](assets/in_app_journey_2.png)

1. 이제 를 사용하여 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [자세히 알아보기](design-in-app.md)

1. 클릭 **[!UICONTROL 트리거 편집]** 트리거를 구성합니다.

   ![](assets/in_app_journey_4.png)

1. 다음에서 **[!UICONTROL 인앱 메시지 트리거]** 창에서 메시지를 트리거할 이벤트 및 기준을 선택합니다.

   1. 클릭 **[!UICONTROL 조건 추가]** 트리거에서 여러 이벤트 또는 기준을 고려하도록 하려는 경우.
   1. 다음에서 **[!UICONTROL 이벤트 선택]** 드롭다운에서 트리거에 대한 이벤트 유형을 선택합니다.
   1. 이벤트가 연결되는 방식을 선택합니다(예: 선택). **[!UICONTROL 및]** 원한다면 **모두** 메시지를 표시하거나 선택하려면 트리거가 true여야 합니다. **[!UICONTROL 또는]** 메시지를 표시하려면 다음을 수행합니다. **다음 중 하나** 이 트리거를 true로 설정합니다.
   1. 클릭 **[!UICONTROL 그룹 만들기]** 트리거를 함께 그룹화합니다.

   ![](assets/in_app_journey_3.png)

1. 인앱 메시지가 활성 상태일 때 트리거 빈도를 선택합니다.

   * **[!UICONTROL 모든 시간 표시]**: 다음에서 이벤트가 선택될 때 항상 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 한 번 표시]**: 다음에서 이벤트를 처음 선택할 때만 이 메시지 표시 **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 클릭스루까지 표시]**: 다음에서 이벤트를 선택하면 이 메시지 표시: **[!UICONTROL 모바일 앱 트리거]** 드롭다운은 SDK에서 &quot;클릭됨&quot; 동작을 사용하여 상호 작용 이벤트를 전송할 때까지 발생합니다.
   * **[!UICONTROL X 회]**: 메시지에 설정된 값에 따라 결정되는 특정 횟수만 표시합니다. **[!UICONTROL 표시할 시간]** 필드.

1. 인앱 메시지를 트리거할 요일 및 특정 시간을 선택하고 을(를) 클릭합니다 **[!UICONTROL 저장]**.

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. 인앱 메시지가 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다.

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md).

## 인앱 활동 제한 사항 {#in-app-activity-limitations}

* 이 기능은 현재 의료 서비스 고객에게 제공되지 않습니다.

* 개인화에는 프로필 속성만 포함될 수 있습니다.

* 인앱 여정은 여정 수명에 연결되어 있습니다. 즉, 프로필에 대한 여정이 종료되면 해당 프로필 내의 모든 인앱 메시지가 해당 프로필에 대해 표시되지 않습니다.  따라서 여정 활동에서 바로 인앱 메시지를 중지할 수 없습니다. 대신, 인앱 메시지가 프로필에 표시되지 않도록 하려면 전체 여정을 종료해야 합니다.

* 테스트 모드에서는 여정의 수명에 따라 인앱 디스플레이가 달라집니다. 테스트 중에 여정이 너무 일찍 종료되지 않도록 하려면 **[!UICONTROL 대기 시간]** 값: **[!UICONTROL 대기]** 활동.

* **[!UICONTROL 반응]** 인앱 열기 또는 클릭에 반응하는 데 활동을 사용할 수 없습니다.

* 활성화 지연은 사용자 프로필이 캔버스의 인앱 활동에 도달하는 순간과 해당 인앱 메시지가 표시되는 시간 사이에 발생할 수 있습니다.

**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)
