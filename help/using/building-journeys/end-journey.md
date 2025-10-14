---
solution: Journey Optimizer
product: journey optimizer
title: 여정 종료
description: Journey Optimizer에서 여정이 종료되는 방법 알아보기
feature: Journeys
role: User
level: Intermediate
keywords: 재입력, 여정, 종료, 라이브, 중지
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
version: Journey Orchestration
source-git-commit: 2a5db6950ac82fd18deb2e4009c9a43247444d6a
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# 여정 종료 {#journey-ending}

## 라이브 여정 종료 방법

여정은 글로벌 여정 시간 제한에 도달하거나 반복 대상 기반 여정의 마지막 발생 후에 닫힙니다. [여정이 닫히는 방법을 알아보세요](#close-journey).

라이브 여정을 종료해야 하는 경우 [수동으로 닫는](#close-to-new-entrances)것이 좋습니다. 그러면 여정 내 신규 고객 도착이 차단됩니다. 이미 여정에 입력한 프로필은 끝까지 경험할 수 있습니다.

또한 긴급 상황이거나 모든 여정 처리를 즉시 종료해야 하는 경우에만 [여정을 중지](#stop-journey)할 수 있습니다. 이미 여정에 들어간 사람은 모두 진행 중단이 됩니다.

>[!IMPORTANT]
>
>* [닫힘](#close-journey) 또는 [중지됨](#stop-journey) 여정을 다시 시작하거나 삭제할 수 없습니다. [새 버전을 만들거나](publishing-the-journey.md#journey-versions-journey-versions) [복제](journey-ui.md#duplicate-a-journey-duplicate-a-journey)할 수 있습니다.
>
>* 완료된 여정만 삭제할 수 있습니다.

## 프로필에서 여정을 종료하는 방법

여정은 다음 두 가지 특정 컨텍스트에서 개인에 대해 종료됩니다.

* 개별 사용자가 경로의 마지막 활동에 도달한 다음 [End 태그](#end-tag)(으)로 이동합니다.
* 개별 사용자가 **조건** 활동(또는 조건이 있는 **대기** 활동)에 도달하고 조건과 일치하지 않습니다.

그런 다음 재입장이 허용되는 경우 개인이 여정에 다시 입장할 수 있습니다. [입장/재입장 관리에 대해 자세히 알아보기](../building-journeys/journey-properties.md#entrance)

## 여정 끝 태그 {#end-tag}

여정을 작성하는 동안 각 경로의 끝에 종료 태그가 표시됩니다. 이 노드는 사용자가 추가할 수 없으며 제거할 수 없으며 해당 레이블만 변경할 수 있습니다. 여정의 각 경로 끝을 표시합니다.

여정에 여러 개의 경로가 있는 경우 보고서를 더 쉽게 읽을 수 있도록 각 끝에 레이블을 추가하는 것이 좋습니다. [여정 보고서](../reports/live-report.md)에 대해 자세히 알아보세요.

![](assets/journey-end.png)

## 여정 닫기 {#close-journey}

다음 이유로 인해 여정이 닫힐 수 있습니다.

* 실행을 완료하고 글로벌 시간 제한(91일)에 도달한 일회성 세그먼트 기반 여정.
* 반복 대상 기반 여정의 마지막 발생 이후.
* [**[!UICONTROL 새 등록 마감]**](#close-to-new-entrances) 단추를 통해 여정을 수동으로 닫습니다.

**91일 여정 글로벌 시간 제한** 후 대상 읽기 여정이 **완료됨** 상태로 전환됩니다. 이 동작은 여정에 입력한 프로필에 대한 모든 정보가 입력한 후 91일 후에 제거되므로 91일 동안만 설정됩니다. 아직 여정에 있는 사람은 자동으로 영향을 받습니다. 91일 제한 시간이 지나면 여정을 종료합니다.  [여정 전역 시간 제한](../building-journeys/journey-properties.md#global_timeout)에 대해 자세히 알아보세요.

>[!TIP]
>
>일회성 세그먼트 기반 여정은 한 번 실행한 후에도 **Live** 상태를 유지합니다. 프로필이 완료되면 다시 입력할 수 없지만 기본 전역 시간 제한이 만료될 때까지 여정은 **Live** 상태로 유지됩니다. **새 등록에 닫기** 옵션을 사용하면 더 빨리 수동으로 닫을 수 있습니다.

### 새 등록 마감 {#close-to-new-entrances}

여정을 수동으로 닫으면 여정에 이미 입력한 고객이 경로를 완료할 수 있지만 새 사용자가 여정을 입력할 수 없게 됩니다. 여정이 닫히면 **[!UICONTROL 닫힘]** 상태가 됩니다. 이 여정은 새로운 개인이 여정에 입력하는 것을 중단합니다. 이미 여정에 있는 프로필은 여정을 정상적으로 완료할 수 있습니다. 기본 전역 시간 제한(91일) 이후 여정이 **완료됨** 상태로 전환됩니다.

여정 목록에서 여정을 닫으려면 여정 이름 오른쪽에 있는 **[!UICONTROL 줄임표]** 단추를 클릭하고 **[!UICONTROL 새 출입구에 닫기]**&#x200B;를 선택합니다.

![](assets/journey-finish-quick-action.png)

다음 작업도 수행할 수 있습니다.

1. **[!UICONTROL 여정]** 목록에서 닫을 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.

   ![](assets/finish_drop_down_list.png){width="50%" align="left" zoomable="yes"}

1. **[!UICONTROL 새 출입문 닫기]**&#x200B;를 클릭하고 대화 상자에서 확인합니다.




## 여정 중지 {#stop-journey}

여정 내 모든 개인의 진행을 중단해야 하는 경우에는 중단할 수 있습니다. 여정 시간 제한을 중지하면 여정에 있는 모든 개인이 제한 시간을 초과합니다. 그러나 여정을 중지하면 이미 여정에 들어간 사람들이 모두 진행 중에 중지됩니다. 여정은 기본적으로 꺼져 있습니다. 여정을 종료하려면 [닫는 것이 좋습니다](#close-journey).

예를 들어, 마케터가 여정이 잘못된 대상을 타기팅하거나 메시지를 전달해야 하는 사용자 지정 작업이 제대로 작동하지 않는다는 것을 인식하는 경우 여정을 중지할 수 있습니다. 여정 목록에서 여정을 중지하려면 여정 이름 오른쪽에 있는 **[!UICONTROL 줄임표]** 단추를 클릭하고 **[!UICONTROL 중지]**&#x200B;를 선택합니다.

![](assets/journey-finish-quick-action.png)

다음 작업도 수행할 수 있습니다.

1. **[!UICONTROL 여정]** 목록에서 중지할 여정을 클릭합니다.
1. 오른쪽 상단에서 아래쪽 화살표를 클릭합니다.

   ![](assets/finish_drop_down_list2.png){width="50%" align="left" zoomable="yes"}

1. **[!UICONTROL 중지]**&#x200B;를 클릭하고 대화 상자에서 확인합니다.

중지되면 여정 상태가 **[!UICONTROL 중지됨]**(으)로 설정됩니다.

>[!CAUTION]
>
>**[!DNL Manage journeys]** 높은 수준의 권한을 가진 사용자로 제한된 여정을 중지할 수 있는 권한. [!DNL Journey Optimizer]이 섹션[에서 &#x200B;](../administration/permissions-overview.md) 사용자의 액세스 권한 관리에 대해 자세히 알아보세요.