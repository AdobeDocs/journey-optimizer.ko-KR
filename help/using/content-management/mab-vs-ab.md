---
title: 실험 보고서에 사용된 통계 계산
description: A/B 테스트와 multi-armed bandit 비교 자세히 알아보기
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 2%

---

# A/B vs Multi-armed bandit 실험 {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

이 페이지에서는 **A/B**&#x200B;와(과) **Multi-Armed Bandit** 실험을 자세히 비교하여 각각의 강점, 제한 사항 및 각 접근 방식이 가장 효과적인 시나리오를 설명합니다.

## A/B {#ab-test}

기존 A/B 실험에는 처리 간에 트래픽을 균등하게 분할하고 실험이 종료될 때까지 이 할당을 유지하는 작업이 포함됩니다. 일단 통계적 유의성에 도달하면, 승소하는 처리를 식별하고 후속적으로 스케일링한다.

### 장점

기존 A/B 실험의 주요 강점은 다음과 같습니다.

* **통계적 엄격함**

  고정 설계는 잘 정의된 오류율과 신뢰 구간을 제공합니다.

  가설 테스트 프레임워크(예: 95% 신뢰도)를 보다 쉽게 적용하고 해석할 수 있습니다.

  제대로 작동된 실험은 긍정 오류(false positive)의 가능성을 줄인다.

* **단순성**

  방법론은 설계와 실행이 간단합니다.

  결과는 비기술적 이해 당사자에게 명확하게 전달될 수 있다.

* **포괄적인 데이터 수집**

  각 치료는 적절한 노출을 받아, 채택 변형뿐만 아니라 저조한 대체 물질에 대한 분석을 가능하게 합니다.

  이 추가 정보는 장기적인 전략적 결정을 알릴 수 있습니다.

* **바이어스 제어**

  고정 할당은 &quot;승자의 저주&quot;나 평균으로의 회귀와 같은 편견에 취약성을 줄입니다.

### 제한 사항

기존 A/B 실험의 주요 제한 사항은 다음과 같습니다.

* **영업 기회 비용**

  트래픽의 상당 부분이 열등한 처리로 향하므로 테스트 중 전환율 또는 매출이 잠재적으로 줄어듭니다.

  실험이 끝날 때까지 채택 처리를 실행할 수 없습니다.

* **고정 기간 요구 사항**

  테스트는 일반적으로 계절성, 시장 변화, 중도 변경 등 외부 조건이 변경되더라도 사전 지정된 지평에 대해 실행해야 합니다.

  실험 중 적응은 제한되어 있습니다.

## Multi-armed bandit {#mab-experiment}

Multi-armed bandit 알고리즘은 적응형 할당을 사용합니다. 증거가 축적될수록 더 많은 트래픽이 더 나은 성과를 보이는 처리로 이동합니다. 최종 결과에만 집중하기보다는 실험 중 누적 보상을 극대화하는 것이 목적이다.

### 장점

Multi-armed bandit 메서드의 주요 강점은 다음과 같습니다.

* **더 빠른 최적화**

  유망한 치료는 더 일찍 우선시하여 검사 중 전반적인 성능이 향상됩니다.

* **적응성**

  할당은 데이터가 수집될 때 지속적으로 업데이트되므로 Multi-armed bandit 을 동적 환경에 적합합니다.

* **기회 비용 절감**

  잘못된 치료는 신속하게 단계적으로 중단되어 트래픽 낭비를 최소화합니다.

* **지속적인 테스트에 대한 적합성**

  트래픽이 많은 지속적인 실험 또는 컨텍스트에 효과적입니다.

### 제한 사항

Multi-armed bandit 메서드의 주요 제한 사항은 다음과 같습니다.

* **더 약한 통계 보장**

  기존의 가설 테스트는 적용하기 더 어렵고, 규칙을 중단하는 것은 덜 명확합니다.

* **투명도 감소**

  적응적 할당은 이해 관계자에게 설명하기 어려울 수 있다.

* **성과가 낮은 치료에 대한 제한된 정보**

  약한 치료는 노출이 거의 없어 진단 insight을 제한합니다.

* **구현 복잡성**

  구성을 잘못 구성할 가능성이 높은 고급 알고리즘 및 인프라가 필요합니다.

## A/B와 Multi-armed bandit 비교 사용 시기

| 시나리오 | 권장 메서드 |
|-|-|
| 탐색적 또는 연구 중심의 테스트를 실행하고 있습니다. | A/B |
| 광고, 권장 사항과 같은 상시 캠페인을 실행 중입니다. | Multi-Armed Bandit |
| 테스트 중에 전환을 극대화하려는 경우 | Multi-Armed Bandit |
| 명확하고 자신감 있는 통찰력을 원합니다. | A/B |
| 계절적 변화 등 빠르게 적응해야 합니다 | Multi-Armed Bandit |
| 트래픽이 제한되어 있으므로 ROI를 신속하게 최적화하려고 합니다. | Multi-Armed Bandit |
| 트래픽이 많고 학습 속도가 느려질 수 있습니다 | A/B |
| 이해 당사자는 명확한 의사 결정 지점을 필요로 합니다. | A/B |

