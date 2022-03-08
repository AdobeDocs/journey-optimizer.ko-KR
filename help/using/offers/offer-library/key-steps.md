---
title: 오퍼를 만드는 주요 단계
description: 오퍼를 만드는 데 필요한 주요 단계를 살펴보십시오.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 13%

---

# 오퍼를 만들고 관리하는 주요 단계 {#key-steps-to-manage-offers}

오퍼를 만들고, 구성하고, 관리하고, 오퍼를 의사 결정에 사용하는 주요 단계는 아래에 나와 있습니다.

![](../../assets/offer-create-manage-process.png)

오퍼를 구성하고, 의사 결정에서 이러한 오퍼를 사용하고, 이메일에서 이 결정을 활용하는 방법을 보여주는 전체 종단간 예제는 다음 단계를 참조하십시오 [이 페이지](../offers-e2e.md).

## 구성 요소 만들기 {#create-components}

오퍼 만들기를 시작하기 전에 오퍼에서 사용할 몇 가지 구성 요소를 정의해야 합니다.

1. **배치 만들기**: 오퍼를 표시하는 데 사용할 컨테이너입니다. You can, for example, create a placement that will be dedicated to offers in the image format only, and situated to the top of your messages.

1. **의사 결정 규칙 만들기** 은 오퍼가 표시될 조건을 지정합니다.

1. **태그 만들기** 오퍼에 연결되므로 오퍼를 쉽게 구성하고 라이브러리에 검색할 수 있습니다.

1. 주어진 배치에 대해 먼저 제공해야 하는 오퍼를 결정하는 규칙을 정의하려는 경우(오퍼의 우선순위 점수를 고려하지 않고) 다음을 수행할 수 있습니다 **등급 공식 만들기**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">배치 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">의사 결정 규칙 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">태그 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">등급 수식 만들기</a></p></td>
</table>

## 오퍼 만들기 및 관리 {#create-and-manage-offers}

1. **Create offers**, and configure their content and properties.

1. **대체 오퍼 만들기**: 고객이 선택한 오퍼에 적합하지 않을 경우 표시할 마지막 수단이 되는 오퍼입니다.

1. **Create a collection** to include the personalized offers you created and use them in a decision.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">오퍼 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">대체 오퍼 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">컬렉션 만들기</a></p></td></tr>
</table>

## 결정 만들기 및 구성 {#create-and-configure-decisions}

1. **결정 만들기** 배치와 개인화된 오퍼 및 대체 오퍼를 결합합니다. This combination will be used by the Offer Decisioning engine to find the best offer for a specific profile.

1. **Configure the decision**. 이렇게 하려면 배치를 선택하고 각 배치에 대해 컬렉션과 폴백을 선택합니다.

1. If needed, you can **assign a ranking formula** to a placement when configuring the decision.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">의사 결정 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">결정 구성</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">순위 지정</a></p></td>
</tr>
</table>
