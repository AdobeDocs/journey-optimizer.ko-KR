---
solution: Journey Optimizer
product: journey optimizer
title: 포크 활동 사용
description: 오케스트레이션된 캠페인에서 포크 활동을 사용하는 방법을 알아봅니다
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 4ba956e83c4e28a6d578ffa093d8b8e5fbd2c50b
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 47%

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

## 예시 {#fork-examples}

다음은 **[!UICONTROL 포크]** 활동의 일반적인 사용입니다. 게재 동작을 비교하기 위해 두 개의 서로 다른 이메일 채널(하나의 마케팅 및 하나의 트랜잭션)을 사용하여 동일한 대상자를 타겟팅하는 것입니다.

**[!UICONTROL 대상 만들기]** 활동에서 대상 모집단을 선택한 후 **[!UICONTROL 포크]**&#x200B;에서 두 개의 병렬 분기를 만듭니다.

* **분기 1**&#x200B;이(가) 마케팅 이메일 채널 활동에 연결합니다. 메시지는 표준 비즈니스 규칙을 따르며 옵트인 프로필에만 전송됩니다.
* **분기 2**&#x200B;이(가) 트랜잭션 전자 메일 채널 활동에 연결합니다. 메시지는 비즈니스 규칙을 무시하고 옵트인 상태에 관계없이 모든 프로필에 전달됩니다.

![](../assets/workflow-fork.png)

이 패턴은 채널 범주 설정이 게재 동작에 미치는 영향을 이해하고 단일 캠페인 실행에서 동일한 대상자에게 다양한 메시지 유형을 보내는 데 유용합니다.
