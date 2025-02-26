---
solution: Journey Optimizer
product: journey optimizer
title: 첫 여정 만들기
description: Adobe Journey Optimizer를 사용하여 첫 번째 여정을 빌드하기 위한 주요 단계
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 첫 번째, 시작, 빠른 시작, 대상, 이벤트, 작업
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 93dab17fc74396887e3b68051be777645e02709f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 25%

---

# 첫 여정 만들기 {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="여정 만들기"
>abstract="**Adobe Journey Optimizer**&#x200B;를 통해 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="여정"
>abstract="고객 여정 설계를 통해 개인화된 상황별 경험을 제공할 수 있습니다. Journey Optimizer를 사용하면 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다. **개요** 탭에는 여정과 관련된 주요 지표가 포함된 대시보드가 &#x200B;&#x200B;표시됩니다. **찾아보기** 탭에는 기존 여정의 목록이 표시됩니다."

Adobe Journey Optimizer에는 마케팅 활동과 일대일 고객 참여를 조화롭게 조정할 수 있는 옴니채널 오케스트레이션 캔버스가 포함되어 있습니다. 사용자 인터페이스를 사용하면 팔레트에서 캔버스로 활동을 쉽게 끌어다 놓아 여정을 빌드할 수 있습니다. 여정 사용자 인터페이스는 [이 페이지](journey-ui.md)에 자세히 설명되어 있습니다.

![여정 캔버스 샘플](assets/journey38.png)


여정을 만드는 주요 단계는 이 페이지에 자세히 설명되어 있습니다. 다음과 같이 간소화됩니다.

![여정 만들기 단계: 만들기, 디자인, 테스트 및 게시](assets/journey-creation-process.png)


여러 단계로 구성된 고객 여정을 구축하면 채널 간에 실시간으로 상호 작용, 오퍼 및 메시지가 시작됩니다. 이 접근 방식은 고객이 자신의 행동과 관련 비즈니스 신호를 기반으로 최적의 순간에 참여할 수 있도록 합니다. 타겟 대상은 행동, 컨텍스트 데이터 및 비즈니스 이벤트를 기반으로 정의할 수 있습니다. 필수 구성 요소는 사용 사례와 작성 중인 [여정 유형](entry-management.md#types-of-journeys)에 따라 다릅니다. 여정 디자인을 시작하기 전에 관련 구성 단계가 완료되었는지 확인하십시오.

* 이벤트가 수신될 때 여정을 통합적으로 트리거하려면 **이벤트를 구성**&#x200B;해야 합니다. 예상 정보와 처리 방법을 정의합니다. [자세히 보기](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* 또한 여정은 지정된 프로필 세트로 메시지를 일괄적으로 보내기 위해 Adobe Experience Platform 대상을 수신할 수 있습니다. 이를 위해서는 **대상자를 만들기**&#x200B;해야 합니다. [자세히 보기](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* 시스템에 대한 연결을 정의하여 여정에서 사용할 조건 등의 추가 정보를 검색할 수 있습니다. 이 연결은 **데이터 원본**&#x200B;을 사용합니다. [자세히 보기](../datasource/about-data-sources.md)

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer에는 [기본 메시지](../building-journeys/journeys-message.md) 기능이 포함되어 있습니다. 서드파티 시스템을 사용하여 메시지를 보내는 경우 **사용자 지정 작업을 만들 수 있습니다**. 이 [섹션](../action/action.md)에서 자세히 알아보세요.

<!--    ![](assets/custom2.png)  -->


데이터 엔지니어로서 데이터 소스, 이벤트 및 작업을 포함하여 여정을 구성하는 단계는 [이 섹션](../configuration/about-data-sources-events-actions.md)에 자세히 설명되어 있습니다.


>[!NOTE]
>
>[이 페이지](../start/guardrails.md)에서 여정 가드레일 및 제한 사항을 자세히 확인할 수 있습니다.

## 여정 만들기 {#jo-build}

여러 단계 여정을 만들려면 다음 단계를 수행합니다.

1. 여정 관리 메뉴 섹션에서 **[!UICONTROL 여정]**&#x200B;을(를) 클릭합니다.

1. 새 여정을 만들려면 **[!UICONTROL 여정 만들기]** 단추를 클릭하십시오.

1. 여정의 구성 창을 편집하여 여정 이름을 정의하고 속성을 설정합니다. [이 여정](journey-properties.md)에서 페이지의 속성을 설정하는 방법을 알아보세요.

   ![](assets/jo-properties.png)

그런 다음 여정 디자인을 시작할 수 있습니다.

## 여정 디자인 {#jo-design}

옴니채널 여정 디자이너를 통해 타기팅된 대상자, 실시간 고객 또는 비즈니스 상호 작용을 기반으로 하는 업데이트 및 직관적인 드래그 앤 드롭 인터페이스를 사용한 옴니채널 메시지를 통해 여러 단계로 구성된 여정을 작성할 수 있습니다.

![](assets/journey38.png)

1. 팔레트에서 캔버스로 이벤트 또는 **대상자 읽기** 활동을 끌어다 놓는 것으로 시작합니다. 여정 디자인에 대한 자세한 내용은 [이 섹션](using-the-journey-designer.md)을 참조하세요.

   ![](assets/read-segment.png)

1. 개인이 수행할 다음 단계를 드래그 앤 드롭합니다. 예를 들어 채널 작업 뒤에 조건을 추가할 수 있습니다. 활동에 대한 자세한 내용은 [이 섹션](about-journey-activities.md)을 참조하세요.

## 여정 테스트 {#jo-test}

여정을 빌드하면 게시하기 전에 테스트할 수 있습니다. Journey Optimizer에서는 여정을 따라 이동할 때 테스트 프로필을 보는 방법으로 &quot;테스트 모드&quot;를 제공하여 활성화 전에 잠재적인 오류를 감지합니다. 빠른 테스트를 실행하면 여정이 올바르게 작동하는지 확인하여 안정적으로 게시할 수 있습니다.

이 [섹션](testing-the-journey.md)에서 자세히 알아보기

## 여정 게시 {#jo-pub}

여정을 활성화하려면 게시를 하고 새 프로필에서 입력할 수 있도록 해야 합니다. 여정을 게시하기 전에 유효하고 오류가 없는지 확인하십시오. 오류가 있는 여정은 게시할 수 없습니다. 이 [섹션](publishing-the-journey.md)에서 여정 게시에 대해 자세히 알아보세요.

![](assets/jo-journeyuc2_32bis.png)

게시되면 전용 보고 도구를 사용하여 여정을 모니터링하여 여정의 효과를 측정할 수 있습니다.

![](assets/jo-dynamic_report_journey_12.png)

이 [섹션](../reports/live-report.md)에서 여정 보고서에 대해 자세히 알아보세요.

>[!NOTE]
>
>**live** 여정으로 수정해야 하는 경우 여정의 [새 버전을 만들고](journey-ui.md#journey-versions).
