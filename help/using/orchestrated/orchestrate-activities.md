---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 구축하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 1%

---

# 캠페인 활동 오케스트레이션 {#orchestrate}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/><b>[활동 오케스트레이션](orchestrate-activities.md)</b><br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[오케스트레이션된 캠페인을 만들었다면](gs-campaign-creation.md), 수행할 다양한 작업을 오케스트레이션할 수 있습니다. 이를 위해 오케스트레이션된 캠페인 다이어그램을 구성할 수 있는 시각적 캔버스가 제공됩니다. 이 다이어그램 내에서 다양한 활동을 추가하고 순차적 순서로 연결할 수 있습니다.

## 활동 추가 {#add}

이 구성 단계에서 다이어그램은 오케스트레이션된 캠페인의 시작을 나타내는 시작 아이콘과 함께 표시됩니다. 첫 번째 활동을 추가하려면 시작 아이콘에 연결된 **+** 단추를 클릭합니다.

다이어그램에 추가할 수 있는 활동 목록이 나타납니다. 사용 가능한 활동은 오케스트레이션된 캠페인 다이어그램 내의 위치에 따라 다릅니다. 예를 들어 첫 번째 활동을 추가할 때 대상을 타겟팅하거나, 오케스트레이션된 캠페인 경로를 분할하거나, **대기** 활동을 설정하여 오케스트레이션된 캠페인 실행을 지연시킬 수 있습니다. 반면 **대상자 작성** 활동 후에는 타깃팅 활동을 통해 대상을 세분화하고, 채널 활동을 통해 대상자에게 게재를 보내거나, 흐름 제어 활동을 통해 오케스트레이션된 캠페인 프로세스를 구성할 수 있습니다.

![](assets/orchestrated-start.png){zoomable="yes"}

활동이 다이어그램에 추가되면 특정 설정으로 활동을 구성할 수 있는 오른쪽 창이 나타납니다. 각 활동을 구성하는 방법에 대한 자세한 내용은 [이 섹션](activities/about-activities.md)에서 확인할 수 있습니다.

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

이 프로세스를 반복하여 오케스트레이션된 캠페인에서 수행하려는 작업에 따라 원하는 만큼 활동을 추가합니다. 두 활동 사이에 새 활동을 삽입할 수도 있습니다. 이렇게 하려면 활동 간 전환에서 **+** 단추를 클릭하고 원하는 활동을 선택한 다음 오른쪽 창에서 구성합니다.

각 활동 간에 전환의 이름을 개인화할 수 있습니다. 이렇게 하려면 전환을 선택하고 오른쪽 창에서 해당 레이블을 변경합니다.

![](assets/canvas-transition.png)

### 캔버스 도구 모음 {#toolbar}

캔버스 도구 모음에서는 활동을 쉽게 조작하고 캔버스에서 탐색할 수 있는 옵션을 제공합니다.

![](assets/orchestrated-toolbar.png)

![여러 선택 모드 아이콘](assets/do-not-localize/canvas-multiple.svg) 여러 활동을 선택하여 한 번에 모두 삭제하거나 복사하여 붙여 넣으십시오. [활동을 복사하여 붙여 넣는 방법 알아보기](#copy)

![회전 아이콘](assets/do-not-localize/canvas-rotate.svg) 캔버스를 세로로 전환합니다.

![화면 아이콘에 맞춤](assets/do-not-localize/canvas-fit.svg) 캔버스 확대/축소 수준을 화면에 적용합니다.

![축소 아이콘](assets/do-not-localize/canvas-zoomout.svg) ![확대 아이콘](assets/do-not-localize/canvas-zoomin.svg) 축소 또는 캔버스

![캠페인 설정 아이콘](assets/do-not-localize/canvas-map.svg) 현재 위치를 보여 주는 캔버스의 스냅숏을 엽니다.

### 활동 관리 {#manage}

활동을 추가할 때 속성 창에서 작업 버튼을 사용할 수 있으므로 여러 작업을 수행할 수 있습니다.

![](assets/activity-action.png)

![삭제 아이콘](assets/do-not-localize/activity-delete.svg) 캔버스에서 활동을 삭제합니다.

![아이콘 비활성화](assets/do-not-localize/activity-disable.svg) ![아이콘 활성화](assets/do-not-localize/activity-enable.svg) 활동을 비활성화/활성화합니다. 오케스트레이션된 캠페인이 실행되면 비활성화된 활동 및 동일한 경로의 다음 활동이 실행되지 않고 오케스트레이션된 캠페인이 중지됩니다.

![일시 중지 아이콘](assets/do-not-localize/activity-pause.svg) ![다시 시작 아이콘](assets/do-not-localize/activity-resume.svg) 활동을 일시 중지/다시 시작합니다. 오케스트레이션된 캠페인이 실행되면 일시 중지된 활동에서 일시 중지됩니다. 동일한 경로에서 해당 작업을 따르는 모든 작업은 실행되지 않습니다.

![복사 아이콘](assets/do-not-localize/activity-copy.svg) 활동을 복사합니다. [활동을 복사하여 붙여 넣는 방법 알아보기](#copy)

![로그 및 작업 아이콘](assets/do-not-localize/activity-logs.svg) 활동의 로그 및 작업에 액세스합니다.

**결합** 또는 **중복 제거**&#x200B;와 같은 여러 **타깃팅** 활동을 사용하면 나머지 모집단을 처리하고 추가 아웃바운드 전환에 포함할 수 있습니다. 예를 들어, **Split** 활동을 사용하는 경우, 보수는 이전에 정의된 하위 집합과 일치하지 않는 모집단으로 구성됩니다. 이 기능을 사용하려면 **[!UICONTROL 보조 항목 생성]** 옵션을 활성화하세요.

### 활동 복사/붙여넣기 {#copy}

활동을 복사하여 오케스트레이션된 캠페인 캔버스에 붙여넣을 수 있습니다. 대상 캠페인은 다른 브라우저 탭에 있을 수 있습니다.

* 활동 하나를 복사하려면 활동 속성 창에서 ![복사 아이콘](assets/do-not-localize/activity-copy.svg) 단추를 클릭하십시오.
* 여러 활동을 복사하려면 캔버스 도구 모음에서 ![다중 선택 모드 아이콘](assets/do-not-localize/canvas-multiple.svg) 아이콘을 클릭합니다.

| 활동 하나 복사 | 여러 활동 복사 |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

활동을 붙여넣으려면 전환에서 **+** 단추를 클릭하고 &quot;x 활동 붙여넣기&quot;를 선택합니다.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## 다이어그램 예 {#example}

다음은 최소 100$의 구매를 한 모든 고객에게 이메일을 보내는 반면 충성도 점수가 50점 미만인 모든 고객은 제외하도록 설계된 오케스트레이션된 캠페인 예입니다.

![](assets/canvas-example-diagram.png){zoomable="yes"}

이를 위해 아래 활동이 추가되었습니다.

* **[!UICONTROL 포크]** 활동은 오케스트레이션된 캠페인을 세 개의 경로로 나눕니다.
* **[!UICONTROL 대상자 만들기]** 활동은 세 고객 집합을 대상으로 합니다.

   * 이메일이 있는 고객,
   * 최소 100$의 구매를 한 고객,
   * 단골 포인트가 50개 미만인 고객

* **[!UICONTROL Combine]** 활동 그룹은 이메일이 있는 고객과 최소 100$ 이상의 구매를 한 고객을 함께 그룹화합니다.
* **[!UICONTROL 결합]** 활동은 충성도 점수가 50점 미만인 고객을 제외합니다.
* **[!UICONTROL 이메일 게재]** 활동에서 결과 고객에게 이메일을 보냅니다.

## 다음 단계 {#next}

오케스트레이션된 캠페인 다이어그램을 성공적으로 디자인한 후 오케스트레이션된 캠페인을 실행하고 다양한 작업의 진행 상황을 추적할 수 있습니다. [오케스트레이션된 캠페인을 시작하고 실행을 모니터링하는 방법을 알아보세요](start-monitor-campaigns.md)
