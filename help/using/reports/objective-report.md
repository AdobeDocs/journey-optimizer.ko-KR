---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 글로벌 보고서
description: Campaign 글로벌 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 4%

---

# 캠페인 글로벌 보고서 {#objective-report}

**[!UICONTROL 보고서 보기]** 단추를 사용하면 Campaign에서 Campaign 글로벌 보고서에 직접 액세스할 수 있습니다.

Campaign **[!UICONTROL 글로벌 보고서]**&#x200B;는 캠페인의 성공 및 오류를 자세히 설명하는 다양한 위젯으로 나뉩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 이 [섹션](../reports/global-report.md#modify-dashboard)을 참조하세요.

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 [이 페이지](global-report.md#list-of-components-global.md)를 참조하세요.

## 캠페인 탭 {#campaign-global-objectives}

### 게재 {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

**[!UICONTROL 캠페인 통계]** 위젯은 캠페인과 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 입력한 프로필]**: 여정을 시작한 프로필 수입니다.

* **[!UICONTROL 작업 전달됨]**: 여정에서 작업이 전달된 총 고유 횟수입니다.

* **[!UICONTROL 작업이 %]**&#x200B;에서 실패했습니다. 여정에서 작업이 실패한 총 고유 횟수와 작업이 전달된 총 고유 횟수를 비교합니다.

### 목표 보고서 {#objective-global}

>[!AVAILABILITY]
>
>**목표 보고서** 기능은 현재 조직 집합(제한된 가용성)에서만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

![](assets/performance_report.gif)

**[!UICONTROL 목표]** 탭을 사용하면 한 개의 특정 지표를 대상으로 하여 게재 보고서를 더 세밀하게 조정할 수 있습니다.

나열된 **[!UICONTROL Objectives]**&#x200B;은(는) 추가 정보를 검색하기 위해 시스템에 대한 연결을 정의하는 **[!UICONTROL 데이터 세트]**&#x200B;에 연결되어 있습니다. 기본 제공 **[!UICONTROL 목표]** 목록을 사용할 수 있지만 새 **[!UICONTROL 데이터 집합]**&#x200B;을(를) 추가하여 고유한 항목을 추가할 수 있습니다. 자세한 절차는 이 [섹션](../reports/reporting-configuration.md)을 참조하세요.

타깃팅할 목표를 선택한 후 두 **[!UICONTROL 성과 개요]** 및 **[!UICONTROL 캠페인 목표]** 위젯에서 게재 성과에 대한 자세한 요약을 제공합니다.

**[!UICONTROL 캠페인 목표]** 위젯을 사용하여 기본 목표와 다른 지표를 비교하도록 선택할 수도 있습니다.

### 실험 보고서 {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

**[!UICONTROL 실험]** 탭은 각 변형의 성능에 대한 주요 인사이트를 제공하며 가장 성공적인 변형을 식별합니다.

최상의 수행자를 정의하는 데 시간이 걸릴 수 있습니다. 이 아이콘은 ![](assets/experimentation_report_1.png)(으)로 표시됩니다.

+++실험 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

**[!UICONTROL 실험 결과]** 위젯은 각 변형의 성능을 자세히 설명합니다. 드롭다운에서 **[!UICONTROL 기준선]**&#x200B;에서 처리 중 하나를 선택하여 기준선을 변경할 수 있습니다. 최고의 치료법은 별 모양 아이콘으로 표시됩니다.

이 표에는 다음 지표가 나와 있습니다.

* **[!UICONTROL 기준선에 대한 상승도]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 고유 아웃바운드 클릭수]**: 아웃바운드 채널의 총 클릭수.

* **[!UICONTROL 프로필]**: 이 처리의 대상으로 지정된 프로필 수입니다.

* **[!UICONTROL 고유 아웃바운드 클릭수/프로필]**: 실험을 만들 때 이전에 선택한 성공 지표의 총 값을 프로필 수로 나눈 값입니다.

**[!UICONTROL 신뢰 구간]** 그래프는 개선과 관련된 불확실성을 측정합니다. 기준 처리와 최상의 성능 처리 사이의 성능 차이를 백분율로 자세히 설명합니다. [자세히 알아보기](../content-management/experiment-calculations.md#confidence-intervals).
+++

이러한 결과와 이를 해석하는 방법에 대한 자세한 내용은 [이 페이지](../content-management/get-started-experiment.md#interpret-results)를 참조하세요.
