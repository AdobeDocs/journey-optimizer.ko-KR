---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 라이브 보고서
description: Campaign 라이브 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 7%

---

# 캠페인 라이브 보고서 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="캠페인 라이브 보고서"
>abstract="캠페인 라이브 보고서를 통해 지난 24시간의 캠페인 영향과 성과만 실시간으로 측정하고 시각화할 수 있습니다. 보고서는 캠페인 성공 사례와 오류를 자세히 설명하는 여러 위젯으로 나눠집니다. 위젯 크기를 조정하거나 위젯을 제거하여 각 보고 대시보드를 수정할 수 있습니다."

캠페인 라이브 보고서는 **[!UICONTROL 라이브 보기]** 버튼을 클릭합니다.

캠페인 **[!UICONTROL 라이브 보고서]** 페이지는 다음 탭에 표시됩니다.

* [Campaign](#campaign-live)
* [이메일](#email-live)
* [푸시](#push-live)
* [SMS](#sms-live)
* [웹](#web-tab)

캠페인 **[!UICONTROL 라이브 보고서]** 은 캠페인의 성공 및 오류를 자세히 설명하는 서로 다른 위젯으로 구분됩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오 [섹션](../reports/live-report.md#modify-dashboard).

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표에 대한 자세한 목록은 다음을 참조하십시오 [이 페이지](live-report.md#list-of-components-live).

## 캠페인 탭 {#campaign-global}

### 게재 {#delivery-global}

다음 **[!UICONTROL 캠페인 통계]** 위젯은 캠페인과 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 입력한 프로필]**: 여정을 시작한 프로필 수입니다.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 이메일 탭 {#email-live}

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 이메일]** 탭 은 campaign에서 전송된 이메일 게재와 관련된 주요 정보를 자세히 설명합니다.

![](assets/campaign_report_live_1.png)

+++이메일 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 전자 메일 전송 통계]** 위젯은 메시지에 대한 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 배달됨]**: 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.

* **[!UICONTROL 오류]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL 이메일로 지표 보내기]** 테이블 및 **[!UICONTROL 이메일 요약]** 그래프는 게재 성공에 대해 자세히 설명합니다.

* **[!UICONTROL 전송]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.

* **[!UICONTROL 오류]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL 열기]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL 클릭 수]**: 게재에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 구독 취소]**: 구독 취소 링크에 대한 클릭 수입니다.

* **[!UICONTROL 스팸 불만]**: 메시지가 스팸 또는 정크 메일로 선언된 횟수입니다.

다음 **[!UICONTROL 바운스 이유]**, **[!UICONTROL 바운스 카테고리]** 및 **[!UICONTROL 하드 및 바운스 - 이메일]** 위젯에는 다음과 같이 바운스된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL 하드 바운스]**: 잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL 소프트 바운스]**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL 무시됨]**: 부재 중 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)와 같은 총 임시 수입니다.

다음 **[!UICONTROL 오류 이유]** 및 **[!UICONTROL 제외 이유]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.

다음 **[!UICONTROL 이메일 - 최상위 수신자 도메인]** 전자 메일을 여는 데 받는 사람이 가장 많이 사용하는 도메인을 그래프 및 표 세부 사항입니다.
+++

## 푸시 알림 탭 {#push-live}

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL 푸시 알림]** 탭 은 campaign에서 전송된 푸시 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_live_2.png)

+++푸시 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

**[!UICONTROL 성능 전송 푸시 알림]**, **[!UICONTROL 푸시 알림 요약]** 및 **[!UICONTROL 지표 보내기 - 푸시별]** 위젯은 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL 전송]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.

* **[!UICONTROL 오류]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL 열기]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL 작업]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)

* **[!UICONTROL 참여 횟수]**: 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.

다음 **[!UICONTROL 오류 이유]** 및 **[!UICONTROL 제외 이유]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.

다음 **[!UICONTROL 통계 보내기 - 실패]** 위젯을 사용하면 발생한 오류 및 반송 수를 확인할 수 있습니다.

다음 **[!UICONTROL 플랫폼별 추적]**, **[!UICONTROL 플랫폼별 보내기]** 및 **[!UICONTROL 플랫폼별 분류]** 그래프 및 표는 운영 시스템에 따라 푸시 알림의 성공을 자세히 설명합니다.
+++

## SMS 탭 {#sms-live}

캠페인에서 **[!UICONTROL 라이브 보고서]**, **[!UICONTROL SMS]** 탭 은 campaign에서 전송된 SMS 게재와 관련된 주요 정보를 자세히 설명합니다.

![](assets/campaign_report_live_3.png)

+++SMS 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL SMS - 통계]** 표는 게재의 성공에 대해 자세히 설명합니다.

* **[!UICONTROL 타깃팅됨]**: 이 게재의 타겟 프로필로 자격을 얻은 사용자 프로필 수입니다.

* **[!UICONTROL 제외]**: 타겟팅된 프로필에서 제외되고 메시지를 받지 못한 사용자 프로필 수입니다.

* **[!UICONTROL 전송]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.

* **[!UICONTROL 오류]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL 클릭 수]**: 총 URL 방문 횟수.

다음 **[!UICONTROL 날짜별 SMS 성능]** 위젯은 그래프와 함께 메시지에 대한 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 전송]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL 바운스 수]**: 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.

* **[!UICONTROL 오류]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL 제외 이유]**, **[!UICONTROL 바운스 수 이유]** 및 **[!UICONTROL 오류 이유]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.
+++

## 웹 탭 {#web-tab}

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 웹]** 탭에서는 웹 페이지에 대한 기본 정보를 자세히 설명합니다.

+++웹 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 웹 성능]** KPI는 방문자가 웹 경험에 대한 참여를 기준으로 관련 주요 정보를 자세히 설명합니다.

* **[!UICONTROL 고유 노출 횟수]**: 웹 경험이 전달된 고유 사용자 수입니다.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 웹 경험 수.

* **[!UICONTROL 클릭 수]**: 총 URL 방문 횟수.

다음 **[!UICONTROL 웹 요약]** 그래프는 관련 기간에 대한 웹 경험(노출 횟수, 고유 노출 횟수 및 클릭 수)의 진화를 보여줍니다.

다음 **[!UICONTROL 요소별 클릭 수]** 표에서는 방문자가 웹 페이지의 다양한 요소와 상호 작용하여 정보를 상세하게 설명합니다.
+++

## 추가 리소스

* [캠페인 시작](../campaigns/get-started-with-campaigns.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [API로 트리거된 캠페인 만들기](../campaigns/api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](../campaigns/modify-stop-campaign.md)
* [캠페인 글로벌 보고서](campaign-global-report.md)
