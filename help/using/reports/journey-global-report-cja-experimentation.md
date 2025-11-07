---
solution: Journey Optimizer
product: journey optimizer
title: 여정 실험 보고서
description: 여정 보고서에서 실험 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a2b4ef74-96a9-4907-ba70-7aee69e45f20
source-git-commit: 45ebae048a748429a1918326526f3756a3e93c4c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 2%

---

# 실험 여정 보고서 {#campaign-global-report-cja-experimentation}

여정 보고서는 실험의 효과를 이해하는 데 필요한 주요 지표와 함께 실험의 성과를 전체적으로 볼 수 있습니다.

Journey Optimizer에서 여정 실험은 두 가지 유형으로 나뉩니다.

* [콘텐츠 실험](../content-management/content-experiment.md)

  콘텐츠 실험에 대해 자세히 설명된 테이블 및 KPI는 경로 실험에 대한 테이블과 동일합니다. 콘텐츠 실험을 설정한 경우 아래 [설명서](#experimentation)를 참조하세요.

* [경로 실험](../building-journeys/optimize.md)

## 경로 실험 {#experimentation}

### 실험 KPI {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

**실험 요약**&#x200B;은(는) 실험의 성과에 대한 주요 통찰력을 제공하고 가장 성공적인 실험을 식별합니다. 최상의 수행자를 정의하는 데 약간의 시간이 걸릴 수 있습니다. 실험이 성공하지 못하면 **결론이 나지 않습니다**.

**실험 주요 성과 지표(KPI)**&#x200B;는 모든 것을 포괄하는 대시보드로 작동하여 실험과 관련된 필수 지표에 대한 분석을 제공합니다.

+++ 실험 KPI 지표에 대해 자세히 알아보기

* **[!UICONTROL 상승도]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#understand-confidence)

+++



### 성공 지표별 변형 {#variant-inbound}

![](assets/cja-experimentation-variants.png)

**성공 메트릭별 변형** 표는 실험을 설정할 때 선택한 성공 메트릭을 기반으로 각 변형이 수행되는 방식을 보여 줍니다.
이러한 결과와 이를 해석하는 방법에 대한 자세한 내용은 [이 페이지](../content-management/get-started-experiment.md#interpret-results)를 참조하세요.

+++ 성공 지표별 변형에 대해 자세히 알아보기

* **[!UICONTROL 사람]**: 메시지 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 인바운드 클릭수]**: 실험을 만들 때 이전에 선택한 성공 지표의 총 값입니다.

* **[!UICONTROL 전환율]**: 실험을 만들 때 이전에 선택한 성공 지표의 총 값을 프로필 수로 나눈 값입니다.

* **[!UICONTROL 상승도]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도 하한]**: 선택한 신뢰 구간 내에서 처리와 기준선 간의 전환율 차이에 대한 가장 낮은 예상 값입니다.

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 신뢰도 상한값]**: 선택한 신뢰 구간 내에서 처리와 기준선 간의 전환율 차이에 대한 가장 높은 예상값입니다.

+++

### 성공 지표에 대한 전환율 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

**[!UICONTROL 신뢰 구간]** 그래프는 선택한 성공 지표에 대해 기준선과 가장 성과가 좋은 처리를 비교하여 가능한 개선 범위를 보여 줍니다. [자세히 알아보기](../content-management/experiment-calculations.md#confidence-intervals).
