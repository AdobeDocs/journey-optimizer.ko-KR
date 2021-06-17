---
title: 의사 결정에서 오퍼 선택 구성
description: 선택 사항을 결정으로 관리하는 방법을 알아봅니다.
feature: 오퍼
topic: 통합
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---

# 의사 결정에서 오퍼 선택 구성 {#offers-selection-in-activities}

## 오퍼 우선 순위 정보 {#about-offers-priority}

기본적으로 몇 개의 오퍼가 결정(이전에 오퍼 활동이라고 함)에서 주어진 배치에 참가할 수 있는 경우 가장 높은 **우선순위**&#x200B;를 가진 오퍼가 고객에게 먼저 전달됩니다. 오퍼를 만들 때 오퍼의 우선순위 점수가 지정됩니다( [개인화된 오퍼 만들기](../offer-library/creating-personalized-offers.md) 참조).

![](../../assets/offer-priority.png)

또한 Journey Optimizer에서 **등급 공식**&#x200B;을 만들 수 있습니다. 오퍼의 우선 순위 점수를 고려하지 않고 주어진 배치에 대해 먼저 제공해야 하는 오퍼를 결정하는 공식입니다.

예를 들어, 종료 날짜가 지금부터 24시간 미만인 모든 오퍼의 우선순위를 늘리거나, 프로필의 관심 영역이 &quot;실행 중&quot;인 경우 &quot;실행 중&quot; 카테고리의 오퍼를 늘릴 수 있습니다.

등급 수식을 만드는 방법에 대한 자세한 내용은 [이 섹션](../offer-library/create-ranking-formulas.md)을 참조하십시오.

## 배치 {#assign-ranking-formula}에 등급 공식 할당

등급 공식이 만들어지면 결정에서 배치에 할당할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 결정을 만들거나 기존 오퍼를 편집한 다음, 오퍼가 포함된 배치를 만듭니다([결정 만들기](../offer-activities/create-offer-activities.md) 참조).

1. 각 배치에 대해 드롭다운 목록에서 **[!UICONTROL Ranking]** 을 선택합니다.

1. **[!UICONTROL Add ranking]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offer-activity-ranking.png)

1. 원하는 등급 공식을 선택하고 **[!UICONTROL Select]** 을 클릭합니다.

   ![](../../assets/ranking-selection.png)

이제 등급 공식이 배치와 연결됩니다.

이 배치에서 여러 오퍼를 표시할 수 있는 경우, 이 결정은 순위 수식의 공식을 사용하여 먼저 전달할 오퍼를 계산합니다.
