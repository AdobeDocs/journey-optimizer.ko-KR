---
solution: Journey Optimizer
product: journey optimizer
title: 포크 활동 사용
description: 오케스트레이션된 캠페인에서 포크 활동을 사용하는 방법을 알아봅니다
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 83%

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

**포크** 활동은 **플로우 제어** 활동입니다. 이 활동을 사용하면 아웃바운드 전환을 만들어서 여러 활동을 동시에 시작할 수 있습니다.

## 포크 활동 구성{#fork-configuration}

**포크** 활동을 구성하려면 다음 단계를 따르십시오.

![](../assets/workflow-fork.png)

1. 오케스트레이션된 캠페인에 **포크** 활동을 추가합니다.
1. 새 아웃바운드 전환을 추가하려면 **전환 추가**&#x200B;를 클릭합니다. 기본적으로 두 개의 전환이 정의됩니다.
1. 각 전환에 레이블을 추가합니다.

## 예{#fork-example}

다음 예에서는 두 가지 **포크** 활동을 사용합니다.

* 한 가지는 두 쿼리 이전에 사용하여 쿼리를 동시에 실행합니다.
* 한 가지는 교차로 이후에 사용하여 대상 모집단에게 이메일과 SMS를 동시에 전송합니다.

![](../assets/workflow-fork-example.png)
