---
title: 오퍼 라이브러리 사용자 인터페이스
description: 오퍼 라이브러리 사용자 인터페이스에 대해 자세히 알아보기
badge: label="레거시" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Beginner, Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 33%

---

# 오퍼 라이브러리 사용자 인터페이스 {#user-interface}

왼쪽 레일의 **[!UICONTROL 의사 결정 관리]** 섹션에는 의사 결정 관리 기능에 액세스할 수 있는 두 가지 메뉴가 있습니다.

**[!UICONTROL 오퍼]** 메뉴를 사용하여 오퍼를 관리하고 전달하십시오.


![](../assets/offers_menu.png)

* **[!UICONTROL 개요]**: [!DNL decision management]의 새로운 기능 화면 단계에 따라 배치, 오퍼 및 컬렉션 설정을 시작합니다. [!DNL decision management]을(를) 이미 알고 있는 경우 가장 최근 오퍼, 컬렉션 및 의사 결정에 대한 개요를 살펴보십시오. [자세히 알아보기](#overview)
* **[!UICONTROL 오퍼]**: 개인화된 오퍼와 대체 오퍼를 만들고 액세스합니다. [오퍼](../offer-library/creating-personalized-offers.md) 및 [대체 오퍼](../offer-library/creating-fallback-offers.md)를 만드는 방법을 알아봅니다.
* **[!UICONTROL 컬렉션]**: 오퍼를 정적 및 동적 컬렉션으로 구성합니다. [자세히 알아보기](../offer-library/creating-collections.md)
* **[!UICONTROL 의사 결정]**: 오퍼를 게재할 의사 결정을 만들고 관리합니다. [자세히 알아보기](../offer-activities/create-offer-activities.md)
* **[!UICONTROL 일괄 의사 결정]**: 주어진 Adobe Experience Platform 대상의 모든 프로필에 오퍼 의사 결정을 전달합니다. [자세히 알아보기](../batch-delivery.md)
* **[!UICONTROL 시뮬레이션]**: 지정된 배치에 대해 테스트 프로필에 게재할 오퍼를 시뮬레이션하여 의사 결정 논리의 유효성을 검사합니다. [자세히 알아보기](../offer-activities/simulation.md)

오퍼 및 의사 결정을 만드는 데 필요한 구성 요소를 만들고 관리하려면 **[!UICONTROL 구성 요소]** 메뉴를 사용하십시오.

![](../assets/offer_activities.png)

* **[!UICONTROL 배치]**: 오퍼가 표시될 배치를 만들고 관리합니다. [자세히 알아보기](../offer-library/creating-placements.md)
* **[!UICONTROL 컬렉션 한정자]**: 오퍼를 구성하고 필터링할 컬렉션 한정자(이전에 &quot;태그&quot;라고 함)를 만들고 관리합니다. [자세히 알아보기](../offer-library/creating-tags.md)
* **[!UICONTROL 규칙]**: 오퍼가 표시되는 조건을 관리합니다. [자세히 알아보기](../offer-library/creating-decision-rules.md)
* **[!UICONTROL 순위]**: 순위 공식을 만들고 관리하여 지정된 배치에 대해 먼저 제시해야 하는 오퍼를 결정합니다. [자세히 알아보기](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>의사 결정 관리 또는 일부 기능에 액세스하는 데 문제가 있는 경우 관리 사용자에게 필요한 권한이 부여되었는지 확인하십시오. [의사 결정 관리에 대한 액세스 권한 부여](starting-offer-decisioning.md#granting-acess-to-decision-management)를 참조하십시오.

## 개요 {#overview}

[!DNL decision management]을(를) 처음 사용하는 경우 **[!UICONTROL 개요]** 탭에서 첫 번째 오퍼 결정 작성을 시작하는 데 필요한 주요 단계를 안내합니다. 화면의 단계에 따라 배치, 오퍼 및 컬렉션을 시작하십시오. 이러한 첫 번째 단계를 완료하면 오퍼 결정을 만들라는 메시지가 표시됩니다.

>[!NOTE]
>
>오퍼를 만들어 의사 결정에 사용하는 주요 단계는 [이 섹션](../offer-library/key-steps.md)에 나와 있습니다.

[!DNL decision management]을(를) 더 잘 알고 있고 이미 하나 이상의 오퍼 결정을 만든 경우 **[!UICONTROL 개요]** 탭에 가장 최근 오퍼, 컬렉션 및 결정이 표시됩니다.

오퍼 또는 의사 결정을 클릭하여 선택한 항목의 세부 정보에 직접 액세스합니다.

오퍼, 컬렉션 또는 결정 목록에 액세스하려면 **[!UICONTROL 모두 보기]** 단추를 클릭하십시오.

![](../assets/overview_view-all.png)

## 검색 및 필터 정보 {#search-and-filter-information}

특정 항목을 찾으려면 **검색 막대**&#x200B;를 사용합니다.

목록 왼쪽 위의 필터 아이콘을 클릭하면 **필터**&#x200B;에 액세스할 수 있습니다. 필터 메뉴에서는 표시된 요소를 다양한 조건에 따라 필터링할 수 있습니다. 예를 들어 이메일 통신 채널 및 이미지 유형 콘텐츠용으로 만들어진 배치를 필터링할 수 있습니다.

![](../assets/filters.png)

## 표시된 정보 사용자 지정 {#customize-displayed-information}

의사 결정 관리 메뉴의 목록은 목록 오른쪽 상단의 구성 단추를 사용하여 개인화할 수 있습니다.

필요에 따라 표시할 정보를 선택할 수 있습니다.

사용자 지정 열은 각 사용자에 대해 저장됩니다.

![](../assets/columns.png)

## 정보 창 {#information-pane}

다른 목록에서 요소를 선택하여 정보를 검색하고 요소에 대한 기본 작업을 수행할 수 있는 정보 창을 표시합니다.

![](../assets/information-pane.png)

이제 오퍼 및 의사 결정 목록을 사용하여 여러 요소에 대량 작업을 수행할 수 있습니다. 이렇게 하려면 원하는 오퍼 또는 의사 결정을 선택한 다음 정보 창에서 수행할 작업을 선택합니다.

기존 오퍼 또는 의사 결정을 복제하여 **[!UICONTROL 초안]** 상태의 복사본을 만들 수도 있습니다. 정보 창이나 오퍼 또는 의사 결정의 세부 보기에서 수행할 수 있습니다.

## 오퍼 및 의사 결정 변경 로그 {#changes-logs}

[!DNL Journey Optimizer]을(를) 통해 오퍼 또는 의사 결정에 대한 모든 변경 내용을 시각화할 수 있습니다. 이렇게 하려면 왼쪽 메뉴에서 **[!UICONTROL 감사]** 메뉴에 액세스합니다. [리소스에 대한 작업을 감사하는 방법을 알아보세요](../../privacy/audit-logs.md)
