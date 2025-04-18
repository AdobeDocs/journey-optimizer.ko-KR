---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에서 대기 활동 사용
description: 오케스트레이션된 캠페인에서 대기 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 78%

---

# 대기 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="대기 활동"
>abstract="**대기** 활동을 사용하여 전환을 활동에서 다른 활동으로 지연합니다."

**대기** 활동은 **흐름 제어** 활동입니다. 이는 실행할 두 활동 사이에 일정 시간이 지나도록 하는 데 사용됩니다. 예를 들어 이메일 게재 활동 후 며칠 동안 대기하고, 후속 작업(리마인더 이메일, 대상자 만들기 등)을 수행하기 전에 대기 기간 동안 발생한 열람수 및 클릭수를 분석하려 할 때 사용할 수 있습니다.

## 구성{#wait-configuration}

**대기** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **대기** 활동을 추가합니다.

1. 인바운드 전환과 아웃바운드 전환 사이의 대기 **기간**&#x200B;을 지정합니다.

1. **기간** 필드에서 시간 단위(초, 분, 시간, 일)를 선택합니다.

## 예{#wait-example}

다음 예제는 일반적인 사용 사례에서의 **대기** 활동을 보여 줍니다. 이벤트 초대 이메일을 전송합니다. 전송된 후 24시간이 지나면 SMS 게재가 동일한 모집단으로 전송됩니다.

![](../assets/workflow-wait-example.png)
