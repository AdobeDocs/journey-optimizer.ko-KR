---
solution: Journey Optimizer
product: journey optimizer
title: AND-join 활동 사용
description: 오케스트레이션된 캠페인에서 AND-join 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 37%

---

# AND-결합 {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-결합 활동"
>abstract="**AND-결합** 활동을 사용하면 오케스트레이션된 캠페인의 여러 실행 분기를 동기화할 수 있습니다. 이전 활동이 모두 완료되면 트리거됩니다. 이로써 오케스트레이션된 캠페인을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](../configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/><b>[및 가입](and-join.md)</b> - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL AND-결합]** 활동은 **[!UICONTROL 흐름 제어]** 활동입니다. 이를 통해 오케스트레이션된 캠페인의 여러 실행 분기를 동기화할 수 있습니다.

이 활동은 모든 인바운드 전환이 활성화되었을 때, 즉 앞선 활동이 모두 완료된 다음에만 아웃바운드 전환을 트리거합니다. 이렇게 하면 오케스트레이션된 캠페인을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다.

## AND-결합 활동 구성{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="병합 옵션"
>abstract="참여하고자 하는 활동을 선택합니다. **기본 세트** 드롭다운에서 유지하고자 하는 인바운드 전환 모집단을 선택합니다."

**[!UICONTROL AND-결합]** 활동을 구성하려면 다음 단계를 따르십시오.

![](../assets/workflow-andjoin.png)

1. 채널 활동과 같은 여러 활동을 추가하여 두 개 이상의 고유한 실행 분기를 만듭니다.

1. 분기 중 하나에 **[!UICONTROL AND-join]** 활동을 삽입합니다.

1. **[!UICONTROL 병합 옵션]** 섹션에서 가입하려는 이전 활동을 모두 선택합니다.

1. **[!UICONTROL 기본 집합]** 드롭다운에서 유지할 인바운드 전환 모집단을 선택합니다.

## 예{#and-join-example}

이 예제에서는 2개의 조정된 캠페인 분기를 보여줍니다. 각 분기는 이메일 게재, 타겟팅 골드 멤버 및 기타 실버를 포함합니다. **[!UICONTROL AND-join]**&#x200B;은(는) 들어오는 두 전환이 모두 트리거되면 활성화되며 7일 지연 후 두 이메일 게재가 모두 완료된 후에만 SMS가 전송됩니다.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
