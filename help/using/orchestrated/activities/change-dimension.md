---
solution: Journey Optimizer
product: journey optimizer
title: 차원 변경 활동 사용
description: 차원 변경 활동을 사용하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 6eb49e954b7906f668b1c1779c16f3e67003307b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 23%

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

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul><br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - <b>[차원 변경](change-dimension.md)</b> - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

마케터는 오케스트레이션된 캠페인 내에서 한 데이터 엔티티에서 관련 엔티티로 전환하여 대상 타깃팅을 향상시킬 수 있습니다. 이를 통해 사용자 프로필을 넘어 구매, 예약 또는 기타 상호 작용과 같은 특정 행동에 집중할 수 있습니다.

이렇게 하려면 **[!UICONTROL 차원 변경]** 활동을 사용하십시오. 오케스트레이션된 캠페인 동안 타겟팅 차원을 조정할 수 있습니다.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 차원 변경 활동 구성 {#configure}

**[!UICONTROL 차원 변경]** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **[!UICONTROL 차원 변경]** 활동을 추가합니다.

   ![](../assets/orchestrated-change-dimension.png)

1. **[!UICONTROL 새 대상 차원]**&#x200B;을(를) 정의합니다. 차원 변경 중에는 모든 레코드가 유지됩니다.


## 예 {#example}

이 사용 사례는 지난 한 달 내에 위시리스트를 만든 프로필에 SMS를 보내는 데 중점을 둡니다.

**[!UICONTROL 대상자 빌드]** 활동으로 시작하여 **[!UICONTROL 위시리스트]** 타겟팅 차원을 사용하여 모든 관련 위시리스트를 식별합니다.

그런 다음 **[!UICONTROL 차원 변경]** 활동을 추가하여 타겟팅 차원을 **[!UICONTROL 위시리스트]**&#x200B;에서 **[!UICONTROL 수신자](으)로 전환합니다.** 이 단계에서는 오케스트레이션된 캠페인 타겟이 해당 위시리스트에 연결된 올바른 프로필을 사용하도록 하여 의도한 프로필로 SMS를 보낼 수 있도록 합니다.

![](../assets/orchestrated-change-dimension-example.png)
