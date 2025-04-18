---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 예약 및 시작
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 예약하고 시작하는 방법을 알아봅니다
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 94ec0430995c26d6c0eaa68f523675997ed0a327
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 3%

---

# 오케스트레이션된 캠페인 예약 및 시작 {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="오케스트레이션된 캠페인 게시"
>abstract="캠페인을 시작하려면 먼저 캠페인을 게시해야 합니다. 게시하기 전에 모든 경고가 해제되었는지 확인하십시오."

오케스트레이션된 작업을 만들고 캔버스에서 수행할 작업을 디자인했으면 이를 게시하고 실행 방법을 모니터링할 수 있습니다.

## 오케스트레이션된 캠페인 시작 {#start}

오케스트레이션된 캠페인을 시작하려면 **[!UICONTROL 캠페인]** 메뉴의 **[!UICONTROL 여러 단계]** 탭으로 이동하여 시작할 캠페인을 선택한 다음 캔버스의 오른쪽 상단에 있는 **[!UICONTROL 시작]** 단추를 클릭하십시오.

오케스트레이션된 캠페인이 실행되면, 캔버스의 각 활동은 오케스트레이션된 캠페인의 끝에 도달할 때까지 순차적 순서로 실행됩니다.

시각적인 흐름을 사용하여 실시간으로 타겟팅된 프로필의 진행 상황을 추적할 수 있습니다. 이렇게 하면 각 활동의 상태와 활동 간에 전환되는 프로필 수를 빠르게 식별할 수 있습니다.

![](assets/workflow-execution.png){zoomable="yes"}

## 오케스트레이션된 캠페인 전환 {#transitions}

오케스트레이션된 캠페인에서 전환을 통해 한 활동에서 다른 활동으로 전송된 데이터는 임시 작업 표에 저장됩니다. 각 전환에 대해 이 데이터를 표시할 수 있습니다. 이렇게 하려면 전환을 선택하여 화면 오른쪽에서 속성을 엽니다.

* 작업 테이블의 스키마를 표시하려면 **[!UICONTROL 스키마 미리 보기]**&#x200B;를 클릭하십시오.
* 선택한 전환에서 전송된 데이터를 시각화하려면 **[!UICONTROL 결과 미리 보기]**&#x200B;를 클릭하십시오.

![](assets/transition.png){zoomable="yes"}

## 활동 실행 모니터링 {#activities}

각 활동 상자의 오른쪽 위 모서리에 있는 시각적 표시기를 사용하여 실행을 확인할 수 있습니다.

| 시각적 표시기 | 설명 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 활동이 현재 실행 중입니다. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 이 활동에는 주의가 필요합니다. 여기에는 게재 전송을 확인하거나 필요한 조치를 취하는 작업이 포함될 수 있습니다. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 활동에 오류가 발생했습니다. 문제를 해결하려면 오케스트레이션된 캠페인 로그를 열어 자세한 내용을 확인하십시오. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 활동이 정상적으로 실행되었습니다. |

## 로그 및 작업 모니터링 {#logs-tasks}

워크플로우 로그 및 작업 모니터링은 오케스트레이션된 캠페인을 분석하고 제대로 실행되고 있는지 확인하는 중요한 단계입니다. 작업 도구 모음 및 각 활동의 속성 창에서 사용할 수 있는 **[!UICONTROL 로그]** 아이콘을 통해 액세스할 수 있습니다.

**[!UICONTROL 로그 및 작업]** 메뉴에서는 모든 사용자 작업을 기록하고 오류가 발생한 오케스트레이션된 캠페인 실행 기록을 제공합니다.
![](assets/workflow-logs.png){zoomable="yes"}

다음 두 가지 유형의 정보를 사용할 수 있습니다.

* **[!UICONTROL 로그]** 탭에는 오케스트레이션된 모든 캠페인 활동의 실행 기록이 들어 있습니다. 시간 순서대로 수행된 작업과 실행 오류를 색인화합니다.
* **[!UICONTROL 작업]** 탭은 활동의 실행 시퀀싱에 대해 자세히 설명합니다.

두 탭 모두에서 표시된 열과 해당 순서를 선택하고 필터를 적용한 다음 검색 필드를 사용하여 원하는 정보를 빠르게 찾을 수 있습니다.

## 오케스트레이션된 캠페인 실행 명령 {#execution-commands}

오른쪽 상단의 작업 표시줄은 오케스트레이션된 캠페인 실행을 관리할 수 있는 명령을 제공합니다. 다음과 같은 작업을 수행할 수 있습니다.

* 실행 **[!UICONTROL 시작]** / **[!UICONTROL 다시 시작]**   오케스트레이션된 캠페인. 그런 다음 진행 중 상태로 전환됩니다. 오케스트레이션된 캠페인이 일시 중지되면 다시 시작됩니다. 그렇지 않으면 시작되고 초기 활동이 활성화됩니다.

* **[!UICONTROL 일시 중지]** 오케스트레이션된 캠페인의 실행을 일시 중지한 다음 일시 중지됨 상태로 전환합니다. 다시 시작될 때까지 새 활동이 활성화되지 않지만 진행 중인 작업은 중단되지 않습니다.

* 실행 중인 오케스트레이션된 캠페인을 **[!UICONTROL 중지]**&#x200B;하여 완료됨 상태로 전환합니다. 진행 중인 작업은 가능한 경우 중단됩니다. 중지된 동일한 위치에서 오케스트레이션된 캠페인에서 다시 시작할 수 없습니다.
