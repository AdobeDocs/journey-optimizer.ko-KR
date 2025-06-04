---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에서 대기 활동 사용
description: 오케스트레이션된 캠페인에서 대기 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 55%

---

# 대기 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="대기 활동"
>abstract="**대기** 활동을 사용하면 한 활동이 다른 활동으로 전환되는 것을 늦출 수 있습니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md) | [오케스트레이션된 캠페인 만들기](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [쿼리 Modeler 작업](orchestrated-query-modeler.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

**대기** 활동은 **흐름 제어** 활동입니다. 이는 실행할 두 활동 사이에 일정 시간이 지나도록 하는 데 사용됩니다. 예를 들어 이메일 게재 활동 후 며칠 동안 대기하고, 후속 작업(리마인더 이메일, 대상자 만들기 등)을 수행하기 전에 대기 기간 동안 발생한 열람수 및 클릭수를 분석하려 할 때 사용할 수 있습니다.

## 구성{#wait-configuration}

**대기** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **대기** 활동을 추가합니다.

1. 인바운드 전환과 아웃바운드 전환 사이의 대기 **기간**&#x200B;을 지정합니다.

1. **기간** 필드에서 시간 단위(초, 분, 시간, 일)를 선택합니다.

## 예{#wait-example}

다음 예제는 일반적인 사용 사례에서의 **대기** 활동을 보여 줍니다. 이벤트 초대 이메일을 전송합니다. 전송된 후 24시간이 지나면 SMS 게재가 동일한 모집단으로 전송됩니다.

![](../assets/workflow-wait-example.png)
