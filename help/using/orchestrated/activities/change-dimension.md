---
solution: Journey Optimizer
product: journey optimizer
title: 차원 변경 활동 사용
description: 차원 변경 활동을 사용하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 32b13d4fd62abc8052c1bf64d8a2d5e97bd0f464
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# 차원 변경 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="여집합 생성"
>abstract="중복으로 제외된 나머지 집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="차원 활동 변경"
>abstract="이 활동을 통해 대상자를 빌드하면서 타기팅 차원을 변경할 수 있습니다. 데이터 템플릿과 입력 차원에 따라 축이 이동됩니다. 예를 들어 “계약” 차원에서 “클라이언트” 차원으로 전환할 수 있습니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](../configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 만들기에 대한 주요 단계](../gs-campaign-creation.md) | [오케스트레이션된 캠페인 만들기](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](../send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [쿼리 Modeler 작업](../orchestrated-query-modeler.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

마케터는 오케스트레이션된 캠페인 내에서 한 엔티티에서 다른 연결된 엔티티로 타겟팅 차원을 전환하고, 다른 데이터 세트를 기반으로 대상 타겟팅을 세분화할 수 있습니다(예: 프로필 사용자에서 특정 작업 또는 예약을 타겟팅하는 방식으로 이동).

이 작업을 수행하려면 **차원 변경** 타깃팅 활동을 사용하십시오. 이 활동을 사용하면 오케스트레이션된 캠페인을 구축할 때 타겟팅 차원을 변경할 수 있습니다. 데이터 템플릿과 입력 차원에 따라 축을 이동합니다.

예를 들어 오케스트레이션된 캠페인의 타겟팅 차원을 &quot;프로필&quot;에서 &quot;계약&quot;으로 전환하여 타겟팅된 계약 소유자에게 메시지를 보낼 수 있습니다.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 차원 변경 활동 구성 {#configure}

**차원 변경** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **차원 변경** 활동을 추가합니다.

   ![](../assets/change-dimension.png)

1. **새 대상 차원**&#x200B;을(를) 정의합니다. 차원 변경 중에는 모든 레코드가 유지됩니다.

1. 오케스트레이션된 캠페인을 실행하여 결과를 확인합니다. 차원 변경 활동 전후의 테이블에서 데이터를 비교하고 오케스트레이션된 캠페인 테이블의 구조를 비교합니다.

## 예 {#example}

이 예제에서는 구매한 모든 프로필에 SMS 게재를 전송하려고 합니다. 이렇게 하려면 먼저 사용자 지정 &quot;구매&quot; 타겟팅 차원에 연결된 **[!UICONTROL 대상자 작성]** 활동을 사용하여 발생한 모든 구매를 타겟팅합니다.

그런 다음 **[!UICONTROL 차원 변경]** 활동을 사용하여 오케스트레이션된 캠페인 타기팅 차원을 &quot;수신자&quot;로 전환합니다. 이를 통해 쿼리와 일치하는 수신자를 타겟팅할 수 있습니다.

![](../assets/change-dimension-example.png)
