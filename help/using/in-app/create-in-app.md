---
title: 인앱 알림 만들기
description: Journey Optimizer에서 인앱 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%

---

# 인앱 메시지 만들기  {#create-in-app}

인앱 메시지는 캠페인 컨텍스트에서 만들어집니다.

>[!BEGINTABS]

>[!TAB 여정에 인앱 메시지 추가]

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

>[!TAB 캠페인에 인앱 메시지 추가]

1. 액세스 권한 **[!UICONTROL 캠페인]** 메뉴를 클릭한 다음 **[!UICONTROL 캠페인 만들기]**.

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인 실행 유형을 선택할 수 있습니다. 예약됨 또는 API 트리거됨. 에서 캠페인 유형에 대해 자세히 알아보기 [이 페이지](../campaigns/create-campaign.md#campaigntype).

1. 에서 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 인앱 메시지]** 그리고 **[!UICONTROL 앱 표면]** 이전에 인앱 메시지에 대해 구성했습니다. 그런 다음 **[!UICONTROL 만들기]**.

   의 인앱 구성에 대해 자세히 알아보십시오 [이 페이지](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 에서 **[!UICONTROL 속성]** 섹션에서 다음을 입력합니다. **[!UICONTROL 제목]** 그리고 **[!UICONTROL 설명]** 설명.

1. 사용자 지정 또는 코어 데이터 사용 레이블을 인앱 메시지에 할당하려면 을(를) 선택합니다 **[!UICONTROL 액세스 관리]**. [자세히 알아보기](../administration/object-based-access.md).

1. 을(를) 클릭합니다. **[!UICONTROL 대상 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 단추입니다. [자세히 알아보기](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. 에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. 클릭 **[!UICONTROL 트리거 편집]** 메시지를 트리거할 이벤트 및 기준을 선택하려면 다음을 수행하십시오.

   1. 클릭 **조건 추가** 트리거에서 여러 이벤트 또는 기준을 고려하도록 하려는 경우.
   1. 이벤트의 연결 방식을 선택합니다(예: 선택). **[!UICONTROL 및]** 원한다면 **둘 다** 메시지를 표시하거나 선택하기 위해 true로 트리거합니다. **[!UICONTROL 또는]** 메시지를 표시하려면 **둘 중 하나** 트리거의 값이 true입니다.
   1. 클릭 **[!UICONTROL 그룹 만들기]** 트리거를 함께 그룹화하는 중입니다.

   ![](assets/in_app_create_3.png)

1. 인앱 메시지가 활성 상태일 때 트리거의 빈도를 선택합니다. 다음 옵션을 사용할 수 있습니다.

   * **[!UICONTROL 항상]**: 이벤트에서 선택된 경우 항상 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 한 번]**: 이벤트에서 처음 선택된 경우에만 이 메시지를 표시합니다. **[!UICONTROL 모바일 앱 트리거]** 드롭다운이 발생합니다.
   * **[!UICONTROL 클릭스루할 때까지]**: 이벤트에서 선택된 경우 이 메시지 표시 **[!UICONTROL 모바일 앱 트리거]** 드롭다운은 SDK에서 &quot;클릭됨&quot; 작업과 함께 상호 작용 이벤트를 전송할 때까지 발생합니다.
   * **[!UICONTROL X 횟수]**: X시간으로 이 메시지를 표시합니다.

1. 필요한 경우 원하는 항목을 선택합니다 **[!UICONTROL 요일]** 또는 **[!UICONTROL 시간]** 인앱 메시지가 표시됩니다.

1. 캠페인은 특정 날짜 또는 반복 빈도에 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 이제 을(를) 사용하여 콘텐츠 디자인을 시작할 수 있습니다 **[!UICONTROL 컨텐츠 편집]** 버튼을 클릭합니다. [자세히 알아보기](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 방법 비디오{#video}

아래 비디오에서는 캠페인에서 인앱 메시지를 만들고, 구성하고, 게시하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)