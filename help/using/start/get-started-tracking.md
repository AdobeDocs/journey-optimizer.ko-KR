---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 추적 시작
description: Journey Optimizer에서 사용할 수 있는 추적 및 모니터링 기능에 대해 알아봅니다
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: 추적, 모니터링, 분석, 보고, 전달성
source-git-commit: 94350929bc9a6c2d33ac551429b844b97be04ae5
workflow-type: tm+mt
source-wordcount: '1837'
ht-degree: 3%

---

# Journey Optimizer에서 추적 시작 {#get-started-tracking}

고객이 커뮤니케이션과 상호 작용하는 방법을 이해하는 것은 의미 있는 경험을 만들고 결과를 도출하는 데 중요합니다. Journey Optimizer은 개인 정보를 보호하고 규정 준수를 유지하면서 고객 행동, 게재 성능 및 시스템 상태를 파악할 수 있는 포괄적인 추적 및 모니터링 기능을 제공합니다.

>[!BEGINSHADEBOX]

**Journey Optimizer에서 추적할 수 있는 항목:**

📧 **전자 메일 상호 작용** - 열기, 클릭 및 링크 성능

🌐 **웹 동작** - 페이지 보기, 클릭 수 및 참여 패턴

🛤️ **여정 성능** - 사용자 지정 지표, 단계 이벤트 및 전환 경로

📊 **전달성 상태** - 바운스 비율, 스팸 불만 및 보낸 사람의 신뢰도

⚙️ **시스템 작업** - 경고, 오류 및 사용자 지정 작업 성능

>[!ENDSHADEBOX]

## 채널 간 고객 상호 작용 추적 {#tracking-by-channel}

Journey Optimizer은 채널별 추적 기능을 제공합니다. 각 채널에 대한 추적을 구성하고 사용하는 방법은 다음과 같습니다.

### 이메일 추적 {#email-tracking}

이메일 추적은 이메일 메시지를 만들 때 자동으로 활성화됩니다. Journey Optimizer은 기본적으로 열기, 클릭 수 및 구독 취소를 추적하므로 추가 구성이 필요하지 않습니다.

**추적 옵션 구성:**

* **추적 사용/사용 안 함** - 전자 메일을 디자인할 때 메시지 수준에서 추적을 제어합니다. 열기, 클릭 수 또는 두 가지 모두를 추적하도록 선택할 수 있습니다. [자세히 알아보기](../email/message-tracking.md)

* **URL 추적 매개 변수 설정** - 표면 수준에서 추적 매개 변수를 구성하여 모든 이메일 링크에 캠페인 식별자(utm_campaign, utm_source 등)를 자동으로 추가합니다. 이렇게 하면 전체 디지털 에코시스템에서 속성 추적을 사용할 수 있습니다. [자세히 알아보기](../email/url-tracking.md)

* **조각에서 링크 추적** - 재사용 가능한 콘텐츠 조각의 모든 링크가 자동으로 추적되어 공유 콘텐츠 구성 요소 전반에 걸쳐 참여를 전체적으로 볼 수 있습니다.

* **미러 페이지 추적 추가** - 미러 페이지 옵션을 활성화하여 조회하는 사용자를 자동으로 추적하여 전자 메일의 웹 버전을 만듭니다. [자세히 알아보기](../email/message-tracking.md#mirror-page)

**성능 모니터링:** 열기, 클릭 수, 링크 수준 성능을 포함한 캠페인 및 여정 보고서에서 실시간 지표를 봅니다. [캠페인 보고서](../reports/campaign-global-report-cja-email.md) | [여정 보고서](../reports/journey-global-report-cja-email.md)

### 웹 추적 {#web-tracking}

웹 추적을 사용하려면 웹 수정 사항과의 사용자 상호 작용을 추적하기 위한 명시적 구성이 필요합니다.

**클릭 추적 설정:**

웹 수정을 디자인할 때 추적할 특정 요소(단추, 이미지, 링크)를 선택할 수 있습니다. 이렇게 하면 추가 코드 없이 이러한 요소에 대한 클릭 추적을 수행할 수 있습니다. [자세히 알아보기](../web/monitor-web-experiences.md)

* **클릭 가능한 요소 추적** - 웹 개인 설정에서 단추, 이미지, 링크 또는 대화형 요소를 선택합니다.
* **자동 데이터 수집** - 구성이 완료되면 Journey Optimizer에서 클릭 이벤트를 자동으로 캡처하여 프로필과 연결합니다
* **실시간으로 모니터링** - 개인화 효과를 확인하기 위해 사용자 상호 작용을 추적합니다.

**추적 데이터 보기:** 보고서의 표시 지표, 클릭스루 비율 및 요소 수준 성능에 액세스합니다. [캠페인 보고서](../reports/campaign-global-report-cja-web.md) | [여정 보고서](../reports/journey-global-report-cja-web.md)

### 푸시 알림 추적 {#push-tracking}

푸시 추적은 자동으로 활성화되고 노출 횟수(게재됨), 클릭 수(탭) 및 열기(앱 실행)를 캡처합니다. 추적 값을 극대화하려면 푸시 콘텐츠에서 클릭 가능한 요소를 구성합니다.

**추적된 요소 구성:**

* **본문 클릭 동작** - 사용자가 알림을 탭할 때 발생하는 동작을 설정합니다. 앱 열기, 딥 링크로 이동 또는 웹 URL을 엽니다. 각 작업은 자동으로 추적됩니다. [자세히 알아보기](../push/design-push.md#on-click-behavior)

* **작업 단추 추가** - 각 단추 작업(앱 열기, 딥링크, 웹 URL)에 대해 독립적으로 추적하는 최대 3개의 단추(Android) 또는 여러 개의 단추(iOS)를 포함합니다. [자세히 알아보기](../push/design-push.md#add-buttons-push)

* **추적 사용** - 푸시 여정 활동 또는 캠페인 추적 설정에서 추적이 사용되는지 확인합니다. [자세히 알아보기](../push/create-push.md#create)

>[!NOTE]
>
>푸시 추적을 사용하려면 모바일 SDK 구현이 필요합니다. 앱에 Adobe Experience Platform Mobile SDK이 제대로 구성되어 있는지 확인합니다.

**참여 분석:** 보고서에서 클릭스루 비율, 단추 성능 및 추적된 링크 세부 정보를 봅니다. [캠페인 보고서](../reports/campaign-global-report-cja-push.md) | [여정 보고서](../reports/journey-global-report-cja-push.md)

### 인앱 메시지 추적 {#inapp-tracking}

인앱 메시지는 디스플레이 및 사용자 상호 작용을 자동으로 추적합니다. 추적 효과를 극대화하도록 트리거 및 콘텐츠를 구성합니다.

**추적 구성:**

* **표시 규칙 설정** - 트리거(앱 시작, 화면 로드), 빈도 규칙 및 대상 조건을 사용하여 인앱 메시지가 표시되는 시기와 위치를 정의합니다. 적절한 구성을 통해 트리거된 메시지와 표시된 메시지를 모두 정확하게 추적할 수 있습니다. [자세히 알아보기](../in-app/create-in-app.md)

* **추적된 요소 추가** - 메시지 콘텐츠에 단추, 링크 및 대화형 요소를 포함합니다. 각 상호 작용은 세부 레이블로 자동으로 추적됩니다.

* **표시 시간 최적화** - 요일 및 시간 규칙을 구성하여 트리거된 메시지가 실제로 사용자에게 표시될 가능성을 최대화합니다.

**추적되는 내용:** Journey Optimizer은 자동으로 표시, 단추 클릭, 해제, 트리거된 지표 및 표시된 지표와 연결된 성능을 캡처합니다. [캠페인 보고서](../reports/campaign-global-report-cja-inapp.md) | [여정 보고서](../reports/journey-global-report-cja-inapp.md)

### SMS 및 MMS 추적 {#sms-tracking}

SMS 추적을 사용하려면 최소 설정이 필요합니다. Journey Optimizer은 메시지에 포함하는 링크를 자동으로 단축하고 추적합니다.

**작동 방식:**

* **자동 링크 추적** - URL 도우미 함수를 사용하여 SMS 콘텐츠에 URL을 추가합니다. Journey Optimizer은 링크를 자동으로 단축하고 추가 구성 없이 클릭 수를 추적합니다. URL 단축법을 사용하려면 먼저 SMS 하위 도메인을 구성해야 합니다. [자세히 알아보기](../sms/create-sms.md#sms-content)

* **인바운드 메시지 추적** - 받는 사람의 회신이 자동으로 캡처되므로 양방향 대화 및 응답 패턴을 모니터링할 수 있습니다.

**지표 보기:** 보고서에서 링크 클릭 데이터, 인바운드 메시지 볼륨 및 메시지 유형 성능에 액세스합니다. [캠페인 보고서](../reports/campaign-global-report-cja-sms.md) | [여정 보고서](../reports/journey-global-report-cja-sms.md)

### 코드 기반 경험 추적 {#code-based-tracking}

코드 기반 경험을 사용하려면 추적 데이터를 Adobe Experience Platform으로 보내기 위한 구현 설정이 필요합니다.

**필수 구성 요소:**

추적이 작동하려면 먼저 상호 작용 이벤트(디스플레이, 클릭 수)를 Adobe Experience Platform으로 보내도록 구현을 구성해야 합니다. 이를 위해서는 다음이 필요합니다.

* Adobe Experience Platform에 대해 구성된 데이터스트림 설정
* Web SDK 또는 Mobile SDK을 사용하여 코드에서 이벤트 컬렉션 구현
* 사용자가 개인화된 콘텐츠를 보거나 클릭할 때 제안 상호 작용 이벤트 보내기

[구현 사전 요구 사항에 대해 자세히 알아보기](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**추적되는 내용:** 구현되면 모든 디지털 접점(웹 사이트, 모바일 앱, IoT 장치 등)에서 디스플레이, 클릭 수, 클릭스루 비율 및 요소 수준 성능을 추적합니다. [캠페인 보고서](../reports/campaign-global-report-cja-code.md) | [여정 보고서](../reports/journey-global-report-cja-code.md)

### 컨텐츠 카드 추적 {#content-card-tracking}

컨텐츠 카드는 사용자 상호 작용을 자동으로 추적합니다. 추적 동작을 제어할 콘텐츠 및 표시 규칙을 구성합니다.

**구현 방법:**

* **추적된 콘텐츠 디자인** - 콘텐츠 카드에 단추와 링크를 추가합니다. 각 대화형 요소는 레이블과 URL을 사용하여 자동으로 추적됩니다.

* **지속성 구성** - 콘텐츠 카드는 앱 세션 간에 유지되므로 장기 참여 패턴을 추적할 수 있습니다. 만료 규칙을 설정하여 카드를 추적할 수 있는 기간을 제어합니다.

* **표시 규칙 설정** - 표시와 상호 작용을 정확하게 추적할 수 있도록 카드가 표시되는 시기와 위치를 정의합니다.

**참여 모니터링:** 여러 세션에서 디스플레이, 클릭 수, 클릭스루 비율 및 참여 패턴을 추적합니다. [캠페인 보고서](../reports/campaign-global-report-cja-content.md) | [여정 보고서](../reports/journey-global-report-cja-content.md)

## 랜딩 페이지 모니터링 {#landing-page-tracking}

랜딩 페이지에는 추가 설정이 필요 없는 내장 추적이 제공됩니다. Journey Optimizer은 방문, 전환 및 바운스 비율을 자동으로 캡처합니다.

**자동으로 추적되는 항목:**

* **방문 횟수** - 도달 범위를 측정하기 위한 총 방문 횟수 및 고유 방문 횟수
* **전환** - 양식 제출, 구독 확인 또는 기타 정의된 작업
* **바운스 비율** - 상호 작용하지 않고 나가는 방문자의 비율입니다.
* **성능 트렌드** - 지표가 발전하는 방식을 보여 주는 시계열 데이터

**성능 최적화:** 추적 데이터를 사용하여 양식 필드를 구체화하고, 콘텐츠 변형을 테스트하고, 효과적인 트래픽 소스를 식별하고, 포기를 줄이십시오. [자세히 알아보기](../reports/lp-report-global-cja.md)

## 여정 및 캠페인 활동 추적 {#journey-campaign-tracking}

채널 수준 추적을 넘어 추적을 구성하여 전반적인 성능을 측정하고 마케팅 이니셔티브 전반에 걸친 고객 행동을 이해합니다.

**캠페인 추적 설정:**
<!--
* **Configure optimization** - When setting up campaigns, enable experimentation or targeting to track which content variations perform best. [Learn more](../campaigns/campaigns-message-optimization.md)-->

* **전환 지표 정의** - 전환(구매, 등록, 다운로드)으로 카운트되는 작업을 지정하여 참여 지표 이상의 캠페인 효과를 측정합니다.

* **예약 설정** - 전송 시간 최적화를 구성하여 다양한 타이밍 전략의 성능을 추적하고 최적의 전송 기간을 식별합니다. [자세히 알아보기](../building-journeys/send-time-optimization.md)

**여정 추적 설정:**

* **사용자 지정 성공 지표 정의** - 표준 참여 지표 외에 비즈니스 목표(구매, 등록, 갱신 등)에 맞게 특정 KPI를 구성합니다. [자세히 알아보기](../building-journeys/success-metrics.md)

* **여정 단계 이벤트 사용** - 고객이 여정을 진행할 때 취하는 모든 작업에 대한 자세한 추적을 활성화합니다. 이를 통해 시작/종료 지점, 경로 선택 및 드롭오프 위치에 대한 세분화된 가시성을 제공합니다. [자세히 알아보기](../reports/journey-step-events-overview.md)

* **사용자 지정 작업 모니터링 구성** - API 호출, 응답 시간 및 오류 패턴을 모니터링하도록 외부 시스템과의 통합에 대한 추적을 설정합니다. [자세히 알아보기](../action/reporting.md)

* **사용자 지정 보고 및 데이터 내보내기** - 더 자세한 분석을 위해 맞춤 보고서를 작성하고 추적 데이터를 외부 시스템으로 내보냅니다. [자세히 알아보기](../reports/sharing-overview.md)

**통합 성능 보기:** 캠페인과 여정 모두에 대한 포괄적인 보고서에 액세스하여 이메일, 푸시, SMS 및 기타 채널 간 성능을 비교하고 최상의 결과를 도출하는 조합을 파악합니다. [캠페인 보고서](../reports/campaign-global-report-cja.md) | [여정 보고서](../reports/journey-global-report-cja.md)

## 최적화 성능 관리 {#optimization-tracking}

Journey Optimizer은 최적화 실험 및 타깃팅 전략을 자동으로 추적합니다. 적절한 데이터 수집을 위해 최적화를 구성합니다.

**최적화 추적 설정:**

* **실험 구성** - 실험을 만들거나 타깃팅을 사용할 때 추적할 지표(전환, 클릭 수, 사용자 지정 이벤트)를 정의합니다. Journey Optimizer은 각 치료에 대한 성능 데이터를 자동으로 수집합니다. [자세히 알아보기](../campaigns/campaigns-message-optimization.md)

* **경로 최적화 설정** - 여정에 **최적화** 활동을 추가하고 여러 경로를 구성합니다. Journey Optimizer은 프로필이 취하는 경로를 자동으로 추적하고 성능을 측정합니다. [자세히 알아보기](../building-journeys/optimize.md)

**결과 분석:** 전환 속도, 통계적 중요도 및 실험 보고서에서 처리 간 상승도를 봅니다. [캠페인 보고서](../reports/campaign-global-report-cja-experimentation.md) | [여정 보고서](../reports/journey-global-report-cja-experimentation.md)

## 의사 결정 성능 추적 {#decisioning-tracking}

Decisioning을 사용하여 콘텐츠를 개인화할 때 Journey Optimizer은 추가 구성 없이도 의사 결정 이벤트, 노출 횟수 및 클릭 수를 자동으로 추적합니다.

**추적 작동 방식:**

* **자동 이벤트 캡처** - Journey Optimizer은 프로필에 대한 결정 항목이 선택될 때마다 결정 이벤트를 자동으로 캡처합니다.
* **노출 추적** - 전자 메일의 경우 노출 수가 자동으로 추적됩니다. 코드 기반 경험의 경우 코드에 제안 표시 이벤트를 구현해야 합니다.
* **클릭 추적** - 결정 항목에 대한 클릭은 자동으로 이메일에서 추적됩니다. 코드 기반 경험에서는 클릭 이벤트를 구현해야 합니다.

**코드 기반 추적을 위한 필수 구성 요소:**

코드 기반 경험에서 의사 결정을 추적하려면 구현에서 Web SDK 또는 Mobile SDK을 사용하여 Adobe Experience Platform에 제안 상호 작용 이벤트(디스플레이 및 클릭)를 전송해야 합니다. [자세히 알아보기](../experience-decisioning/gs-experience-decisioning.md)

**성과 분석:** 보고서에서 의사 결정 KPI를 보고, 의사 결정 항목을 비교하고, 선택 전략을 분석하고, AI 모델 성과를 모니터링합니다. [자세히 알아보기](../experience-decisioning/cja-reporting.md)

## 추적 데이터 사용 제어 {#data-governance}

데이터 거버넌스 정책을 사용하면 조직 전체에서 추적 데이터가 사용되는 방법을 제어할 수 있습니다.

* **중요 추적 데이터에 레이블 지정** - 추적된 동작 데이터(예: 상태 콘텐츠 클릭, 금융 제품 상호 작용)에 거버넌스 레이블을 적용하여 중요 또는 규제 대상으로 표시합니다.

* **데이터 사용 제한** - 레이블이 지정된 추적 데이터를 특정 채널에서 사용하거나 서드파티 시스템으로 내보내거나 특정 개인화 시나리오에 사용할 수 없도록 하는 정책을 만듭니다.

* **자동 적용** - Journey Optimizer은 여정 및 캠페인을 만들 때 거버넌스 정책을 자동으로 확인하여 정의된 정책을 위반하여 추적된 데이터가 사용되는 경우 게시를 차단합니다.

데이터 거버넌스는 GDPR 및 CCPA와 같은 규정을 준수하는 동시에 승인된 경계 내에서 고객 행동을 추적하고 분석할 수 있도록 합니다. [자세히 알아보기](../action/action-privacy.md)

## 전달성 및 시스템 상태 모니터링 {#monitoring-capabilities}

참여 추적 외에, 메시지가 받은 편지함에 도달하고 시스템이 최적의 성능을 발휘하도록 모니터링을 구성하십시오.

**사전 모니터링 설정:**

* **경고 구성** - 여정 오류, 사용자 지정 작업 오류 및 중요한 문제에 대한 실시간 알림을 설정하여 문제에 신속하게 대처합니다. [자세히 알아보기](../reports/alerts.md)

* **감사 로그 사용** - 감사 로깅을 활성화하여 규정 준수 및 문제 해결을 위해 리소스에 대한 모든 작업을 추적합니다. [자세히 알아보기](../privacy/audit-logs.md)

* **통합 모니터링** - 사용자 지정 작업 성능 및 외부 시스템 연결을 추적하여 통합 문제를 조기에 식별합니다. [자세히 알아보기](../action/reporting.md)

**게재 가능성 모니터링:**

* **금지 목록을 정기적으로 검토**&#x200B;하여 주소가 차단된 이유를 파악하고 목록 안전 상태를 유지하십시오. [자세히 알아보기](../reports/suppression-list.md)

* **게재 오류를 분석**&#x200B;하여 오류를 진단하고 수정 작업을 수행합니다. [자세히 알아보기](../configuration/email-error-types.md)

* 받은 편지함 배치를 최대화하려면 DMARC, SPF 및 DKIM의 **모범 사례를 따르세요**. [자세히 알아보기](../reports/deliverability.md)

## 다음 단계: 추적 데이터 액세스 {#access-tracking-data}

추적이 구성되면 Journey Optimizer의 기본 보고 기능을 통해 데이터에 액세스할 수 있습니다.

* **실시간 모니터링** - 문제를 빠르게 식별하기 위해 여정 및 캠페인이 실행되는 동안 실시간 지표를 봅니다.
* **과거 분석** - 과거 성과를 분석하여 트렌드를 이해하고 향후 캠페인을 최적화합니다.
* **고급 분석** - 정교한 크로스 채널 분석 및 속성 모델링을 위해 Customer Journey Analytics에 연결

[보고 시작](../reports/gs-reports.md) | [Customer Journey Analytics 통합에 대해 알아보기](../reports/cja-ajo.md)

## 주요 항목 탐색 {#explore-topics}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="지표" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>성공 지표 구성</strong></a>
    </div>
    <p>
    <em>비즈니스 목표에 맞는 사용자 지정 KPI 추적</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="전달성" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>게재 가능성 모니터링</strong></a>
    </div>
    <p>
    <em>메시지가 고객 받은 편지함에 도달하는지 확인</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="보고" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>보고 살펴보기</strong></a>
    </div>
    <p>
    <em>여정 및 캠페인에 대한 실시간 및 내역 보고서 액세스</em>
    <p>
  </td>
</tr>
</table>

