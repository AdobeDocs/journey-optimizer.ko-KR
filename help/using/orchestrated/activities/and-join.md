---
solution: Journey Optimizer
product: journey optimizer
title: AND 조인 활동 사용
description: 오케스트레이션된 캠페인에서 AND 조인 활동을 사용하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 88%

---

# AND-결합 {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-결합 활동"
>abstract="**AND-결합** 활동을 사용하면 오케스트레이션된 캠페인의 여러 실행 분기를 동기화할 수 있습니다. 이전 활동이 모두 완료되면 트리거됩니다. 이로써 오케스트레이션된 캠페인을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](../gs-schemas.md)</li><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[리타기팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/><b>[And 조인](and-join.md)</b> - [대상자 빌드](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상자 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**[!UICONTROL AND-결합]** 활동은 **[!UICONTROL 흐름 제어]** 활동입니다. 사용하면 오케스트레이션된 캠페인의 여러 실행 분기를 동기화할 수 있습니다. 

이 활동은 모든 인바운드 전환이 활성화되었을 때, 즉 앞선 활동이 모두 완료된 다음에만 아웃바운드 전환을 트리거합니다. 이렇게 하면 오케스트레이션된 캠페인을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다.

## AND-결합 활동 구성{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="병합 옵션"
>abstract="참여하고자 하는 활동을 선택합니다. **기본 세트** 드롭다운에서 유지하고자 하는 인바운드 전환 모집단을 선택합니다."

**[!UICONTROL AND-결합]** 활동을 구성하려면 다음 단계를 따릅니다.

![](../assets/workflow-andjoin.png)

1. 채널 활동 등 여러 활동을 추가하여 별개의 실행 분기를 두 개 이상 만듭니다.

1. 이 분기 중 하나에 **[!UICONTROL AND 조인]** 활동을 추가합니다.

1. **[!UICONTROL 병합 옵션]** 섹션에서 조인할 이전 활동을 모두 선택합니다.

1. **[!UICONTROL 기본 집합]** 드롭다운에서 유지할 인바운드 전환 집단을 선택합니다.

## 예{#and-join-example}

이 예에서는 조정된 캠페인 분기 두 개를 보여줍니다. 하나는 골드 회원, 다른 하나는 실버 회원을 각각 타기팅하는 이메일 게재를 다룹니다. **[!UICONTROL AND 조인]**&#x200B;은 들어오는 두 전환이 모두 트리거되면 활성화되며, 7일 지연 후 두 이메일 전송이 모두 완료된 후에만 SMS가 전송됩니다.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
