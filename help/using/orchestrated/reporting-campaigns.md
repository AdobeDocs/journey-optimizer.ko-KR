---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 보고
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인에 대한 보고서에 액세스하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8cb569a2-a4a0-45a5-b7f9-f5a591e44335
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 58%

---

# 오케스트레이션된 캠페인 보고 {#report-campaigns}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/><b>[보고](reporting-campaigns.md)<b> | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[리타기팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[And 조인](activities/and-join.md) - [대상자 빌드](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상자 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

오케스트레이션된 캠페인은 강력한 보고 기능을 통해 실행 가능한 인사이트를 제공합니다. 이러한 인사이트를 통해 대상자 행동을 더 잘 이해하고, 고객 여정의 각 단계 성과를 측정하며, 데이터 중심의 결정을 내려 향후 캠페인을 최적화할 수 있습니다. 자세한 지표와 시각화를 통해 참여를 추적하고 타겟팅 전략을 세밀하게 조정하여 영향을 극대화할 수 있습니다.

![](assets/report-orchestrated.png)

## 보고서 유형 {#reporting-types}

<table style="table-layout:auto; width: 100%; border-collapse: collapse;">
  <tbody>
    <tr>
      <td><a href="../reports/live-report.md"><img alt="라이브 보고서" src="assets/last-24hours.png"></a></td>
      <td>
        <b>라이브 보고서</b>를 사용하여 내장된 대시보드에서 오케스트레이션된 캠페인의 영향과 성과를 실시간으로 측정하고 시각화할 수 있습니다. 오케스트레이션된 캠페인이 <b>최근 24시간 보고서 보기</b> 메뉴에서 실행되는 즉시 <b>실시간 보고서</b>에서 데이터를 사용할 수 있습니다. <a href="../reports/live-report.md">이 섹션</a>에서 라이브 보고서에 대해 자세히 알아보십시오.
      </td>
        </br>
    </tr>
    <tr style="background-color: #FFFFFF;">
      <td><a href="../reports/report-gs-cja.md"><img alt="전체 기간 보고서" src="assets/all-time-report.png"></a></td>
      <td>
        <b>전체 시간 보고서</b>는 Customer Journey Analytics 기능과 완벽하게 통합되어 두 플랫폼에서 보고를 표준화하고 데이터 일관성과 안정성을 향상시킵니다. <a href="../reports/report-gs-cja.md">이 섹션에서</a> 전체 시간 보고서에 대해 자세히 알아보십시오.
      </td>
    </tr>
  </tbody>
</table>

## 채널 보고서 살펴보기

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../reports/campaign-global-report-cja-email.md"><img alt="이메일" src="../channels/assets/do-not-localize/email.png"></a><br/><a href="../reports/campaign-global-report-cja-email.md"><strong>이메일 보고서</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a><br/><a href="../reports/campaign-global-report-cja-sms.md"><strong>SMS 보고서</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-push.md"><img alt="푸시" src="../channels/assets/do-not-localize/push.png"></a><a href="../reports/campaign-global-report-cja-push.md"><strong>푸시 보고서</strong></a></td>
</tr></table>

