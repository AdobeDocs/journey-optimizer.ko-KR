---
title: 여정 종료
description: 여정 종료
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 57bdeadc-5801-4036-a272-c622634d5281
source-git-commit: d740b9efdba164f548fb07d6d9a96fc2c2796eff
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 2%

---

# 여정 라이프사이클{#journey-lifecyle}

## 여정의 프로필{#profile-journey}

단일 여정:

* 재시작이 활성화된 경우, 프로필은 여러 번 여정을 입력할 수 있지만, 해당 여정의 이전 인스턴스를 완전히 종료한 후에는 해당를 수행할 수 없습니다.

* 다시 입장할 수 없는 경우 프로필은 동일한 여정의 여러 번 입력할 수 없습니다

프로필 재시작에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../building-journeys/journey-gs.md#change-properties).

세그먼트 읽기 여정:

* 비반복 여정의 경우: 프로필이 여정에 한 번 및 한 번만 입력합니다.
* 반복 여정의 경우: 프로필이 여정/예상 상태에 있는 경우 각 되풀이 시에 들어갑니다. 만약 그가 여전히 이전 반복에서 여정에 있다면, 그는 처음부터 다시 시작합니다.

읽기 세그먼트로 시작하는 비즈니스 이벤트 여정:

이 여정은 비즈니스 이벤트의 수신을 기반으로 하며, 프로필이 예상 세그먼트에 자격을 갖는 경우 수신한 각 비즈니스 이벤트에 대한 여정을 입력합니다. 즉, 이 프로필은 동일한 여정에서 동시에 여러 번, 다른 비즈니스 이벤트의 컨텍스트에서 여러 번 있을 수 있습니다.

## 여정 종료{#journey-ending}

여정은 두 개의 특정 컨텍스트에서 개인에 대해 종료될 수 있습니다.

* 사람이 경로의 마지막 활동에 도달합니다.
* 사람이 도착합니다 **조건** 활동(또는 **대기** 활동(조건 포함)과 일치하지 않습니다.

그런 다음 본인이 다시 입장할 수 있는 경우 여정을 다시 입력할 수 있습니다. [이 페이지](../building-journeys/journey-gs.md#change-properties)를 참조하십시오

라이브 여정을 종료하려면 라이브를 닫는 것이 좋습니다. 여정에 신규 고객이 도착한 것은 봉쇄될 것이다. 여정에 이미 입력한 고객은 끝까지 경험할 수 있습니다. [이 섹션](../building-journeys/journey-end.md#close-journey)을 참조하십시오

여정이 긴급하고 모든 처리가 여정에서 즉시 종료되어야 하는 경우에만를 중지할 수 있습니다. 이미 여정에 입장한 사람은 모두 진행 중입니다. [이 섹션](../building-journeys/journey-end.md#stop-journey)을 참조하십시오

>[!NOTE]
>
>닫힘 또는 정지된 여정은 다시 시작할 수 없습니다.

### 여정 끝 태그{#end-tag}

여정을 작성하는 동안 각 경로의 끝에 &quot;끝 태그&quot;가 표시됩니다. 이 노드는 사용자가 추가할 수 없으며 제거할 수 없으며 해당 레이블만 변경할 수 있습니다. 여정의 각 경로의 끝을 표시합니다. 여정에 여러 경로가 있는 경우 보고서를 쉽게 읽을 수 있도록 각 끝에 레이블을 추가하는 것이 좋습니다. [이 페이지](../reports/live-report.md)를 참조하십시오.

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

### 여정 닫기{#close-journey}

다음 이유로 인해 여정을 닫을 수 있습니다.

* 여정은 를 통해 수동으로 닫힙니다 **[!UICONTROL Close to new entrances]** 버튼을 클릭합니다.
* 실행이 완료된 원샷 세그먼트 기반 여정.
* 반복 세그먼트 기반 여정이 마지막으로 발생한 이후.

여정을 수동으로 닫으면 이미 여정에 로그인한 고객이 경로를 완료할 수 있지만, 새 사용자는 여정에 들어갈 수 없습니다. 여정을 닫으면(위의 이유 중 하나) 상태가 됩니다 **[!UICONTROL Closed]**. 여정은 새 개인이 여정에 들어갈 수 있도록 하는 것을 중지합니다. 여정에 이미 있는 사람은 여정을 정상적으로 완료할 수 있습니다. 기본 글로벌 시간 초과 30일 이후에는 여정이 **완료됨** 상태. 다음 보기 [섹션](../building-journeys/journey-gs.md#global_timeout).

닫힌 여정 버전은 다시 시작하거나 삭제할 수 없습니다. 새 버전을 만들거나 복제할 수 있습니다. 완료된 여정만 삭제할 수 있습니다.

여정 목록에서 여정을 닫으려면 **[!UICONTROL Ellipsis]** 여정 이름의 오른쪽에 있는 버튼을 선택하고 **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

다음 작업도 수행할 수 있습니다.

1. 에서 **[!UICONTROL Journeys]** 목록에서 닫을 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.

   ![](assets/finish_drop_down_list.png)

1. 클릭 **[!UICONTROL Close to new entrances]**, 그리고 대화 상자에서 확인합니다.

### 여정 중지{#stop-journey}

여정에 있는 모든 개인의 진행 상태를 중지해야 하는 경우 중지할 수 있습니다. 여정을 중지하면 여정의 모든 개인이 시간 초과됩니다. 하지만 여정을 중지하려면 이미 여정에 들어온 모든 사용자가 해당 진행 중에 중지된다는 것입니다. 여정은 기본적으로 꺼져 있습니다. 여정을 종료하려면 종료해야 합니다.

중지된 여정 버전을 다시 시작할 수 없습니다.

중지되면 여정 상태가 **[!UICONTROL Stopped]**.

예를 들어, 마케터가 여정이 잘못된 대상을 타깃팅하거나 메시지를 전달해야 하는 사용자 지정 작업이 제대로 작동하지 않는다는 것을 알고 있으면 여정을 중지할 수 있습니다. 여정 목록에서 여정을 중지하려면 **[!UICONTROL Ellipsis]** 여정 이름의 오른쪽에 있는 버튼을 선택하고 **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

다음 작업도 수행할 수 있습니다.

1. 에서 **[!UICONTROL Journeys]** 목록에서 중지할 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.
   ![](assets/finish_drop_down_list.png)
1. 클릭 **[!UICONTROL Stop]**, 그리고 대화 상자에서 확인합니다.
