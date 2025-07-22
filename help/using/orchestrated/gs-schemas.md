---
solution: Journey Optimizer
product: journey optimizer
title: 구성 단계
description: DDL을 업로드하여 Adobe Experience Platform 내에서 관계형 스키마를 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 81f0338935ee36b152963f2b1c0e7989b86f5f8a
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 5%

---

# 스키마 및 데이터 세트 시작{#gs-schemas}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

이 안내서에서는 관계형 스키마를 만들고, 오케스트레이션된 캠페인을 위한 데이터 세트를 구성하고, 데이터를 수집하는 프로세스를 안내합니다.

![](assets/do-not-localize/schema_admin.png)

1. [관계형 스키마를 수동으로 만들기](manual-schema.md) 또는 [DDL 파일 사용](file-upload-schema.md)

   테이블, 속성 및 관계를 포함한 데이터 모델의 구조를 정의합니다. 빠른 설정을 위해 사용자 인터페이스에서 스키마를 수동으로 작성하거나 DDL 파일을 업로드하도록 선택하십시오.

1. [링크 스키마] (file-upload-md)

   스키마 간의 관계를 설정하여 데이터 일관성을 보장하고 엔티티 간 쿼리를 활성화합니다. 예를 들어 충성도 거래를 수신자에게 연결하거나 브랜드를 대상으로 보상을 연결할 수 있습니다.

1. [데이터 수집](ingest-data.md)

   SFTP, 클라우드 스토리지 또는 데이터베이스와 같이 지원되는 소스에서 Adobe Experience Platform으로 데이터를 가져옵니다.

