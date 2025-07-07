---
solution: Journey Optimizer
product: journey optimizer
title: 규칙 빌더를 사용하여 작업
description: 오케스트레이션된 캠페인에 대한 규칙을 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 10%

---


# 규칙 빌더를 사용하여 작업 {#orchestrated-rule-builder}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | <b>[규칙 빌더로 작업](orchestrated-rule-builder.md)</b><br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

오케스트레이션된 캠페인에는 다양한 기준을 기반으로 데이터베이스를 필터링하는 프로세스를 간소화하는 규칙 빌더가 함께 제공됩니다. 규칙 빌더는 매우 복잡하고 긴 쿼리를 효율적으로 관리하여 향상된 유연성과 정밀성을 제공합니다.

또한 조건 내에 사전 정의된 필터를 지원하므로 포괄적인 대상 타기팅 및 세분화 전략에 고급 표현식 및 연산자를 활용하는 동시에 쿼리를 쉽게 세분화할 수 있습니다.

## 규칙 빌더에 액세스

쿼리 모델러는 데이터를 필터링하기 위한 규칙을 정의해야 하는 모든 상황에서 사용할 수 있습니다.

| 사용 | 예 |
|  ---  |  ---  |
| **대상자 빌드**: **[!UICONTROL 대상자 빌드]** 활동을 사용하여 오케스트레이션된 캠페인에서 타깃팅할 모집단을 지정하고 필요에 맞게 새 대상자를 쉽게 만들 수 있습니다. [대상자를 만드는 방법을 알아봅니다](../orchestrated/activities/build-audience.md) | ![대상 만들기 인터페이스에 액세스하는 방법을 보여 주는 이미지](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **캠페인 캔버스에 조건 만들기**: **[!UICONTROL 분할]** 활동을 사용하여 캠페인 캔버스 내에 규칙을 적용하여 특정 요구 사항에 맞춥니다. [분할 활동을 사용하는 방법 알아보기](../orchestrated/activities/split.md) | ![워크플로 사용자 지정 옵션에 액세스하는 방법을 보여 주는 이미지](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **고급 필터 만들기**: 워크플로 로그 또는 타겟팅 차원과 같은 목록에 표시된 데이터를 필터링하는 규칙을 만듭니다. | ![목록 필터를 사용자 지정하는 방법을 보여 주는 이미지](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## 규칙 빌더 인터페이스 {#interface}

규칙 빌더는 쿼리를 빌드하는 중앙 캔버스와 규칙에 대한 정보를 제공하는 속성 창을 제공합니다.

![규칙 빌더 인터페이스를 표시하는 이미지](assets/rule-builder-interface.png)

* **중앙 캔버스**&#x200B;에서 다른 구성 요소를 추가하고 결합하여 규칙을 만듭니다. [규칙을 만드는 방법을 알아봅니다](../orchestrated/build-query.md)

* **[!UICONTROL 규칙 속성]** 창은 규칙에 대한 정보를 제공합니다. 다양한 작업을 수행하여 규칙을 확인하고 필요에 맞게 규칙을 확인할 수 있습니다.

  이 창은 대상자를 만들기 위한 쿼리를 작성할 때 표시됩니다. [쿼리를 확인하고 확인하는 방법을 알아보세요](build-query.md#check-and-validate-your-query)
