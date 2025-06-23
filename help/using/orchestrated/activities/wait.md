---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에서 대기 활동 사용
description: 오케스트레이션된 캠페인에서 대기 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 38b65200435e0b997e79aefbb66549b9168188fd
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 14%

---

# 대기 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="대기 활동"
>abstract="**대기** 활동을 사용하면 한 활동이 다른 활동으로 전환되는 것을 늦출 수 있습니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](../configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 만들기에 대한 주요 단계](../gs-campaign-creation.md) | [오케스트레이션된 캠페인 만들기](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](../send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [쿼리 Modeler 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 대기]** 활동은 오케스트레이션된 캠페인에서 두 활동 간의 지연을 유도하는 데 사용되는 **[!UICONTROL 흐름 제어]** 구성 요소입니다. 이렇게 하면 후속 활동이 시간을 더 잘 맞추고 사용자 참여와 더 관련이 있는지 확인하는 데 도움이 됩니다.

예를 들어 후속 메시지를 보내기 전에 열기 및 클릭을 추적하기 위해 이메일 게재 후 며칠 동안 기다릴 수 있습니다.

## 구성{#wait-configuration}

**[!UICONTROL 대기]** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **[!UICONTROL 대기]** 활동을 추가합니다.

1. 요구 사항에 가장 적합한 대기 유형을 선택합니다.

   * **[!UICONTROL 기간]**: 다음 활동으로 진행하기 전에 지연 시간을 초, 분, 시간 또는 일 단위로 지정합니다.

   * **[!UICONTROL 고정 시간]**: 다음 활동이 시작되는 특정 날짜와 시간을 설정합니다.

   ![](../assets/wait_activity.png)

## 예{#wait-example}

다음 예제에서는 일반적인 사용 사례에서 **[!UICONTROL 대기]** 활동을 보여줍니다.  생일을 축하하는 프로필로 프로모션 코드가 포함된 이메일이 전송됩니다. 29일 이후에는 생일 프로모션 코드가 곧 만료된다는 알림과 함께 SMS가 동일한 그룹으로 전송됩니다.

![](../assets/wait-example.png)
