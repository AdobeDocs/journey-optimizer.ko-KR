---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer을 사용하여 오케스트레이션된 캠페인에서 메시지 테스트 및 유효성 검사
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인에서 증명을 보내고, 콘텐츠 및 개인화를 확인하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 54d8b2fb-745d-459c-85d6-c224aa5e352e
source-git-commit: f64fa51fa753fe62eecb6199946615f4d5c4f767
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 11%

---

# 메시지 테스트 및 유효성 검사 {#orchestrated-proofs}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

설명서 진행 중

>[!ENDSHADEBOX]

캠페인 관리자는 미리 정의된 내부 검토자 목록에 개인화된 메시지의 **증명 버전**&#x200B;을 전송하여 모든 콘텐츠, 개인화 및 링크가 본격적인 시작 전에 예상대로 작동하도록 할 수 있습니다.
