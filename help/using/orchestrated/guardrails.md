---
solution: Journey Optimizer
product: journey optimizer
title: 조정된 캠페인 보호 및 제한 사항
description: 오케스트레이션된 캠페인 보호 및 제한 사항에 대해 알아봅니다
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 5%

---

# 가드레일 및 제한 사항 {#guardrails}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul><br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 데이터 흐름에서 데이터 세트로의 제한

Adobe Experience Platform의 각 데이터 세트는 한 번에 하나의 활성 데이터 흐름에만 연결할 수 있습니다. 이 1:1 카디널리티는 강단에 의해 엄격히 시행됩니다.

데이터 소스를 전환해야 하는 경우(예: Amazon S3에서 Salesforce으로):

데이터 세트에 연결된 기존 데이터 흐름을 삭제해야 합니다.

그런 다음 동일한 데이터 세트에 매핑된 새 소스로 새 데이터 흐름을 만듭니다.

이렇게 하면 신뢰할 수 있는 데이터 수집이 보장되며, 증분 업데이트를 위해 정의된 기본 키와 버전 관리 속성(예: 마지막으로 수정한 날짜)에 따라 달라지는 CDC(변경 데이터 캡처)를 사용할 때 필수적입니다.


## 관계형 스키마/데이터 수집 제한 사항

* 스키마 수 - 최대 관계형 스키마(관계형 데이터 저장소의 테이블) 수는 200개입니다.
* 관계형 스키마 크기 - Campaign Orchestration의 최대 관계형 스키마 크기는 100GB입니다.
* 데이터 수집 빈도 - Campaign Orchestration에 대한 일괄 데이터 수집 빈도는 15분마다 1개를 초과할 수 없습니다.
* 변경/업데이트 - 일별 업데이트/변경은 주어진 관계형 스키마에 대한 총 레코드의 20% 미만이어야 합니다.
