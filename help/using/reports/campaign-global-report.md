---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 글로벌 보고서
description: Campaign 글로벌 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 94d6ebe6e0ad5fa48eaad9d8cfa8cff584f2b819
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 캠페인 글로벌 보고서 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="캠페인 글로벌 보고서"
>abstract="캠페인 글로벌 보고서를 사용하여 선택된 기간에 대해 캠페인의 영향을 측정할 수 있습니다. 보고서는 캠페인 성공 사례와 오류를 자세히 설명하는 여러 위젯으로 나눠집니다. 위젯 크기를 조정하거나 위젯을 제거하여 각 보고 대시보드를 수정할 수 있습니다."

>[!AVAILABILITY]
>
>현재 보고 경험은 2025년 1월부터 종료됩니다. 이 날짜 이후에는 새로운 보고 경험이 표준이 됩니다. 원활한 전환을 위해 새로운 기능을 숙지하는 것이 좋습니다. [Journey Optimizer 새 보고 인터페이스를 시작합니다.](report-gs-cja.md)

**모든 시간** 탭에서 액세스할 수 있는 글로벌 보고서에는 최소 2시간 전에 발생한 이벤트가 표시되고 선택한 기간 동안의 이벤트가 포함됩니다. 반면 라이브 보고서는 이벤트 발생으로부터 최소 2분의 시간 간격을 가지고 지난 24시간 내에 발생한 이벤트에 중점을 둡니다.

**[!UICONTROL 보고서 보기]** 단추를 사용하면 Campaign에서 Campaign 글로벌 보고서에 직접 액세스할 수 있습니다.

![](assets/campaign_report_global_5.png)

Campaign **[!UICONTROL 전역 보고서]** 페이지가 다음 탭과 함께 표시됩니다.

* [Campaign](#campaign-global)
* [이메일](#email-global)
* [인앱](#inapp-global)
* [푸시](#push-global)
* [SMS](#sms-global)
* [웹](#web-tab)
* [다이렉트 메일](#direct-mail-global)

Campaign **[!UICONTROL 글로벌 보고서]**&#x200B;는 캠페인의 성공 및 오류를 자세히 설명하는 다양한 위젯으로 나뉩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 이 [섹션](../reports/global-report.md#modify-dashboard)을 참조하세요.

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 [이 페이지](global-report.md#list-of-components-global.md)를 참조하세요.

## 캠페인 탭 {#campaign-global}

### 게재 {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="캠페인 통계"
>abstract="캠페인 통계 위젯은 입력된 프로필, 전달된 작업 등 캠페인과 관련된 주요 정보를 자세히 설명합니다."

![](assets/campaign_report_global_1.png)

**[!UICONTROL 캠페인 통계]** KPI는 포괄적인 대시보드 역할을 하며 캠페인과 관련된 주요 지표에 대한 자세한 분류를 제공합니다. 여기에는 프로필 및 게재된 작업 수와 같은 필수 정보가 포함되어 있으며, 이를 통해 캠페인의 성능과 참여를 철저히 파악할 수 있습니다.

+++ Campaign의 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 대상]**: 타깃팅된 프로필 수입니다.

* **[!UICONTROL 동작 배달]**: 동작이 배달된 총 고유 횟수입니다.

* **[!UICONTROL 작업이 %]**&#x200B;에서 실패했습니다. 작업이 배달된 총 고유 시간 수와 비교하여 작업이 실패한 고유 시간의 백분율입니다.

+++

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../content-management/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.


### Experimentation report {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Success metric"
>abstract="The total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles."

![](assets/experimentation_report_3.png)

The **[!UICONTROL Experimentation]** tab provides key insights into the performance of each variant, and identifies the most successful one.

Note that defining the best performer might take some time, it will be represented by this icon ![](assets/experimentation_report_1.png).

+++Learn more on the different metrics and widgets available for the Experimentation report.

The **[!UICONTROL Experiment result]** widget details the performance of each variant. You can change your baseline by selecting one of the treatment from the **[!UICONTROL Baseline]** the drop-down. The best treatment will be represented with a star icon.

For a deep-dive in these results and how to interpret them, refer to [this page](../content-management/get-started-experiment.md#interpret-results).

The table presents the following metrics:

* **[!UICONTROL Lift over baseline]**: Measure of the percentage improvement in conversion rate of a given treatment over the baseline.

* **[!UICONTROL Confidence]**: Evidence that a given treatment is the same as the baseline treatment. [Learn more](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Unique outbound clicks]**: Total count of clicks across outbound channels.

* **[!UICONTROL Profiles]**: Number of profiles targeted for this treatment.

* **[!UICONTROL Unique outbound clicks/profiles]**: Total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles.

The **[!UICONTROL Confidence interval]** graph measures uncertainty around improvement. It details the percentage difference in performance between the baseline and the best performing treatment. [Learn more](../content-management/experiment-calculations.md#confidence-intervals). 

![](assets/experimentation_report_4.png)

The last widget provides data related to the **[!UICONTROL Success metric]** you previously selected for your Treatments. You have the option to select a different targeted metric from the **[!UICONTROL Metric]** drop-down menu to track alternative data.
    
>[!CAUTION]
>
>When working with experimentation filtered metrics, please note that changing the Metric selection from the drop-down on the comparison page for experimentation will not retain the filter value. For example, switching from "Clicks" to "Unique clicks" will lead to the loss of the applied filter, rendering the comparison inaccurate or invalid.

+++
-->

## 이메일 탭 {#email-global}

### 이메일 - 전송 통계 {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="이메일 - 전송 통계"
>abstract="이메일 - 전송 통계 테이블에는 대상 지정 또는 게재됨 등과 같은 이메일에 대한 필수 데이터가 요약되어 있습니다."

![](assets/campaign_email_sending.png)

**[!UICONTROL 전자 메일 전송 통계]** 표에는 전자 메일 캠페인과 관련된 필수 데이터에 대한 포괄적인 요약이 나와 있습니다. 여기에는 타겟팅된 대상의 크기 및 배달된 이메일 수와 같은 주요 지표가 자세히 설명되어 있어 이메일의 효율성과 도달에 대한 중요한 통찰력을 제공합니다.

+++ 이메일 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 타깃팅]**: 전송 프로세스 중에 처리된 총 전자 메일 수입니다.

* **[!UICONTROL 전송됨]**: 전자 메일의 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 메시지 수와 관련하여 보낸 전자 메일 수입니다.

* **[!UICONTROL 게재율]**: 전자 메일을 성공적으로 보낸 비율입니다.

* **[!UICONTROL 바운스 수]**: 보낸 총 메시지 수와 관련하여 보내는 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 바운스 비율]**: 보낸 전자 메일과 비교하여 반송된 전자 메일의 비율입니다.

* **[!UICONTROL 오류]**: 보내는 동안 프로필로 보낼 수 없는 총 오류 수입니다.

* **[!UICONTROL 오류율]**: 보낸 전자 메일과 비교하여 보내지 못하게 하는 전송 프로세스 중 발생한 오류의 비율입니다.

* **[!UICONTROL 다시 시도]**: 다시 시도 큐에 있는 전자 메일 수입니다.

* **[!UICONTROL 제외됨]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

+++

### 이메일 - 추적 통계 {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="이메일 - 추적 통계"
>abstract="이메일 - 추적 통계 테이블은 이메일의 프로필 활동에 대한 데이터를 제공합니다."

![](assets/campaign_email_tracking.png)

**[!UICONTROL 전자 메일 - 추적 통계]** 표에는 전자 메일 캠페인과 관련된 프로필 활동에 대한 자세한 계정이 있습니다. 여기에는 열람, 클릭 수 및 기타 관련 참여 지표에 대한 지표가 포함되며 프로필이 이메일 콘텐츠와 상호 작용하는 방식에 대한 포괄적인 보기를 제공합니다.

+++ 이메일에 대한 자세한 내용 - 추적 통계 지표

* **[!UICONTROL 열기]**: 이메일을 연 횟수입니다.

* **[!UICONTROL 고유 열기 수]**: 열린 전자 메일의 비율입니다.

* **[!UICONTROL 열람율]**: 배달된 전자 메일 수와 비교하여 열린 전자 메일의 총 수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 고유 클릭 수]**: 전자 메일의 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 고유 클릭률]**: 전자 메일과 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL 구독 취소]**: 구독 취소 링크의 클릭 수입니다.

* **[!UICONTROL 스팸 고객 불만]**: 메시지가 스팸 또는 정크로 선언된 횟수입니다.

+++

### 이메일 - 전송 성능 {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="이메일 - 전송 성능"
>abstract="이메일 - 전송 성능 그래프는 전송된 이메일에 관한 포괄적인 데이터를 제공하여 게재 및 바운스와 같은 주요 지표에 대한 인사이트를 제공하고 이메일 게재 프로세스를 자세하게 분석할 수 있습니다."

![](assets/campaign_email_sending_performance.png)

**[!UICONTROL 전자 메일 - 전송 성능]** 그래프는 전송된 전자 메일과 관련된 데이터를 종합적으로 볼 수 있도록 해주며 배달됨 및 바운스 수와 같은 주요 지표에 대한 통찰력을 제공합니다. 이를 통해 이메일 전송 프로세스를 자세히 분석할 수 있으므로 이메일 캠페인의 효율성과 성능에 대한 중요한 정보를 제공합니다.

+++ 이메일에서 자세히 알아보기 - 성능 지표 보내기

* **[!UICONTROL 배달됨]**: 보낸 총 전자 메일 수와 관련하여 보낸 전자 메일 수입니다.

* **[!UICONTROL 바운스 수]**: 보낸 전자 메일의 총 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 다시 시도]**: 다시 시도 큐에 있는 전자 메일 수입니다.

* **[!UICONTROL 오류]**: 보내는 동안 프로필로 보낼 수 없는 총 오류 수입니다.

+++

### 이메일 - 바운스 이유 및 범주 {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="이메일 - 바운스 범주"
>abstract="이메일 - 바운스 범주 그래프와 테이블은 일시적 오류와 영구적 오류 모두에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="이메일 - 바운스 이유"
>abstract="이메일 - 바운스 이유 그래프와 테이블에는 바운스된 메시지와 관련하여 사용 가능한 데이터가 있습니다."

![](assets/campaign_email_bounces.png)

**[!UICONTROL 전자 메일 - 반송 이유]** 및 **[!UICONTROL 전자 메일 - 반송 범주]** 위젯은 반송된 메시지와 관련된 사용 가능한 데이터를 컴파일하여 전자 메일 반송 이면의 특정 이유 및 범주에 대한 자세한 통찰력을 제공합니다.

바운스에 대한 자세한 내용은 [제외 목록](../reports/suppression-list.md) 페이지를 참조하세요.

+++ 이메일에 대한 자세한 내용 - 바운스 범주 지표

* **[!UICONTROL 하드 바운스]**: 잘못된 전자 메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL 소프트 바운스]**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL 무시됨]**: 부재 중과 같은 총 임시 항목 수 또는 기술적인 오류(예: 발신자 유형이 postmaster인 경우).

+++


### 이메일 - 오류 이유 {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="이메일 - 오류 이유"
>abstract="이메일 - 오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 발생한 특정 오류를 확인할 수 있습니다."

![](assets/campaign_email_error_reasons.png)

**[!UICONTROL 오류 원인]** 그래프 및 표는 전송 프로세스 중에 발생한 특정 오류에 대한 가시성을 제공하여 오류의 특성 및 발생에 대한 중요한 정보를 제공합니다.

테이블, 막대 차트 또는 도넛에서 전환하도록 선택할 수 있습니다.

### 이메일 - 제외된 이유 {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="이메일 - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

![](assets/campaign_email_excluded.png)

**[!UICONTROL 제외된 이유]** 그래프와 표는 타깃팅된 대상에서 사용자 프로필을 제외하여 메시지가 수신되지 않는 다양한 요인을 포괄적으로 보여 줍니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.

### 도메인별로 전송 및 게재 {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sent_domains"
>title="도메인별로 전송 및 게재"
>abstract="도메인별로 전송 및 게재 테이블 및 그래프는 도메인별로 분류된 이메일 분석을 통해 이메일 커뮤니케이션의 전반적인 성능에 대한 심층적인 인사이트를 제공합니다."

![](assets/campaign_email_sent_domains.png)

**[!UICONTROL 도메인에서 보낸 사람 및 배달]** 테이블 및 그래프는 도메인 수준에서 전자 메일의 세부 분류를 제공하여 전자 메일 성능에 대한 포괄적인 통찰력을 제공합니다.

+++ 도메인에서 보낸 사람 및 배달한 사람 지표에 대해 자세히 알아보기

* **[!UICONTROL 전송됨]**: 전자 메일의 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 전자 메일 수와 관련하여 보낸 전자 메일 수입니다.

+++

### 도메인별 바운스 및 오류 {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_domains"
>title="도메인별 바운스 및 오류"
>abstract="도메인별 바운스 및 오류 그래프와 테이블은 도메인 수준의 세분화된 분석을 통해 이메일 전송 프로세스 중에 발생한 특정 오류에 대한 인사이트를 제공합니다."

![](assets/campaign_email_bounce_domains.png)

**[!UICONTROL 도메인별 바운스 및 오류]** 그래프 및 표는 전송 프로세스 중에 발생한 특정 오류에 대한 도메인 수준 분석을 제공하여 발생한 문제에 대한 자세한 분석을 제공합니다.

+++ 도메인별 바운스 및 오류에 대한 자세한 내용 지표

* **[!UICONTROL 바운스 수]**: 보낸 전자 메일의 총 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생한 총 오류 수로 인해 프로필로 전자 메일이 전송되지 않았습니다.

+++

### 도메인별 열기 및 클릭 {#opens-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_open_domains"
>title="도메인별 열기 및 클릭"
>abstract="도메인별 열기 및 클릭 그래프와 테이블은 도메인 수준의 자세한 분석을 통해 대상자가 이메일에 참여하는 방식을 포괄적으로 확인할 수 있습니다."

![](assets/campaign_email_open_domains.png)

**[!UICONTROL 도메인별 열기 및 클릭 수]** 그래프 및 표에는 프로필과 사용자의 전자 메일 참여에 대한 도메인 수준의 분류가 표시되어 다양한 도메인이 콘텐츠와 상호 작용하는 방식에 대한 중요한 통찰력을 제공합니다.

+++ 도메인별 열기 및 클릭 지표에 대해 자세히 알아보기

* **[!UICONTROL 열기]**: 이메일을 연 횟수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

+++

### 도메인별 바운스 이유 {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_reasons_domains"
>title="도메인별 바운스 이유"
>abstract="도메인별 바운스 이유 그래프와 테이블은 도메인 수준의 분석을 통해 일시적 오류와 영구적 오류 모두에 대한 포괄적인 인사이트를 제공합니다. 자세한 분석은 바운스된 메시지의 구체적인 이유에 대한 유용한 정보를 제공합니다."

![](assets/campaign_email_bounce_reasons_domains.png)

**[!UICONTROL 도메인별 바운스 이유]** 그래프 및 표는 일시적인 오류와 영구적인 오류에 대한 도메인 수준의 데이터 분석을 제공하여 반송 메시지의 발생 원인에 대한 자세한 통찰력을 제공합니다.

+++ 도메인 메트릭별 바운스 이유에 대해 자세히 알아보기

* **[!UICONTROL 열기]**: 이메일을 연 횟수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

+++

### 이메일 - 상위 URL {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="이메일 - 상위 URL"
>abstract="이메일 - 상위 URL 그래프 및 테이블에서는 방문자 트래픽이 가장 높은 이메일 내 URL에 대한 포괄적인 개요를 제공하므로 추천 링크를 확인할 수 있습니다."

![](assets/campaign_email_topurl.png)

**[!UICONTROL 이메일 - 상위 URL]** 그래프 및 표는 가장 높은 방문자 트래픽을 유도하는 이메일 내 URL에 대한 포괄적인 개요를 제공합니다. 이를 통해 가장 인기 있는 링크를 식별하고 우선 순위를 지정할 수 있으므로 이메일의 특정 콘텐츠와 함께 프로필 참여를 보다 잘 이해할 수 있습니다.

### 이메일 - 최고 수신자 도메인 {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="이메일 - 최고 수신자 도메인"
>abstract="이메일 - 최고 수신자 도메인 그래프 및 테이블에서는 수신자가 이메일을 열 때 가장 자주 사용하는 도메인에 대한 자세한 분석을 통해 수신자 동작에 대한 귀중한 인사이트를 제공합니다."

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> **[!UICONTROL 전자 메일 - 최고 수신자 도메인]** 위젯의 정확률은 99.95%입니다.

**[!UICONTROL 전자 메일 - 최고 수신자 도메인]** 그래프 및 표에는 프로필이 전자 메일을 여는 데 가장 많이 사용하는 도메인에 대한 자세한 분류가 제공됩니다. 이렇게 하면 프로필 동작에 대한 중요한 통찰력을 제공하여 선호하는 플랫폼을 이해하는 데 도움이 됩니다.

+++ 이메일에 대한 자세한 내용 - 최고 수신자 도메인 지표

* **[!UICONTROL 배달됨]**: 보낸 총 전자 메일 수와 관련하여 보낸 전자 메일 수입니다.

* **[!UICONTROL 게재율]**: 전자 메일을 성공적으로 보낸 비율입니다.

* **[!UICONTROL 바운스 + 오류율]**: 보낸 전자 메일과 비교하여 반송된 전자 메일의 비율입니다.

+++

### 이메일 - 최적화 {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>**[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]** 위젯은 전자 메일에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 [이 페이지](../building-journeys/journeys-message.md#send-time-optimization)를 참조하세요.

**[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]** 위젯은 최적화 여부에 관계없이 메시지와 관련된 기본 정보를 자세히 설명합니다.

+++ 전송 시간 최적화 지표에 대해 자세히 알아보기

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 열기]**: 메시지가 열린 횟수입니다.

* **[!UICONTROL 클릭 수]**: 전자 메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 보낸 총 메시지 수와 관련하여 보내는 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

+++

### 이메일 - 오퍼 {#email-offers}

![](assets/campaign_email_offers.png)

**[!UICONTROL 오퍼 통계]**, **[!UICONTROL 시간 경과에 따른 오퍼 통계]** 및 **[!UICONTROL 오퍼 상세 통계]** 위젯은 오퍼의 성공과 타깃팅된 대상자에 대한 영향을 측정합니다.

+++ 이메일에 대한 자세한 내용 - 오퍼 지표

* **[!UICONTROL 전송된 오퍼]**: 오퍼에 대한 총 전송 수입니다.

* **[!UICONTROL 오퍼 노출]**: 전자 메일에서 오퍼를 연 횟수입니다.

* **[!UICONTROL 오퍼 클릭 수]**: 전자 메일에서 오퍼를 클릭한 횟수입니다.

* **[!UICONTROL 배치 이름]**: 오퍼를 표시하는 데 사용되는 배치 이름입니다. 배치에 대한 자세한 내용은 이 [페이지](../offers/offer-library/creating-placements.md)를 참조하세요.

* **[!UICONTROL 오퍼 이름]**: 게재에 추가된 오퍼의 이름입니다. 배치에 대한 자세한 내용은 이 [페이지](../offers/offer-library/creating-personalized-offers.md)를 참조하세요.

* **[!UICONTROL 전송된 오퍼]**: 오퍼에 대한 총 전송 수입니다.

* **[!UICONTROL 오퍼 노출률]**: 전송된 오퍼 수와 비교하여 열린 오퍼의 비율입니다.

+++

## 인앱 탭 {#inapp-global}

**[!UICONTROL 인앱]** 탭은 Campaign **[!UICONTROL 전역 보고서]**&#x200B;에서 캠페인에서 보낸 인앱 메시지와 관련된 기본 정보를 자세히 설명합니다.

### 인앱 성능 {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="인앱 성능"
>abstract="인앱 성능 KPI는 방문자의 인앱 메시지 참여에 대한 필수 인사이트를 제공합니다."

![](assets/campaign_inapp_performance.png)

**[!UICONTROL 인앱 성과]** KPI는 방문자의 인앱 메시지 참여에 대한 중요한 통찰력을 제공하여 인앱 캠페인의 효과와 영향을 평가하는 데 중요한 지표를 제공합니다.

+++ 인앱 성능 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 노출 수]**: 인앱 메시지가 전달된 고유 사용자 수.

* **[!UICONTROL 노출 수]**: 모든 사용자에게 전달된 인앱 메시지의 총 수입니다.

* **[!UICONTROL 상호 작용]**: 인앱 메시지의 총 참여 수입니다. 여기에는 클릭, 해제 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

+++

### 유형별 상호 작용 {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="유형별 상호 작용"
>abstract="유형별 상호 작용 그래프와 테이블에서는 클릭, 해제 또는 상호 작용을 추적하여 사용자가 인앱 메시지와 상호 작용하는 방식을 자세히 설명합니다."

![](assets/campaign_inapp_interactions.png)

**[!UICONTROL 유형별 상호 작용]** 그래프와 표는 프로필이 인앱 메시지와 상호 작용하는 방법, 클릭, 해제 등의 추적 작업 또는 기타 모든 유형의 상호 작용에 대한 자세한 설명을 제공합니다.

### 인앱 요약 {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="인앱 요약"
>abstract="인앱 요약 그래프에서는 지정된 기간 동안의 인앱 노출 횟수 및 상호 작용 진행 상황을 보여 줍니다."

![](assets/campaign_inapp_summary.png)

**[!UICONTROL 인앱 요약]** 그래프는 지정된 기간 동안 인앱 노출 횟수 및 상호 작용의 진행률을 보여 주며 인앱 메시지 성능에 대한 포괄적인 개요를 제공합니다.

+++ 인앱 요약 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 노출 수]**: 인앱 메시지가 전달된 고유 사용자 수.

* **[!UICONTROL 노출 수]**: 모든 사용자에게 전달된 인앱 메시지의 총 수입니다.

* **[!UICONTROL 상호 작용]**: 인앱 메시지의 총 참여 수입니다. 여기에는 클릭, 해제 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

+++

## 푸시 알림 탭 {#push-global}

**[!UICONTROL 푸시 알림]** 탭은 Campaign **[!UICONTROL 전역 보고서]**&#x200B;에서 캠페인에서 보낸 푸시 알림과 관련된 기본 정보를 자세히 설명합니다.

### 푸시 알림 - 전송 통계 {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="푸시 알림 - 전송 통계"
>abstract="푸시 알림 전송 통계 테이블에는 대상 지정 메시지 또는 게재된 메시지 등과 같은 푸시 알림에 대한 필수 데이터가 요약되어 있습니다."

![](assets/campaign_push_sending.png)

**[!UICONTROL 푸시 알림 - 전송 통계]** 표에는 타깃팅된 메시지 수 및 배달된 메시지 수와 같은 주요 지표를 포함하여 푸시 알림과 관련된 필수 데이터에 대한 간결한 요약이 제공됩니다.

+++ 푸시 알림에 대한 자세한 내용 - 통계 지표 전송

* **[!UICONTROL 실행 시간]**: 되풀이하는 푸시 알림의 모든 실행 시작 시간입니다. 하나 이상의 되풀이하는 푸시 알림만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

* **[!UICONTROL 타깃팅]**: 분석 중에 처리된 총 푸시 알림 수입니다.

* **[!UICONTROL 전송됨]**: 푸시 알림에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.

* **[!UICONTROL 게재 속도]**: 푸시 알림이 성공적으로 전송된 비율입니다.

* **[!UICONTROL 바운스 수]**: 총 푸시 알림 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 바운스 비율]**: 보낸 푸시 알림과 비교하여 반송된 푸시 알림의 비율입니다.

* **[!UICONTROL 오류]**: 프로필로 보낼 수 없는 총 오류 수입니다.

* **[!UICONTROL 오류율]**: 전송을 방지하는 동안 발생한 오류의 백분율과 전송된 푸시 알림의 백분율입니다.

* **[!UICONTROL 제외됨]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

+++

### 푸시 알림 - 추적 통계 {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="푸시 알림 - 추적 통계"
>abstract="푸시 추적 통계는 푸시 알림에 대한 프로필 활동 데이터를 제공합니다."

![](assets/campaign_push_tracking.png)

**[!UICONTROL 푸시 알림- 추적 통계]** 위젯은 푸시 알림과 연결된 프로필 활동에 대한 자세한 스냅숏을 제공하여 참여 및 푸시 알림 효과에 대한 중요한 통찰력을 제공합니다.

+++ 푸시 알림 - 추적 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 실행 시간]**: 되풀이하는 푸시 알림의 모든 실행 시작 시간입니다. 하나 이상의 되풀이하는 푸시 알림만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

* **[!UICONTROL 열기]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 해제).

+++

### 푸시 알림 - 전송 요약 {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="푸시 알림 - 전송 요약"
>abstract="푸시 알림 전송 요약 그래프는 전송된 푸시 알림에 사용할 수 있는 데이터를 표시합니다."

![](assets/campaign_push_sending_summary.png)

**[!UICONTROL 푸시 알림 - 전송 요약]** 그래프는 푸시 알림 활동에 대한 분석을 표시하는 동적 표현을 제공합니다. 이 그래픽 표현은 전송된 푸시 알림에 대한 포괄적인 분석을 제공합니다.

+++ 푸시 알림 - 요약 지표 전송에 대해 자세히 알아보기

* **[!UICONTROL 열기]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 해제).

* **[!UICONTROL 바운스 수]**: 전송된 총 푸시 알림 수와 관련하여 누적된 총 오류 및 자동 반환 처리 횟수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.

* **[!UICONTROL 오류]**: 프로필로 보낼 수 없는 총 오류 수입니다.

+++

### 푸시 알림 - 최적화 {#push-optimized}

>[!NOTE]
>
>**[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]** 위젯은 푸시 알림에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 [이 페이지](../building-journeys/journeys-message.md#send-time-optimization)를 참조하세요.

**[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]** 위젯은 최적화 여부에 관계없이 메시지와 관련된 기본 정보를 자세히 설명합니다.

+++ 푸시 알림 - 전송 시간 최적화 지표에 대해 자세히 알아보기

* **[!UICONTROL 배달됨]**: 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.

* **[!UICONTROL 열기]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 해제).

* **[!UICONTROL 바운스 수]**: 보낸 총 푸시 알림 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

+++

### 푸시 알림 - 오류 이유 {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="푸시 알림 - 오류 이유"
>abstract="오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 발생한 특정 오류를 확인할 수 있습니다."

![](assets/campaign_push_error_reasons.png)

**[!UICONTROL 오류 원인]** 테이블 및 그래프는 푸시 알림 전송 프로세스 중에 발생한 특정 오류를 식별하는 기능을 제공하므로 이 과정에서 발생한 문제에 대한 자세한 통찰력을 제공합니다.

### 푸시 알림 - 제외된 이유 {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="푸시 알림 - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

![](assets/campaign_push_excluded.png)

**[!UICONTROL 제외된 이유]** 그래프와 표에는 타깃팅된 프로필에서 제외된 사용자 프로필이 푸시 알림을 받지 못하는 다양한 이유가 표시됩니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.

### 푸시 알림 - 플랫폼별 분류 {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="푸시 알림 - 플랫폼별 분류"
>abstract="푸시 알림 - 플랫폼별 분류 그래프 및 테이블에서는 프로필의 운영 체제를 기반으로 푸시 알림의 성공에 대한 분류를 제공합니다."

![](assets/campaign_push_breakdown.png)

**[!UICONTROL 푸시 알림 - 플랫폼별 분류]** 그래프 및 표는 푸시 알림의 성공에 대한 자세한 분석을 제공하며 프로필의 운영 체제에 따른 통찰력을 제공합니다. 이 분류는 푸시 알림이 다양한 플랫폼에서 어떻게 작동하는지 이해하는 데 도움이 됩니다.

+++ 푸시 알림 - 플랫폼 지표별 분류에 대해 자세히 알아보기

* **[!UICONTROL 타깃팅]**: 분석 중에 처리된 총 푸시 알림 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.

* **[!UICONTROL 열기]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 해제).

* **[!UICONTROL 바운스 수]**: 전송된 총 푸시 알림 수와 관련하여 누적된 총 오류 및 자동 반환 처리 횟수입니다.

* **[!UICONTROL 오류]**: 프로필로 보낼 수 없는 총 오류 수입니다.

* **[!UICONTROL 제외됨]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

+++

## SMS 탭 {#sms-global}

**[!UICONTROL SMS]** 탭은 Campaign **[!UICONTROL 전역 보고서]**&#x200B;에서 캠페인에서 보낸 SMS 메시지와 관련된 기본 정보를 자세히 설명합니다.

### SMS - 전송 통계 {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS - 전송 통계"
>abstract="SMS - 전송 통계 테이블에는 대상 지정 메시지 또는 게재된 메시지 등과 같은 SMS 메시지에 대한 필수 데이터가 요약되어 있습니다."

![](assets/campaign_sms_sending.png)

**[!UICONTROL SMS - 전송 통계]** 표에는 SMS 메시지와 관련된 필수 데이터에 대한 간략한 요약이 있으며, 여기에는 타겟팅된 메시지 수 및 배달된 메시지 수와 같은 주요 지표가 포함되어 있습니다.

+++ SMS에 대해 자세히 알아보기 - 통계 지표 보내기

* **[!UICONTROL 실행 시간]**: 되풀이하는 SMS 메시지를 실행할 때마다 시작 시간입니다. 하나 또는 여러 개의 반복 SMS 메시지만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

* **[!UICONTROL 대상]**: 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 제외됨]**: 대상 프로필에서 제외된, 메시지를 받지 못한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: SMS 메시지의 총 전송 횟수입니다.

* **[!UICONTROL 바운스 수]**: 보낸 SMS 메시지의 총 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 오류]**: 프로필로 보낼 수 없는 총 오류 수입니다.

+++

### SMS - 추적 통계 {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_sms_tracking_statistics"
>title="SMS - 추적 통계"
>abstract="SMS - 추적 통계 위젯은 방문자와 귀하 URL의 상호 작용과 관련된 필수 정보의 포괄적인 개요를 제공합니다."

![](assets/campaign_sms_tracking.png)

**[!UICONTROL SMS - 추적 통계]** 위젯은 방문자의 URL 참여와 관련된 주요 정보에 대한 자세한 개요를 제공하여 SMS 메시지의 효과에 대한 통찰력을 제공합니다.

+++ SMS에 대해 자세히 알아보기 - 추적 통계 지표

* **[!UICONTROL 실행 시간]**: 되풀이하는 SMS를 실행할 때마다 시작 시간입니다. 하나 또는 여러 개의 반복 SMS만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

* **[!UICONTROL 클릭 수]**: SMS 메시지에서 콘텐츠를 클릭한 횟수입니다.

+++

### SMS - 날짜별 성능 {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS - 날짜별 성능"
>abstract="SMS - 날짜별 성능 위젯은 그래픽 표시를 통해 메시지에 대한 주요 정보를 제공합니다."

![](assets/campaign_sms_performance.png)

**[!UICONTROL 날짜별 SMS 성능]** 위젯에서는 그래프로 표시된 메시지와 관련된 주요 정보에 대한 자세한 개요를 제공하여 특정 기간의 성능 추세에 대한 통찰력을 제공합니다.

+++ SMS에 대한 자세한 내용 - 일자별 성능 지표

* **[!UICONTROL 전송됨]**: SMS 메시지의 총 전송 횟수입니다.

* **[!UICONTROL 바운스 수]**: 보낸 SMS 메시지의 총 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 오류]**: 프로필로 보낼 수 없는 총 오류 수입니다.

+++

### SMS - 오류 이유 {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS - 오류 이유"
>abstract="SMS - 오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 발생한 특정 오류를 확인할 수 있습니다."

![](assets/campaign_sms_error_reasons.png)

**[!UICONTROL 오류 원인]** 그래프와 표를 사용하면 SMS 메시지를 보내는 동안 발생한 특정 오류를 식별할 수 있으므로 발생한 문제를 철저히 분석할 수 있습니다.

### SMS - 제외된 이유 {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

![](assets/campaign_sms_excluded.png)

**[!UICONTROL 이유 제외]** 그래프 및 표는 타깃팅된 대상에서 사용자 프로필을 제외하여 SMS 메시지를 받지 못하게 하는 다양한 요인을 시각적으로 나타냅니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.

### SMS - 바운스 이유 {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS - 바운스 이유"
>abstract="바운스 이유 그래프와 테이블에는 바운스된 메시지와 관련하여 사용 가능한 데이터가 있습니다."

**[!UICONTROL 반송 원인]** 그래프와 표는 반송된 SMS 메시지와 관련된 데이터에 대한 포괄적인 개요를 제공하여 SMS 메시지 반송 인스턴스의 특정 이유에 대한 중요한 통찰력을 제공합니다.

### SMS - 링크를 통한 클릭 {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS - 링크를 통한 클릭"
>abstract="SMS - 링크를 통한 클릭 위젯은 메시지의 URL을 사용한 방문자 참여에 대한 필수 인사이트를 제공합니다."

![](assets/campaign_sms_clicks.png)

**[!UICONTROL SMS - 링크를 통한 클릭 수]** 위젯은 메시지에 포함된 URL에 대한 방문자의 참여에 대한 중요한 통찰력을 제공하여 가장 많은 상호 작용을 유발하는 링크에 대한 중요한 정보를 제공합니다.

## 웹 탭 {#web-tab}

**[!UICONTROL Web]** 탭은 Campaign **[!UICONTROL 전역 보고서]**&#x200B;에서 웹 페이지와 관련된 기본 정보를 자세히 설명합니다.

### 웹 성능 {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="웹 성능"
>abstract="웹 성능 KPI는 방문자의 웹 경험 참여에 대한 포괄적인 정보를 제공합니다."

![](assets/campaign_web_performance.png)

**[!UICONTROL 웹 성능]** KPI는 노출 횟수 및 상호 작용과 같은 주요 지표를 포함하여 방문자의 웹 페이지 참여에 대한 포괄적인 통찰력을 제공합니다.

+++ 웹 성능 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 노출 수]**: 웹 경험이 제공된 고유 사용자 수입니다.

* **[!UICONTROL 노출 수]**: 모든 사용자에게 전달된 총 웹 경험 수입니다.

* **[!UICONTROL 상호 작용 비율]**: 웹 페이지 참여 비율입니다. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

+++

### 웹 요약 {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="웹 요약"
>abstract="웹 요약 그래프는 지정된 기간 동안의 노출 횟수, 고유한 노출 횟수, 상호 작용을 포함한 웹 경험의 진행 상황을 보여 줍니다."

![](assets/campaign_web_summary.png)

**[!UICONTROL 웹 요약]** 그래프는 관련 기간 동안 웹 경험(노출 횟수, 고유 노출 횟수 및 상호 작용)의 발전 상태를 보여 줍니다.

+++ 웹 요약 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 노출 수]**: 웹 경험이 제공된 고유 사용자 수입니다.

* **[!UICONTROL 노출 수]**: 모든 사용자에게 전달된 총 웹 경험 수입니다.

* **[!UICONTROL 상호 작용]**: 웹 페이지에 대한 총 참여 수입니다. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

+++

### 요소별 상호 작용 {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="요소별 상호 작용"
>abstract="요소별 상호 작용 테이블은 웹 페이지의 다양한 요소에 대한 방문자의 참여의 주요 정보를 제공합니다."

![](assets/campaign_web_interactions.png)

**[!UICONTROL 요소별 상호 작용]** 표에는 웹 페이지의 다양한 요소에 대한 방문자의 참여와 관련된 포괄적인 정보가 표시되어 사용자 상호 작용 및 환경 설정에 대한 중요한 통찰력을 제공합니다.

+++ 요소 지표별 상호 작용에 대해 자세히 알아보기

* **[!UICONTROL 상호 작용]**: 웹 페이지에 대한 총 참여 수입니다. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

* **[!UICONTROL 상호 작용 비율]**: 웹 페이지 참여 비율입니다. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

+++

## DM 탭 {#direct-mail-global}

Campaign **[!UICONTROL 전역 보고서]**&#x200B;에서 **[!UICONTROL DM]** 탭은 DM 메시지와 관련된 기본 정보를 자세히 설명합니다.

### 다이렉트 메일 - 전송 통계 {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="다이렉트 메일 - 전송 통계"
>abstract="다이렉트 메일 전송 통계 테이블에는 대상 지정 메시지 또는 게재된 메시지 등과 같은 다이렉트 메일 메시지에 대한 필수 데이터가 요약되어 있습니다."

![](assets/campaign_direct_sending.png)

**[!UICONTROL DM - 전송 통계]** 표에는 DM 메시지와 관련된 필수 데이터에 대한 간략한 요약이 있으며, 여기에는 타겟팅된 메시지 수 및 배달된 메시지 수와 같은 주요 지표가 포함됩니다.

+++ DM - 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 실행 시간]**: 되풀이하는 DM을 실행할 때마다 시작 시간입니다. 하나 이상의 되풀이 DM만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

* **[!UICONTROL 대상]**: DM 메시지의 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: DM 메시지의 총 전송 수입니다.

* **[!UICONTROL 오류]**: 보내는 동안 프로필로 보낼 수 없는 총 오류 수입니다.

* **[!UICONTROL 제외됨]**: 대상 프로필에서 제외되고 DM 메시지를 받지 못한 사용자 프로필 수입니다.

+++

### 다이렉트 메일 - 오류 이유 {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="다이렉트 메일 - 오류 이유"
>abstract="다이렉트 메일 - 오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 발생한 특정 오류를 확인할 수 있습니다."

![](assets/direct-mail-report_1.png)

**[!UICONTROL DM - 오류 원인]** 그래프와 표는 DM 메시지를 보내는 동안 발생한 특정 오류를 식별하는 수단을 제공하여 발생한 모든 문제를 자세히 분석할 수 있도록 합니다.

### 다이렉트 메일 - 제외된 이유 {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="다이렉트 메일 - 제외된 이유"
>abstract="다이렉트 메일 제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

![](assets/campaign_direct_excluded.png)

**[!UICONTROL DM - 제외된 이유]** 그래프와 표는 대상 대상자에서 사용자 프로필을 제외하여 DM 메시지를 받지 못하게 한 다양한 요인을 시각적으로 보여 줍니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.

## 추가 리소스

* [캠페인 시작](../campaigns/get-started-with-campaigns.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [API 트리거 캠페인 만들기](../campaigns/api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](../campaigns/modify-stop-campaign.md)
* [캠페인 라이브 보고서](campaign-live-report.md)
