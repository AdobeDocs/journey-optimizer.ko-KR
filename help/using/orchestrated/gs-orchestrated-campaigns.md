---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 시작
description: 오케스트레이션된 캠페인으로 시작하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 34788c05cdcdcbc0c261df3f931a5bc1786fff5f
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 7%

---

# 오케스트레이션된 캠페인 시작 {#orchestrated-camp}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| <b>[오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)</b><br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer]의 Campaign Orchestration은 정교하고 브랜드에서 시작한 마케팅 캠페인을 채널 전체에 걸쳐 지원하므로 규모에 맞게 참여, 매출 및 고객 충성도를 높일 수 있습니다.

크로스 채널 마케팅은 필수적이지만 오케스트레이션된 캠페인을 통해 원활하게 이루어집니다. 드래그하여 놓는 시각적 인터페이스를 통해 세그먼테이션에서 메시지 게재에 이르기까지 여러 채널에 걸쳐 복잡한 마케팅 워크플로우를 디자인하고 자동화할 수 있습니다. 속도, 제어 및 효율성을 위해 구축된 하나의 직관적인 환경에서 모든 작업이 수행됩니다.

## 핵심 기능

Campaign Orchestration은 다음 네 가지 주요 요소를 기반으로 구축됩니다.

<table>
<tr style="border: 0;">
<td><img alt="온디맨드 대상" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>온디맨드 대상</b><br/>데이터 집합 간에 즉시 쿼리하여 데이터 형식과 차원의 조합을 사용하여 대상 세그먼트를 만듭니다.</td></tr>
<tr style="border: 0;">
<td><img alt="다중 엔티티 세그멘테이션 및 전송" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>다중 엔터티 세분화 및 전송</b><br/>개인 기반 캠페인을 넘어 제품 카탈로그, 스토어 위치 또는 서비스 데이터와 같은 엔터티를 사용하여 정확하게 타깃팅하십시오.</td></tr>
<tr style="border: 0;">
<td><img alt="사전 전송 가시성 및 정밀도" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>가시성과 정밀도를 미리 전송</b><br/>실행 전에 정확한 세분화 수와 전체 캠페인 범위를 가져와 정확성과 신뢰도를 보장합니다.</td></tr>
<tr style="border: 0;">
<td><img alt="여러 단계 캠페인 워크플로" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>여러 단계 캠페인 워크플로</b><br/>일일 메시지부터 계절별 판촉 행사 또는 주요 제품 출시와 같은 복잡한 캠페인에 이르기까지 여러 단계 캠페인을 디자인합니다.</td></tr>
</table>

## 오케스트레이션된 캠페인 및 여정

오케스트레이션된 캠페인 시각화는 여정과 유사하지만 다양한 목적 및 사용 사례를 해결합니다.

* **여정** - 각 프로필이 각자의 속도로 다른 단계를 진행하는 1에서 1까지의 캔버스입니다. 각 고객의 상태는 해당 컨텍스트 내에서 유지되어 실시간 작업을 트리거합니다.

* **오케스트레이션된 캠페인** - 여정과 달리 오케스트레이션된 캠페인은 세그먼트를 계산하는 일괄 처리 캔버스를 사용하여 작동합니다. 모든 프로필이 동시에 처리됩니다.

## 전제 조건

오케스트레이션된 캠페인을 사용하기 전에 적절한 권한이 있는지 확인해야 합니다. 오케스트레이션된 캠페인에 대한 액세스는 오케스트레이션된 캠페인 관리자, 오케스트레이션된 캠페인 승인자, 오케스트레이션된 캠페인 관리자 또는 오케스트레이션된 캠페인 뷰어와 같은 관련 **[!UICONTROL 제품 프로필]**&#x200B;에 할당된 사용자로 제한됩니다.

오케스트레이션된 캠페인 기능에 액세스할 수 없는 경우 관리자에게 연락하여 필요한 권한을 요청하십시오.

➡️[오케스트레이션된 캠페인과 관련된 제품 프로필에 대해 자세히 알아보세요](../administration/ootb-product-profiles.md)

## 더 자세히 알아보기

이제 오케스트레이션된 캠페인이 무엇인지 이해했으므로, 이 기능을 사용하기 시작하려면 이들 설명서 섹션을 자세히 살펴보십시오.

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
<a href="create-orchestrated-campaign.md">
<img alt="리드" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>오케스트레이션된 캠페인 만들기</strong>
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
