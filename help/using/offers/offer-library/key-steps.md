---
title: 오퍼를 만드는 주요 단계
description: 오퍼를 만드는 데 필요한 주요 단계를 살펴보십시오.
feature: 오퍼
topic: 통합
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 11%

---

# 오퍼 {#key-steps} 를 만들고 관리하는 주요 단계

오퍼를 만들고, 구성하고, 관리하고, 오퍼를 의사 결정에 사용하는 주요 단계는 아래에 나와 있습니다.

![](../../assets/offer-create-manage-process.png)

오퍼를 구성하는 방법을 보여주는 전체 종단간 예제는 의사 결정에서 사용하고 이메일에서 이 결정을 활용하십시오. 이 페이지](../offers-e2e.md)a0/>을(를) 확인하십시오.[

## 구성 요소 만들기

오퍼 만들기를 시작하기 전에 오퍼에서 사용할 몇 가지 구성 요소를 정의해야 합니다.

1. **오퍼를** 보여주는 데 사용할 컨테이너인 배치를 만듭니다. 예를 들어 이미지 형식의 오퍼에만 사용할 배치를 만들고 메시지 상단에 배치할 수 있습니다.

1. **오퍼가** 표시될 조건을 지정하는 결정 규칙을 만듭니다.

1. **오퍼** 에 연결할 태그를 만들어 쉽게 구성하고 라이브러리에 검색할 수 있습니다.

1. 주어진 배치에 대해 어떤 오퍼가 먼저 제시되어야 하는지 결정하는 규칙을 정의하려는 경우(오퍼의 우선순위 점수를 고려하지 않고) **등급 공식**&#x200B;을 만들 수 있습니다.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">배치 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">의사 결정 규칙 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">태그 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">등급 수식 만들기</a></p></td>
</table>

## 오퍼 만들기 및 관리

1. **오퍼를 만들고**, 오퍼의 컨텐츠와 속성을 구성합니다.

1. **고객이 선택한 오퍼에 적합하지 않을 경우 표시할 마지막 리조트 오퍼인 대체 오퍼를 만듭니다**.

1. **만든** 개인화된 오퍼를 포함하여 결정에 사용할 컬렉션을 만듭니다.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">오퍼 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">대체 오퍼 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">컬렉션 만들기</a></p></td></tr>
</table>

## 결정 만들기 및 구성

1. **배치** 와 개인화된 오퍼 및 대체 오퍼를 결합하는 결정을 만듭니다. 이 조합은 특정 프로필에 가장 적합한 오퍼를 찾기 위해 Offer decisioning 엔진에서 사용합니다.

1. **결정을 구성합니다**. 이렇게 하려면 배치를 선택하고 각 배치에 대해 컬렉션과 폴백을 선택합니다.

1. 필요한 경우, 결정을 구성할 때 순위 공식&#x200B;**을 배치에 할당할 수 있습니다.**

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">의사 결정 만들기</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">결정 구성</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">순위 지정</a></p></td>
</tr>
</table>
