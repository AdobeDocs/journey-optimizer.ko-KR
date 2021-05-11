---
title: 여정 활동 정보
description: 여정 활동에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 25%

---

# 여정 활동 정보 {#about-journey-activities}

![](../assets/do-not-localize/badge.png)

다양한 이벤트, 오케스트레이션 및 작업 활동을 조합하여 여러 단계로 구성된 크로스 채널 시나리오를 작성할 수 있습니다.

## 이벤트 활동 {#event-activities}

기술 사용자가 구성한 이벤트(이 페이지[이 페이지](../event/about-events.md) 참조)는 모두 팔레트의 첫 번째 카테고리에 화면 왼쪽에 표시됩니다. 다음 이벤트 활동을 사용할 수 있습니다.

* [일반 이벤트](../building-journeys/general-events.md)
* [반응](../building-journeys/reaction-events.md)
* [세그먼트 자격 조건](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

이벤트 활동을 드래그하여 놓아 여정을 시작합니다. 두 번 클릭할 수도 있습니다.

![](../assets/journey44.png)

## 오케스트레이션 활동 {#orchestration-activities}

화면의 왼쪽에 있는 팔레트에서 다음 오케스트레이션 활동을 사용할 수 있습니다.

* [조건](../building-journeys/condition-activity.md)
* [종료](../building-journeys/end-activity.md)
* [대기](../building-journeys/wait-activity.md)
* [세그먼트 읽기](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## 작업 활동 {#action-activities}

팔레트의 화면 왼쪽에 있는 **[!UICONTROL Events]** 및 **[!UICONTROL Orchestration]** 아래에는 **[!UICONTROL Actions]** 범주가 있습니다. 다음 작업 활동을 사용할 수 있습니다.

* [메시지](../building-journeys/journeys-message.md)
* [사용자 정의 작업](../building-journeys/using-custom-actions.md)
* [점프](../building-journeys/jump.md)

![](../assets/journey58.png)

이곳에는 사용 가능한 다양한 통신 채널의 활동이 표시됩니다. 이러한 구성 요소를 결합하여 크로스 채널 시나리오를 만들 수 있습니다.

사용자 지정 작업을 구성한 경우 여기에 표시됩니다([이 페이지](../building-journeys/using-custom-actions.md) 참조).

## 우수 사례 {#best-practices}

대부분의 활동에서는 **[!UICONTROL Label]**&#x200B;을 정의할 수 있습니다. 그러면 캔버스에서 활동 아래에 표시되는 이름에 접미어를 추가합니다. 이 기능은 여정에서 동일한 활동을 여러 번 사용하고 보다 쉽게 식별하려는 경우에 유용합니다. 또한 오류 발생 시 디버깅을 보다 쉽게 수행할 수 있으며 보고서를 보다 쉽게 읽을 수 있습니다. 옵션 **[!UICONTROL Description]**&#x200B;을 추가할 수도 있습니다.

![](../assets/journey59bis.png)

작업 또는 조건에 오류가 발생하면 개별 여정이 중지됩니다. 이 작업을 계속 진행할 수 있는 유일한 방법은 **[!UICONTROL Add an alternative path in case of a timeout or an error]** 상자를 선택하는 것입니다 . [이 섹션](../building-journeys/using-the-journey-designer.md#paths)을 참조하십시오.

![](../assets/journey42.png)
