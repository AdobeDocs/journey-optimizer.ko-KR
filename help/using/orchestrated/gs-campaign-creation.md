---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 생성을 위한 주요 단계
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기의 주요 원칙 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 27%

---


# 오케스트레이션된 캠페인 생성을 위한 주요 단계 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="오케스트레이션된 캠페인"
>abstract="이 화면에서 오케스트레이션된 캠페인의 전체 목록에 액세스하고 현재 상태, 마지막/다음 실행 일자를 확인하고 오케스트레이션된 새 캠페인을 만들 수 있습니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md) | [오케스트레이션된 캠페인 만들기](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [쿼리 Modeler 작업](orchestrated-query-modeler.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

오케스트레이션된 캠페인을 시각적 캔버스로 빌드하여 세그멘테이션, 캠페인 실행 및 파일 처리와 같은 크로스 채널 프로세스를 디자인할 수 있습니다.

## 오케스트레이션된 캠페인 액세스

**[!UICONTROL 캠페인]** 메뉴에서 여러 단계 탭으로 이동하여 오케스트레이션된 캠페인의 전체 목록에 액세스합니다.

목록의 오케스트레이션된 각 캠페인에는 현재 [상태](#status), 마지막으로 실행되거나 수정된 시간 및 다음에 예약된 실행 날짜와 시간에 대한 정보가 표시됩니다.

목록의 오른쪽 상단에 있는 **[!UICONTROL 사용자 정의 레이아웃에 대한 열 구성]** 아이콘을 클릭하여 표시된 열을 사용자 정의할 수 있습니다. 이렇게 하면 오케스트레이션된 각 캠페인에 대한 마지막 활동 오류 또는 적용된 타겟팅 차원과 같은 추가 정보를 목록에 추가할 수 있습니다.

또한 목록에서 쉽게 검색할 수 있도록 검색 창과 필터를 사용할 수 있습니다. 예를 들어, 오케스트레이션된 캠페인을 필터링하여 캠페인에 속하는 캠페인이나 특정 날짜 범위 동안 처리된 캠페인만 표시할 수 있습니다.

오케스트레이션된 캠페인을 복제하거나 삭제하려면 줄임표 버튼을 클릭한 다음 **[!UICONTROL 복제]** 또는 **[!UICONTROL 삭제]**&#x200B;를 선택하십시오.

>[!NOTE]
>
>오케스트레이션된 캠페인이 진행 중인 경우 복제할 수 있지만 삭제할 수는 없습니다.

## 오케스트라 캠페인의 내부는 무엇입니까? {#gs-ms-campaign-inside}

오케스트레이션된 캠페인 캔버스는 일어날 일을 표현한 것입니다. 앞으로 수행할 다양한 작업과 이러한 작업이 어떻게 서로 연결되어 있는지 설명합니다.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

오케스트레이션된 각 캠페인에는 다음이 포함됩니다.

* **활동**: 활동은 수행할 작업입니다. 다양한 활동이 다이어그램에 아이콘으로 표시됩니다. 각 활동에는 특정 속성과 모든 활동에 공통되는 다른 속성이 있습니다.

  오케스트레이션된 캠페인 다이어그램에서 주어진 활동은 여러 작업, 특히 반복이나 반복 작업이 있는 작업을 생성할 수 있습니다.

* **전환**: 전환은 원본 활동을 대상 활동에 연결하고 해당 시퀀스를 정의합니다.

* **작업 테이블**: 작업 테이블에는 전환에 의해 전달되는 모든 정보가 포함됩니다. 오케스트레이션된 각 캠페인에서는 몇 개의 작업 테이블을 사용합니다. 이러한 표에 전달된 데이터는 오케스트레이션된 캠페인의 수명 주기 전체에서 사용할 수 있습니다.

## 상태 및 라이프사이클 {#status}

캠페인은 여러 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 오케스트레이션된 캠페인을 만들고 저장했습니다.
* **[!UICONTROL 진행 중]**: 오케스트레이션된 캠페인이 현재 실행 중입니다.
* **[!UICONTROL 완료됨]**: 오케스트레이션된 캠페인 실행이 완료되었습니다.
* **[!UICONTROL 일시 중지됨]**: 오케스트레이션된 캠페인이 일시 중지되었습니다.
* **[!UICONTROL 오류]**: 오케스트레이션된 캠페인에 오류가 발생했습니다. 오케스트레이션된 캠페인을 열고 로그 및 작업에 액세스하여 오류를 식별하고 해결합니다.
