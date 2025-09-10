---
solution: Journey Optimizer
product: journey optimizer
title: 여정 보고서
description: 여정 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 30d4f967-e085-44f1-973d-11e79f693e6e
source-git-commit: 158d9d9a1070e1d842183e5bd6cb5ce8e38834c5
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 1%

---

# 여정 보고서 {#journey-global-report}

**여정 보고서**&#x200B;는 여정과 관련된 필수 지표에 대한 분석을 제공하는 모든 기능을 포함하는 대시보드로 작동합니다. 여기에는 입력된 프로필 수 및 실패한 개별 여정의 인스턴스 등 세부 정보가 포함되며, 이를 통해 여정의 효율성 및 참여 수준에 대한 포괄적인 insight을 제공합니다.

**보고서 보기** 단추를 사용하면 여정에서 **[!UICONTROL 여정 보고서]**&#x200B;에 직접 액세스할 수 있습니다.

![](assets/gs-cja-report-3.png)

Customer Journey Analytics Workspace과 데이터를 필터링하고 분석하는 방법에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home)를 참조하세요.

## 여정 개요 {#journey-global}

**[!UICONTROL 여정]** 보고서를 통해 여정에 대한 가장 중요한 추적 데이터를 명확하게 볼 수 있습니다.

### 여정 KPI {#journey-perfomance}

![](assets/cja-journey-kpis.png)

**[!UICONTROL 여정]** 주요 성과 지표(KPI)는 모든 것을 포괄하는 대시보드로 작동하여 여정과 관련된 필수 지표에 대한 분석을 제공합니다. 여기에는 입력된 프로필 수 및 실패한 개별 여정 인스턴스 등의 세부 정보가 포함되며, 이를 통해 여정의 효율성 및 참여 수준에 대한 포괄적인 insight을 제공할 수 있습니다.

+++ 여정 KPI 지표에 대해 자세히 알아보기

* **[!UICONTROL 여정 참여]**: 여정에서 보낸 메시지를 받은 총 고유 개인 수로, 여정에서 지정된 작업 지점에 도달한 고유한 프로필을 나타냅니다.

* **[!UICONTROL 여정 입력]**: 여정의 시작 이벤트에 도달한 총 개인 수입니다.

* **[!UICONTROL 여정 종료]**: 여정을 종료한 총 개인 수

+++

### 여정 통계 {#journey-stats}

![](assets/cja-journey-stats.png)

**[!UICONTROL 여정 통계]** 표에는 여정에 대한 중요한 데이터에 대한 자세한 요약이 있습니다. 여기에는 실패 및 성공 항목 수와 같은 주요 지표가 포함되어 있어 이메일과 여정의 성능과 도달에 대한 중요한 통찰력을 제공합니다.

+++ 여정 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 여정 제외]**: 사전 정의된 기준이나 제외 규칙으로 인해 여정에서 제외된 총 개인 수.

* **[!UICONTROL 여정 참여]**: 여정에서 보낸 메시지를 받은 총 고유 개인 수로, 여정에서 지정된 작업 지점에 도달한 고유한 프로필을 나타냅니다.

* **[!UICONTROL 여정 입력]**: 여정의 시작 이벤트에 도달한 총 개인 수입니다.

* **[!UICONTROL 여정 종료]**: 여정을 종료한 총 개인 수

* **[!UICONTROL 여정 실패]**: 실행되지 않은 총 개별 여정 수입니다.

* **[!UICONTROL 고유 여정 입력]**: 여정의 시작 이벤트에 도달한 개인 총 수, 한 프로필의 여러 상호 작용을 고려하지 않습니다.

* **[!UICONTROL 고유 여정 종료]**: 여정을 종료한 총 개인 수, 한 프로필의 여러 상호 작용을 고려하지 않습니다.

* **[!UICONTROL 고유 여정 실패]**: 실행되지 않은 개별 여정의 총 수입니다. 한 프로필의 여러 상호 작용은 고려되지 않습니다.

+++

## 여정 제외 {#journey-exclusion}

**[!UICONTROL 여정 제외]** 표에는 사용자 프로필을 제외하는 다양한 요인에 대한 포괄적인 보기가 표시됩니다.

## 액션 오류 {#action-error}

![](assets/cja-journey-action-error.png)

**[!UICONTROL 작업 오류]** 위젯에서는 여정 작업에 대해 발생한 다양한 오류를 자세히 설명합니다.

## 여정 캔버스 {#journey-canvas}

![](assets/cja-journey-canvas.png)

**[!UICONTROL 여정 캔버스]** 위젯을 사용하면 타겟팅된 프로필이 여정을 탐색할 때의 궤적을 시각적으로 추적할 수 있습니다. [Customer Journey Analytics 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

다음 옵션을 사용하여 캔버스 사용자 지정을 개선합니다.

* **[!UICONTROL 노드 유형]** 드롭다운 메뉴에서 원하는 활동 유형(예: 메시지 또는 조건)을 추가하거나 제거합니다.
* **[!UICONTROL 백분율 값]**&#x200B;을(를) 조정하여 다른 여정 경로 간의 흐름 분포를 결정합니다.
* 레이블, 조건을 포함하거나 깔끔한 표시를 선택하도록 **[!UICONTROL 화살표 설정]**&#x200B;을(를) 사용자 지정합니다.
* **[!UICONTROL 폴아웃 표시]** 옵션을 활성화하여 캔버스에서 직접 여정을 종료한 프로필을 시각화하십시오.

**[!UICONTROL 노드 유형]** 필터링을 사용할 때 다음 규칙이 적용됩니다.

* 노드에서 여정을 만들 때 해당 노드가 **[!UICONTROL 노드 유형]** 필터를 통해 제외된 경우에도 세그먼트의 이전 단계의 노드를 포함합니다.

* **[!UICONTROL 여정 형식]** 필터를 통해 노드의 이전 단계에 있는 노드가 제외된 경우 화살표로 구성된 세그먼트를 만들 수 없습니다. 이 경우 해당 화살표에서 마우스 오른쪽 버튼 클릭 기능이 비활성화됩니다.

## 액션 성능 {#action-performance}

### 시간에 따른 성능 {#action-overtime}

![](assets/cja-journey-action-performance.png)

**[!UICONTROL 시간 경과에 따른 성능]** 그래프를 사용하면 작업의 대상 프로필로 간주되는 기준을 충족하는 프로필 수를 식별하고 분석할 수 있습니다. 이 시각화는 전략의 효과에 대한 중요한 통찰력을 제공하고 성능을 최적화하기 위해 데이터 기반의 결정을 내리는 데 도움이 됩니다.

### 작업 개요 {#action-overview}

![](assets/cja-journey-action-overview.png)

**[!UICONTROL 작업 개요]** 테이블은 포괄적인 대시보드 역할을 하며 여정의 작업과 관련된 주요 지표를 분석할 수 있도록 합니다. 여기에는 상호 작용 횟수 및 클릭스루 비율 등 중요한 세부 정보가 포함됩니다

+++ 작업 개요 지표에 대해 자세히 알아보기

* **[!UICONTROL 노드 입력]**: 여정 내의 특정 노드에 입력한 총 개인 수입니다.

* **[!UICONTROL 여정 실패]**: 실행되지 않은 총 개별 여정 수입니다.

* **[!UICONTROL 클릭스루 비율]**: 작업과 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL 클릭 수]**: 작업에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 작업 수와 관련하여 보낸 작업 수입니다.

+++

## 이벤트 성능 {#events-performance}

### 시간에 따른 성능 {#event-overtime}

![](assets/cja-journey-performance-event.png)

**[!UICONTROL 시간 경과에 따른 성능]** 그래프를 통해 이벤트의 대상 프로필로 적합한 프로필의 수를 식별하고 분석할 수 있습니다. 이 강력한 도구는 시간 경과에 따른 트렌드 및 패턴을 추적하는 데 도움이 되며 이벤트 전략을 최적화하는 데 유용한 통찰력을 제공합니다.

### 이벤트 개요 {#event-overview}

![](assets/cja-journey-events-overview.png)

**[!UICONTROL 이벤트 개요]** 표는 시간 경과에 따라 이벤트 기준을 충족하는 프로필의 수를 보여줍니다. 이 도구를 사용하면 자격률의 패턴을 식별하여 이벤트 전략을 구체화할 수 있습니다.

+++ 여정 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 사람]**: 이벤트의 대상 프로필로 적합한 사용자 프로필 수입니다.

+++

## 타깃팅 개요 {#targeting}

![](assets/cja-journey-targeting-overview.png)

콘텐츠에 대해 **[!UICONTROL 타깃팅 규칙]**&#x200B;을(를) 설정하는 경우 **[!UICONTROL 타깃팅 개요]** 표에는 각 규칙의 타깃팅된 프로필이 콘텐츠와 상호 작용하는 방법을 보여 주는 주요 참여 지표에 대한 자세한 보기가 제공됩니다.

➡️ [타깃팅 규칙에 대해 자세히 알아보기](../campaigns/campaigns-message-optimization.md)

+++ 타겟팅 개요 지표에 대해 자세히 알아보기

* **[!UICONTROL 사람]**: 이벤트의 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 고유 클릭 수]**: 전자 메일의 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 고유 클릭률]**: 최소 한 번 이상 클릭한 대상 프로필의 비율입니다.

+++
