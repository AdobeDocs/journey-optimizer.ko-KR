---
title: 오퍼를 만드는 주요 단계
description: 오퍼를 만드는 데 필요한 주요 단계를 살펴보십시오.
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 5%

---

# 오퍼를 만들고 관리하는 주요 단계 {#key-steps-to-manage-offers}

오퍼를 만들고, 구성하고, 관리하고, 의사 결정에 사용하는 주요 단계는 아래에 나와 있습니다.

![](../assets/offer-create-manage-process.png)

오퍼를 구성하고 의사 결정에 사용하며 이 의사 결정을 전자 메일에 활용하는 방법을 보여 주는 전체 전체 엔드 투 엔드 예제는 [이 페이지](../offers-e2e.md)를 확인하십시오.

## 구성 요소 만들기 {#create-components}

오퍼 만들기를 시작하기 전에 오퍼에 사용할 몇 가지 구성 요소를 정의해야 합니다.

1. 오퍼를 표시하는 데 사용할 컨테이너인 [배치를 만듭니다](creating-placements.md). 예를 들어, 이미지 형식으로만 오퍼 전용이 되고 메시지 맨 위에 배치되는 배치를 만들 수 있습니다.

1. 오퍼를 표시할 조건을 지정하는 [의사 결정 규칙을 만듭니다](creating-decision-rules.md).

1. 오퍼에 연결할 [컬렉션 한정자를 만듭니다](creating-tags.md)(이전에는 &quot;태그&quot;라고 함). 이를 통해 라이브러리를 쉽게 구성하고 검색할 수 있습니다.

1. 오퍼의 우선 순위 점수를 고려하지 않고 주어진 배치에 대해 먼저 제시해야 할 오퍼를 결정하는 규칙을 정의하려면 [순위 공식을 만듭니다](../ranking/create-ranking-formulas.md).

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 오퍼 만들기 및 관리 {#create-and-manage-offers}

1. [오퍼를 만들고](creating-personalized-offers.md), 해당 콘텐츠와 속성을 구성합니다.

1. 고객이 선택한 오퍼에 적합하지 않을 경우 표시할 마지막 대체 오퍼인 [대체 오퍼를 만듭니다](creating-fallback-offers.md).

1. 만든 개인화된 오퍼를 포함하고 의사 결정에 사용하려면 [컬렉션을 만들기](creating-collections.md)하십시오.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 의사 결정 만들기 및 구성 {#create-and-configure-decisions}

1. [배치를 개인화된 오퍼 및 대체 오퍼와 결합하는 결정을 만듭니다](../offer-activities/create-offer-activities.md). 이 조합은 의사 결정 엔진이 특정 프로필에 대한 최상의 오퍼를 찾는 데 사용됩니다.

1. [결정을 구성합니다](../offer-activities/create-offer-activities.md#add-decision-scopes). 이렇게 하려면 배치를 선택하고 각 배치에 대해 컬렉션과 대체 항목을 선택합니다.

1. 필요한 경우 결정을 구성할 때 [등급 수식](../offer-activities/configure-offer-selection.md#assign-ranking-formula) 또는 [AI 등급](../offer-activities/configure-offer-selection.md#use-ranking-strategy)을 배치에 할당할 수 있습니다.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->