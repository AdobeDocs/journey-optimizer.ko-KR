---
solution: Journey Optimizer
product: journey optimizer
title: 분할 활동 사용
description: 오케스트레이션된 캠페인에서 분할 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: e71cbc5b29a31e2f23b408ae8c8b73379a44275d
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 77%

---

# 분할 {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="분할 활동"
>abstract="**분할** 활동은 필터링 규칙 또는 집단 크기와 같은 다양한 선택 기준에 따라 수신 집단을 여러 하위 집합으로 세그먼트화할 수 있습니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](../gs-schemas.md)</li><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[리타기팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[And 조인](and-join.md) - [대상자 빌드](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상자 저장](save-audience.md) - <b>[분할](split.md)</b> - [대기](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**[!UICONTROL 분할]** 활동은 필터링 규칙 또는 집단 크기와 같은 다양한 선택 기준에 따라 들어오는 집단을 여러 하위 집합으로 세분화할 수 있는 **[!UICONTROL 타기팅]** 활동입니다.

## 분할 활동 구성 {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="분할 활동용 세그먼트"
>abstract="수신 집단을 세그먼트로 나누려면 원하는 만큼 하위 집합을 추가합니다.<br/></br>**분할** 활동이 실행되면 집단이 활동에 추가된 순서대로 여러 하위 집합에 걸쳐 세그먼트로 나뉩니다. 오케스트레이션된 캠페인을 시작하기 전에 화살표 버튼을 사용하여 필요에 맞는 순서로 하위 세트를 정렬했는지 확인하십시오."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="분할 활동 필터"
>abstract="하위 집합에 필터링 조건을 적용하려면 **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하고 규칙 빌더를 사용하여 원하는 필터링 규칙을 구성합니다. 예를 들어 데이터베이스에 이메일 주소가 존재하는 수신 집단의 프로필을 포함합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="분할 활동 제한"
>abstract="하위 집합에서 선택한 프로필 수를 제한하려면 **[!UICONTROL 제한 활성화]** 옵션을 토글하고 포함할 집단의 수 또는 백분율을 지정합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="분할 활동 정렬"
>abstract="하위 집합에 대해 집단 제한을 설정할 때 특정 프로필 속성을 기준으로 선택한 프로필의 등급을 오름차순 또는 내림차순으로 지정할 수 있습니다. 이렇게 하려면 정렬 활성화 옵션을 토글합니다. 이렇게 하려면 **정렬 활성화** 옵션을 토글합니다. 예를 들어 구매 금액이 가장 높은 상위 50개 프로필만 포함하도록 하위 집합을 제한할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="여집합 생성 분할"
>abstract="모든 하위 집합을 구성한 후에는 하위 집합과 일치하지 않는 나머지 집단을 선택하여 추가 아웃바운드 전환에 포함할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="동일 테이블의 모든 하위 집합 생성"
>abstract="모든 하위 집합을 단일 출력 전환으로 그룹화하려면 이 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="빈 전환 건너뛰기"
>abstract="수신 집단이 비어 있는 경우, **[!UICONTROL 빈 전환 건너뛰기]** 옵션을 토글하여 이 하위 집합에 대한 출력 전환을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="출력 집단의 중복 활성화"
>abstract=" **[!UICONTROL 출력 집단의 중복 활성화]** 옵션을 사용하면 여러 하위 집합에 속하는 집단을 관리할 수 있습니다. 확인란을 선택하지 않으면 분할 활동은 수신자가 여러 하위 집합의 기준을 충족하더라도 여러 출력 전환에 표시되지 않습니다. 기준이 일치하는 첫 번째 탭의 대상에 포함됩니다. 확인란을 선택하면 필터 조건을 충족하는 경우 여러 하위 집합에서 수신자를 찾을 수 있습니다."

**[!UICONTROL 분할]** 활동을 구성하려면 다음 단계를 따릅니다.

1. 오케스트레이션된 캠페인에 **[!UICONTROL 분할]** 활동을 추가합니다.

1. 활동 구성 창이 기본 하위 집합과 함께 열립니다. 수신 모집단을 세그먼트화하기 위해 원하는 만큼 하위 집합을 추가하려면 **[!UICONTROL 세그먼트 추가]** 버튼을 클릭합니다.

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >**분할** 활동은 하위 집합을 추가된 순서대로 처리합니다. 예를 들어 첫 번째 하위 집합이 집단의 70%를 포함하면 그 다음 하위 집합은 나머지 30%에 기준을 적용합니다.
   >
   >오케스트레이션된 캠페인을 실행하기 전에 하위 집합의 순서가 의도한 대로 지정되어 있는지 확인하십시오. 화살표 버튼을 사용하여 하위 집합의 위치를 조정합니다.

1. 하위 집합이 추가되면 해당 활동은 하위 집합만큼이 출력 전환을 표시합니다. 오케스트레이션된 캠페인 캔버스에서 쉽게 식별할 수 있도록 각 하위 세트의 레이블을 변경하는 것이 좋습니다.

1. 각 하위 집합에 대한 필터 구성:

   1. 하위 집합을 클릭하여 설정을 엽니다.

   1. **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하여 규칙 빌더를 사용하여 필터링 규칙을 정의합니다. 예를 들어 올바른 전자 메일 주소가 있는 프로필을 선택합니다.

      ![](../assets/orchestrated-split-1.png)

   1. 선택하는 프로필의 수를 제한하려면 **[!UICONTROL 제한 활성화]**&#x200B;를 사용하도록 설정하고 숫자나 백분율을 지정합니다.

   1. 하위 집합이 비어 있을 때 전환을 건너뛰려면 **[!UICONTROL 빈 전환 건너뛰기]를 활성화합니다.**

1. 어떤 하위 집합과도 일치하지 않는 프로필을 포함하려면 **[!UICONTROL 여집합 생성]**&#x200B;을 활성화합니다. 이렇게 하면 나머지 집단에 대한 추가 아웃바운드 전환이 만들어집니다.

   >[!NOTE]
   >
   >**[!UICONTROL 모든 하위 집합을 동일한 테이블에 생성]**&#x200B;을 활성화하면 모든 하위 집합을 단일 전환으로 그룹화합니다.

1. 프로필이 여러 하위 집합에 표시되도록 하려면 **[!UICONTROL 결과 집단 오버랩 활성화]**&#x200B;를 사용합니다.

   * **선택하지 않는 경우** 각 프로필은 하나의 하위 집합에만 할당되며, 다른 하위 집합에 들어갈 수 있더라도 기준이 일치하는 첫 번째 하위 집합에만 할당됩니다.

   * **선택하는 경우** 프로필이 각 하위 집합에 대한 조건을 충족하기만 하면 여러 하위 집합에 포함시킬 수 있습니다.

이제 활동이 구성되었습니다. 오케스트레이션된 캠페인 실행에서 모집단은 활동에 추가된 순서로 다른 하위 집합으로 분할됩니다.

## 예{#split-example}

다음 예에서는 **[!UICONTROL 분할]** 활동을 통해 사용하려는 커뮤니케이션 채널을 기반으로 대상자를 별개의 하위 집합으로 세그먼트화합니다.

* **하위 집합 1 “이메일”**: 전화번호를 입력한 프로필을 포함합니다.

* **하위 집합 2 “sms”**: 데이터베이스에 휴대폰 번호가 저장된 프로필을 타기팅합니다.

* **여집합 전환**: 하위 집합 기준을 충족하지 않는 나머지 프로필을 캡처합니다.

![](../assets/orchestrated-split-3.png)
