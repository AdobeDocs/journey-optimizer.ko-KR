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
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 2%

---

# 여정에서 인앱 메시지 만들기 {#create-in-app-journey}

>[!AVAILABILITY]
>
>인앱 활동은 현재 사용자만 선택할 수 있는 베타로 제공됩니다. beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주세요.

1. 여정을 열고 을(를) 끌어다 놓습니다 **[!UICONTROL 인앱]** 활동의 **[!UICONTROL 작업]** 섹션에 있는 마지막 항목이 될 필요가 없습니다.

   프로필이 여정 끝에 도달하면 프로필에 표시되는 모든 인앱 메시지가 자동으로 만료됩니다. 이러한 이유로, 인앱 활동 후에 대기 활동이 자동으로 추가되어 적절한 타이밍을 보장합니다.

   ![](assets/in_app_journey_1.png)

1. 을(를) 입력합니다. **[!UICONTROL 레이블]** 및 **[!UICONTROL 설명]** 참조하십시오.

1. 을(를) 선택합니다 [인앱 표면](inapp-configuration.md) 를 사용하십시오.

   ![](assets/in_app_journey_2.png)

1. 이제 을(를) 사용하여 콘텐츠 디자인을 시작할 수 있습니다 **[!UICONTROL 컨텐츠 편집]** 버튼을 클릭합니다. [자세히 알아보기](design-in-app.md)

1. 클릭 **[!UICONTROL 트리거 편집]** 트리거 를 구성합니다.

   ![](assets/in_app_journey_4.png)

1. 인앱 메시지가 활성 상태일 때 트리거의 빈도를 선택합니다.

   * **[!UICONTROL 항상 표시]**: 이벤트에서 선택된 경우 항상 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 한 번 표시]**: 이벤트에서 처음 선택된 경우에만 이 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 클릭스루할 때까지 표시]**: 이벤트에서 선택된 경우 이 메시지 표시 **[!UICONTROL 모바일 앱 트리거]** 드롭다운은 SDK에서 &quot;클릭됨&quot; 작업과 함께 상호 작용 이벤트를 전송할 때까지 발생합니다.

1. 에서 **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 메시지를 트리거할 이벤트 및 기준을 선택합니다.

   1. 왼쪽 드롭다운에서 메시지를 트리거하는 데 필요한 이벤트를 선택합니다.
   1. 오른쪽 드롭다운에서 선택한 이벤트에 필요한 유효성 검사를 선택합니다.
   1. 을(를) 클릭합니다. **[!UICONTROL 추가]** 트리거에서 여러 이벤트 또는 기준을 고려하려면 버튼을 클릭합니다. 그런 다음 위의 단계를 반복합니다.
   1. 이벤트의 연결 방식을 선택합니다(예: 선택). **[!UICONTROL 및]** 원한다면 **둘 다** 메시지를 표시하거나 선택하기 위해 true로 트리거합니다. **[!UICONTROL 또는]** 메시지를 표시하려면 **둘 중 하나** 트리거의 값이 true입니다.
   1. 클릭 **[!UICONTROL 저장]** 트리거 가 구성된 경우.

   ![](assets/in_app_journey_3.png)

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. 인앱 메시지가 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다.

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md).

## 인앱 활동 제한 사항 {#in-app-activity-limitations}

* 이 기능은 현재 Healthcare 고객에게 제공되지 않습니다.

* 개인화에는 프로필 속성만 포함할 수 있습니다.

* 인앱 디스플레이는 여정 수명과 연결되어 있습니다. 즉, 여정이 프로필에 대해 종료되면 해당 여정의 모든 인앱 메시지가 해당 프로필에 대해 표시되지 않습니다. 즉, 여정 활동에서 직접 인앱을 중지할 수 없습니다. 그 여정을 끝내야 합니다.
* 인앱 디스플레이는 여정의 수명은 연결되어 있습니다. 즉, 특정 사용자 프로필에 대해 여정이 완료되면 해당 여정 내의 모든 인앱 메시지가 해당 프로필에 대해 표시되지 않습니다. 따라서 여정 활동에서 직접 인앱 메시지를 중지할 수 없습니다. 대신 인앱 메시지가 프로필에 표시되지 않도록 전체 여정을 종료해야 합니다.

* 이 기능을 사용하면 아직 **[!UICONTROL 반응]** 활동은 인앱 열기 또는 클릭에 반응합니다.

* 사용자 프로필이 캔버스에서 인앱 활동에 도달하는 순간 및 해당 인앱 메시지를 보기 시작하는 시간 사이에 활성화 지연이 발생합니다. 이 지연 시간은 15분에서 1시간 까지입니다.

**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)