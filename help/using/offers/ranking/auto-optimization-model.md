---
product: experience platform
solution: Experience Platform
title: 자동 최적화 모델
description: 자동 최적화 모델에 대해 자세히 알아보기
feature: Ranking, Offers
role: User
level: Intermediate
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: 0ea2ed03a476e0b64a8ebfadde403ff9f9e57bba
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# 자동 최적화 모델 {#auto-optimization-model}

자동 최적화 모델은 비즈니스 클라이언트가 설정한 KPI(반환)를 극대화하는 오퍼를 제공하는 것을 목표로 합니다. 이러한 KPI는 전환율, 수익 등의 형태일 수 있습니다. 이 시점에서 자동 최적화는 타겟으로 오퍼 전환을 사용하여 오퍼 클릭을 최적화하는 데 중점을 둡니다. 자동 최적화는 개인화되지 않으며 오퍼의 &quot;글로벌&quot; 성능을 기반으로 최적화됩니다.

## 제한 사항 {#limitations}

의사 결정 관리에 자동 최적화 모델을 사용할 경우 아래의 제한 사항이 적용됩니다.

* 자동 최적화 모델은 Batch Decisioning API에서 작동하지 않습니다.
* 모델을 만드는 데 필요한 피드백을 경험 이벤트로 보내야 합니다. 다음에서 자동으로 전송되어서는 안 됩니다. [!DNL Journey Optimizer] 채널.

## 용어 {#terminology}

다음 용어는 자동 최적화에 대해 논의할 때 유용합니다.

* **Multi-armed bandit**: A [multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} 최적화에 대한 접근 방식은 탐색적 학습과 해당 학습의 이용 간에 균형을 이룹니다.

* **톰슨 샘플링**: Thompson 샘플링은 즉각적인 성과를 극대화하는 것으로 알려진 것을 활용하는 것과 향후 성과를 향상시킬 수 있는 새로운 정보를 축적하는 투자 사이에서 균형을 이루어야 하는 방식으로 조치가 순차적으로 취해지는 온라인 의사 결정 문제에 대한 알고리즘입니다. [자세히 알아보기](#thompson-sampling)

* [**베타 배포**](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}: Set of continuous [probability distributions](https://en.wikipedia.org/wiki/Probability_distribution){target="_blank"} defined on the interval [0, 1] [parameterized](https://en.wikipedia.org/wiki/Statistical_parameter){target="_blank"} by two positive [shape parameters](https://en.wikipedia.org/wiki/Shape_parameter){target="_blank"}.

## 톰슨 샘플링 {#thompson-sampling}

자동 최적화의 기본이 되는 알고리즘은 다음과 같습니다. **톰슨 샘플링**. 이 절에서는 Thompson 표본추출의 직관에 대해 논의한다.

[톰슨 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}베이지안 도적들 또는 베이지안 도적들은 다무장 도적 문제에 대한 베이지안 접근이다.  기본 아이디어는 각 오퍼의 평균 보상 ??를 로 처리하는 것입니다. **확률변수** 그리고 지금까지 수집한 데이터를 사용하여 평균 보상에 대한 &quot;믿음&quot;을 업데이트합니다. 이 &quot;믿음&quot;은 수학적으로 **사후확률분포** - 기본적으로 각 오퍼에 대해 보상이 해당 값을 가질 가능성(또는 확률)과 함께 평균 보상에 대한 값의 범위입니다. 그리고 모든 결정에 대해 **이러한 후위 보상 분포 각각에서 한 점을 샘플링합니다.** 샘플링된 보상이 가장 높은 값을 가진 오퍼를 선택합니다.

이 프로세스는 아래 그림과 같으며, 여기서는 3개의 오퍼가 있습니다. 처음에 우리는 자료로부터 아무런 증거도 가지고 있지 않으며, 우리는 모든 제안들이 균일한 사후 보상 분포를 가지고 있다고 가정한다. 우리는 각 오퍼의 사후 보상 분포에서 샘플을 도출한다. 오퍼 2의 배포에서 선택한 샘플의 값이 가장 높습니다. 다음은 의 예입니다. **탐험**. 오퍼 2를 표시한 후 잠재적 보상(예: 전환/전환 없음)을 수집하고 아래 설명된 대로 베이즈 정리를 사용하여 오퍼 2의 사후 분포를 업데이트합니다.  이 프로세스를 계속 진행하고 오퍼가 표시되고 보상이 수집될 때마다 사후 분포를 업데이트합니다. 두 번째 그림에서는 오퍼 3이 선택되었습니다. 오퍼 1이 가장 높은 평균 보상(사후 보상 분포는 오른쪽으로 가장 멀리 있음)을 제공함에도 불구하고 각 분포에서 샘플링하는 프로세스는 명백히 최적이 아닌 오퍼 3을 선택하게 만들었습니다. 이를 통해 Offer 3의 진정한 보상 분배에 대해 자세히 알아볼 수 있는 기회를 제공합니다.

더 많은 표본이 수집될수록 신뢰도는 증가하고, 가능한 보상에 대한 보다 정확한 추정치가 얻어진다(더 좁은 보상 분포에 해당함). 더 많은 증거가 확보됨에 따라 우리의 신념을 업데이트하는 이러한 과정은 다음과 같이 알려져 있다. **베이지안 추론**.

결국, 하나의 오퍼(예를 들어, 오퍼 1)가 명백한 승자일 경우, 그 사후 보상 분포는 다른 오퍼들과 분리될 것이다. 이 시점에서 각 결정에 대해 오퍼 1에서 표본으로 추출된 보상이 가장 높을 가능성이 있으며, 우리는 더 높은 확률로 선택할 것이다. 이 은(는) **착취** - 우리는 오퍼 1이 최선이라는 강한 믿음을 가지고 있으며, 따라서 보상을 최대화하기 위해 선택되어지고 있습니다.

![](../assets/ai-ranking-thompson-sampling.png)

**그림 1**: *모든 결정에 대해 우리는 후기 보상 분포에서 한 점을 표본으로 삼는다. 샘플 값(전환율)이 가장 높은 오퍼가 선택됩니다. 초기 단계에서는 데이터에서 오퍼의 전환율에 대한 증거가 없으므로 모든 오퍼가 균일한 분포를 갖습니다. 우리가 더 많은 표본을 수집함에 따라, 후방 분포는 더 좁고 더 정확해진다. 궁극적으로 전환율이 가장 높은 오퍼가 매번 선택됩니다.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**기술 세부 정보**

배포를 계산/업데이트하기 위해 다음을 사용합니다. **베이즈 정리**. 각 오퍼에 대해 ***i***, 우리는 그들의 ***P(??i)를 계산하려고 한다 | data)***예: 각 오퍼에 대해 ***i***, 보상 값의 가능성 **??i** 은 해당 오퍼에 대해 지금까지 수집한 데이터를 고려할 때 입니다.

베이즈 정리에서:

***Posteral = Liability * Prior***

다음 **사전 확률** 은 결과를 생성할 확률에 대한 초기 추측입니다. 몇 가지 증거가 수집된 후 확률은 다음과 같이 알려져 있습니다. **사후 확률**. 

자동 최적화는 이진 보상(클릭/클릭 안 함)을 고려하도록 설계되었습니다. 이 경우 가능성은 N개의 시도에서 성공한 횟수이며 **이항 분포**. 어떤 우도 함수의 경우, 어떤 전조를 선택하면, 후위는 전차와 같은 분포에 있게 된다. 이러한 이전 은 다음과 같습니다. **공액 선행**. 이러한 종류의 선행은 사후분포의 계산을 매우 간단하게 만든다. 다음 **베타 배포** 는 이항 우도(이항 보상) 이전의 컨쥬게이트이며, 따라서 이전 및 사후 확률 분포에 편리하고 합리적인 선택입니다.베타 분포는 두 개의 매개 변수를 사용합니다. ***α*** 및 ***β***. 이러한 매개 변수는 성공 및 실패 횟수와 다음에 의해 주어진 평균 값으로 생각할 수 있습니다.

![](../assets/ai-ranking-beta-distribution.png)

위에서 설명한 것과 같은 가능성 함수는 성공(전환)과 f 실패(전환 없음)가 있는 이항 분포로 모델링되며, q는 [확률변수](https://en.wikipedia.org/wiki/Random_variable){target="_blank"} with a [beta distribution](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}.

이전 은 베타 분포로 모델링되고 사후 분포는 다음 형식을 취합니다.

![](../assets/ai-ranking-posterior-distribution.svg)

사후는 기존의 모수에 성공과 실패의 횟수를 더하는 것만으로 계산된다 ***α***, ***β***.

자동 최적화의 경우 위의 예에서 보듯이 이전 분포부터 시작합니다 ***Beta(1, 1)*** (균일 분포) 모든 오퍼에 대해, 주어진 오퍼에 대해 s 성공 및 f 실패를 얻은 후 후위는 매개 변수가 있는 Beta 분포가 됩니다 ***(s+α, f+β)*** 을 참조하십시오.
+++

**관련 항목**:

Thompson 샘플링에 대한 자세한 내용은 다음 연구 논문을 참조하십시오.
* [톰슨 표본추출에 관한 실증적 평가](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [Multi-armed Bandit 문제에 대한 Thompson 표본 분석](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}

## 냉시동 문제 {#cold-start}

&quot;콜드 스타트&quot; 문제는 새 오퍼가 캠페인에 추가되고 새 오퍼의 전환율에 대해 사용할 수 있는 데이터가 없을 때 발생합니다. 이 기간 동안 이 새 오퍼의 전환율에 대한 정보를 수집하는 동안 성능 저하를 최소화하기 위해 이 새 오퍼를 얼마나 자주 선택하는지에 대한 전략을 마련해야 합니다. 이 문제를 해결하는 데 사용할 수 있는 솔루션은 여러 가지가 있습니다. 우리가 그 착취를 많이 희생하지 않으면서 이 새로운 제안의 탐사 사이에서 균형을 찾는 것이 핵심이다. 현재 새 오퍼의 전환율(이전 배포)에 대한 초기 예상으로 &quot;균일 배포&quot;를 사용합니다. 기본적으로 우리는 모든 전환율 값을 동일한 발생 확률을 제공한다.


![](../assets/ai-ranking-cold-start-strategies.png)

**그림 2**: *3개의 오퍼가 있는 캠페인을 고려하십시오. 캠페인이 라이브인 동안 오퍼 4가 캠페인에 추가됩니다. 처음에 우리는 오퍼 4의 전환율에 대한 데이터가 없으며 콜드 스타트 문제를 처리해야 합니다. 당사는 이 새로운 오퍼에 대한 데이터를 수집하는 동안 오퍼 4의 전환율에 대한 초기 추측으로 균일 분포를 사용합니다. 에 설명된 대로 [톰슨 샘플링](#thompson-sampling) 섹션, 사용자에게 표시될 오퍼를 선택하기 위해 오퍼의 사후 보상 배포에서 포인트를 샘플링하고 샘플 값이 가장 높은 오퍼를 선택합니다. 위의 예에서 오퍼 4가 선택되고 나중에 수집된 보상에 따라 이 오퍼의 후방 분포가 다음에 설명된 대로 업데이트됩니다. [톰슨 샘플링](#thompson-sampling) 섹션.*

## 상승도 측정 {#lift}

&quot;상승도&quot;는 기준선 전략(무작위로 오퍼 제공)과 비교하여 순위 서비스에 배포된 전략의 성과를 측정하는 데 사용되는 지표입니다.

예를 들어, 순위 서비스에 사용되는 Thompson 샘플링(TS) 전략의 성과를 측정하려는 경우 KPI가 전환율(CVR)이면 기준 전략에 대한 TS 전략의 &quot;상승도&quot;는 다음과 같이 정의됩니다.

![](../assets/ai-ranking-lift.png)
