---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기 및 예약
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 만들고 예약하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 5ebc82f566d416a177a3278816c60d896a10eff6
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 12%

---


# 오케스트레이션된 캠페인 생성 및 예약 {#create-first-campaign}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/><b>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)</b><br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer]에서 오케스트레이션된 캠페인을 만들고 실행 일정을 구성하여 시작 시기와 실행 빈도를 제어합니다. 일일, 주별 또는 월별 빈도 등 유연한 예약 옵션을 사용하여 특정 날짜 및 시간에 캠페인을 즉시 시작하거나, 반복적으로 시작하도록 선택합니다.

## 캠페인 만들기 {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="오케스트레이션된 캠페인 목록"
>abstract="**오케스트레이션** 탭에는 모든 오케스트레이션된 캠페인이 나열됩니다. 오케스트레이션된 캠페인의 이름을 클릭하여 편집할 수 있습니다. 오케스트레이션된 새 캠페인을 추가하려면 **오케스트레이션된 캠페인 만들기** 버튼을 사용합니다."

오케스트레이션된 캠페인을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 캠페인]** 메뉴로 이동하여 **[!UICONTROL 오케스트레이션]** 탭을 선택하고 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

   ![](assets/inventory-create.png)

1. 캠페인의 이름과 설명을 입력합니다.

1. *(선택 사항)* **[!UICONTROL 태그]** 필드를 사용하여 Adobe Experience Platform 통합 태그를 캠페인에 지정하십시오. 이를 통해 오케스트레이션된 캠페인 목록에서 쉽게 분류하고 검색을 개선할 수 있습니다. [태그를 사용하여 작업하는 방법을 알아봅니다](../start/search-filter-categorize.md#tags).

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

이제 오케스트레이션된 캠페인이 만들어지고 오케스트레이션된 캠페인 목록에 표시됩니다. 캠페인 캔버스에서 ![캠페인 설정 아이콘](assets/do-not-localize/campaign-settings.svg) 아이콘을 클릭하여 언제든지 이러한 속성을 업데이트할 수 있습니다.

## 캠페인 예약 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="스케줄러"
>abstract="캠페인 관리자는 특정 시간에 자동으로 캠페인이 시작되도록 일정을 예약하여 마케팅 커뮤니케이션을 위한 정확한 타이밍과 정확한 타기팅 데이터를 확보할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="스케줄러 유효성"
>abstract="스케줄러의 유효 기간을 정의할 수 있습니다. 영구적(기본값)이거나 특정 날짜까지 유효할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="스케줄러 옵션"
>abstract="스케줄러의 빈도를 정의합니다. 특정 순간, 하루에 한 번 또는 여러 번, 일주일 또는 한 달로 실행할 수 있습니다."

기본적으로 오케스트레이션된 캠페인은 수동으로 활성화될 때 시작되고 관련 활동이 실행되면 종료됩니다. 실행을 지연하거나 반복해서 해당 캠페인을 실행하려는 경우 캠페인에 대한 일정을 정의할 수 있습니다.

최적의 성능과 예상 동작을 보장하기 위해 오케스트레이션된 캠페인을 예약할 때 다음 모범 사례를 고려하십시오.

* 오케스트레이션된 캠페인이 전체 시스템 성능을 저해하고 데이터베이스에 블록을 생성할 수 있으므로 15분 간격으로 실행되도록 예약하지 마십시오.
* 오케스트레이션된 캠페인에서 일회성 메시지를 보내려면 **Once**&#x200B;를 실행하도록 설정할 수 있습니다.
* 오케스트레이션된 캠페인에서 반복 메시지를 보내려면 **예약** 옵션을 사용하고 실행 빈도를 설정해야 합니다. 반복 게재 활동에서는 일정을 정의할 수 없습니다.

캠페인 일정을 구성하려면 다음 단계를 수행합니다.

1. 캠페인을 열고 **[!UICONTROL 가능한 빨리]** 단추를 클릭합니다.

   ![](assets/create-schedule.png)

1. 캠페인의 실행 빈도를 선택한 다음 사용 가능한 옵션을 구성합니다. 설정은 선택한 빈도에 따라 다릅니다.

   +++Once

   지정된 날짜 및 시간에 캠페인을 한 번 실행합니다.

   * **[!UICONTROL 날짜]**: 캠페인을 실행할 날짜를 선택하십시오.
   * **[!UICONTROL 시간]**: 캠페인을 실행할 특정 시간을 선택하십시오.

   +++

   +++매일

   매일 또는 선택한 날짜에 캠페인을 실행합니다.

   * **[!UICONTROL 일별 반복]**: 캠페인의 실행 빈도를 선택하십시오.
      * **[!UICONTROL 매일]**: 주말을 포함하여 매일 캠페인을 실행합니다.
      * **[!UICONTROL 평일]**: 월요일부터 금요일까지만 캠페인을 실행합니다.
      * **[!UICONTROL 특정 기간 동안]**: 정의된 날짜 범위(예: 7월 1일부터 7월 15일까지) 내에서 매일 캠페인을 실행합니다. 캠페인이 이 범위를 벗어나면 실행되지 않습니다.
      * **[!UICONTROL 선택한 요일]**: 지정된 요일(예: 월요일, 수요일, 금요일)에만 캠페인을 실행합니다.

   * **[!UICONTROL 시작 시간]**: 매일 캠페인을 실행해야 하는 시간을 정의합니다.

   +++

   +++하루에 여러 번

   같은 날 캠페인을 여러 번 실행합니다. 특정 시간을 선택하거나 주기적 빈도를 설정할 수 있습니다.

   * **[!UICONTROL 선택한 시간]**: 캠페인이 실행되는 특정 시간을 선택하고 일일 반복을 구성합니다(매일 또는 특정 요일에 실행).
   * **[!UICONTROL 정기]**: n분 또는 시간마다 캠페인을 실행하도록 선택합니다. 실행이 허용된 날짜 내에서 시간 범위를 정의할 수도 있습니다.

   +++

   +++매주

   캠페인을 매주 실행하고 특정 날짜에 대한 옵션을 사용할 수 있습니다.

   * **[!UICONTROL 빈도]**: 캠페인을 실행할 빈도(예: 매주, 2주마다)를 선택하십시오.
   * **[!UICONTROL 날짜부터 시작]**: 반복을 시작해야 하는 날짜를 선택합니다.
   * **[!UICONTROL 매일 반복]**: 실행할 특정 요일(예: 매주 월요일 및 목요일)을 선택하십시오.
   * **[!UICONTROL 시작 시간]**: 선택한 날짜에 캠페인을 실행할 시간을 설정합니다.

   +++

   +++월별

   캠페인을 매월 실행하여 특정 날짜에 대한 옵션을 제공합니다.

   * **[!UICONTROL 월별 반복]**: 캠페인이 매월 실행되는지 또는 특정 달에만 실행되는지 여부를 선택합니다.
   * **[!UICONTROL 일별 반복]**:
      * **[!UICONTROL 매일]**: 주말을 포함하여 해당 월의 모든 달력 날짜에 캠페인을 실행합니다.
      * **[!UICONTROL 월의 마지막 날]**: 매월 마지막 달력(예: 1월 31일, 2월 28/29일)에만 캠페인을 실행합니다.
      * **[!UICONTROL 특정 날짜(예: 15일)]**: 지정한 날(예: 매월 15일)에 캠페인을 실행합니다.
      * **[!UICONTROL 첫 번째/마지막 또는 n번째 요일]**(예: 첫 번째 월요일):      지정된 요일(예: 매주 15일)에 캠페인을 실행합니다.
      * **[!UICONTROL 선택한 요일]**: 지정된 날짜에 캠페인을 실행합니다.

   * **[!UICONTROL 시작 시간]**: 캠페인을 실행할 시간을 설정합니다.

   +++

1. **[!UICONTROL 유효 기간]** 설정을 사용하여 특정 시작 및 종료 날짜를 정의하고 제한된 기간 동안 캠페인 실행을 제한합니다.

1. 반복 일정의 경우 **[!UICONTROL 시작 시간 미리 보기]** 단추를 클릭하여 현재 구성을 기반으로 정확한 예정된 실행 날짜 및 시간을 미리 봅니다. 이렇게 하면 활성화 전에 일정을 확인하고 캠페인이 예상대로 실행되는지 확인할 수 있습니다.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]에서 캠페인을 예약할 때 시작 날짜/시간이 원하는 첫 번째 게재에 맞춰졌는지 확인하십시오. 반복 캠페인의 경우 초기 예약 시간이 이미 경과한 경우 캠페인은 반복 규칙에 따라 다음 사용 가능한 시간 슬롯으로 롤오버됩니다.

다음 예제에서는 오케스트레이션된 캠페인이 2025년 10월 1일부터 2026년 1월 1일까지 매주 오전 9시와 12시에 하루에 두 번 실행되도록 활동을 구성합니다.

![오전 9시와 12시에 하루에 두 번 캠페인을 실행하도록 스케줄러가 구성되었습니다](assets/scheduler-sample.png){width="50%" align="left"}

## 다음 단계 {#next}

캠페인 설정 및 일정이 구성되면 수행할 다양한 작업의 오케스트레이션을 시작할 수 있습니다. [캠페인 활동을 오케스트레이션하는 방법을 알아보세요](../orchestrated/orchestrate-activities.md)
