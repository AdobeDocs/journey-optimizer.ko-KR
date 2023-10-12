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
source-git-commit: 2e8476636fafcba77cbd25ca13324652178224ed
workflow-type: tm+mt
source-wordcount: '3192'
ht-degree: 3%

---

# 캠페인 글로벌 보고서 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="캠페인 글로벌 보고서"
>abstract="캠페인 글로벌 보고서를 사용하여 선택된 기간에 대해 캠페인의 영향을 측정할 수 있습니다. 보고서는 캠페인 성공 사례와 오류를 자세히 설명하는 여러 위젯으로 나눠집니다. 위젯 크기를 조정하거나 위젯을 제거하여 각 보고 대시보드를 수정할 수 있습니다."

전역 보고서, 다음에서 액세스 가능: **모든 시간** 탭에는 최소 2시간 전에 발생한 이벤트가 표시되며, 선택한 기간 동안의 이벤트도 표시됩니다. 반면 라이브 보고서는 이벤트 발생으로부터 최소 2분의 시간 간격을 가지고 지난 24시간 내에 발생한 이벤트에 중점을 둡니다.

Campaign 글로벌 보고서는 Campaign에서 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다.

![](assets/campaign_report_global_5.png)

캠페인 **[!UICONTROL 글로벌 보고서]** 다음 탭이 있는 페이지가 표시됩니다.

* [Campaign](#campaign-global)
* [이메일](#email-global)
* [인앱](#inapp-global)
* [푸시](#push-global)
* [SMS](#sms-global)
* [웹](#web-tab)
* [다이렉트 메일](#direct-mail-global)

캠페인 **[!UICONTROL 글로벌 보고서]** 은 캠페인의 성공 및 오류를 자세히 설명하는 다양한 위젯으로 나뉩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [섹션](../reports/global-report.md#modify-dashboard).

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 을 참조하십시오. [이 페이지](global-report.md#list-of-components-global.md)

## 캠페인 탭 {#campaign-global}

### 게재 {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="캠페인 통계"
>abstract="Campaign의 통계 위젯에는 입력된 프로필 및 게재된 작업과 같은 캠페인과 관련된 기본 정보가 자세히 표시됩니다."

![](assets/campaign_report_global_1.png)

다음 **[!UICONTROL 캠페인 통계]** 위젯은 캠페인과 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 입력된 프로필]**: 여정을 시작한 프로필 수입니다.

* **[!UICONTROL 액션 전달됨]**: 여정의 작업이 전달된 총 고유 횟수입니다.

* **[!UICONTROL %의 액션 실패]**: 작업이 전달된 총 고유 횟수와 비교하여 여정에서 작업이 실패한 총 고유 횟수입니다.

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### 실험 보고서 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="성공 지표"
>abstract="실험 생성 시 이전에 선택한 성공 지표의 합계 값을 프로필 수로 나눈 값입니다."

![](assets/experimentation_report_3.png)

다음 **[!UICONTROL 실험]** 탭은 각 변형의 성능에 대한 주요 인사이트를 제공하며 가장 성공적인 변형을 식별합니다.

최상의 수행자를 정의하는 데 시간이 걸릴 수 있습니다. 이 아이콘으로 표시됩니다. ![](assets/experimentation_report_1.png).

+++실험 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 실험 결과]** 위젯은 각 변형의 성능을 자세히 설명합니다. 에서 처리 중 하나를 선택하여 기준선을 변경할 수 있습니다. **[!UICONTROL 기준선]** 드롭다운. 최고의 치료법은 별 모양 아이콘으로 표시됩니다.

이 표에는 다음 지표가 나와 있습니다.

* **[!UICONTROL 기준선 위로 올림]**: 기준선에 대한 해당 처리의 전환율 개선 비율을 측정합니다.

* **[!UICONTROL 신뢰도]**: 주어진 치료가 기준 치료와 동일하다는 증거. [자세히 알아보기](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 고유 아웃바운드 클릭수]**: 아웃바운드 채널 간 총 클릭 수.

* **[!UICONTROL 프로필]**: 이 처리의 대상으로 삼은 프로필 수입니다.

* **[!UICONTROL 고유 아웃바운드 클릭수/프로필]**: 실험을 만들 때 이전에 선택한 성공 지표의 총 값을 프로필 수로 나눈 값입니다.

다음 **[!UICONTROL 신뢰 구간]** 그래프는 개선 관련 불확실성을 측정합니다. 기준 처리와 최상의 성능 처리 사이의 성능 차이를 백분율로 자세히 설명합니다. [자세히 알아보기](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

마지막 위젯은 **[!UICONTROL 성공 지표]** 이전에 치료를 선택했습니다. 다음에서 다른 타겟팅된 지표를 선택할 수 있습니다. **[!UICONTROL 지표]** 드롭다운 메뉴를 사용하여 대체 데이터를 추적할 수 있습니다.

>[!CAUTION]
>
>실험으로 필터링된 지표로 작업할 때 실험을 위해 비교 페이지의 드롭다운에서 지표 선택을 변경해도 필터 값이 유지되지 않습니다. 예를 들어 &quot;클릭 수&quot;에서 &quot;고유 클릭 수&quot;로 전환하면 적용된 필터가 손실되어 비교가 부정확하거나 유효하지 않게 됩니다.

+++

이러한 결과에 대한 자세한 내용과 해석 방법은 다음을 참조하십시오. [이 페이지](../campaigns/get-started-experiment.md#interpret-results).

## 이메일 탭 {#email-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="이메일 - 전송 통계"
>abstract="이메일 - 전송 통계 표에는 타겟팅됨 또는 게재됨 등 이메일에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="이메일 - 추적 통계"
>abstract="이메일 - 추적 통계 표에는 이메일의 프로필 활동에 대한 데이터가 제공됩니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="이메일 - 전송 성능"
>abstract="이메일 - 전송 성능 그래프는 전송된 이메일에 대한 포괄적인 데이터를 제시하며 게재 및 바운스와 같은 주요 지표에 대한 통찰력을 제공하여 이메일 게재 프로세스를 자세히 분석할 수 있도록 합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="이메일 - 반송 범주"
>abstract="이메일 - 바운스 카테고리 그래프 및 표는 임시 오류와 영구 오류에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="이메일 - 반송 원인"
>abstract="이메일 - 반송 원인 그래프 및 표에는 반송된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="이메일 - 오류 원인"
>abstract="이메일 - 오류 원인 그래프 및 테이블을 사용하면 전송 프로세스 중에 발생한 특정 오류를 식별할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="이메일 - 제외된 이유"
>abstract="제외된 이유 그래프 및 표는 사용자 프로필이 타겟팅된 대상에서 제외되고 메시지가 수신되지 않은 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="이메일 - 상위 URL"
>abstract="이메일 - 상단 URL 그래프 및 표는 가장 높은 방문자 트래픽을 수신하는 이메일 내의 URL에 대한 포괄적인 개요를 제공하여 가장 인기 있는 링크를 식별할 수 있도록 합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="이메일 - 최고 수신자 도메인"
>abstract="이메일 - 최고 수신자 도메인 그래프 및 표는 수신자가 이메일을 여는 데 가장 자주 사용하는 도메인에 대한 세부 분류를 제공하므로 수신자 행동에 대한 중요한 통찰력을 제공합니다."

![](assets/campaign_report_global_2.png)

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 이메일]** 탭에서는 Campaign에서 보낸 이메일 게재와 관련된 기본 정보를 자세히 설명합니다.

+++이메일 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 이메일 전송 통계]** 그래프는 이메일의 성공 여부를 자세히 설명합니다.

* **[!UICONTROL 타깃팅됨]**: 전송 프로세스 중에 처리된 총 메시지 수입니다.

* **[!UICONTROL 전송됨]**: 이메일의 총 전송 수입니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 게재율]**: 성공적으로 전송된 메시지의 비율입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

* **[!UICONTROL 바운스 비율]**: 보낸 이메일과 비교하여 반송된 이메일의 비율.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

* **[!UICONTROL 오류율]**: 전송 프로세스 중에 발생하여 전송되지 않은 오류의 백분율입니다.

* **[!UICONTROL 다시 시도]**: 다시 시도 큐에 있는 이메일 수입니다.

* **[!UICONTROL 제외됨]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

다음 **[!UICONTROL 이메일 - 추적 통계]** 위젯에는 이메일에 대한 프로필 활동에 사용 가능한 데이터가 포함되어 있습니다.

* **[!UICONTROL 열림]**: 이메일을 연 횟수입니다.

* **[!UICONTROL 고유 열람 수]**: 열린 이메일의 비율입니다.

* **[!UICONTROL 열람률]**: 배달된 이메일 수와 비교하여 열린 이메일의 총 수입니다.

* **[!UICONTROL 클릭수]**: 이메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 고유 클릭수]**:이메일에서 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 고유 클릭률]**: 이메일과 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL 구독 취소]**: 구독 취소 링크의 클릭 수입니다.

* **[!UICONTROL 스팸 고객 불만]**: 메시지가 스팸 또는 정크로 선언된 횟수입니다.

다음 **[!UICONTROL 전송 성능]** 그래프에는 다음과 같이 보낸 이메일에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

* **[!UICONTROL 다시 시도]**: 다시 시도 큐에 있는 이메일 수입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

다음 **[!UICONTROL 바운스 이유]** 및 **[!UICONTROL 바운스 범주]** 위젯에는 다음과 같이 반송된 메시지와 관련하여 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL 하드 바운스]**: 잘못된 이메일 주소와 같은 영구 오류의 총 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL 소프트 바운스]**: 전체 받은 편지함과 같은 총 임시 오류 수.

* **[!UICONTROL 무시됨]**: 부재 중이거나 기술적인 오류와 같은 총 임시 항목 수(발신자 유형이 postmaster인 경우).

바운스에 대한 자세한 내용은 [비표시 목록](../reports/suppression-list.md) 페이지를 가리키도록 업데이트하는 중입니다.

다음 **[!UICONTROL 오류 원인]** 그래프 및 표를 통해 전송 프로세스 중에 발생한 오류를 확인할 수 있습니다.

다음 **[!UICONTROL 제외된 이유]** 그래프와 표에는 타겟팅된 프로필에서 제외된 사용자 프로필에서 메시지를 받지 못하게 한 다양한 이유가 표시됩니다.

다음 **[!UICONTROL 이메일 - 상위 URL]** 그래프와 표는 이메일의 어떤 URL이 가장 많이 방문했는지 설명합니다.

다음 **[!UICONTROL 이메일 - 상위 수신자 도메인]** 그래프 및 표에는 프로필이 이메일을 여는 데 가장 많이 사용하는 도메인이 자세히 설명되어 있습니다.

>[!CAUTION]
>
> 다음 **[!UICONTROL 이메일 - 상위 수신자 도메인]** 위젯의 정확도는 99.95%입니다.

다음 **[!UICONTROL 최적화 및 비최적화]** 그래프는 최적화 여부에 관계없이 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 열림]**: 메시지가 열린 횟수입니다.

* **[!UICONTROL 클릭수]**: 이메일에서 콘텐츠를 클릭한 횟수입니다.

다음 **[!UICONTROL 전송 시간 최적화]** 전송 방법에 따라 이메일의 성공 여부를 세부적으로 설명합니다(최적화 또는 일반).

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

>[!NOTE]
>
>다음 **[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]**  위젯은 이메일에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 을 참조하십시오. [이 페이지](../building-journeys/journeys-message.md#send-time-optimization).

+++

## 인앱 탭 {#inapp-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="인앱 성능"
>abstract="인앱 성과 KPI는 방문자의 인앱 메시지 참여에 대한 중요한 통찰력을 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="유형별 상호 작용"
>abstract="유형별 상호 작용 그래프 및 표는 사용자가 클릭, 무시 또는 상호 작용을 추적하여 인앱 메시지와 상호 작용하는 방법을 자세히 설명합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="인앱 요약"
>abstract="인앱 요약 그래프는 지정된 기간 동안 인앱 노출 횟수 및 상호 작용의 진행 상황을 보여 줍니다."

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 인앱]** 탭에서는 캠페인에 전송된 인앱 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_global_6.png)

+++인앱 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 인앱 성능]** KPI는 다음과 같이 방문자의 인앱 메시지 참여와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 고유 노출 횟수]**: 인앱 메시지가 전달된 고유 사용자 수.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 인앱 메시지 수입니다.

* **[!UICONTROL 상호 작용 비율]**: 인앱 메시지 참여 비율. 여기에는 클릭, 해제 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

다음 **[!UICONTROL 유형별 상호 작용]** 그래프 및 표는 사용자가 클릭, 무시 또는 상호 작용을 추적하여 인앱 메시지와 상호 작용하는 방법을 자세히 설명합니다.

다음 **[!UICONTROL 인앱 요약]** 그래프는 관련 기간 동안 인앱 노출 횟수 및 상호 작용의 진행 상황을 보여 줍니다.
+++

## 푸시 알림 탭 {#push-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="푸시 알림 - 전송 통계"
>abstract="푸시 알림 전송 통계 표에는 타깃팅된 메시지 또는 게재된 메시지와 같은 푸시 알림에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="푸시 알림 - 추적 통계"
>abstract="푸시 추적 통계는 푸시 알림의 프로필 활동에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="푸시 알림 - 전송 요약"
>abstract="푸시 알림 전송 요약 그래프는 전송된 푸시 알림에 사용할 수 있는 데이터를 표시합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="푸시 알림 - 제외된 이유"
>abstract="제외된 이유 그래프 및 표는 사용자 프로필이 타겟팅된 대상에서 제외되고 메시지가 수신되지 않은 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="푸시 알림 - 오류 원인"
>abstract="오류 원인 그래프 및 테이블을 사용하면 전송 프로세스 중에 발생한 특정 오류를 식별할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="푸시 알림 - 플랫폼별 분류"
>abstract="플랫폼별 분류 그래프 및 표는 프로필의 운영 체제를 기반으로 푸시 알림의 성공에 대한 분류를 제공합니다."

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 푸시 알림]** 탭에서는 캠페인에 전송된 푸시 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_global_3.png)인앱 성과 KPI는 방문자의 인앱 메시지 참여와 관련된 주요 정보를 자세히 설명합니다.

+++푸시 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 푸시 알림 - 전송 통계]** 표에서 푸시 알림과 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 타깃팅됨]**: 분석 중에 처리된 총 메시지 수입니다.

* **[!UICONTROL 전송됨]**: 푸시 알림에 대한 총 전송 수입니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 게재율]**: 성공적으로 전송된 메시지의 비율입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

* **[!UICONTROL 바운스 비율]**: 전송된 푸시 알림과 비교하여 반송된 푸시 알림의 비율입니다.

* **[!UICONTROL 오류]**: 프로필로 전송되지 않도록 하여 발생한 총 오류 수입니다.

* **[!UICONTROL 오류율]**: 전송을 방지하는 동안 발생한 오류의 백분율이 전송된 푸시 알림과 비교됩니다.

* **[!UICONTROL 제외됨]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

다음 **[!UICONTROL 푸시 - 추적 통계]** 푸시 알림에 대한 프로필 활동에 사용 가능한 데이터를 포함합니다.

* **[!UICONTROL 열림]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 열람률]**: 열린 푸시 알림의 백분율입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 버튼 클릭 또는 해제)

* **[!UICONTROL 참여 횟수]**: 이 푸시 알림에 대한 총 열기 및 작업 수(프로필에서 푸시를 열었거나 버튼을 클릭한 경우)

* **[!UICONTROL 참여율]**: 이 푸시 알림에 대한 열기 및 작업 비율(프로필에서 푸시를 열거나 버튼을 클릭한 경우)입니다.

다음 **[!UICONTROL 푸시 알림 요약]** 그래프에는 다음과 같이 전송된 푸시 알림에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL 열림]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 버튼 클릭 또는 해제)

* **[!UICONTROL 바운스]**: 총 보낸 메시지 수와 관련하여 누적된 총 오류 및 자동 반환 처리 수입니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 오류]**: 프로필로 전송되지 않도록 하여 발생한 총 오류 수입니다.

>[!NOTE]
>
>다음 **[!UICONTROL 최적화 및 비최적화]** 및 **[!UICONTROL 전송 시간 최적화]**  위젯은 푸시 알림에 대해 전송 시간 최적화 옵션이 활성화된 경우에만 사용할 수 있습니다. 전송 시간 최적화에 대한 자세한 내용은 을 참조하십시오. [이 페이지](../building-journeys/journeys-message.md#send-time-optimization).

다음 **[!UICONTROL 최적화 및 비최적화]** 그래프는 최적화 여부에 관계없이 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 열림]**: 푸시 알림이 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 버튼 클릭 또는 해제)

다음 **[!UICONTROL 전송 시간 최적화]** 전송 방식에 따라 푸시 알림의 성공 여부를 세부적으로 설명합니다(최적화 또는 일반).

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

다음 **[!UICONTROL 오류 원인]** 그래프와 표를 통해 발생한 오류를 확인할 수 있습니다.

다음 **[!UICONTROL 제외된 이유]** 그래프와 표에는 타겟팅된 프로필에서 제외된 사용자 프로필에서 메시지를 받을 수 없는 다양한 원인이 표시됩니다.

다음 **[!UICONTROL 플랫폼별 분류]** 그래프와 표는 프로필의 운영 체제에 따라 푸시 알림의 성공을 자세히 설명합니다.
+++

## SMS 탭 {#sms-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS - 전송 통계"
>abstract="SMS 전송 통계 표에는 타겟팅 또는 게재된 메시지와 같은 SMS 메시지에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS - 오류 원인"
>abstract="SMS - 오류 원인 그래프 및 테이블을 사용하면 전송 프로세스 중에 발생한 특정 오류를 식별할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS - 일자별 성능"
>abstract="날짜별 SMS 성능 위젯은 그래픽 표시를 통해 메시지에 대한 주요 정보를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS - 제외된 이유"
>abstract="제외된 이유 그래프 및 표는 사용자 프로필이 타겟팅된 대상에서 제외되고 메시지가 수신되지 않은 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS - 반송 원인"
>abstract="반송 원인 그래프 및 표에는 반송된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS - 링크를 통한 클릭 수"
>abstract="SMS - 링크를 통한 클릭 수 위젯은 메시지의 URL에 대한 방문자의 참여에 대한 중요한 인사이트를 제공합니다"

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL SMS]** 탭에서는 캠페인에 전송된 SMS 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_global_4.png)

+++SMS 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL SMS - 전송 통계]** 표에서 SMS 메시지의 성공 여부를 확인할 수 있습니다.

* **[!UICONTROL 타깃팅됨]**: 타겟 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 제외됨]**: 타겟팅된 프로필에서 제외되고 메시지를 받지 못한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: SMS 메시지의 총 전송 횟수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

* **[!UICONTROL 오류]**: 프로필로 전송되지 않도록 하여 발생한 총 오류 수입니다.

다음 **[!UICONTROL 일자별 SMS 성능]** 위젯은 그래프로 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전송됨]**: SMS 메시지의 총 전송 횟수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 보낸 메시지 수와 관련된 오류의 수입니다.

* **[!UICONTROL 오류]**: 프로필로 전송되지 않도록 하여 발생한 총 오류 수입니다.

다음 **[!UICONTROL 제외 이유]** 및 **[!UICONTROL 반송 원인]** 및 **[!UICONTROL 오류 원인]** 그래프와 테이블을 사용하면 전송 프로세스 중에 발생한 오류와 제외 사항을 확인할 수 있습니다.

다음 **[!UICONTROL SMS - 링크를 통한 클릭 수]** 위젯은 방문자의 URL 참여와 관련된 기본 정보를 자세히 설명합니다.

+++

## 웹 탭 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="웹 성능"
>abstract="웹 성능 KPI는 방문자의 웹 경험 참여에 대한 포괄적인 정보를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="웹 요약"
>abstract="웹 요약 그래프는 지정된 기간 동안 노출 횟수, 고유 노출 횟수 및 상호 작용을 포함한 웹 경험의 진행 상황을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="요소별 상호 작용"
>abstract="요소별 상호 작용 테이블은 웹 페이지에서 방문자의 다양한 요소 참여에 대한 주요 정보를 제공합니다."

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 웹]** 탭에서는 웹 페이지와 관련된 기본 정보를 자세히 설명합니다.

![](assets/web-report.png)

+++웹 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 웹 성능]** KPI는 다음과 같이 방문자의 웹 경험 참여와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 고유 노출 횟수]**: 웹 경험이 전달된 고유 사용자 수.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 웹 경험 수입니다.

* **[!UICONTROL 상호 작용 비율]**: 웹 페이지 참여 비율. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

다음 **[!UICONTROL 웹 요약]** 그래프는 관련 기간 동안 웹 경험의 진행 상황(노출 횟수, 고유 노출 횟수 및 상호 작용)을 보여 줍니다.

다음 **[!UICONTROL 요소별 상호 작용]** 표에서는 웹 페이지의 다양한 요소에 대한 방문자의 참여도와 관련된 기본 정보를 자세히 설명합니다.
+++

## 다이렉트 메일 탭 {#direct-mail-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="DM - 전송 통계"
>abstract="DM 전송 통계 표에는 타겟팅 또는 게재된 메시지와 같은 DM 메시지에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="다이렉트 메일 - 오류 원인"
>abstract="DM - 오류 원인 그래프 및 테이블을 사용하면 전송 프로세스 중에 발생한 특정 오류를 식별할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="DM - 제외된 이유"
>abstract="DM 제외 이유 그래프 및 표는 타겟 대상에서 제외한 사용자 프로필이 메시지를 받지 못하게 된 다양한 요인을 보여 줍니다."

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 다이렉트 메일]** 탭에서는 DM 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/direct-mail-report_1.png)

+++DM 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL DM - 전송 통계]** dm의 성공 여부는 다음 표에 자세히 설명되어 있습니다.

* **[!UICONTROL 타깃팅됨]**: 이 DM의 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: 이 DM에 대한 총 전송 수입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

* **[!UICONTROL 제외됨]**: 타겟팅된 프로필에서 제외되고 DM을 받지 않은 사용자 프로필 수입니다.

다음 **[!UICONTROL DM - 제외된 이유]** 및 **[!UICONTROL 다이렉트 메일 - 오류 원인]** 그래프와 테이블을 사용하면 전송 프로세스 중에 발생한 오류와 제외 사항을 확인할 수 있습니다.
+++

## 추가 리소스

* [캠페인 시작](../campaigns/get-started-with-campaigns.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [API 트리거 캠페인 만들기](../campaigns/api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](../campaigns/modify-stop-campaign.md)
* [캠페인 라이브 보고서](campaign-live-report.md)
