---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에 대한 관계형 스키마 만들기
description: 오케스트레이션된 캠페인에 대한 관계형 스키마를 만들고 관리하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b0125a50-d187-49fc-ad12-bbe6650f8f1e
source-git-commit: f8fa52c89659918ef3837f88ddb03c219239f4ee
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 38%

---

# 관계 스키마 만들기 {#orchestrated-schemas}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

스키마는 데이터의 구조와 형식을 나타내고 검증합니다. 실제 오브젝트(예: 사람)에 대한 추상적인 정의를 제공하고 해당 오브젝트의 각 인스턴스에 포함되어야 하는 데이터(예: 이름, 생일 등)를 간략하게 설명해 줍니다.

![관계형 옵션이 선택된 스키마 만들기 단추](assets/create-relational-schema.png)
