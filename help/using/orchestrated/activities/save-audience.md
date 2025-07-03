---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 저장 활동 사용
description: 오케스트레이션된 캠페인에서 대상자 저장 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 3%

---

# 대상자 저장 {#save-audience}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/><b>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)</b><br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

**[!UICONTROL 대상자 저장]** 활동은 오케스트레이션된 캠페인에서 이전에 생성된 모집단에서 기존 대상자를 업데이트하거나 새 대상자를 만들 수 있는 **[!UICONTROL 타깃팅]** 활동입니다. 이 대상자를 만들면 응용 프로그램 대상자 목록에 추가되며 **[!UICONTROL 대상자]** 메뉴에서 액세스할 수 있습니다.

이 활동은 동일한 오케스트레이션된 캠페인 내에서 계산된 대상 세그먼트를 보존하여 향후 캠페인에서 재사용할 수 있도록 하는 데 특히 유용합니다. 일반적으로 결과 모집단을 캡처하고 저장하기 위해 **[!UICONTROL 대상 만들기]** 또는 **[!UICONTROL 결합]**&#x200B;과 같은 다른 타깃팅 활동에 연결됩니다.

## 대상자 저장 활동 구성 {#save-audience-configuration}

**대상자 저장** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **대상자 저장** 활동을 추가합니다.

1. **모드** 드롭다운에서 수행할 작업을 선택합니다.

   * **기존 대상자를 만들거나 업데이트**: **대상자 레이블**&#x200B;을(를) 정의합니다. 대상이 이미 있으면 업데이트되고, 그렇지 않으면 새 대상이 만들어집니다.

   * **기존 대상 업데이트**: 기존 대상 목록에서 업데이트할 **대상**&#x200B;을 선택합니다.

1. 기존 대상에 적용되는 **업데이트 모드**&#x200B;를 선택하십시오.

   * **대상 콘텐츠를 새 데이터로 바꾸기**: 모든 대상 콘텐츠가 바뀌고 이전 데이터가 손실됩니다. **대상자 저장** 활동의 인바운드 전환에서 수집한 데이터만 유지됩니다. 이 옵션은 업데이트한 대상자의 대상자 유형과 타겟팅 차원을 지웁니다.

   * **새 데이터가 있는 전체 대상**: 이전 대상 콘텐츠는 유지되고 **대상 저장** 활동의 인바운드 전환에서 수집한 데이터가 여기에 추가됩니다.

1. **대상자 저장** 활동 후에 전환을 추가하려면 **아웃바운드 전환 생성** 옵션을 선택합니다.

저장한 대상자의 콘텐츠는 **대상자** 메뉴에서 액세스할 수 있는 대상자의 세부 사항 보기에서 사용할 수 있습니다. 이 보기에서 사용할 수 있는 열은 오케스트레이션된 캠페인 **대상자 저장** 활동의 인바운드 전환 열에 해당합니다.

## 예 {#save-audience-example}

다음 예제는 타깃팅에서 간단한 대상 업데이트를 보여 줍니다. 스케줄러는 한 달에 한 번 오케스트레이션된 캠페인을 실행합니다. 쿼리는 사용 가능한 여러 응용 프로그램에 가입된 모든 프로필을 검색합니다. **대상자 저장** 활동은 마지막으로 오케스트레이션된 캠페인 실행 이후 서비스 구독을 취소한 프로필을 제거하고 새로 구독한 프로필을 추가하여 대상자를 업데이트합니다.
