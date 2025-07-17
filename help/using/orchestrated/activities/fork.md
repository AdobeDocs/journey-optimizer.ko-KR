---
solution: Journey Optimizer
product: journey optimizer
title: 포크 활동 사용
description: 오케스트레이션된 캠페인에서 포크 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 6eb49e954b7906f668b1c1779c16f3e67003307b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 27%

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

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul><br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - <b>[포크](fork.md)</b> - [조정](reconciliation.md) - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**[!UICONTROL Fork]** 활동은 여러 개의 아웃바운드 전환을 만들 수 있는 **[!UICONTROL 흐름 제어]** 구성 요소로, 여러 활동을 동시에 실행할 수 있습니다.

## 포크 활동 구성{#fork-configuration}

**[!UICONTROL 포크]** 활동을 구성하려면 다음 단계를 따르십시오.

![](../assets/workflow-fork.png)

1. 오케스트레이션된 캠페인에 **[!UICONTROL 포크]** 활동을 추가합니다.

1. **[!UICONTROL 레이블]**&#x200B;을(를) 정의합니다.

1. 각 아웃바운드 전환에 레이블을 지정합니다. 기본적으로 두 개의 전환이 제공됩니다.

1. 전환을 제거하려면 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 아이콘을 클릭하십시오.

1. 필요한 경우 **[!UICONTROL 전환 추가]**&#x200B;를 클릭하여 아웃바운드 전환을 더 추가합니다.
