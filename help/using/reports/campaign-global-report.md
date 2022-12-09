---
solution: Journey Optimizer
product: journey optimizer
title: Campaign 글로벌 보고서
description: Campaign 글로벌 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Campaign 글로벌 보고서 {#campaign-global-report}

Campaign 글로벌 보고서는 **[!UICONTROL All time]** 버튼을 클릭합니다.

![](assets/campaign_report_global_5.png)

캠페인 **[!UICONTROL Global report]** 페이지는 다음 탭에 표시됩니다.

* [캠페인](#campaign-global)
* [이메일](#email-global)
* [푸시](#push-global)
* [SMS](#sms-global)

캠페인 **[!UICONTROL Global report]** 은 캠페인의 성공 및 오류를 자세히 설명하는 서로 다른 위젯으로 구분됩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오 [섹션](../reports/global-report.md#modify-dashboard).

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 세부 목록을 보려면 다음을 참조하십시오 [이 페이지](global-report.md#list-of-components-global.md)

## 캠페인 탭 {#campaign-global}

### 배달 {#delivery-global}

![](assets/campaign_report_global_1.png)

다음 **[!UICONTROL Campaign's Statistics]** 위젯은 캠페인과 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL Entered profiles]**: 여정을 시작한 프로필 수입니다.

* **[!UICONTROL Actions delivered]**: 여정에서 작업이 전달된 총 고유 횟수입니다.

* **[!UICONTROL Actions failed in %]**: 작업이 전달된 총 고유 시간과 비교하여 여정에서 작업이 실패한 총 고유 횟수.

## 이메일 탭 {#email-global}

![](assets/campaign_report_global_2.png)

캠페인에서 **[!UICONTROL Global report]**, **[!UICONTROL Email]** 탭 은 Campaign에서 전송된 이메일 게재와 관련된 주요 정보를 자세히 설명합니다.

+++이메일 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL Email Sending Statistics]** 그래프는 게재 성공에 대해 자세히 설명합니다.

* **[!UICONTROL Targeted]**: 게재 분석 중에 처리된 총 메시지 수입니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Delivery Rate]**: 성공적으로 보낸 메시지 비율입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Bounce Rate]**: 전송된 이메일과 비교하여 바운스된 이메일의 비율입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL Error Rate]**: 전송 중에 발생한 오류로 인해 전송된 이메일과 비교하여 전송되지 못했습니다.

* **[!UICONTROL Retries]**: 다시 시도 큐에 있는 전자 메일 수입니다.

* **[!UICONTROL Excluded]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

다음 **[!UICONTROL Email - Tracking statistics]** 위젯에는 게재를 위해 수신자 활동에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Opens]**: 게재에서 게재를 연 횟수입니다.

* **[!UICONTROL Unique Opens]**: 연 게재의 백분율입니다.

* **[!UICONTROL Open Rate]**: 연 총 이메일 수와 배달된 이메일 수 비교

* **[!UICONTROL Clicks]**: 이메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL Unique Clicks]**: 이메일의 콘텐츠를 클릭한 수신자 수입니다.

* **[!UICONTROL Unique Click Rate]**: 게재와 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL Unsubscriptions]**: 구독 취소 링크에 대한 클릭 수입니다.

* **[!UICONTROL Spam complaints]**: 메시지가 스팸 또는 정크 메일로 선언된 횟수입니다.

다음 **[!UICONTROL Sending Statistics]** 그래프에는 다음과 같이 전송된 이메일에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Retries]**: 다시 시도 큐에 있는 전자 메일 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL Bounce Reasons]** 및 **[!UICONTROL Bounce categories]** 위젯에는 다음과 같이 바운스된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Hard bounce]**: 잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL Soft bounce]**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**: 부재 중 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)와 같은 총 임시 수입니다.

바운스에 대한 자세한 내용은 [제외 목록](../reports/suppression-list.md) 페이지.

다음 **[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류를 확인할 수 있습니다.

다음 **[!UICONTROL Excluded reasons]** 그래프와 테이블에는 타겟팅된 프로필에서 제외된 사용자 프로필이 메시지를 받지 못한 다양한 이유가 표시됩니다.

다음 **[!UICONTROL Email - Top Url]** 가장 많이 방문한 게재 URL을 그래프 및 표 세부 사항으로 설명합니다.

다음 **[!UICONTROL Email - Top recipient domain]** 전자 메일을 여는 데 받는 사람이 가장 많이 사용하는 도메인을 그래프 및 표 세부 사항입니다.

>[!NOTE]
>
>다음 **[!UICONTROL Optimized vs non optimized]** 및 **[!UICONTROL Send time optimization]**  위젯은 전송에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 [이 페이지](../building-journeys/journeys-message.md#send-time-optimization).

다음 **[!UICONTROL Optimized vs non optimized]** 그래프는 메시지가 최적화되었는지 여부에 따라 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.
* **[!UICONTROL Opens]**: 게재에서 게재를 연 횟수입니다.
* **[!UICONTROL Clicks]**: 이메일에서 콘텐츠를 클릭한 횟수입니다.

다음 **[!UICONTROL Send time optimization]** 전송 방법에 따라 게재 성공 여부를 자세히 설명합니다. 최적화되었습니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.
* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.
+++

## 푸시 알림 탭 {#push-global}

캠페인에서 **[!UICONTROL Global report]**, **[!UICONTROL Push notification]** 탭 은 campaign에서 전송된 푸시 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_global_3.png)

+++푸시 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL Push notification - Sending statistics]** 표는 그래프 및 KPI를 사용하여 푸시 알림에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Targeted]**: 게재 분석 중에 처리된 총 메시지 수입니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Delivery Rate]**: 성공적으로 보낸 메시지 비율입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Bounce Rate]**: 전송된 푸시 알림과 비교하여 바운스된 푸시 알림의 비율입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL Error Rate]**: 전송 중에 발생한 오류로 인해 전송된 푸시 알림과 비교하여 전송되지 못했습니다.

* **[!UICONTROL Excluded]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

다음 **[!UICONTROL Push - Tracking statistics]** 게재에 대해 수신자 활동에 사용할 수 있는 데이터를 포함합니다.

* **[!UICONTROL Opens]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL Open Rate]**: 열린 푸시 알림의 비율입니다.

* **[!UICONTROL Actions]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)

* **[!UICONTROL Engagements]**: 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.

* **[!UICONTROL Engagement Rate]**: 이 푸시 알림에 대한 열기 및 작업의 비율(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.

다음 **[!UICONTROL Push notification summary]** 그래프에는 다음과 같이 전송된 푸시 알림에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Opens]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL Actions]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

>[!NOTE]
>
>다음 **[!UICONTROL Optimized vs non optimized]** 및 **[!UICONTROL Send time optimization]**  위젯은 전송에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 [이 페이지](../building-journeys/journeys-message.md#send-time-optimization).

다음 **[!UICONTROL Optimized vs non optimized]** 그래프는 메시지가 최적화되었는지 여부에 따라 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.
* **[!UICONTROL Opens]**: 게재에서 게재를 연 횟수입니다.
* **[!UICONTROL Actions]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)

다음 **[!UICONTROL Send time optimization]** 전송 방법에 따라 게재 성공 여부를 자세히 설명합니다. 최적화되었습니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.
* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

다음 **[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류를 확인할 수 있습니다.

다음 **[!UICONTROL Excluded reasons]** 그래프와 테이블에는 타겟팅된 프로필에서 제외된 사용자 프로필이 메시지를 받지 못한 다양한 이유가 표시됩니다.

다음 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 및 **[!UICONTROL Breakdown by platform]** 그래프 및 표는 수신자의 운영 시스템에 따라 푸시 알림의 성공을 자세히 설명합니다.
+++

## SMS 탭 {#sms-global}

캠페인에서 **[!UICONTROL Global report]**, **[!UICONTROL SMS]** 탭 은 campaign에서 전송된 SMS 게재와 관련된 주요 정보를 자세히 설명합니다.

![](assets/campaign_report_global_4.png)

+++SMS 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL SMS - Sending statistics]** 표는 게재의 성공에 대해 자세히 설명합니다.

* **[!UICONTROL Targeted]**: 이 게재의 타겟 프로필로 자격을 얻은 사용자 프로필 수입니다.

* **[!UICONTROL Excluded]**: 타겟팅된 프로필에서 제외되고 메시지를 받지 못한 사용자 프로필 수입니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL SMS Performance by date]** 위젯은 그래프와 함께 메시지에 대한 주요 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** 및 **[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.
+++

## 추가 리소스

* [캠페인 시작](../campaigns/get-started-with-campaigns.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [API로 트리거된 캠페인 만들기](../campaigns/api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](../campaigns/modify-stop-campaign.md)
* [Campaign 라이브 보고서](campaign-live-report.md)
