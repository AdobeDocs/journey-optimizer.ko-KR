---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 저장 활동 사용
description: 오케스트레이션된 캠페인에서 대상자 저장 활동을 사용하는 방법을 알아봅니다.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 81f0338935ee36b152963f2b1c0e7989b86f5f8a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 67%

---

# 대상자 저장 {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="대상자 활동 저장"
>abstract="**대상자 저장** 활동은 기존 대상자를 업데이트하거나 이전에 조직된 캠페인에서 생성된 모집단으로부터 새 대상자를 만들 수 있는 **타겟팅** 활동입니다. 이 대상자를 만들면 애플리케이션 대상자 목록에 추가되며 **대상자** 메뉴에서 액세스할 수 있습니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](../gs-schemas.md)</li><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[리타기팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[And 조인](and-join.md) - [대상자 빌드](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - <b>[대상자 저장](save-audience.md)</b> - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**[!UICONTROL 대상자 저장]** 활동은 오케스트레이션된 캠페인에서 이전에 생성된 모집단을 기반으로 새 대상자를 만들거나 기존 대상자를 업데이트하는 데 사용되는 **[!UICONTROL 타깃팅]** 활동입니다. 저장하면 응용 프로그램 대상자 목록에 대상자가 추가되고 **[!UICONTROL 대상자]** 메뉴에서 액세스할 수 있습니다.

일반적으로 동일한 캠페인 워크플로우 내에 구축된 대상 세그먼트를 캡처하여 향후 캠페인에서 재사용할 수 있도록 하는 데 사용됩니다. 일반적으로 최종 타깃팅된 모집단을 저장하기 위해 **[!UICONTROL 대상 만들기]** 또는 **[!UICONTROL 결합]**&#x200B;과 같은 다른 타깃팅 활동과 연결됩니다.

## 대상자 저장 활동 구성 {#save-audience-configuration}

**[!UICONTROL 대상자 저장]** 활동을 구성하려면 다음 단계를 따릅니다.

1. 오케스트레이션된 캠페인에 **[!UICONTROL 대상자 저장]** 활동을 추가합니다.

1. 저장된 대상자를 식별하는 **[!UICONTROL 대상자 레이블]**&#x200B;을 입력합니다.

1. **[!UICONTROL 대상자 속성 추가]**&#x200B;를 클릭하여 대상자 데이터를 구성하고 나중에 재사용할 수 있도록 저장하는 방법을 정의합니다.

   ![](../assets/save-audience-1.png)

1. 그런 다음 정확한 프로필 확인을 위해 적절한 **[!UICONTROL 기본 ID 필드]**&#x200B;와 **[!UICONTROL ID 네임스페이스]**&#x200B;를 선택합니다.

   ![](../assets/save-audience-2.png)

1. 오케스트레이션된 캠페인을 저장하고 게시하여 설정을 완료합니다. 이렇게 하면 대상자가 생성되고 저장됩니다.

**[!UICONTROL 대상자]** 메뉴를 통해 액세스할 수 있는 대상자 세부 사항 보기에서 저장한 대상자의 콘텐츠를 확인할 수 있습니다.

![](../assets/save-audience-3.png)

## 예 {#save-audience-example}

다음 예에서는 타겟팅을 사용하여 간단한 대상자를 만드는 방법을 보여 줍니다. 쿼리는 지난 30일 이내에 구매한 모든 프로필을 식별합니다. 그런 다음 **[!UICONTROL 대상자 저장]** 활동은 이러한 프로필을 캡처하여 최근 구매자의 재사용 가능한 대상자를 만듭니다.

![](../assets/save-audience-4.png)
