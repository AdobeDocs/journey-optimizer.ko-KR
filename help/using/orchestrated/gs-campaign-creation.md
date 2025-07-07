---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인을 만드는 주요 단계
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기의 주요 원칙 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 3%

---


# 오케스트레이션된 캠페인을 만드는 주요 단계 {#orchestrated-campaign-creation}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/><b>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md)</b> | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

이 페이지에서는 설정 및 디자인에서 모니터링 및 보고에 이르기까지 오케스트레이션된 캠페인을 구축하고 실행하는 필수 단계를 안내합니다.

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="#create"><img alt="Create & schedule your campaign" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="#create"><strong>Create & schedule your campaign</strong></a></td>
<td><a href="#orchestrate"><img alt="Orchestrate campaign activities" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="#orchestrate"><strong>Orchestrate campaign activities</strong></a></td>
<td><a href="#start"><img alt="Start & monitor your campaign" src="../../channels/assets/do-not-localize/push.png"></a><a href="#start"><strong>Start & monitor your campaign</strong></a></td>
<td><a href="#report"><img alt="Analyze & report on results" src="../../channels/assets/do-not-localize/push.png"></a><a href="#report"><strong>Analyze & report on results</strong></a></td>
</tr></table>-->



## 1단계: 캠페인 만들기 및 예약 {#create}

먼저 오케스트레이션된 캠페인을 만들고 실행해야 하는 *when*&#x200B;을(를) 정의해야 합니다. 1회 푸시든 반복 여정이든 타이밍 및 빈도를 완벽하게 제어할 수 있습니다.

👉 [캠페인을 만들고 예약하는 방법을 알아보세요](../orchestrated/create-orchestrated-campaign.md)

## 2단계: 캠페인 활동 오케스트레이션 {#orchestrate}

캠페인이 만들어지면 그 배후에 있는 논리를 디자인할 차례입니다. 시각적 캔버스를 사용하여 타깃팅, 게재 및 흐름 제어 활동을 결합하여 고객 경험을 구체화할 수 있습니다.

👉 [활동 오케스트레이션 방법 알아보기](../orchestrated/orchestrate-activities.md)

## 3단계: 캠페인 시작 및 모니터링 {#start}

거의 다 되었습니다! 문제를 파악하려면 먼저 테스트 모드에서 캠페인을 실행하십시오. 그런 다음 게시하고 실시간 실행을 실시간으로 모니터링합니다. 진행 상황을 추적하고 오류를 확인한 다음 프로필이 각 단계에서 어떻게 진행되는지 확인하십시오.

👉 [캠페인을 시작하고 모니터링하는 방법 알아보기](../orchestrated/start-monitor-campaigns.md)

## 4단계: 결과 분석 및 보고 {#report}

출시 후 기본 제공 보고서를 사용하여 무엇이 작동하고 개선할 수 있는지 파악합니다. 실시간 대시보드 및 심층적인 분석을 통해 향후 캠페인을 최적화하고 전략을 구체화할 수 있습니다.

👉 [보고에 대해 알아보기](../orchestrated/reporting-campaigns.md)
