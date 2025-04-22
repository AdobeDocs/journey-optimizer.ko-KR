---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 시작
description: 오케스트레이션된 캠페인으로 시작하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: d75e1fdda85c2e29c53fbabf4d33efeb48a786ab
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 16%

---

# 오케스트레이션된 캠페인 시작 {#ms-camp}

>[!BEGINSHADEBOX]

**목차**

* 오케스트레이션된 캠페인 시작
* 구성
   * [오케스트레이션된 캠페인 구성](gs-campaign-config.md)
   * [관계형 스키마 만들기](ms-schemas.md)
* 오케스트레이션된 첫 번째 캠페인 만들기
   * [주요 원칙](gs-campaign-creation.md)
   * [오케스트레이션된 캠페인 만들기](create-ms-campaign.md)
   * [캠페인 설정 구성](ms-campaign-settings.md)
   * [활동 시작](activities/about-activities.md)
   * [활동 오케스트레이션](orchestrate-activities.md)
* [메시지 개인화](ms-personalization.md)
* [쿼리 작성](ms-query-modeler.md)
* [메시지 테스트 및 유효성 검사](ms-proofs.md)
* [캠페인 예약 및 시작](start-monitor-campaigns.md)
* 활동 목록: [및 연결](activities/and-join.md) - [대상 빌드](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [채널 작업](activities/channels.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [파일 로드](activities/load-file.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [테스트](activities/test.md) - [대기](activities/wait.md)
* [보고](reporting-campaigns.md)

>[!ENDSHADEBOX]

오케스트레이션된 캠페인은 강력한 브랜드가 시작한 일괄 캠페인 기능을 도입하여 Adobe Journey Optimizer을 향상하므로 고급 세분화 전략을 사용하여 크로스 채널 캠페인을 계획하고 오케스트레이션할 수 있습니다.

## 오케스트레이션된 캠페인이란?

크로스 채널 마케팅은 고객에게 효과적으로 다가가고자 하는 모든 비즈니스에 필수적입니다. Adobe Journey Optimizer은 마케팅 캠페인을 쉽게 관리하는 데 도움이 되는 복잡한 프로세스를 디자인할 수 있는 포괄적인 그래픽 환경을 제공합니다. 오케스트레이션된 캠페인을 통해 프로세스 및 작업의 전체 범위를 오케스트레이션하고, 세그먼트 만들기, 메시지 준비에서 게재에 이르기까지 마케팅 캠페인의 모든 측면에 대한 속도와 규모를 개선할 수 있습니다. 또한 캠페인 오케스트레이션을 위해 사용하기 쉬운 단일 인터페이스로 채널을 동기화할 수 있습니다.

오케스트레이션된 캠페인의 가장 큰 장점 중 하나는 모든 채널에서 고객에게 개인화된 콘텐츠를 간단하게 전달할 수 있다는 것입니다. 고객이 이메일을 통해 메시지를 수신하든 아니면 모바일을 통해 메시지를 수신하든 Adobe Journey Optimizer을 통해 모든 채널에서 일관되고 상황에 맞는 경험을 제공할 수 있으므로 모든 고객의 여정을 고유한 경험으로 변환할 수 있습니다.

오케스트레이션된 캠페인은 다용도가 뛰어나고, 대상을 관리하거나 메시지를 보내는 타겟팅, 데이터를 조작하는 데이터 관리(ETL) 및 데이터 가져오기를 비롯한 다양한 컨텍스트에서 사용할 수 있습니다.

포괄적인 그래픽 환경을 통해 세분화, 캠페인 실행, 파일 처리 등의 프로세스를 디자인할 수 있습니다. 오케스트레이션된 캠페인에는 작업을 할당하거나 수행된 작업을 승인하도록 하여 사용자를 참여시킬 수도 있으므로, 팀의 작업을 보다 쉽게 관리하고 모든 작업이 올바르게 수행되도록 보장합니다.


## 여정 편성 및 캠페인 편성

Campaign Orchestration은 대규모로 브랜드 커뮤니케이션을 디자인, 전송 및 추적하는 선도적인 모듈입니다. 프로필 및 비프로필 엔티티를 결합하여 효과적인 개인화를 위해 기존 데이터 세그먼트를 활용하여 타겟팅된 대상자에게 마케팅 메시지를 자동으로 배포할 수 있습니다. 캠페인 중심 활동에 적합한 Campaign Orchestration은 일관되고 효율적인 메시지 전달(종종 미리 예약됨)을 보장하여 고객 참여를 유도하고 주요 마케팅 목표를 지원합니다.

Campaign Orchestration은 다중 엔터티를 Adobe Journey Optimizer으로 활성화하여 대상 세분화를 재정의하고 특정 상태, 이벤트, 계약 또는 예약 등에 따라 타겟팅된 메시징을 용이하게 합니다. 프로필 이외의 엔티티에 커뮤니케이션을 보내거나 엔티티에 대한 쿼리를 만들 수 있으므로 전체 보기를 가지고 광범위한 통찰력을 캡처하여 대상을 구축할 수 있습니다.

Campaign Orchestration은 데이터 중심의 의사 결정을 가능하게 하며, 동적 강화 데이터 세트에 대해 여러 소스를 활용합니다.


## 더 자세히 알아보기

워크플로가 무엇인지, Adobe Campaign에서 워크플로를 통해 무엇을 할 수 있는지 이해했으므로 이제 해당 설명서 섹션을 자세히 살펴보고 기능을 사용하여 작업을 시작할 차례입니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="gs-campaign-creation.md">
<img alt="워크플로 액세스 및 관리" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>구성 단계</strong></a>
</div>
<p>
</td>
<td>
<a href="create-ms-campaign.md">
<img alt="리드" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-ms-campaign.md"><strong>오케스트레이션된 캠페인 만들기</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="드물게" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>활동 작업</strong></a>
</div>
<p></td>
</tr></table>
