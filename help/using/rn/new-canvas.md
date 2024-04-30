---
solution: Journey Optimizer
product: journey optimizer
title: 새 여정 인터페이스
feature: Release Notes
topic: Content Management
description: 새 여정 인터페이스
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: b6b3f710d08fb7f0949e75521ce126fa43d6cdc5
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 2%

---

# 향상된 Journey Designer 시작하기 {#new-canvas}

이제 Journey Optimizer에서 **간소화된 여정 모델** 이는 사용자 경험과 내부 프로세스를 개선하는 것을 목표로 합니다. 4월 릴리스부터 다음과 같은 기능을 사용할 수 있습니다.

* A **다시 디자인된 여정 캔버스** 현대화된 UI 경험을 위해 만들어짐
* A **라이브 보고** 여정 캔버스에서 직접 사용할 수 있는 UI

>[!NOTE]
>
>이 기능의 롤아웃은 점진적입니다. 변경 사항이 바로 표시되지 않을 수 있습니다.

## 여정 모델에 대한 업데이트

새 여정 모델은 기존 모델과 함께 사용됩니다. 즉, 을 사용하는 여정이 있을 것입니다. **두 개의 다른 모델**:

* 레거시 모델
* 새 모델

레거시 모델의 모든 여정은 그대로 유지됩니다. 편집하거나, 테스트하거나, 게시할 수 있습니다. 기존 모델의 여정에서 만든 새 버전도 유지됩니다. 다음 항목이 있습니다. **기능 변경 사항 없음** 그 여정 주위에.

아래 스크린샷에서 볼 수 있듯이 노드는 라운드 형태입니다. 이는 레거시 모델의 여정에 대한 이전 UI입니다.

![](assets/new-canvas.png)

그러나 다음을 수행하는 경우 **새 여정 만들기** 또는 **기존 항목 복제**, 새 모델에 포함될 예정입니다. 기존 모델의 여정은 대부분의 고객이 새 고객으로 전환될 때까지 계속 지원됩니다.

새로운 여정 모델에는 한 가지 제한이 있습니다. **기존 모델에서 새 모델로 활동을 복사하고 붙여넣을 수 없으며 그 반대의 경우도 가능합니다**. 이 작업을 수행하려면 기존 여정을 복제하여 새 모델로 전환한 다음 활동을 복사하는 것이 좋습니다.

아래 스크린샷에는 여정 캔버스에 대해 다시 설계된 UI가 표시됩니다(새 모델에서만 사용 가능).

![](assets/new-canvas2.png)

**여정 디자이너에 추가된 모든 새 기능(라이브 보고 포함)은 이제부터 새 모델의 여정에 대해서만 사용할 수 있습니다.**

## 향상된 여정 캔버스 디자인

새로운 여정 모델을 통해 향상된 새로운 기능을 소개합니다 **여정 캔버스 UI**: Adobe Experience Cloud 솔루션 및 앱 생태계에 원활하게 적합하여 직관적이고 효율적인 사용자 경험을 제공합니다. 새 모델의 모든 여정은 해당 새 디자인을 기반으로 합니다.

![](assets/new-canvas3.gif)

이제 활동이 다음 기능의 사각형 상자로 표시됩니다.

* 활동 유형을 나타내는 첫 번째 줄은 더 많은 컨텍스트 정보(대상 읽기에서 선택한 대상의 이름이 포함됨)로 덮어쓰거나, 하나를 정의하는 경우 사용자 지정 레이블로 덮어쓰는 경우가 많습니다.
* 두 번째 줄은 항상 활동 유형을 나타냅니다.

![](assets/new-canvas4.png)

이 새 UI는 다음을 제공하여 여정 캔버스의 가독성을 향상시킵니다. **더 명확한 활동 레이블 및 유형**.

또한 제품 팀이 클릭 수를 줄여 캔버스에 정보를 추가할 수 있습니다. &quot;추가 정보&quot;의 한 가지 예는 여정 캔버스에 라이브 보고를 포함하여, 오류로 인해 활동이 들어오고 나가는 프로필을 볼 수 있는 것입니다.

![](assets/new-canvas5.png)


## 여정 캔버스에서 라이브 보고

향상된 여정 캔버스 레이아웃 외에도 사용자가 다음에서 실시간 보고 지표를 볼 수 있는 새로운 기능이 도입되었습니다 **지난 24시간**&#x200B;라이브 보고라고 하며 여정 캔버스 내에서 바로 사용됩니다.

새 모델을 사용하는 모든 라이브 여정 내의 각 활동에 대해 다음에 액세스할 수 있습니다.

* 이 활동에 들어가는 프로필 수입니다.
* 오류로 인해 이 활동을 종료하는 프로필 수입니다.

![](assets/new-canvas6bis.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
