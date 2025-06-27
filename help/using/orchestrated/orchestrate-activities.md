---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 구축하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: f64fa51fa753fe62eecb6199946615f4d5c4f767
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 2%

---

# 캠페인 활동 오케스트레이션 {#orchestrate}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/><b>[활동 오케스트레이션](orchestrate-activities.md)</b><br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[오케스트레이션된 캠페인을 만들었다면](gs-campaign-creation.md) 오케스트레이션된 캠페인 메뉴에서 또는 캠페인 내에서 수행할 다양한 작업을 오케스트레이션할 수 있습니다. 이를 위해 오케스트레이션된 캠페인 다이어그램을 구성할 수 있는 시각적 캔버스가 제공됩니다. 이 다이어그램 내에서 다양한 활동을 추가하고 순차적 순서로 연결할 수 있습니다.

## 활동 추가 {#add}

이 구성 단계에서 다이어그램은 오케스트레이션된 캠페인의 시작을 나타내는 시작 아이콘과 함께 표시됩니다. 첫 번째 활동을 추가하려면 시작 아이콘에 연결된 **+** 단추를 클릭합니다.

다이어그램에 추가할 수 있는 활동 목록이 나타납니다. 사용 가능한 활동은 오케스트레이션된 캠페인 다이어그램 내의 위치에 따라 다릅니다. 예를 들어 첫 번째 활동을 추가할 때 대상을 타겟팅하거나, 오케스트레이션된 캠페인 경로를 분할하거나, **대기** 활동을 설정하여 오케스트레이션된 캠페인 실행을 지연시킬 수 있습니다. 반면 **대상자 작성** 활동 후에는 타깃팅 활동을 통해 대상을 세분화하고, 채널 활동을 통해 대상자에게 게재를 보내거나, 흐름 제어 활동을 통해 오케스트레이션된 캠페인 프로세스를 구성할 수 있습니다.

![](assets/orchestrated-start.png){zoomable="yes"}

활동이 다이어그램에 추가되면 특정 설정으로 새로 추가된 활동을 구성할 수 있는 오른쪽 창이 나타납니다. 각 활동을 구성하는 방법에 대한 자세한 내용은 [이 섹션](activities/about-activities.md)에서 확인할 수 있습니다.

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

이 프로세스를 반복하여 오케스트레이션된 캠페인에서 수행하려는 작업에 따라 원하는 만큼 활동을 추가합니다. 두 활동 사이에 새 활동을 삽입할 수도 있습니다. 이렇게 하려면 활동 간 전환에서 **+** 단추를 클릭하고 원하는 활동을 선택한 다음 오른쪽 창에서 구성합니다.

활동을 제거하려면 캔버스에서 활동을 선택하고 활동 속성에서 **삭제** 아이콘을 클릭하십시오.

>[!TIP]
>
>각 활동 간에 전환의 이름을 개인화할 수 있습니다. 이렇게 하려면 전환을 선택하고 오른쪽 창에서 해당 레이블을 변경합니다.

## 도구 모음 {#toolbar}

캔버스의 오른쪽 위 모서리에 있는 도구 모음은 활동을 쉽게 조작하고 캔버스에서 탐색할 수 있는 옵션을 제공합니다.

* **여러 선택 모드**: 여러 활동을 선택하여 한꺼번에 삭제하거나 복사하여 붙여 넣으십시오. [이 섹션](#copy)을 참조하십시오.
* **회전**: 캔버스를 세로로 전환합니다.
* **화면에 맞춤**: 캔버스 확대/축소 수준을 화면에 맞춥니다.
* **축소** / **확대**: 캔버스를 축소하거나 확대합니다.
* **맵 표시**: 현재 위치를 보여 주는 캔버스의 스냅숏을 엽니다.

![](assets/orchestrated-toolbar.png){zoomable="yes"}{width="50%"}

## 활동 관리 {#manage}

활동을 추가할 때 속성 창에서 작업 버튼을 사용할 수 있으므로 여러 작업을 수행할 수 있습니다.

![](assets/activity-action.png){zoomable="yes"}

다음과 같은 작업을 수행할 수 있습니다.

* 캔버스에서 활동을 **삭제**&#x200B;합니다.
* 활동을 **사용 안 함/사용**&#x200B;합니다. 오케스트레이션된 캠페인이 실행되면 비활성화된 활동 및 동일한 경로의 다음 활동이 실행되지 않고 오케스트레이션된 캠페인이 중지됩니다.
* 활동을 **일시 중지/다시 시작**&#x200B;합니다. 오케스트레이션된 캠페인이 실행되면 일시 중지된 활동에서 일시 중지됩니다. 동일한 경로에서 해당 작업을 따르는 모든 작업은 실행되지 않습니다.
* 활동을 **복사**&#x200B;합니다. [이 섹션](#copy)을 참조하십시오.
* 활동의 **로그 및 작업**&#x200B;에 액세스합니다.

**결합** 또는 **중복 제거**&#x200B;와 같은 여러 **타깃팅** 활동을 사용하면 나머지 모집단을 처리하고 추가 아웃바운드 전환에 포함할 수 있습니다. 예를 들어, **Split** 활동을 사용하는 경우, 보수는 이전에 정의된 하위 집합과 일치하지 않는 모집단으로 구성됩니다. 이 기능을 사용하려면 **보조 항목 생성** 옵션을 활성화하세요.

## 활동 이동 또는 복사 {#move-copy}

### 활동 복사/붙여넣기 {#copy}

오케스트레이션된 캠페인 활동을 복사하여 워크플로우에 붙여넣을 수 있습니다. 오케스트레이션된 대상 캠페인은 다른 브라우저 탭에 있을 수 있습니다.

활동을 복사하려면 두 가지 선택 사항이 있습니다.

* 작업 버튼을 사용하여 활동 하나를 복사합니다.

  ![](assets/orchestrated-copy-1.png){zoomable="yes"}{width="70%"}

* 도구 모음 버튼을 사용하여 여러 활동을 복사합니다.

  ![](assets/orchestrated-copy-2.png){zoomable="yes"}{width="70%"}

복사된 활동을 붙여넣으려면 전환에서 **+** 단추를 클릭하고 &quot;X 활동 붙여넣기&quot;를 선택합니다.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

<!--
### Move activities and their child nodes {#move}

Journey Optimizer allows you to move an activity, along with the entire content of its child nodes (including all transitions and activities within it) to the end of another transition within the same orchestrated campaign.

This process disconnects the activity and everything in its outbound transition from the initial location, moving it to the new target transition.

To move an activity:

1. Select the activity you wish to move.
1. In the activity's properties pane, click the **Move** button.
1. Select the transition where you want to place the activity and its outbound transition, then confirm.

![](assets/activity-move.png)


## Execution options {#execution}

All activities allow you to manage their execution options. Select an activity and click on the **Execution options** button. This lets you define the activity's execution mode and behavior in case of errors.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}


### Properties

The **Execution** field allows you to define the action to be carried out when the task is started.

The **Maximum execution duration** field allows you to specify a duration such as "30s" or "1h". If the activity is not finished after the duration specified has been elapsed, an alert is triggered. This has no impact on how the orchestrated campaign functions.

The **Time zone** field allows you to select the time zone of the activity. Adobe Journey Optimizer allows you to manage the time differences between multiple countries on the same instance. The setting applied is configured when the instance is created.

**The Affinity** field allows you to force an orchestrated campaign or an orchestrated campaign activity to execute on a particular machine. To do this, you must specify one or several affinities for the orchestrated campaign or activity in question.

The **Behavior** field allows you to define the procedure to follow if asynchronous tasks are used.

### Error management

The **In case of error** field allows you to specify the action to be carried out should the activity encounter an error.

### Initialization script

The **Initialization script** lets you initialize variables or modify activity properties. Click the **Edit code** button and type the snippet of code to execute. The script is called when the activity executes. 

## Example {#example}

Here is an orchestrated campaign example designed to send an email to all customers (other than VIP customers) with an email who are interested in coffee machines.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

To achieve this, activities below have been added:

* A **[!UICONTROL Fork]** activity that divides the orchestrated campaign into three paths (one for each set of customer),
* **[!UICONTROL Build audience]** activities to target the three sets of customers:

    * Customers with an email,
    * Customers belonging to the pre-existing "Interrested in Coffee Machine(s)" audience,
    * Customers belonging to the pre-existing "VIP ro reward" audience.

* A **[!UICONTROL Combine]** activity that groups together customers with an email and those interested in coffee machines,
* A **[!UICONTROL Combine]** activity that excludes VIP customers,
* An **[!UICONTROL Email delivery]** activity that sends an email to the resulting customers. 

Once you have completed the orchestrated campaign, add en **[!UICONTROL End]** activity at the end of the diagram. This activity allow you to visually mark the end of a workflow and has no functional impact.

After successfully designing the orchestrated campaign diagram, you can execute the orchestrated campaign and track the progress of its various tasks. [Learn how to start an orchestrated campaign and monitor its execution](start-monitor-campaigns.md)
-->