---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer 실험에 사용되는 통계 계산
description: 실험을 실행할 때 사용되는 통계 계산에 대해 자세히 알아보기
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: 내용, 실험, 통계, 계산
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# 통계 계산 이해 {#experiment-calculations}

이 문서에서는 Adobe Journey Optimizer에서 실험을 실행할 때 사용되는 통계 계산에 대해 설명합니다.

실험 사용 [고급 통계 방법](../content-management/assets/confidence_sequence_technical_details.pdf) 계산하려면 **신뢰 시퀀스** 및 **신뢰도**&#x200B;을 사용하여 필요한 기간 동안 실험을 실행하고 결과를 지속적으로 모니터링할 수 있습니다.

이 문서에서는 실험의 작동 방식을 설명하고 Adobe의 **항상 유효한 신뢰 시퀀스**.

전문가 사용자의 경우 기술 세부 정보 및 참조는에 자세히 설명되어 있습니다. [이 페이지](../content-management/assets/confidence_sequence_technical_details.pdf).

## 통계 테스트 및 오류 제어 {#statistical-testing}

실험을 실행할 때 두 집단 간에 차이가 있는지, 그리고 그 차이가 우연으로 인한 것일 가능성을 판단하려고 한다.

일반적으로 다음과 같은 두 가지 가설이 있습니다.

* 다음 **귀무 가설** 치료에는 아무런 영향이 없다는 의미입니다.
* 다음 **대체 가설** 즉, 치료에는 효과가 있습니다.

통계적 유의성에서 목표는 귀무가설을 기각하기 위한 증거의 강도를 평가해 보는 것이다. 주목해야 할 한 가지 중요한 점은 통계적 유의성은 치료가 성공적일 가능성이 아니라 얼마나 달라질 가능성을 판단하기 위해 사용된다는 것입니다. 통계적 유의성을 와 함께 사용하는 이유다. **상승도**.

효과적인 실험에는 잘못된 추론을 야기할 수 있는 다양한 유형의 오류가 고려되어야 합니다.

![](assets/technote_1.png)

위의 표에는 다양한 유형의 오류가 나와 있습니다.

* **긍정 오류(I형 오류)**: 실제로 true인 경우 null 가설에 대한 잘못된 거부입니다. 온라인 실험의 맥락에서 이것은 비록 동일하지만 결과 지표가 각 처리 간에 다르다는 잘못된 결론을 내리는 것을 의미한다.
  </br>실험을 실행하기 전에 일반적으로 임계값을 선택합니다 `\alpha`. 실험이 실행되면 `p-value` 는 계산되며, `null if p < \alpha`.선택 `/alpha` 예를 들어, 누군가의 삶이 영향을 받을 수 있는 임상 실험에서 잘못된 대답을 얻은 결과를 기반으로 합니다. `\alpha = 0.005`. 온라인 실험에서 일반적으로 사용되는 임계값은 다음과 같습니다. `\alpha = 0.05`즉, 장기적으로 100번의 실험 중 5번의 실험이 긍정 오류(false positive)가 될 것으로 예상합니다.

* **거짓 음성(Type-II 오류)**: false이지만 귀무 가설을 기각하지 못함을 의미합니다. 실험의 경우, 이것은 사실상 그것이 다를 때, 귀무 가설을 기각하지 않는다는 것을 의미한다. 이러한 유형의 오류를 제어하려면 일반적으로 실험에 다음과 같이 정의된 특정 전원을 보장할 충분한 사용자가 있어야 합니다. `1 - \beta`(예: 1에서 유형 II 오류의 확률을 뺀 값).

대부분의 통계 추론 기술을 사용하려면 판별하려는 효과 크기와 오류 허용치()를 기반으로 미리 샘플 크기를 수정해야 합니다.`\alpha` 및 `\beta`)에 앞서 있습니다. 그러나 Adobe Journey Optimizer의 방법론은 샘플 크기에 대해 결과를 지속적으로 볼 수 있도록 설계되었습니다.

## Adobe 통계 방법: 항상 유효한 신뢰 시퀀스

A **신뢰 시퀀스** 는 의 순차적 아날로그입니다. **신뢰 구간**&#x200B;예: 실험을 백 번 반복하고 실험에 참여하는 모든 신규 사용자에 대해 평균 지표와 관련 95%-신뢰 시퀀스의 추정치를 계산하는 경우. 95% 신뢰 시퀀스에는 100개의 실험 중 95개의 지표의 실제 값이 포함됩니다. 95% 신뢰 구간은 모든 신규 사용자가 아닌 동일한 95% 적용 범위를 보장하기 위해 실험당 한 번만 계산할 수 있습니다. 따라서 신뢰 시퀀스를 사용하면 가양성 오류율을 증가시키지 않고 실험을 지속적으로 모니터링할 수 있습니다.

단일 실험에 대한 신뢰 시퀀스와 신뢰 구간 간의 차이는 아래 애니메이션에 표시됩니다.

![](assets/technote_2.gif)

**신뢰 시퀀스** 실험의 초점을 가설 검정이 아닌 추정으로 옮깁니다. 즉, 통계적 유의성의 임계값에 기초한 귀무 가설의 거절 여부 보다는 처치 간 수단 차이의 정확한 추정에 초점을 맞춥니다.

그러나 간의 관계와 유사한 방식으로 `p-values`, 또는 **신뢰도**, 및 **신뢰 구간**, 사이에는 또한 관계가 있습니다 **신뢰 시퀀스** 및 유효한 모든 시간 `p-values`또는 언제든지 유효한 신뢰입니다. 신뢰도와 같은 양의 친숙도가 주어지면, Adobe은 두 가지를 모두 제공합니다. **신뢰 시퀀스** 언제든지 해당 보고서에 대한 신뢰도가 유효합니다.

의 이론적 기초 **신뢰 시퀀스** martingales로 알려진 임의의 변수들의 연쇄에 대한 연구에서 나온 것이다. 아래 전문가 독자에 대한 몇 가지 주요 결과가 포함되었지만, 실무자의 취지는 명확합니다.

>[!NOTE]
>
>신뢰 서열은 신뢰 구간의 안전한 순차적 유사체로 해석될 수 있다. 신뢰 구간을 사용하면 미리 결정된 샘플 크기에 도달한 후에만 실험을 해석할 수 있습니다. 그러나 신뢰 시퀀스를 사용하면 원하는 시간에 실험의 데이터를 보고 해석할 수 있으며 실험을 안전하게 중단하거나 계속할 수 있습니다. 해당 항상 유효한 신뢰도 또는 `p-value`는 또한 언제든지 해석하는 것이 안전합니다.

신뢰 시퀀스가 &quot;유효한 시간&quot;이므로, 동일한 샘플 크기에서 사용되는 고정 대상 기간 방법론보다 더 보수적일 것이라는 점을 참고하십시오. 신뢰 시퀀스의 경계는 일반적으로 신뢰 구간 계산보다 넓은 반면, 언제든지 유효한 신뢰도는 고정 대상 기간 신뢰 계산보다 작습니다. 이 보수의 이점은 여러분이 항상 여러분의 결과를 안전하게 해석할 수 있다는 것이다.

## 실험에 결론이 있다고 선언

![](assets/experimentation_report_2.png)

실험 보고서를 볼 때마다 Adobe은 이 시점까지 실험에 누적된 데이터를 분석하고 항시 유효한 신뢰도가 적어도 하나의 처리에 대해 임계값 95%를 넘으면 실험을 &quot;결정적&quot;이라고 선언합니다.

이때 전환율 또는 프로필 표준화된 지표 값을 기반으로 가장 성과가 좋은 처리가 보고서 화면 맨 위에 강조 표시되고 테이블 형식 보고서에 별표로 표시됩니다. 기준선과 함께 95%보다 큰 신뢰도를 갖는 처리만이 이러한 결정에서 고려된다.

두 가지 이상의 치료법이 있을 때, 본페로니 수정 링크를 사용하여 여러 비교 문제를 수정하고, 가족 단위 오류율을 제어합니다. 이러한 시나리오에서, 신뢰도가 95%보다 크고 신뢰 구간이 겹치는 다수의 치료들이 존재할 수도 있다. 이 경우 Adobe Journey Optimizer은 전환율(또는 프로필 표준화된 지표 값)이 가장 높은 전환율을 최고의 수행자로 선언합니다.