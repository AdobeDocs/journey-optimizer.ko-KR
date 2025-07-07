---
solution: Journey Optimizer
product: journey optimizer
title: 여정 테스트 또는 게시 전 오류 문제 해결
description: 여정을 테스트하거나 게시하기 전에 오류를 해결하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 문제 해결, 문제 해결, 여정, 확인, 오류
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 61498b61f7f05e0553fe575c980fd1bee08500a3
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 40%

---

# 여정 테스트 전 오류 해결 {#troubleshooting}

이 섹션에서는 테스트 또는 게시 전에 여정 문제를 해결하는 방법에 대해 알아봅니다. 아래 나열된 모든 검사는 여정이 테스트 모드에 있거나 여정이 라이브 상태일 때 수행할 수 있습니다. 테스트 모드에서 아래의 모든 검사를 수행한 후에 게시를 진행하는 것이 좋습니다. [이 페이지](../building-journeys/testing-the-journey.md)의 테스트 모드에 대해 자세히 알아보세요.

여정 이벤트의 문제 해결 방법, 프로필이 여정에 입력되었는지 여부, 프로필이 페이지를 탐색하는 방법, 메시지가 [이 페이지에서 전송되는지 여부](troubleshooting-execution.md)를 알아봅니다.

인바운드 액션을 사용 중인 경우 이 페이지에서 [문제를 해결하는 방법](troubleshooting-inbound.md)을 알아보세요.

## 활동 오류 {#activity-errors}

여정을 테스트하고 게시하기 전에 모든 활동이 올바르게 구성되었는지 확인하십시오. 시스템에서 오류가 계속 감지되면 테스트나 게시를 수행할 수 없습니다.

캔버스에서 활동 자체에 경고 기호가 표시되면서 오류가 나타납니다. 커서를 느낌표 위에 놓으면 오류 메시지가 표시됩니다. 활동을 선택하면 오류가 발생한 줄이 경고와 함께 표시됩니다. 예:

* 필수 필드가 비어 있으면 오류가 표시됩니다

  ![](assets/journey63.png)

* 캔버스에서 두 활동의 연결이 끊기면 경고가 표시됩니다

  ![](assets/canvas-disconnected.png)

## 여정 오류 {#canvas-errors}

캔버스 위의 **[!UICONTROL 경고]** 단추에서도 오류가 표시됩니다. 이 단추를 사용하면 시스템에서 감지된 오류와 테스트 모드 활성화 또는 여정 게시를 방지할 수 있습니다.

시스템에서 두 종류의 문제를 감지합니다. **오류** 및 **경고**. 오류는 게시 및 테스트 활성화를 차단합니다. 경고는 테스트 활성화 또는 게시를 차단하지 않는 잠재적인 문제를 나타냅니다. 문제에 대한 설명 그리고 ERR_XXX_XXX 유형의 문제 로그 ID가 표시됩니다. 이렇게 하면 문제를 식별하는 데 도움이 될 수 있습니다.

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

여정에서 전체적으로 발생하는 오류와 경고가 목록에 먼저 나타납니다. 특정 활동과 관련된 오류와 경고는 그 뒤에 활동 순서별로 또는 여정 내 등장 순서별로 왼쪽에서 오른쪽으로 나열됩니다. 경고 목록의 맨 아래에 있는 **[!UICONTROL 세부 정보 복사]** 단추를 사용하여 문제를 해결하는 데 유용한 여정에 대한 기술 정보를 복사할 수 있습니다.

## 대체 경로 추가 {#canvas-add-path}

다음 여정 활동에 대해 오류가 발생한 경우 대체 동작을 정의할 수 있습니다. **[!UICONTROL 조건]** 및 **[!UICONTROL 동작]**.

작업 또는 조건에 오류가 발생하면 개별 여정이 중지됩니다. 이를 지속할 수 있는 유일한 방법은 문제를 해결하는 것이다. 여정이 중단되지 않도록 하기 위해 **[!UICONTROL 활동 속성에서 시간 초과 또는 오류 발생 시 대체 경로를 추가]** 옵션을 선택할 수도 있습니다. 자세한 내용은 [이 섹션](../building-journeys/using-the-journey-designer.md#paths)을 참조하십시오.
