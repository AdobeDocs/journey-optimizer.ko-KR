---
solution: Journey Optimizer
product: journey optimizer
title: 여정 종료
description: Journey Optimizer에서 여정이 어떻게 종료되는지 알아보십시오
feature: Journeys
role: User
level: Beginner
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# 여정 종료{#journey-ending}

여정은 두 개의 특정 컨텍스트에서 개인에 대해 종료될 수 있습니다.

* 사람이 경로의 마지막 활동에 도달합니다.
* 사람이 도착합니다 **조건** 활동(또는 **대기** 활동(조건 포함)과 일치하지 않습니다.

그런 다음 다시 입장할 수 있는 경우 여정을 다시 시작할 수 있습니다. 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md#change-properties)

라이브 여정을 종료하려면 여정을 종료하는 것이 좋습니다. 그러면 새로운 손님들의 여정이 차단됩니다. 이미 여정에 들어온 고객은 처음부터 끝까지 경험할 수 있습니다. 자세한 내용은 [이 섹션](../building-journeys/journey.md#close-journey)

응급상황이 발생하고 모든 처리를 여정에서 즉시 종료해야 하는 경우에만 여정을 중지할 수 있습니다. 이미 여정을 시작한 사람들은 모두 진행 중에 멈춥니다. 자세한 내용은 [이 섹션](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>닫힌 여정 또는 중지된 여정은 재개할 수 없습니다.

## 여정 끝 태그{#end-tag}

여정을 작성하는 동안 각 경로의 끝에 &quot;끝 태그&quot;가 표시됩니다. 이 노드는 사용자가 추가할 수 없으며 제거할 수 없으며 해당 레이블만 변경할 수 있습니다. 여정의 각 경로의 끝을 표시합니다. 여정에 여러 경로가 있는 경우 보고서를 쉽게 읽을 수 있도록 각 끝에 레이블을 추가하는 것이 좋습니다. 자세한 내용은 [이 페이지](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## 여정 닫기{#close-journey}

다음과 같은 이유로 여정이 닫을 수 있습니다.

* 여정은 를 통해 수동으로 닫힙니다 **[!UICONTROL Close to new entrances]** 버튼을 클릭합니다.
* 실행이 완료된 원샷 세그먼트 기반 여정.
* 반복 세그먼트 기반 여정의 마지막 발생 이후.

여정을 수동으로 종료하면 이미 여정에 들어온 고객이 경로를 완료할 수 있지만 새 사용자가 여정에 들어갈 수 없게 됩니다. 여정이 닫히면(위의 이유 중 하나) 상태가 됩니다 **[!UICONTROL Closed]**. 이 여정은 새로운 개인이 여정을 시작할 수 있도록 하는 것을 중지합니다. 이미 여행 중인 사람은 정상적으로 여정을 완료할 수 있습니다. 기본 글로벌 시간 초과 30일 이후에는 여정이 **완료됨** 상태. 다음 보기 [섹션](../building-journeys/journey-gs.md#global_timeout).

닫힌 여정 버전은 다시 시작하거나 삭제할 수 없습니다. 새 버전을 만들거나 복제할 수 있습니다. 완료된 여정도 삭제할 수 있습니다.

여정 목록에서 여정을 닫으려면 **[!UICONTROL Ellipsis]** 여정 이름의 오른쪽에 있는 버튼을 선택하고 **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

다음을 수행할 수도 있습니다.

1. 에서 **[!UICONTROL Journeys]** 목록에서 닫을 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.

   ![](assets/finish_drop_down_list.png)

1. 클릭 **[!UICONTROL Close to new entrances]**, 그리고 대화 상자에서 확인합니다.

## 여정 중지{#stop-journey}

여정에 있는 모든 개인의 진행 상황을 중지해야 하는 경우 중지할 수 있습니다. 여정을 중지하면 여정에 있는 모든 개인이 시간 초과됩니다. 하지만 여정을 멈추는 것은 이미 여정에 들어온 모든 사람들이 진행 중에 중지된다는 것을 포함합니다. 여정은 기본적으로 꺼져 있습니다. 여정을 종료하려면 여정을 닫는 것이 좋습니다.

중지된 여정 버전을 다시 시작할 수 없습니다.

중지되면 여정 상태가 (으)로 설정됩니다 **[!UICONTROL Stopped]**.

예를 들어 마케터가 여정이 잘못된 대상을 타깃팅하거나 메시지를 전달해야 하는 사용자 지정 작업이 제대로 작동하지 않는 것을 알고 여정을 중지할 수 있습니다. 여정 목록에서 여정을 중지하려면 **[!UICONTROL Ellipsis]** 여정 이름의 오른쪽에 있는 버튼을 선택하고 **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

다음을 수행할 수도 있습니다.

1. 에서 **[!UICONTROL Journeys]** 목록에서 중지할 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.
   ![](assets/finish_drop_down_list.png)
1. 클릭 **[!UICONTROL Stop]**, 그리고 대화 상자에서 확인합니다.
