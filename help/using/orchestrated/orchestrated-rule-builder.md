---
solution: Journey Optimizer
product: journey optimizer
title: 규칙 빌더를 사용하여 작업
description: 오케스트레이션된 캠페인에 대한 규칙을 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 4%

---


# 규칙 빌더를 사용하여 작업 {#orchestrated-rule-builder}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 구성](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | <b>[규칙 빌더로 작업](orchestrated-rule-builder.md)</b><br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

오케스트레이션된 캠페인에는 다양한 기준을 기반으로 데이터베이스를 필터링하는 프로세스를 간소화하는 규칙 빌더가 함께 제공됩니다. 규칙 빌더는 매우 복잡하고 긴 쿼리를 효율적으로 관리하여 향상된 유연성과 정밀성을 제공합니다.

또한 조건 내에 사전 정의된 필터를 지원하므로 사용자가 쿼리를 쉽게 세분화할 수 있는 동시에 포괄적인 대상 타기팅 및 세분화 전략에 고급 표현식 및 연산자를 활용할 수 있습니다.

## 규칙 빌더에 액세스

대상을 타기팅하기 위해 **[!UICONTROL 대상 작성]** 활동에서 쿼리를 작성할 때 규칙 빌더를 사용할 수 있습니다. 이를 통해 타깃팅할 모집단을 지정하고 필요에 따라 맞춤화된 새 대상을 손쉽게 만들 수 있습니다.

![대상 만들기 활동을 보여 주는 이미지](assets/rule-builder-query.png)

## 규칙 빌더 인터페이스 {#interface}

규칙 빌더는 쿼리를 빌드하는 중앙 캔버스와 규칙에 대한 정보를 제공하는 속성 창을 제공합니다.

![규칙 빌더 인터페이스를 표시하는 이미지](assets/rule-builder-interface.png)

* **중앙 캔버스**&#x200B;에서 다른 구성 요소를 추가하고 결합하여 규칙을 만듭니다. [규칙을 만드는 방법을 알아봅니다](../orchestrated/build-query.md)

* **[!UICONTROL 규칙 속성]** 창은 규칙에 대한 정보를 제공합니다. 다양한 작업을 수행하여 규칙을 확인하고 필요에 맞게 규칙을 확인할 수 있습니다.

  이 창은 대상자를 만들기 위한 쿼리를 작성할 때 표시됩니다. [쿼리를 확인하고 확인하는 방법을 알아보세요](build-query.md#check-and-validate-your-query)
