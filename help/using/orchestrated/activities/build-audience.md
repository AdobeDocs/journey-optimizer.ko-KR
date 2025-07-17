---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 작성 활동 사용
description: 오케스트레이션된 캠페인에서 대상자 빌드 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 31%

---

# 대상자 빌드 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="대상자 빌드 활동"
>abstract="**대상자 빌드** 활동을 통해 오케스트레이션된 캠페인에 참여할 대상자를 정의할 수 있습니다. 오케스트레이션된 캠페인 컨텍스트에서 메시지를 전송할 때 메시지 대상자는 채널 활동에서 정의되지 않고 **대상자 빌드** 활동에서 정의됩니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](../gs-schemas.md)</li><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - <b>[대상 작성](build-audience.md)</b> - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

마케터는 직관적인 인터페이스를 통해 복잡한 대상 세그먼트를 만들 수 있으므로 다양한 기준과 행동을 기반으로 사용자를 타겟팅하여 캠페인을 보다 효과적으로 조정할 수 있습니다.

이렇게 하려면 **[!UICONTROL 대상자 작성]** 타깃팅 활동을 사용하십시오. 이 활동은 오케스트레이션된 캠페인에 들어가는 대상자를 정의합니다. 오케스트레이션된 캠페인의 일부로 메시지를 보낼 때 대상자는 오케스트레이션된 캠페인 내부가 아닌 **[!UICONTROL 대상자 빌드]** 활동에서 정의됩니다.

## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="새 게재를 디자인할 때 대상자를 사용하는 것과 같은 방식으로 대상자를 선택합니다."

**[!UICONTROL 대상자 빌드]** 활동을 구성하려면 다음 단계를 따르십시오.

1. **[!UICONTROL 대상자 빌드]** 활동을 추가합니다.

   ![](../assets/build-audience.png)

1. **[!UICONTROL 레이블]**&#x200B;을(를) 정의합니다.

1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.

1. **[!UICONTROL 차원 타겟팅]**&#x200B;을 선택합니다. 타기팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타기팅하는 집단을 정의할 수 있습니다. 기본적으로 대상은 수신자 중에서 선택됩니다.

1. **[!UICONTROL 계속을 클릭합니다]**.

1. 쿼리 모델러를 사용하여 쿼리를 정의합니다. [이 섹션에서 쿼리 모델러에 대해 자세히 알아보세요](../orchestrated-rule-builder.md)

1. 대상이 비어 있을 때 아웃바운드 전환을 생성할지 여부를 지정합니다.

## 예시{#build-audience-examples}

다음은 두 개의 **[!UICONTROL 대상자 작성]** 활동으로 오케스트레이션된 캠페인의 예입니다. 첫 번째 타겟은 장바구니에 항목이 있는 프로필이며 이메일 게재가 뒤따릅니다. 두 번째 타겟은 위시리스트 다음에 SMS 게재가 있는 프로필입니다.

![](../assets/build-audience-2.png)
