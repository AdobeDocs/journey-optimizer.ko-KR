---
title: 여정에서 인앱 알림 만들기
description: 여정에 인앱 메시지를 추가하는 방법 알아보기
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: d27fa0192b72de79fefb52b472bd06c6511a8b70
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 2%

---


# 여정에 인앱 메시지 만들기 {#create-in-app-journey}

여정에 인앱 메시지를 추가하려면 다음 단계를 수행합니다.

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

   * **[!UICONTROL 항상]**: 다음에서 이벤트가 선택될 때 항상 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 한 번]**: 다음에서 이벤트를 처음 선택할 때만 이 메시지 표시 **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 클릭스루할 때까지]**: 다음에서 이벤트를 선택하면 이 메시지 표시: **[!UICONTROL 모바일 앱 트리거]** 드롭다운은 SDK에서 &quot;클릭됨&quot; 동작을 사용하여 상호 작용 이벤트를 전송할 때까지 발생합니다.
   * **[!UICONTROL X 회]**: 메시지에 설정된 값에 따라 결정되는 특정 횟수만 표시합니다. **[!UICONTROL 표시할 시간]** 필드.

1. 인앱 메시지를 트리거할 요일 및 특정 시간을 선택하고 을(를) 클릭합니다 **[!UICONTROL 저장]**.

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. 인앱 메시지가 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다.

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md).

## 인앱 보고서  {#inapp-report}

여정에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 인앱]** 탭에서는 여정에 전송된 인앱 게재와 관련된 기본 정보를 자세히 설명합니다.

자세히 알아보기 [여정 글로벌 보고서](../reports/journey-global-report.md).

![](assets/in-app-journey-report.png)

+++인앱 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 인앱 성능]** KPI는 다음과 같이 방문자의 인앱 메시지 참여와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 고유 노출 횟수]**: 인앱 메시지가 전달된 고유 사용자 수.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 인앱 메시지 수입니다.

* **[!UICONTROL 클릭률]**: 인앱 메시지에 포함된 버튼과 상호 작용한 사용자와 메시지를 본 사용자의 비율.

* **[!UICONTROL 취소율]**: 수신자가 무시한 인앱 메시지 비율입니다.

다음 **[!UICONTROL 인앱 요약]** 그래프는 관련 기간 동안 인앱 노출 횟수의 발전을 보여 줍니다.

다음 **[!UICONTROL 버튼을 통한 클릭 수]** 그래프 및 표에는 버튼당 수신자 동작에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL 클릭수]**: 인앱 메시지에 포함된 버튼과 상호 작용한 총 수신자 수입니다.

* **[!UICONTROL 클릭률]**: 인앱 메시지에 포함된 버튼과 상호 작용한 사용자와 메시지를 본 사용자의 비율.
+++

**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)
