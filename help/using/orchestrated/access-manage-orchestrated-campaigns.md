---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에 액세스 및 관리
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기의 주요 원칙 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 5ebc82f566d416a177a3278816c60d896a10eff6
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 21%

---

# 오케스트레이션된 캠페인에 액세스 및 관리 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="오케스트레이션된 캠페인"
>abstract="이 화면에서 오케스트레이션된 캠페인의 전체 목록에 액세스하고 현재 상태, 마지막/다음 실행 일자를 확인하고 오케스트레이션된 새 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="작업"
>abstract="이 섹션에는 오케스트레이션된 캠페인 내부에서 사용되는 모든 액션이 나열됩니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/><b>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)</b> | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## 오케스트레이션된 캠페인 액세스

**[!UICONTROL 캠페인]** 메뉴로 이동한 다음 **[!UICONTROL 오케스트레이션]** 탭을 선택하여 오케스트레이션된 캠페인의 전체 목록에 액세스합니다.

![오케스트레이션된 캠페인 인벤토리를 보여 주는 이미지](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

목록에서 오케스트레이션된 각 캠페인에는 캠페인의 현재 [상태](#status), 연결된 채널 및 태그 또는 마지막으로 수정한 시간 등의 정보가 표시됩니다. ![레이아웃 구성 단추](assets/do-not-localize/inventory-configure-layout.svg) 단추를 클릭하여 표시된 열을 사용자 지정할 수 있습니다.

또한 목록에서 쉽게 검색할 수 있도록 검색 창과 필터를 사용할 수 있습니다. 예를 들어, 오케스트레이션된 캠페인을 필터링하여 지정된 채널 또는 태그와 연결된 캠페인 또는 특정 날짜 범위 동안 만들어진 캠페인만 표시할 수 있습니다.

캠페인 인벤토리의 추가 작업 단추![ 단추를 표시하는 ](assets/do-not-localize/rule-builder-icon-more.svg)이미지를 사용하면 아래에 설명된 다양한 작업을 수행할 수 있습니다.

![캠페인 인벤토리 이미지](assets/inventory-actions.png)

* **[!UICONTROL 모든 시간 보고서 보기]** / **[!UICONTROL 최근 24시간 보고서 보기]** - 보고서에 액세스하여 오케스트레이션된 캠페인의 영향과 성능을 측정하고 시각화할 수 있습니다. [오케스트레이션된 캠페인 보고에 대한 자세한 정보](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL 태그 편집]** - 캠페인에 연결된 태그를 편집합니다.
* **[!UICONTROL 복제]** - 경우에 따라 오케스트레이션된 캠페인을 복제해야 합니다. 예를 들어 중지된 캠페인을 실행하거나 예약된 캠페인의 실행 빈도를 변경할 수 있습니다.
* **[!UICONTROL 삭제]** - 캠페인을 삭제합니다. 이 작업은 **[!UICONTROL 초안]** 캠페인에서만 사용할 수 있습니다.
* **[!UICONTROL 보관]** - 캠페인을 보관합니다. 보관된 모든 캠페인은 마지막 수정 날짜 후 30일 후에 정기 일정에 따라 삭제됩니다. 이 작업은 **[!UICONTROL 초안]** 캠페인을 제외한 모든 캠페인에 사용할 수 있습니다.

## 오케스트라 캠페인의 내부는 무엇입니까? {#gs-ms-campaign-inside}

오케스트레이션된 캠페인 캔버스는 일어날 일을 표현한 것입니다. 앞으로 수행할 다양한 작업과 이러한 작업이 어떻게 서로 연결되어 있는지 설명합니다.

![오케스트레이션된 캠페인 캔버스를 표시하는 이미지](assets/canvas-example.png)

오케스트레이션된 각 캠페인에는 다음이 포함됩니다.

* **활동**: 활동은 수행할 작업입니다. 다양한 활동이 다이어그램에 아이콘으로 표시됩니다. 각 활동에는 특정 속성과 모든 활동에 공통되는 다른 속성이 있습니다.

  오케스트레이션된 캠페인 다이어그램에서 주어진 활동은 여러 작업, 특히 반복이나 반복 작업이 있는 작업을 생성할 수 있습니다.

* **전환**: 전환은 원본 활동을 대상 활동에 연결하고 해당 시퀀스를 정의합니다.

* **작업 테이블**: 작업 테이블에는 전환에 의해 전달되는 모든 정보가 포함됩니다. 오케스트레이션된 각 캠페인에서는 몇 개의 작업 테이블을 사용합니다. 이러한 표에 전달된 데이터는 오케스트레이션된 캠페인의 수명 주기 전체에서 사용할 수 있습니다.

## 캠페인 상태 {#status}

오케스트레이션된 캠페인은 여러 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 오케스트레이션된 캠페인이 만들어졌습니다. 아직 게시되지 않았습니다.
* **[!UICONTROL 게시]**: 오케스트레이션된 캠페인이 게시되고 있습니다.
* **[!UICONTROL Live]**: 오케스트레이션된 캠페인이 게시되어 실행 중입니다.
* **[!UICONTROL 예약됨]**: 오케스트레이션된 캠페인 실행이 예약되었습니다.
* **[!UICONTROL 완료됨]**: 오케스트레이션된 캠페인 실행이 완료되었습니다. 완료 상태는 캠페인이 오류 없이 메시지 전송을 완료한 후 최대 3일까지 자동으로 할당됩니다.
* **[!UICONTROL 닫힘]**: 이 상태는 반복 캠페인이 닫혔을 때 표시됩니다. 캠페인은 모든 활동이 완료될 때까지 실행을 계속하지만 더 이상 프로필이 캠페인을 입력할 수 없습니다.
* **[!UICONTROL 보관됨]**: 오케스트레이션된 캠페인이 보관되었습니다. 보관된 모든 캠페인은 마지막 수정 날짜 후 30일 후에 정기 예약이 삭제됩니다. 필요한 경우 보관된 캠페인을 복제하여 계속 작업할 수 있습니다.
* **[!UICONTROL 중지됨]**: 오케스트레이션된 캠페인 실행이 중지되었습니다. 캠페인을 다시 시작하려면 복제해야 합니다. 시에르외르레스테라아베크삼각형
