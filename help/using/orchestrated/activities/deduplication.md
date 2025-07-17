---
solution: Journey Optimizer
product: journey optimizer
title: 중복 제거 활동 사용
description: 중복 제거 활동을 사용하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 6eb49e954b7906f668b1c1779c16f3e67003307b
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 31%

---

# 중복 제거 {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="중복 요소 식별을 위한 필드"
>abstract="**중복 요소 식별을 위한 필드** 섹션에서 **속성 추가** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="중복 제거 활동"
>abstract="**중복 제거** 활동을 통해 인바운드 활동의 결과에서 중복 요소를 삭제할 수 있습니다. 주로 타기팅 활동 이후와 대상 데이터를 사용할 수 있는 활동 이전에 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="여집합 생성"
>abstract="중복으로 제외된 나머지 집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="중복 제거 설정"
>abstract="수신 데이터에서 중복 요소를 삭제하려면 아래 필드에서 중복 제거 방법을 정의합니다. 기본적으로 하나의 레코드만 유지됩니다. 또한 표현식 또는 속성을 기반으로 중복 제거 모드를 선택해야 합니다. 기본적으로 중복에서 제외할 레코드는 무작위로 선택됩니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul><br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - <b>[중복 제거](deduplication.md)</b> - [데이터 보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**[!UICONTROL 중복 제거]** 활동은 **[!UICONTROL 타깃팅]** 활동입니다. 이 활동을 사용하면 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다(예: 수신자 목록에서 중복된 프로필). **[!UICONTROL 중복 제거]** 활동은 일반적으로 타겟팅 활동 다음부터 타겟팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

## 중복 제거 활동 구성{#deduplication-configuration}

**[!UICONTROL 중복 제거]** 활동을 구성하려면 다음 단계를 따르십시오.


1. 오케스트레이션된 캠페인에 **[!UICONTROL 중복 제거]** 활동을 추가합니다.

1. **[!UICONTROL 중복 요소 식별을 위한 필드]** 섹션에서 **[!UICONTROL 속성 추가]** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다.

   ![](../assets/deduplication-1.png)

1. **[!UICONTROL 중복 제거 설정]** 섹션에서 [중복을 사용하여 유지할 레코드 수] 필드를 선택합니다. 기본값은 1이며, 이 경우 중복 그룹당 하나의 레코드가 유지됩니다. 모든 중복을 유지하려면 0으로 설정합니다.

   예를 들어 레코드 A와 B가 Y의 중복이고 레코드 C가 Z의 중복인 경우:

   * **필드 값이 1**&#x200B;인 경우: Y 및 Z 레코드만 유지됩니다.
   * **필드 값이 0**&#x200B;인 경우: 모든 레코드(A, B, C, Y, Z)가 유지됩니다.
   * **필드 값이 2인 경우**: C와 Z는 유지되고 A, B, Y의 두 값은 임의로 또는 중복 제거 방법에 따라 유지됩니다.

1. **[!UICONTROL 중복 제거 방법]**&#x200B;을 선택하세요. 각 중복 그룹에서 유지할 레코드를 시스템에서 결정하는 방법을 정의합니다.

   * **[!UICONTROL 무작위 선택]**: 중복 중에서 유지할 레코드를 임의로 선택합니다.
   * **[!UICONTROL 식 사용]**: 사용자가 정의한 식을 기준으로 값이 가장 높거나 가장 낮은 레코드를 유지합니다.
   * **[!UICONTROL 비어 있지 않은 값]**: 선택한 필드가 비어 있지 않은 레코드를 유지합니다(예: 전화 번호가 있는 프로필만 유지).
   * **[!UICONTROL 값 목록 팔로우]**: 하나 이상의 필드에 대해 특정 값의 우선 순위를 지정할 수 있습니다. 예를 들어 &quot;국가&quot;가 프랑스로 설정된 레코드에 우선 순위를 지정할 수 있습니다. 필드를 선택하거나 사용자 지정 식을 만들려면 **[!UICONTROL 특성]**&#x200B;을(를) 클릭하십시오. **[!UICONTROL 추가 단추]**&#x200B;를 사용하여 우선 순위 순서대로 기본 설정 값을 입력하십시오.

   ![](../assets/deduplication-2.png)

1. 나머지 모집단을 활용하려면 **[!UICONTROL 보조 항목 생성]** 옵션을 선택하십시오. 보완은 모든 중복으로 구성됩니다. 그런 다음 추가 전환이 활동에 추가됩니다.

## 예{#deduplication-example}

다음 예제에서는 **[!UICONTROL 중복 제거]** 활동을 사용하여 게재를 보내기 전에 대상 대상에서 중복 레코드를 제거합니다. 대상자는 먼저 비어 있지 않은 이메일 필드가 있는 프로필만 포함하도록 필터링됩니다. 그런 다음 **[!UICONTROL 중복 제거]** 활동에서는 전자 메일 주소를 사용하여 중복을 식별하고 제외합니다.

![](../assets/deduplication-3.png)
