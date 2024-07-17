---
solution: Journey Optimizer
product: journey optimizer
title: 여정 활동 시작
description: 여정 활동 시작
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 여정, 활동, 시작하기, 이벤트, 작업
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 9562a194244e2a3323680d98cc8aa5ed65d93a67
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 13%

---

# 여정 활동 시작 {#about-journey-activities}

다양한 이벤트, 오케스트레이션 및 작업 활동을 결합하여 여러 단계로 구성된 크로스 채널 시나리오를 작성할 수 있습니다.

## 이벤트 활동 {#event-activities}

개인화된 여정은 온라인 구매와 같은 이벤트에 의해 트리거됩니다. 프로필이 여정에 들어오면 한 개인으로 이동하며 두 개인이 동일한 속도로 또는 동일한 경로를 따라 이동하지 않습니다. 이벤트로 여정을 시작하면 이벤트가 수신될 때 여정이 트리거됩니다. 그런 다음 여정의 각 사람은 여정에 정의된 다음 단계를 개별적으로 따릅니다.

기술 사용자가 구성한 이벤트([이 페이지](../event/about-events.md) 참조)는 모두 화면 왼쪽의 팔레트의 첫 번째 범주에 표시됩니다. 다음 이벤트 활동을 사용할 수 있습니다.

* [일반 이벤트](../building-journeys/general-events.md)
* [반응](../building-journeys/reaction-events.md)
* [대상 자격 조건](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

여정 활동을 끌어다 놓아 이벤트를 시작합니다. 더블 클릭할 수도 있습니다.

![](assets/journey44.png)

## 오케스트레이션 활동 {#orchestration-activities}

오케스트레이션 활동은 여정의 다음 단계를 결정하는 데 도움이 되는 다양한 조건입니다. 지원 사례가 개설되어 있거나 없는 경우, 현재 위치의 일기 예보, 구매를 완료했거나 완료하지 않은 경우 또는 충성도 포인트 10,000에 도달한 경우일 수 있습니다.

화면 왼쪽에 있는 팔레트에서 다음 오케스트레이션 활동을 사용할 수 있습니다.

* [조건](../building-journeys/condition-activity.md)
* [대기](../building-journeys/wait-activity.md)
* [대상자 읽기](../building-journeys/read-audience.md)

![](assets/journey49.png)

## 작업 활동 {#action-activities}

작업은 메시지 전송과 같은 일종의 트리거 결과로 발생하고자 하는 작업입니다. 이는 고객이 경험하는 여정 중 하나입니다.

화면 왼쪽의 팔레트에서 **[!UICONTROL 이벤트]** 및 **[!UICONTROL 오케스트레이션]** 아래에 **[!UICONTROL 작업]** 범주가 있습니다. 다음 작업 활동을 사용할 수 있습니다.

* [이메일, SMS, 푸시](../building-journeys/journeys-message.md)
* [사용자 정의 작업](../building-journeys/using-custom-actions.md)
* [점프](../building-journeys/jump.md)

![](assets/journey58.png)

이곳에는 사용 가능한 다양한 통신 채널의 활동이 표시됩니다. 이러한 세그먼트를 결합하여 크로스채널 시나리오를 만들 수 있습니다.

사용자 지정 작업을 구성한 경우 여기에 표시됩니다. [자세히 알아보기](../building-journeys/using-custom-actions.md)).

## 모범 사례 {#best-practices}

### 레이블 추가

대부분의 활동을 통해 **[!UICONTROL 레이블]**&#x200B;을(를) 정의할 수 있습니다. 캔버스에서 활동 아래에 표시되는 이름에 접미사를 추가합니다. 이 기능은 여정에서 동일한 활동을 여러 번 사용하고 이러한 활동을 보다 쉽게 식별하려는 경우 유용합니다. 또한 오류의 경우 디버깅이 더 쉬워지고 보고서를 더 쉽게 읽을 수 있습니다. 선택적 **[!UICONTROL 설명]**&#x200B;을 추가할 수도 있습니다.

![](assets/journey-action-label.png)

>[!NOTE]
>
>일부 활동의 경우 해당 ID가 창에도 표시됩니다. 이 ID는 변경될 수 있는 레이블보다 안정적인 키로 보고에 사용할 수 있습니다.

### 고급 매개 변수 관리 {#advanced-parameters}

대부분의 활동에는 수정할 수 없는 많은 고급 및/또는 기술 매개 변수가 표시됩니다.

![](assets/journey-advanced-parameters.png)

가독성을 높이기 위해 **[!UICONTROL 읽기 전용 필드 숨기기]** 단추를 사용하여 이러한 매개 변수를 숨길 수 있습니다.

![](assets/journey-hide-read-only-fields.png)

일부 특정 컨텍스트에서는 특정 용도로 이러한 매개 변수의 값을 재정의할 수 있습니다. 값을 강제 적용하려면 필드의 오른쪽에 있는 **[!UICONTROL 매개 변수 무시 활성화]** 아이콘을 클릭합니다. [자세히 알아보기](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 대체 경로 추가

작업 또는 조건에 오류가 발생하면 개별 여정이 중지됩니다. **[!UICONTROL 시간 초과 또는 오류 발생 시 대체 경로를 추가]** 확인란을 선택하여 계속하는 방법만 있습니다. [이 섹션](../building-journeys/using-the-journey-designer.md#paths)을 참조하십시오.

![](assets/journey42.png)
