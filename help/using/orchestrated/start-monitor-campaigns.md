---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer로 오케스트레이션된 캠페인 시작 및 모니터링
description: Adobe Journey Optimizer를 사용하여 오케스트레이션된 캠페인을 시작하고 모니터링하는 방법을 알아봅니다.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 73%

---

# 오케스트레이션된 캠페인 시작 및 모니터링 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="오케스트레이션된 캠페인 게시"
>abstract="캠페인을 시작하려면 먼저 캠페인을 게시해야 합니다. 게시하기 전에 모든 오류가 해결되었는지 확인하십시오."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/><b>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)</b><br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[리타기팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[And 조인](activities/and-join.md) - [대상자 빌드](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상자 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

오케스트레이션된 캠페인을 만들고 캔버스에서 수행할 작업을 디자인하면 캠페인을 게시하고 실행이 어떻게 이루어지는지 모니터링할 수 있습니다.

테스트 모드에서 캠페인을 실행하여 캠페인 실행과 다양한 활동의 결과를 확인할 수도 있습니다.

## 게시하기 전에 캠페인 테스트 {#test}

[!DNL Journey Optimizer]을(를) 사용하면 시작하기 전에 오케스트레이션된 캠페인을 테스트할 수 있습니다. 캠페인이 만들어지면 기본적으로 **초안** 상태가 됩니다. 이 상태에서는 캠페인을 수동으로 실행하여 흐름을 테스트할 수 있습니다.

**[!UICONTROL 대상자 저장]** 활동 및 채널 활동을 제외한 캔버스의 모든 활동이 실행됩니다. 데이터나 대상자에게는 기능적인 영향을 주지 않습니다.

캠페인을 테스트하는 방법:

1. 오케스트레이션된 캠페인을 엽니다.
2. **[!UICONTROL 시작]**&#x200B;을 클릭합니다.

![](assets/campaign-start.png){zoomable="yes"}

캠페인의 각 활동은 다이어그램의 끝에 도달할 때까지 순차적으로 실행됩니다.

테스트 중에 캔버스에서 작업 표시줄을 사용하여 캠페인 실행을 제어할 수 있습니다. 여기에서는 다음을 수행할 수 있습니다.

* 언제든지 실행을 **중지**&#x200B;합니다.
* 실행을 다시 **시작**&#x200B;합니다.
* 이전에 문제로 인해 일시 중지된 실행을 **다시 시작**&#x200B;합니다.

실행 중에 오류 또는 경고가 발생하면 캔버스 도구 모음의 **[!UICONTROL 경보]** / **[!UICONTROL 경고]** 아이콘을 통해 알림을 받습니다.

![](assets/campaign-warning.png){zoomable="yes"}

각 활동에 직접 표시되는 [시각적 상태 표시기](#activities)를 사용하여 실패한 활동을 빠르게 식별할 수도 있습니다. 자세한 문제 해결 방법이 필요한 경우 오류와 오류 발생 컨텍스트에 대해 상세한 정보를 제공하는 [캠페인의 로그](#logs-tasks)를 엽니다.

유효성을 검사하면 캠페인을 게시할 수 있습니다.

## 캠페인 게시 {#publish}

캠페인을 테스트하여 준비가 완료되면 **[!UICONTROL 게시]**&#x200B;를 클릭하여 라이브로 만듭니다.

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>**[!UICONTROL 게시]** 단추가 비활성화되어 있으면(회색으로 표시됨) 작업 표시줄에서 로그에 액세스하고 오류 메시지를 확인하십시오. 캠페인을 게시하려면 먼저 모든 오류를 수정해야 합니다.

시각적 흐름이 다시 시작되고, 실제 프로필이 실시간으로 여정을 따라 흐르기 시작합니다.

게시 작업이 실패하는 경우(예: 메시지 콘텐츠 누락) 경고 메시지가 표시되며 문제를 해결한 후 다시 시도해야 합니다. 게시 성공 시 캠페인은 즉시 또는 일정에 따라 실행을 시작하고 **초안**&#x200B;에서 **라이브** 상태로 이동하고 &quot;읽기 전용&quot;이 됩니다.

## 캠페인 실행 모니터링 {#monitor}

### 시각적 흐름 모니터링 {#flow}

테스트 또는 라이브 모드에서 실행하는 동안에는 시각적 흐름을 통해 프로필이 실시간으로 여정을 따라 움직이는 모습을 볼 수 있습니다. 작업 간에 전환되는 프로필 수가 표시됩니다.

![](assets/workflow-execution.png){zoomable="yes"}

전환을 통해 한 활동에서 다른 활동으로 전송된 데이터는 임시 작업 테이블에 저장됩니다. 각 전환에 대해 이 데이터를 표시할 수 있습니다. 활동 간에 전달된 데이터를 확인하는 방법은 다음과 같습니다.

1. 전환을 선택합니다.
1. 작업 테이블 스키마를 보려면 속성 창에서 **[!UICONTROL 스키마 미리 보기]**&#x200B;를 클릭합니다. 전송된 데이터를 보려면 **[!UICONTROL 결과 미리 보기]**&#x200B;를 선택합니다.

![](assets/transition.png){zoomable="yes"}

### 활동 실행 표시기 {#activities}

시각적 상태 표시기는 각 활동이 어떻게 수행되고 있는지 이해하는 데 도움이 됩니다.

| 시각적 표시기 | 설명 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 활동이 현재 실행 중입니다. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 이 활동에는 주의가 필요합니다. 이 주의에는 게재 전송을 확인하거나 필요한 조치를 취하는 작업이 포함될 수 있습니다. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 활동에서 오류가 발생했습니다. 문제를 해결하려면 오케스트레이션된 캠페인 로그를 열어 자세한 내용을 확인합니다. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 활동이 성공적으로 실행되었습니다. |

### 로그 및 작업 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="로그 및 작업"
>abstract="**로그 및 작업** 화면은 모든 사용자 액션과 발생한 오류를 기록하며 오케스트레이션된 캠페인 실행의 기록을 제공합니다."

로그 및 작업 모니터링은 오케스트레이션된 캠페인을 분석하여 제대로 실행되고 있는지 확인하기 위해 중요한 단계입니다. 캔버스 도구 모음의 테스트 및 라이브 모드 모두, 또는 각 활동의 속성 창에서 사용할 수 있는 **[!UICONTROL 로그]** 버튼을 통해 로그 및 작업에 액세스할 수 있습니다.

**[!UICONTROL 로그 및 작업]** 화면은 모든 사용자 액션과 발생한 오류를 기록하여 캠페인 실행에 대한 완전한 기록을 제공합니다.

![](assets/workflow-logs.png){zoomable="yes"}

다음과 같은 두 가지 정보를 사용할 수 있습니다.

* **[!UICONTROL 로그]** 탭에는 모든 작업 및 오류의 시간순 기록이 포함되어 있습니다.
* **[!UICONTROL 작업]** 탭에서는 활동의 단계별 실행 시퀀스를 자세히 설명합니다.

두 탭 모두에서 표시된 열과 그 순서를 선택하고 필터를 적용하고 검색 필드를 사용하여 원하는 정보를 빠르게 찾을 수 있습니다.
