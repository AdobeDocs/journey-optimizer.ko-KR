---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Experimentation Accelerator 지표
description: 실험을 효과적으로 수행하고 통찰력을 생성할 수 있는 역량 향상
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 내용, 실험, 복수, 대상자, 처리
hide: true
hidefromtoc: true
exl-id: 74868625-f4ea-44f9-ae2a-8e5fdd22a081
source-git-commit: 70fce6fae4db58c72496945c50155dbd0b4986b4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 2%

---

# 지표 {#experiment-accelerator-metrics}

>[!BEGINSHADEBOX]

* [Journey Optimizer Experimentation Accelerator 시작](experiment-accelerator.md)
* [Journey Optimizer Experimentation Accelerator을 사용한 AI의 데이터 사용](experiment-accelerator-security.md)
* [Journey Optimizer Experimentation Accelerator 우수 사례](experiment-accelerator-best-practices.md)
* [실험 모니터링](experiment-accelerator-monitor.md)
* **[실험 지표](experiment-accelerator-metrics.md)**

>[!ENDSHADEBOX]

**[!UICONTROL 지표]** 페이지에는 Journey Optimizer 및 Target 실험의 성공 지표가 한 곳에 표시되어 성능 모니터링, 비교 및 더 자세한 통찰력을 사용할 수 있습니다.

## 대시보드 {#dashboard}

**[!UICONTROL 지표]** 탭에 액세스할 때 Journey Optimizer 및 Adobe Target에서 사용 가능한 모든 성공 지표가 통합 보기로 나열되므로 이니셔티브 간 성과를 추적하고, 결과를 비교하고, 주의가 필요한 영역을 신속하게 식별할 수 있습니다.

![](assets/do-not-localize/Smock_Filter_18_N.svg)Source **[!UICONTROL 또는]**&#x200B;활성 실험에 사용&#x200B;**[!UICONTROL 을 통한 필터링과 같은 컨텍스트별 옵션을 제공하는]**&#x200B;을(를) 클릭하여 필터에 액세스합니다.

또는 검색 막대에 지표의 이름을 입력하여 지표를 신속하게 찾을 수 있습니다.

![](assets/experiment-monitor-metrics.png)

## 지표 세부 정보 {#metric-details}

### 시간 경과에 따른 증분

![](assets/experiment-monitor-metrics-2.png)

**[!UICONTROL 시간 경과에 따른 증분]** 차트는 선택한 지표가 선택한 시간 범위에서 어떤 추세를 보이는지 시각적으로 분류합니다. 드롭다운 메뉴를 사용하여 일별 또는 주별 보기 간에 전환하여 세부 기간 수준을 조정합니다.

다음 요약 값을 빠른 참조에 사용할 수 있습니다.

* **[!UICONTROL 합계]**: 보고 기간 동안 선택한 지표의 누적 값입니다.

* **[!UICONTROL 평균]**: 선택한 시간 범위에서 계산된 지표의 일반적인 값입니다. 일별 또는 주별 변동을 균형 있게 조정함으로써 정상 성능의 보다 명확한 그림을 제공하고 비교 기준선으로 사용할 수 있다.

* **[!UICONTROL 전환율]**: 치료를 본 후 원하는 작업(예: 구매, 등록)을 완료한 프로필의 백분율입니다.

각 값은 이전 기간보다 백분율 변경이 포함되어 있어, 성과가 개선되고 있는지, 하락하고 있는지, 아니면 안정적으로 유지되고 있는지 쉽게 알 수 있습니다.

### 실험 효과

이 섹션에는 선택한 시간대(최근 90일, 최근 30일 또는 최근 7일) 내의 모든 활성 실험이 표시되고 지표에 대한 해당 기여도가 강조 표시됩니다.

다음 지표를 사용할 수 있습니다.

* **[!UICONTROL 상승도]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도]**: 해당 처리가 기준 처리와 동일하다는 증거입니다. [자세히 알아보기](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 기여도]**: 특정 실험 또는 처리에 기인할 수 있는 지표의 전체 변경 비율입니다. 이를 통해 상대적 영향이 가장 큰 이니셔티브를 식별할 수 있습니다.
