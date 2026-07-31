---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 보고서
description: Campaign 보고서에서 사용자 지정 채널 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: a8927f55a10a60111fc2f5db68b3a34329d1cc35
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# 사용자 지정 채널 캠페인 보고서 {#campaign-global-report-cja-custom-channel}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer에서 사용자 지정 채널 캠페인 보고서를 읽고 사용자 지정 채널 호출에 대한 KPI, 결과, 지연 및 결과 분류를 검토하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

캠페인에서 **[!UICONTROL 보고서]** 버튼을 클릭한 다음 **[!UICONTROL 모든 시간 보고서 보기]**&#x200B;를 선택하여 사용자 지정 채널 캠페인 보고서에 액세스할 수 있습니다. [자세히 알아보기](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPI {#kpis-custom}

![](assets/kpis-custom.png)

**[!UICONTROL KPI]** 섹션은 사용자 지정 채널 호출의 작동 상태 및 안정성에 대한 통합된 보기를 제공합니다.

+++ KPI 지표에 대해 자세히 알아보기

* **[!UICONTROL 성공한 호출]**: 오류 없이 유효한 응답을 반환하는 총 HTTP 호출 수입니다.

* **[!UICONTROL 4xx 오류]**: 클라이언트측 오류로 인해 실패한 호출 수로, 구성 문제 또는 끝점 오류를 강조 표시합니다.

* **[!UICONTROL 5xx 오류]**: 서버측 오류로 인해 실패한 호출 수로, 구성 문제 또는 끝점 오류를 강조 표시합니다.

* **[!UICONTROL 시간 초과 호출]**: 최대 응답 시간을 초과하여 실패한 호출 수입니다. 이렇게 하면 외부 끝점과 관련하여 지연 또는 성능 문제를 표면화하는 데 도움이 됩니다.

* **[!UICONTROL 호출 전 오류]**: HTTP 호출이 외부 끝점에 수행되기 전에 실패한 사용자 지정 채널 전송 수입니다. 이러한 오류는 외부 시스템이 아닌 [!DNL Journey Optimizer]의 자체 인프라 계층에서 발생하며 인증 오류, 요청 생성 오류 및 HTTP 구문 분석 오류가 포함됩니다.

* **[!UICONTROL 평균 대기 시간]**: 성공한 호출, 오류 및 시간 제한을 포함하여 모든 HTTP 호출에 대한 평균 종단 간 응답 시간(밀리초)입니다.

+++

## 사용자 지정 채널 결과 {#outcomes-custom}

![](assets/outcomes-custom.png)

**[!UICONTROL 결과]** 그래프는 선택한 기간에 대한 HTTP 호출 KPI 트렌드를 표시하며, 세부기간은 선택한 시간 범위(7일 보고서의 경우 일별, 1일 시간 범위의 경우 시간별, 1시간 시간 범위의 경우 분별)에 따라 달라지는 반면, **[!UICONTROL 결과 분류]** 테이블은 이러한 HTTP 호출 지표의 최상위 수준의 엔드포인트당 전체 지표부터 해당 엔드포인트를 사용하는 사용자 지정 채널당 지표까지, 최하위 수준의 캠페인 및 여정에 이르기까지 계층적으로 분류합니다.

+++ 결과 분류 지표에 대해 자세히 알아보기

* **[!UICONTROL 사용자 지정 채널 성공]**: 오류 없이 유효한 응답을 반환하는 총 HTTP 호출 수입니다.

* **[!UICONTROL 4xx 오류]**: 클라이언트측 오류로 인해 실패한 호출 수로, 구성 문제 또는 끝점 오류를 강조 표시합니다.

* **[!UICONTROL 5xx 오류]**: 서버측 오류로 인해 실패한 호출 수로, 구성 문제 또는 끝점 오류를 강조 표시합니다.

* **[!UICONTROL 시간 초과 호출]**: 최대 응답 시간을 초과하여 실패한 호출 수입니다. 이렇게 하면 외부 끝점과 관련하여 지연 또는 성능 문제를 표면화하는 데 도움이 됩니다.

* **[!UICONTROL 호출 전 오류]**: HTTP 호출이 외부 끝점에 수행되기 전에 실패한 사용자 지정 채널 전송 수입니다. 이러한 오류는 외부 시스템이 아닌 [!DNL Journey Optimizer]의 자체 인프라 계층에서 발생하며 인증 오류, 요청 생성 오류 및 HTTP 구문 분석 오류가 포함됩니다.

* **[!UICONTROL 호출]**: 성공한 호출, 오류 및 시간 제한을 포함한 총 HTTP 호출 수

+++

## 지연 {#latency-custom}

![](assets/latency-custom.png)

**[!UICONTROL 지연]** 그래프 및 표는 지연 지표의 추세를 시각화합니다. 이러한 뷰를 통해 성능 패턴을 추적하고, 최대 지연 기간을 식별하고, 시간 경과에 따른 최적화 또는 시스템 변경의 영향을 모니터링할 수 있습니다.

+++ 지연 지표에 대해 자세히 알아보기

* **[!UICONTROL 평균 대기 시간]**: 성공한 호출, 오류 및 시간 제한을 포함하여 모든 HTTP 호출에 대한 평균 종단 간 응답 시간(밀리초)입니다.

* **[!UICONTROL 성공한 평균 대기 시간]**: 오류 없이 유효한 응답을 반환하는 HTTP 호출의 평균 전체 응답 시간(밀리초)입니다.

+++
