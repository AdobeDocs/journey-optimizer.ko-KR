---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 보고
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인에 대한 보고서에 액세스하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8cb569a2-a4a0-45a5-b7f9-f5a591e44335
source-git-commit: 08746d3689c7ad2db49b991db792cdc41c889f75
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 9%

---

# 오케스트레이션된 캠페인 보고 {#report-campaigns}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/><b>[보고](reporting-campaigns.md)</b> | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

오케스트레이션된 캠페인은 강력한 보고 기능을 통해 실행 가능한 통찰력을 제공합니다. 이러한 통찰력을 통해 대상자 행동을 더 잘 이해하고, 고객 여정의 각 단계 성과를 측정하며, 데이터 중심의 결정을 내려 향후 캠페인을 최적화할 수 있습니다. 자세한 지표와 시각화를 통해 참여를 추적하고 타겟팅 전략을 세밀하게 조정하여 영향을 극대화할 수 있습니다.

![](assets/report-orchestrated.png)

## 보고서 유형 {#reporting-types}

<table style="table-layout:auto; width: 100%; border-collapse: collapse;">
  <tbody>
    <tr>
      <td><a href="../reports/live-report.md"><img alt="라이브 보고서" src="assets/last-24hours.png"></a></td>
      <td>
        <b>라이브 보고서</b>를 사용하여 내장된 대시보드에서 오케스트레이션된 캠페인의 영향과 성과를 실시간으로 측정하고 시각화할 수 있습니다. 오케스트레이션된 캠페인이 <b>최근 24시간 보고서 보기</b> 메뉴에서 실행되는 즉시 <b>실시간 보고서</b>에서 데이터를 사용할 수 있습니다. 이 섹션<a href="../reports/live-report.md">에서 실시간 보고서 </a>에 대해 자세히 알아보세요.
      </td>
        </br>
    </tr>
    <tr style="background-color: #FFFFFF;">
      <td><a href="../reports/report-gs-cja.md"><img alt="전체 기간 보고서" src="assets/all-time-report.png"></a></td>
      <td>
        <b>모든 시간 보고서</b>는 Customer Journey Analytics 기능과 완전히 통합되어 두 플랫폼 간에 보고를 표준화하고 데이터 일관성과 안정성을 개선합니다. 이 섹션<a href="../reports/report-gs-cja.md">에서 모든 시간 보고서 </a>에 대해 자세히 알아보세요.
      </td>
    </tr>
  </tbody>
</table>

## 채널 보고서 살펴보기

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../reports/campaign-global-report-cja-email.md"><img alt="이메일" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../reports/campaign-global-report-cja-email.md"><strong>이메일 보고서</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-sms.md"><img alt="sms" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../reports/campaign-global-report-cja-sms.md"><strong>SMS 보고서</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-push.md"><img alt="푸시" src="../../channels/assets/do-not-localize/push.png"></a><a href="../reports/campaign-global-report-cja-push.md"><strong>보고서 푸시</strong></a></td>
</tr></table>

