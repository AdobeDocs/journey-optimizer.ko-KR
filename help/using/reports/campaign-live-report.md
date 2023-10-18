---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 라이브 보고서
description: Campaign 라이브 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 39%

---

# 캠페인 라이브 보고서 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="캠페인 라이브 보고서"
>abstract="캠페인 라이브 보고서를 통해 지난 24시간의 캠페인 영향과 성과만 실시간으로 측정하고 시각화할 수 있습니다. 보고서는 캠페인 성공 사례와 오류를 자세히 설명하는 여러 위젯으로 나눠집니다. 위젯 크기를 조정하거나 위젯을 제거하여 각 보고 대시보드를 수정할 수 있습니다."

[최근 24시간] 탭에서 액세스할 수 있는 라이브 보고서에는 지난 24시간 내에 발생한 이벤트를 표시하며 이벤트 발생에서 최소 2분 간격이 있습니다. 이에 비해 글로벌 보고서는 최소 2시간 전에 발생한 이벤트에 중점을 두며 선택한 기간 동안의 이벤트를 다룹니다.

Campaign 라이브 보고서는 캠페인에서 **[!UICONTROL 라이브 뷰]** 단추를 클릭합니다.

캠페인 **[!UICONTROL 라이브 보고서]** 다음 탭이 있는 페이지가 표시됩니다.

* [Campaign](#campaign-live)
* [이메일](#email-live)
* [인앱](#inapp-live)
* [푸시](#push-live)
* [SMS](#sms-live)
* [웹](#web-tab)
* [다이렉트 메일](#direct-mail-tab)

캠페인 **[!UICONTROL 라이브 보고서]** 은 캠페인의 성공 및 오류를 자세히 설명하는 다양한 위젯으로 나뉩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [섹션](../reports/live-report.md#modify-dashboard).

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 을 참조하십시오. [이 페이지](live-report.md#list-of-components-live).

## 캠페인 탭 {#campaign-live}

### 게재 {#delivery-live}

다음 **[!UICONTROL 캠페인 통계]** 위젯은 캠페인과 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 입력된 프로필]**: 여정을 시작한 프로필 수입니다.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 이메일 탭 {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="이메일 - 전송 통계"
>abstract="이메일 - 전송 통계 그래프에는 지난 24시간 동안의 대상 지정 또는 게재됨 등과 같은 이메일에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="이메일 - 통계"
>abstract="이메일 - 통계 테이블은 지난 24시간 동안 이메일의 프로필 활동에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="이메일 - 바운스 범주"
>abstract="이메일 - 바운스 범주 그래프와 테이블은 지난 24시간 동안의 일시적 오류와 영구적 오류에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="이메일 - 날짜별 성능"
>abstract="이메일 - 날짜별 성능 그래프는 전송된 이메일에 관한 지난 24시간의 포괄적인 데이터를 제공하여 게재 및 바운스와 같은 주요 지표에 대한 통찰력을 제공하고 이메일 게재 프로세스를 자세하게 분석할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="이메일 - 바운스 이유"
>abstract="이메일 - 바운스 이유 그래프와 테이블에는 지난 24시간 동안 바운스된 메시지와 관련하여 사용 가능한 데이터가 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="이메일 - 오류 이유"
>abstract="이메일 - 오류 이유 그래프와 테이블을 통해 지난 24시간 동안 전송 프로세스 중에 발생한 특정 오류를 확인할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="이메일 - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 지난 24시간 동안 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="이메일 - 최고 수신자 도메인"
>abstract="이메일 - 최고 수신자 도메인 그래프 및 테이블에서는 수신자가 이메일을 열 때 가장 자주 사용하는 도메인에 대한 자세한 분석을 통해 지난 24시간의 수신자 동작에 대한 귀중한 통찰력을 제공합니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 이메일]** 탭은 캠페인에서 보낸 이메일과 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_live_1.png)

+++이메일 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 이메일 전송 통계]** 위젯은 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않는 총 오류 수입니다.

다음 **[!UICONTROL 이메일로 지표 보내기]** 테이블 및 **[!UICONTROL 이메일 요약]** 그래프는 이메일의 성공 여부를 자세히 설명합니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않는 총 오류 수입니다.

* **[!UICONTROL 열림]**: 메시지가 열린 횟수입니다.

* **[!UICONTROL 클릭수]**: 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 구독 취소]**: 구독 취소 링크의 클릭 수입니다.

* **[!UICONTROL 스팸 고객 불만]**: 메시지가 스팸 또는 정크로 선언된 횟수입니다.

다음 **[!UICONTROL 바운스 이유]** 및 **[!UICONTROL 바운스 범주]** 위젯에는 다음과 같이 반송된 메시지와 관련하여 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL 하드 바운스]**: 잘못된 이메일 주소와 같은 영구 오류의 총 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL 소프트 바운스]**: 전체 받은 편지함과 같은 총 임시 오류 수.

* **[!UICONTROL 무시됨]**: 부재 중이거나 기술적인 오류와 같은 총 임시 항목 수(발신자 유형이 postmaster인 경우).

다음 **[!UICONTROL 오류 원인]** 및 **[!UICONTROL 제외 이유]** 그래프와 표를 사용하면 전송 프로세스 중에 발생한 오류와 제외 사항을 확인할 수 있습니다.

다음 **[!UICONTROL 이메일 - 최고 수신자 도메인]** 그래프 및 표는 수신자가 이메일을 여는 데 가장 많이 사용하는 도메인을 자세히 설명합니다.
+++

## 인앱 탭 {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="인앱 성능"
>abstract="인앱 성능 KPI는 지난 24시간 동안 방문자의 인앱 메시지 참여에 대한 필수 통찰력을 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="유형별 상호 작용"
>abstract="유형별 상호 작용 그래프와 테이블에서는 지난 24시간 동안의 클릭, 해제 또는 상호 작용을 추적하여 사용자가 인앱 메시지와 상호 작용하는 방식을 자세히 설명합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="인앱 요약"
>abstract="인앱 요약 그래프에서는 지난 24시간 동안의 인앱 노출 횟수 및 상호 작용 진행 상황을 보여 줍니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 인앱]** 탭에서는 캠페인에서 보낸 인앱 메시지와 관련된 기본 정보를 자세히 설명합니다.

+++인앱 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 인앱 성능]** KPI는 다음과 같이 방문자의 인앱 메시지 참여와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전송된 인앱 메시지의 총 수입니다.

* **[!UICONTROL 상호 작용]**: 인앱 메시지를 사용한 총 참여 수입니다. 여기에는 클릭, 해제 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

다음 **[!UICONTROL 인앱 요약]** 그래프는 관련 기간 동안 인앱 노출 횟수 및 상호 작용의 진행 상황을 보여 줍니다.

다음 **[!UICONTROL 유형별 상호 작용]** 그래프 및 표는 사용자가 클릭, 무시 또는 상호 작용을 추적하여 인앱 메시지와 상호 작용하는 방법을 자세히 설명합니다.

+++

## 푸시 알림 탭 {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="푸시 알림 - 전송 성능"
>abstract="푸시 알림 전송 성능 그래프에는 지난 24시간 동안의 오류, 게재된 메시지 등 푸시 알림에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="푸시 알림 - 통계"
>abstract="푸시 통계 테이블은 지난 24시간 동안의 푸시 알림 수신자 활동에 대한 데이터를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="푸시 알림 - 전송 요약"
>abstract="푸시 알림 전송 요약 그래프에는 지난 24시간 동안 전송된 푸시 알림에 사용 가능한 데이터가 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="푸시 알림 - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 지난 24시간 동안 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="푸시 알림 - 오류 이유"
>abstract="오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 지난 24시간 동안 발생한 특정 오류를 확인할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="푸시 알림 - 플랫폼별 분류"
>abstract="플랫폼별 분류 그래프 및 테이블은 수신자의 운영 체제를 기준으로 지난 24시간 동안의 푸시 알림 성공 분류를 제공합니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 푸시 알림]** 탭에서는 캠페인에서 전송된 푸시 알림과 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_live_2.png)

+++푸시 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

**[!UICONTROL 푸시 알림 전송 성능]**, **[!UICONTROL 푸시 알림 요약]** 및 **[!UICONTROL 푸시 알림 - 통계]** 위젯은 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

* **[!UICONTROL 열림]**: 메시지가 열린 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 버튼 클릭 또는 해제)

* **[!UICONTROL 참여 횟수]**: 이 푸시 알림에 대한 총 열기 및 작업 수(프로필에서 푸시를 열었거나 버튼을 클릭한 경우)

다음 **[!UICONTROL 오류 원인]** 및 **[!UICONTROL 제외 이유]** 그래프 및 표를 사용하면 전송 프로세스 중에 발생한 오류 및 제외 사항을 확인할 수 있습니다.

다음 **[!UICONTROL 전송 통계 - 실패]** 위젯을 통해 발생한 오류 및 바운스 수를 볼 수 있습니다.

다음 **[!UICONTROL 플랫폼을 통한 추적]**, **[!UICONTROL 플랫폼을 통한 전송]** 및 **[!UICONTROL 플랫폼별 분류]** 그래프 및 표는 운영 체제에 따라 푸시 알림의 성공 여부를 자세히 설명합니다.
+++

## SMS 탭 {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS - 통계"
>abstract="SMS 전송 통계 테이블에는 지난 24시간 동안의 대상 지정 메시지 또는 게재된 메시지 등과 같은 SMS 메시지에 대한 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS - 날짜별 성능"
>abstract="SMS 날짜별 성능 위젯은 그래픽 표시를 통해 지난 24시간 동안의 메시지에 대한 주요 정보를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS - 오류 원인"
>abstract="SMS - 오류 이유 그래프와 테이블을 통해 전송 프로세스 중에 지난 24시간 동안 발생한 특정 오류를 확인할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS - 제외된 이유"
>abstract="제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 지난 24시간 동안 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS - 바운스 이유"
>abstract="바운스 이유 그래프와 테이블에는 지난 24시간 동안 바운스된 메시지와 관련하여 사용 가능한 데이터가 있습니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL SMS]** 탭에서는 캠페인에서 보낸 SMS 메시지와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_live_3.png)

+++SMS 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL SMS - 통계]** 표에서 SMS 메시지의 성공 여부를 확인할 수 있습니다.

* **[!UICONTROL 타깃팅됨]**: 타겟 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 제외됨]**: 타겟팅된 프로필에서 제외되고 메시지를 받지 못한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않는 총 오류 수입니다.

* **[!UICONTROL 클릭수]**: 총 URL 방문 수

다음 **[!UICONTROL 일자별 SMS 성능]** 위젯은 그래프로 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 바운스]**: 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

다음 **[!UICONTROL 제외 이유]**, **[!UICONTROL 반송 원인]** 및 **[!UICONTROL 오류 원인]** 그래프와 테이블을 사용하면 전송 프로세스 중에 발생한 오류와 제외 사항을 확인할 수 있습니다.
+++

## 웹 탭 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="웹 성능"
>abstract="웹 성능 KPI는 지난 24시간 동안 웹 경험에 대한 방문자의 참여와 관련된 포괄적인 정보를 제공합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="웹 요약"
>abstract="웹 요약 그래프는 지난 24시간 동안의 노출 횟수, 고유한 노출 횟수, 상호 작용을 포함한 웹 경험의 진행 상황을 보여 줍니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="요소별 상호 작용"
>abstract="요소별 상호 작용 테이블은 지난 24시간 동안 웹 페이지의 다양한 요소에 대한 방문자의 참여의 주요 정보를 제공합니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 웹]** 탭에서는 웹 페이지와 관련된 기본 정보를 자세히 설명합니다.

+++웹 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 웹 성능]** KPI는 다음과 같이 방문자의 웹 경험 참여와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 웹 경험 수입니다.

* **[!UICONTROL 상호 작용]**: 웹 페이지에 대한 총 참여 수입니다. 여기에는 클릭 또는 기타 상호 작용과 같이 사용자가 수행한 모든 작업이 포함됩니다.

다음 **[!UICONTROL 웹 요약]** 그래프는 지난 24시간 동안 웹 경험(노출 횟수, 고유 노출 횟수 및 상호 작용)이 발전한 모습을 보여 줍니다.

다음 **[!UICONTROL 요소별 상호 작용]** 표에서는 웹 페이지의 다양한 요소에 대한 방문자의 참여도와 관련된 기본 정보를 자세히 설명합니다.
+++

## 다이렉트 메일 탭 {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="다이렉트 메일 - 전송 통계"
>abstract="다이렉트 메일 전송 통계 테이블에는 대상 지정 메시지 또는 게재된 메시지 등과 같은 다이렉트 메일 메시지에 대한 지난 24시간 동안의 필수 데이터가 요약되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="다이렉트 메일 - 오류 이유"
>abstract="다이렉트 메일 - 오류 원인 그래프 및 테이블을 통해 지난 24시간 동안 발생한 특정 오류를 확인할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="다이렉트 메일 - 제외된 이유"
>abstract="다이렉트 메일 제외된 이유 그래프와 테이블에서는 타겟팅된 대상자에서 제외된 사용자 프로필이 지난 24시간 동안 메시지를 받지 못하는 다양한 요인을 보여 줍니다."

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 다이렉트 메일]** 탭에서는 DM과 관련된 기본 정보를 자세히 설명합니다.

![](assets/direct-mail-report_2.png)

+++DM 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL DM - 전송 통계]** 다음 표에서 다이렉트 메일의 성공 여부를 자세히 확인할 수 있습니다.

* **[!UICONTROL 타깃팅됨]**: 타겟 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 전송됨]**: 총 전송 수입니다.

* **[!UICONTROL 오류]**: 전송 프로세스 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

* **[!UICONTROL 제외됨]**: 타겟팅된 프로필에서 제외되고 DM을 받지 않은 사용자 프로필 수입니다.

다음 **[!UICONTROL DM - 제외된 이유]** 및 **[!UICONTROL 다이렉트 메일 - 오류 원인]** 그래프와 표를 사용하면 전송 프로세스 중에 발생한 오류와 제외 사항을 확인할 수 있습니다.
+++

## 추가 리소스

* [캠페인 시작](../campaigns/get-started-with-campaigns.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [API 트리거 캠페인 만들기](../campaigns/api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](../campaigns/modify-stop-campaign.md)
* [캠페인 글로벌 보고서](campaign-global-report.md)
