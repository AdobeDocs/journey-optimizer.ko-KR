---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 보고서
description: 캠페인 보고서에서 실험 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---


# 실험 캠페인 보고서 {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="성공 지표"
>abstract="실험 생성 시 이전에 선택한 성공 지표의 합계 값을 프로필 수로 나눈 값입니다."

## 실험 {#experimentation}

**[!UICONTROL 실험]** 탭은 각 변형의 성능에 대한 주요 인사이트를 제공하며 가장 성공적인 변형을 식별합니다.

최상의 수행자를 정의하는 데 약간의 시간이 걸릴 수 있습니다. 실험이 성공하지 못하면 **결론이 나지 않습니다**.

![](assets/cja-experimentation-1.png)

### 실험 KPI {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

**[!UICONTROL 실험]** 주요 성과 지표(KPI)는 모든 것을 포괄하는 대시보드로 작동하여 실험과 관련된 필수 지표에 대한 분석을 제공합니다.

+++ 실험 KPI 지표에 대해 자세히 알아보기

* **[!UICONTROL 상승도]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

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

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL 신뢰도 상한값]**: 선택한 신뢰 구간 내에서 처리와 기준선 간의 전환율 차이에 대한 가장 높은 예상값입니다.

+++

### 성공 지표에 대한 전환율 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)


**[!UICONTROL 신뢰 구간]** 그래프는 선택한 성공 지표에 대해 기준선과 가장 성과가 좋은 처리를 비교하여 가능한 개선 범위를 보여 줍니다. [자세히 알아보기](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).