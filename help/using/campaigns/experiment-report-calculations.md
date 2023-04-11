---
title: 실험 보고서에 사용된 통계 계산
description: 실험 보고서를 실행할 때 사용되는 통계 계산에 대해 자세히 알아보십시오
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Advertising"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# 실험 보고서의 통계 계산 {#experiment-report-calculations}

>[!BEGINSHADEBOX]

이 설명서에서 찾을 내용:

* [콘텐츠 실험 시작](get-started-experiment.md)
* [콘텐츠 실험 만들기](content-experiment.md)
* [통계 계산 이해](experiment-calculations.md)
* [실험 보고서 구성](reporting-configuration.md)
* **[실험 보고서의 통계 계산](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

이 페이지에서는 Adobe Journey Optimizer의 캠페인에 대한 실험 보고서에 사용된 세부 통계 계산에 대해 설명합니다.

이 페이지는 기술 사용자를 위한 것입니다.

## 전환율

전환율 또는 **평균**, um<sub>ν</sub> 각 치료를 위해 `ν` 실험에서는 지표 합과 해당 지표에 지정된 프로필 수의 비율로 정의됩니다. N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

여기, Y<sub>iν</sub> 은 각 프로필에 대한 목표 지표의 값입니다 `i`지정된 변형에 지정된 *ν*. 목표 지표가 &quot;고유&quot; 지표인 경우, 즉 특정 작업을 수행하는 프로필 수의 카운트입니다. 이것은 전환율로 표시되며, 백분율로 포맷됩니다. 지표가 &quot;카운트&quot; 또는 &quot;합계&quot; 지표(예: 이메일 열기, 각각 수입)이면 지표에 대한 평균 추정은 &quot;프로필당 카운트&quot; 또는 &quot;프로필당 값&quot;으로 표시됩니다.

필요한 경우 표현식에 샘플 표준 편차가 사용됩니다.

![](assets/statistical_2.png){width="225" align="center"}

## 상승도 {#lift}

변형 간의 상승도  *ν*&#x200B;및 컨트롤 변형  *ν<sub>0</sub>* 은 개별 전환율이 위에서 정의된 대로 아래 계산으로 정의된 전환율의 상대 &quot;델타&quot;입니다. 백분율로 표시됩니다.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 개별 치료를 위한 언제든지 유효한 신뢰 구간

여정 실험 패널에는 실험에서의 개별 처리에 대한 &quot;언제든 유효한&quot; 신뢰 구간(신뢰 시퀀스)이 표시됩니다.

개별 변형에 대한 신뢰 시퀀스 `ν` 는 Adobe에서 사용하는 통계 방법론의 중심입니다. 에서 해당 정의를 찾을 수 있습니다. [이 페이지](https://doi.org/10.48550/arXiv.2103.06476) (다음에서 복제) [Waudby-Smith가 Al.]).

대상 매개 변수를 추정하는 데 관심이 있는 경우 `ψ` 실험에서의 변형의 전환율, &#39;고정 시간&#39; 신뢰 구간(CI) 시퀀스 간의 이분법 및 시간 균일한 신뢰 시퀀스(CS) 간의 이분법은 다음과 같이 요약할 수 있습니다.

![](assets/statistical_4.png){width="500" align="center"}

일반 신뢰 구간의 경우 타겟 매개 변수가 값 범위 내에 있다는 확률적 ċ 보장<sub>n</sub> 는 단일 고정 값에서만 유효합니다. `n` (다음과 같은 경우) `n` 는 샘플 수입니다.) 반대로 신뢰 시퀀스의 경우 항상 샘플 크기의 모든 값이 보장됩니다 `t`로 설정하면 관심 매개 변수의 &quot;true&quot; 값이 범위 내에 있습니다.

이렇게 하면 온라인 테스트에 매우 중요한 몇 가지 심층적인 의미가 있습니다.

* CS는 새로운 데이터를 사용할 수 있게 될 때마다 선택적으로 업데이트됩니다.
* 실험은 지속적으로 모니터링, 적응적으로 정지 또는 계속될 수 있다.
* 유형-I 오류는 데이터 종속적 시간을 포함하여 모든 중지 시간에 제어됩니다.

Adobe은 평균 예상 개별 변형에 대해 체감형 신뢰도 시퀀스를 사용합니다 `μ` 에는 다음 양식이 있습니다.

![](assets/statistical_5.png){width="300" align="center"}

수행:

* `N` 는 해당 변형에 대한 단위 수입니다.
* `σ` 는 표준 편차의 샘플 예상(위에 정의됨)입니다.
* `α` 는 원하는 유형-I 오류 수준(또는 잘못된 범위 가능성)입니다. 항상 0.05로 설정됩니다.
* ρ<sup>2개</sup> 는 CS가 가장 가까운 샘플 크기를 조정하는 상수입니다. Adobe이 유니버설 값을 ρ 선택함<sup>2개</sup> = 10<sup>-2.8</sup>: 온라인 실험에서 표시되는 전환율 유형에 적합합니다.

## 신뢰도 {#confidence}

Adobe에서 사용하는 신뢰도는 평균 처리 효과에 대한 신뢰 시퀀스를 반전하여 얻은 &quot;언제든지 유효한&quot; 신뢰도입니다.

정확하게 말하자면, 두 개의 샘플로 *t* 두 변형 간의 수단의 차이점을 테스트합니다. 에는 1:1 매핑이 있습니다 *p*-이 테스트에 대한 값 및 의미에서의 차이에 대한 신뢰 구간. 유추로, 언제나 유효함 *p*-value는 평균 처리 효과 추정기의 (언제든 유효한) 신뢰 시퀀스를 반전하여 얻을 수 있습니다.

![](assets/statistical_6.png){width="200" align="center"}

여기, *E* 이는 예상입니다. 사용된 견적 도구는 역 성향 가중치(IPW) 견적 도구입니다. 고려 N = N<sub>0</sub> +N<sub>1</sub> 단위, 각 단위에 대한 변형 할당 `i` 레이블 지정<sub>i</sub>= 0,1 단위를 변형에 할당하는 경우 `ν`= 0,1. 사용자에게 고정 확률(성향)이 있는 경우<sub>0</sub>, (1-파이)<sub>0</sub>)이고, 그 결과 지표는 Y입니다.<sub>i</sub>를 입력하면 평균 처리 효과를 위한 IPW 견적 도구는 다음과 같습니다.

![](assets/statistical_12.png){width="400" align="center"}

그 점에 주목해 *f* 는 영향 기능인 Audby-Smith et al입니다. 은 이 견적 도구 의 신뢰 시퀀스를 보여 주었습니다.

![](assets/statistical_7.png){width="500" align="center"}

경험적 추정치로 할당 확률 대체: 바늘<sub>0</sub> = N<sub>0</sub>/N, 상기 분산 용어는 개별 샘플 평균 추정에 대하여 나타낼 수 있다<sub>0,1</sub> 표준 편차 추정,<sub>0,1</sub> 로서의:

![](assets/statistical_8.png){width="500" align="center"}

다음으로, 테스트 통계 z = (um)를 사용한 일반 가설 테스트를 상기하십시오.<sub>A</sub>-um<sub>0</sub>/sigma<sub>p</sub>) 다음 간에 통신합니다. `p`-값 및 신뢰 구간:

![](assets/statistical_9.png){width="500" align="center"}

여기서 `Φ` 표준 정규의 누적 분포입니다. 언제든 유효한 경우 `p`-values, 위에 정의된 평균 처리 효과에 대한 신뢰 시퀀스가 있는 경우 이 관계를 변환할 수 있습니다.

![](assets/statistical_10.png){width="600" align="center"}

마지막으로, **언제든 유효한 신뢰** is:

![](assets/statistical_11.png){width="200" align="center"}

## 실험 확정 선언

두 개의 팔을 사용한 실험의 경우 Journey Optimizer 실험 패널에 실험이 &quot;실험&quot;이라는 메시지가 표시됩니다 **확정** 언제든지 유효한 신뢰도가 95%를 초과하는 경우(즉, 언제든 유효한 신뢰) `p`-value가 5% 미만).

두 개 이상의 변형이 있는 경우 Bonferonni 보정이 적용되어 가족 단위 오류 비율을 제어합니다. 실험 대상 `K` 치료 및 단일 기준선(제어) 치료에는 `K-1` 독립적인 가설 테스트. Bonferonni 보정은 제어와 주어진 변형이 항상 유효한 경우 동일한 수단이 있다는 null 가설을 거부한다는 것을 의미합니다 `p`-value(위에 정의됨)가 임계값 미만입니다. `α/(K-1)`.

## 성과가 가장 좋은 암

실험이 확정되면 최고의 성과가 나타나는 암이 표시됩니다. 이 팔은 컨트롤이 포함된 Set 및 모든 Arm 중에서 가장 뛰어난 성능(가장 높은 평균 또는 전환율)을 가진 팔입니다 `p`-Bonferonni 임계값 미만입니다.
