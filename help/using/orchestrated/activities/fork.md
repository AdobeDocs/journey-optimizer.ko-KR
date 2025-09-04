---
solution: Journey Optimizer
product: journey optimizer
title: 포크 활동 사용
description: 오케스트레이션된 캠페인에서 포크 활동을 사용하는 방법을 알아봅니다
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

---


# 포크 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="포크 활동"
>abstract="**포크** 활동을 사용하면 아웃바운드 전환을 만들어서 여러 활동을 동시에 시작할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="포크 활동 전환"
>abstract="기본적으로 **포크** 활동을 통해 두 개의 전환을 만듭니다. **전환 추가** 버튼을 클릭하여 추가 아웃바운드 전환을 정의하고 해당 레이블을 입력합니다."

**[!UICONTROL 포크]** 활동은 여러 개의 아웃바운드 전환을 만들 수 있는 **[!UICONTROL 흐름 제어]** 구성 요소로, 여러 활동을 동시에 실행할 수 있습니다.

## 포크 활동 구성{#fork-configuration}

**[!UICONTROL 포크]** 활동을 구성하려면 다음 단계를 따릅니다.

![](../assets/workflow-fork.png)

1. 오케스트레이션된 캠페인에 **[!UICONTROL 포크]** 활동을 추가합니다.

1. **[!UICONTROL 레이블]**&#x200B;을 정의합니다.

1. 각 아웃바운드 전환에 레이블을 할당합니다. 기본적으로 두 개의 전환이 제공됩니다.

1. 전환을 제거하려면 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 아이콘을 클릭합니다.

1. 필요한 경우 **[!UICONTROL 전환 추가]**&#x200B;를 클릭하여 아웃바운드 전환을 더 추가합니다.
