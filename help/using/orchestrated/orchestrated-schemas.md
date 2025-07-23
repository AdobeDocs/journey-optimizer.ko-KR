---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에 대한 관계형 스키마 만들기
description: 오케스트레이션된 캠페인에 대한 관계형 스키마를 만들고 관리하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b0125a50-d187-49fc-ad12-bbe6650f8f1e
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 72%

---

# 관계 스키마 만들기 {#orchestrated-schemas}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[리타기팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[And 조인](activities/and-join.md) - [대상자 빌드](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상자 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

스키마는 데이터의 구조와 형식을 나타내고 검증합니다. 실제 오브젝트(예: 사람)에 대한 추상적인 정의를 제공하고 해당 오브젝트의 각 인스턴스에 포함되어야 하는 데이터(예: 이름, 생일 등)를 간략하게 설명해 줍니다.

![관계형 옵션이 선택된 스키마 만들기 버튼](assets/create-relational-schema.png)
