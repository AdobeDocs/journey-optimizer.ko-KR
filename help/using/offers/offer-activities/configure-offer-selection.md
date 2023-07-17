---
title: 의사 결정에서 오퍼 선택 구성
description: 의사 결정에 대한 오퍼 선택을 관리하는 방법 알아보기
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 6%

---

# 의사 결정에서 오퍼 선택 구성 {#offers-selection-in-decisions}

여러 오퍼가 주어진 배치에 적합한 경우 의사 결정을 구성할 때 각 프로필에 가장 적합한 오퍼를 선택하는 방법을 선택할 수 있습니다. 오퍼의 순위를 지정할 수 있는 기준:
* 오퍼 우선 순위
* 순위 공식
* [AI 등급](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## 오퍼 우선 순위 {#offer-priority}

기본적으로 여러 오퍼가 의사 결정에서 주어진 배치에 적합한 경우 오퍼가 가장 높음 **우선 순위** 는 고객에게 먼저 제공됩니다.

![](../assets/offer-priority.png)

오퍼를 만들 때 오퍼의 우선 순위 점수가 지정됩니다. 에서 개인화된 오퍼를 만드는 방법을 알아봅니다 [이 섹션](../offer-library/creating-personalized-offers.md).

## 순위 공식 {#assign-ranking-formula}

Journey Optimizer에서는 오퍼 우선 순위 외에도 다음을 만들 수 있습니다 **등급 수식**. 오퍼의 우선 순위 점수를 고려하지 않고, 주어진 배치에 대해 먼저 제시해야 할 오퍼를 결정하는 수식입니다.

예를 들어 종료 날짜가 지금부터 24시간 미만인 모든 오퍼의 우선순위를 늘리거나, 프로필의 관심 지점이 &quot;실행 중&quot;인 경우 &quot;실행 중&quot; 카테고리의 오퍼를 늘릴 수 있습니다.

등급 수식 만들기 방법 알아보기 [이 섹션](../ranking/create-ranking-formulas.md).

공식이 생성되면 의사 결정의 배치에 지정할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 결정을 만들거나 기존 결정을 편집합니다. [의사 결정 만들기](../offer-activities/create-offer-activities.md)를 참조하십시오.

1. 오퍼를 포함할 배치를 추가합니다. 다음을 참조하십시오 [배치 만들기](../offer-library/creating-placements.md).

1. 각 배치에 대해 컬렉션을 추가합니다. 다음을 참조하십시오 [컬렉션 만들기](../offer-library/creating-collections.md).

1. 선택 **[!UICONTROL 공식]** 등급 방법으로 을 클릭한 다음 을 클릭합니다. **[!UICONTROL 순위 추가]**.

   ![](../assets/offer-activity-ranking.png)

1. 원하는 수식을 선택하고 **[!UICONTROL 선택]**.

   ![](../assets/ranking-selection.png)

이제 순위 공식이 배치와 연결됩니다.

여러 오퍼가 이 배치에 표시될 수 있는 경우, 결정은 선택한 공식을 사용하여 먼저 게재할 오퍼를 계산합니다.

## AI 등급 {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

AI 모델을 선택하여 주어진 프로필에 대해 표시할 오퍼에 자동으로 등급을 지정하는 교육된 모델 시스템을 사용할 수도 있습니다. 에서 AI 모델을 만드는 방법을 알아봅니다. [이 섹션](../ranking/create-ranking-strategies.md).

AI 모델이 만들어지면 의사 결정의 배치에 할당할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 결정을 만들거나 기존 결정을 편집합니다. [의사 결정 만들기](../offer-activities/create-offer-activities.md)를 참조하십시오.

1. 오퍼를 포함할 배치를 추가합니다. 다음을 참조하십시오 [배치 만들기](../offer-library/creating-placements.md).

1. 각 배치에 대해 컬렉션을 추가합니다. 다음을 참조하십시오 [컬렉션 만들기](../offer-library/creating-collections.md).

1. 오퍼 등급을 다음으로 지정하도록 선택합니다. **[!UICONTROL AI 등급]** 드롭다운 목록에서 다음을 클릭합니다. **[!UICONTROL 순위 추가]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. 만든 AI 모델을 선택합니다. 모델의 모든 세부 정보가 표시됩니다.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. **[!UICONTROL 선택]**&#x200B;을 클릭합니다. 이제 AI 모델이 배치와 연결됩니다.

여러 오퍼가 적합한 경우 교육된 모델 시스템은 주어진 배치에 대해 먼저 제시해야 하는 오퍼를 결정합니다.

