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
source-git-commit: fec72c63d41a41adce5107082c50a68a7b8c0af2
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 3%

---

# Journey Optimizer에서 추적 시작 {#get-started-tracking}

추적을 사용하면 캠페인 효과를 측정하고, 고객 경험을 최적화하고, 메시지가 의도한 수신자에게 도달하는지 확인할 수 있습니다. Journey Optimizer은 고객 상호 작용, 게재 성능 및 시스템 상태를 캡처하는 포괄적인 추적 기능을 제공하여 개인 정보를 존중하고 규정 준수를 유지하면서 데이터 중심의 의사 결정을 내리는 데 도움이 됩니다.

대부분의 추적은 메시지 및 여정을 만들 때 자동으로 구성됩니다. 고급 시나리오의 경우 사용자 지정 지표를 설정하고 URL 매개 변수를 구성하고 외부 분석 플랫폼과 통합할 수 있습니다. 기본 제공 보고서를 통해 추적 데이터에 액세스하거나 Customer Journey Analytics에서 더 자세한 분석을 위해 내보냅니다.

>[!BEGINSHADEBOX]

Journey Optimizer에서 추적할 수 있는 사항:

📧 **전자 메일 상호 작용** - 열기, 클릭 및 링크 성능

🌐 **웹 동작** - 페이지 보기, 클릭 수 및 참여 패턴

🛤️ **여정 성능** - 사용자 지정 지표, 단계 이벤트 및 전환 경로

📊 **전달성 상태** - 바운스 비율, 스팸 불만 및 보낸 사람의 신뢰도

⚙️ **시스템 작업** - 경고, 오류 및 사용자 지정 작업 성능

>[!ENDSHADEBOX]

시작하는 데 도움이 되도록 다음 필수 추적 및 모니터링 항목을 살펴보십시오.

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

## 채널 간 고객 상호 작용 추적 {#tracking-by-channel}

Journey Optimizer은 채널별 추적 기능을 제공합니다. 각 채널에 대한 추적을 구성하고 사용하는 방법은 다음과 같습니다.

+++이메일 추적

이메일 추적은 이메일 메시지를 만들 때 자동으로 활성화됩니다. Journey Optimizer은 기본적으로 열기, 클릭 수 및 구독 취소를 추적하므로 추가 구성이 필요하지 않습니다.

**추적 옵션 구성:**

* **추적 사용/사용 안 함** - 전자 메일을 디자인할 때 메시지 수준에서 추적을 제어합니다. 열기, 클릭 수 또는 두 가지 모두를 추적하도록 선택할 수 있습니다. [자세히 알아보기](../email/message-tracking.md)

* **URL 추적 매개 변수 설정** - 표면 수준에서 추적 매개 변수를 구성하여 모든 이메일 링크에 캠페인 식별자(utm_campaign, utm_source 등)를 자동으로 추가합니다. 이렇게 하면 전체 디지털 에코시스템에서 속성 추적을 사용할 수 있습니다. [자세히 알아보기](../email/url-tracking.md)

* **저장된 조각에서 링크 추적** - 추적이 활성화된 콘텐츠에서 조각을 저장하면 다른 여정 또는 캠페인에서 다시 사용할 때 해당 조각의 링크가 추적된 상태로 유지됩니다. [자세히 알아보기](../content-management/save-fragments.md)

* **미러 페이지 추적 추가** - 미러 페이지 옵션을 활성화하여 조회하는 사용자를 자동으로 추적하여 전자 메일의 웹 버전을 만듭니다. [자세히 알아보기](../email/message-tracking.md#mirror-page)

**성능 모니터링:** 열기, 클릭 수, 링크 수준 성능을 포함한 캠페인 및 여정 보고서에서 실시간 지표를 봅니다. [캠페인 보고서](../reports/campaign-global-report-cja-email.md) | [여정 보고서](../reports/journey-global-report-cja-email.md)

+++

+++웹 추적

웹 추적을 사용하려면 웹 수정 사항과의 사용자 상호 작용을 추적하기 위한 명시적 구성이 필요합니다.

**클릭 추적 설정:**

웹 페이지를 작성할 때 추적할 특정 요소(단추, 이미지, 링크)를 선택할 수 있습니다. 이렇게 하면 추가 코드 없이 이러한 요소에 대한 클릭 추적을 수행할 수 있습니다. [자세히 알아보기](../web/monitor-web-experiences.md)

* **클릭 가능한 요소를 추적합니다** - 웹 개인 설정에서 단추, 이미지, 링크 또는 대화형 요소를 선택합니다.
* **자동 데이터 수집** - 구성이 완료되면 Journey Optimizer에서 클릭 이벤트를 자동으로 캡처하여 프로필과 연결합니다.
* **실시간으로 모니터링** - 개인화 효과를 확인하기 위해 사용자 상호 작용을 추적합니다.

**추적 데이터 보기:** 보고서의 표시 지표, 클릭스루 비율 및 요소 수준 성능에 액세스합니다. [캠페인 보고서](../reports/campaign-global-report-cja-web.md) | [여정 보고서](../reports/journey-global-report-cja-web.md)

+++

+++푸시 알림 추적

푸시 추적은 자동으로 활성화되고 노출 횟수(게재됨), 클릭 수(탭) 및 열기(앱 실행)를 캡처합니다. 추적 값을 극대화하려면 푸시 콘텐츠에서 클릭 가능한 요소를 구성합니다.

**추적된 요소 구성:**

* **본문 클릭 동작** - 사용자가 알림을 탭할 때 발생하는 동작을 설정합니다. 앱 열기, 딥 링크로 이동 또는 웹 URL을 엽니다. 각 작업은 자동으로 추적됩니다. [자세히 알아보기](../push/design-push.md#on-click-behavior)

* **작업 단추 추가** - 각 단추 작업(앱 열기, 딥링크, 웹 URL)에 대해 독립적으로 추적하는 최대 3개의 단추(Android) 또는 여러 개의 단추(iOS)를 포함합니다. [자세히 알아보기](../push/design-push.md#add-buttons-push)

* **추적 사용** - 푸시 여정 활동 또는 캠페인 추적 설정에서 추적이 사용되는지 확인합니다. [자세히 알아보기](../push/create-push.md#create)

>[!NOTE]
>
>푸시 추적을 사용하려면 모바일 SDK 구현이 필요합니다. 앱에 Adobe Experience Platform Mobile SDK이 제대로 구성되어 있는지 확인합니다. [자세히 알아보기](../push/push-configuration.md#integrate-mobile-app)

**참여 분석:** 보고서에서 클릭스루 비율, 단추 성능 및 추적된 링크 세부 정보를 봅니다. [캠페인 보고서](../reports/campaign-global-report-cja-push.md) | [여정 보고서](../reports/journey-global-report-cja-push.md)

+++

+++인앱 메시지 추적

인앱 메시지는 디스플레이 및 사용자 상호 작용을 자동으로 추적합니다. 추적 효과를 극대화하도록 트리거 및 콘텐츠를 구성합니다.

**추적 설정:**

* **표시 규칙 정의** - 트리거(앱 시작, 화면 로드), 빈도 규칙 및 대상 조건을 사용하여 인앱 메시지가 표시되는 시기와 위치를 설정합니다. 적절한 구성을 통해 트리거된 메시지와 표시된 메시지를 모두 정확하게 추적할 수 있습니다.

* **추적된 요소 추가** - 메시지 콘텐츠에 단추, 링크 및 대화형 요소를 포함합니다. 각 상호 작용은 세부 레이블로 자동으로 추적됩니다.

* **표시 시간 최적화** - 요일 및 시간 규칙을 구성하여 트리거된 메시지가 실제로 사용자에게 표시될 가능성을 최대화합니다.

[인앱 메시지 구성 방법 알아보기](../in-app/create-in-app.md)

**추적되는 내용:** Journey Optimizer은 자동으로 표시, 단추 클릭, 해제, 트리거된 지표 및 표시된 지표와 연결된 성능을 캡처합니다. [캠페인 보고서](../reports/campaign-global-report-cja-inapp.md) | [여정 보고서](../reports/journey-global-report-cja-inapp.md)

+++

+++SMS 및 MMS 추적

SMS 추적을 사용하려면 최소 설정이 필요합니다. Journey Optimizer은 메시지에 포함하는 링크를 자동으로 단축하고 추적합니다.

**작동 방식:**

* **자동 링크 추적** - URL 도우미 함수를 사용하여 SMS 콘텐츠에 URL을 추가합니다. Journey Optimizer은 링크를 자동으로 단축하고 추가 구성 없이 클릭 수를 추적합니다. URL 단축법을 사용하려면 먼저 SMS 하위 도메인을 구성해야 합니다. [자세히 알아보기](../sms/sms-subdomains.md)

* **인바운드 메시지 추적** - 받는 사람의 회신이 자동으로 캡처되므로 양방향 대화 및 응답 패턴을 모니터링할 수 있습니다. [자세히 알아보기](../sms/sms-opt-out.md#sms-native-keywords)

**지표 보기:** 보고서에서 링크 클릭 데이터, 인바운드 메시지 볼륨 및 메시지 유형 성능에 액세스합니다. [캠페인 보고서](../reports/campaign-global-report-cja-sms.md) | [여정 보고서](../reports/journey-global-report-cja-sms.md)

+++

+++코드 기반 경험 추적

코드 기반 경험을 사용하려면 추적 데이터를 Adobe Experience Platform으로 보내기 위한 구현 설정이 필요합니다.

**필수 구성 요소:**

추적이 작동하려면 먼저 상호 작용 이벤트(디스플레이, 클릭 수)를 Adobe Experience Platform으로 보내도록 구현을 구성해야 합니다. 이를 위해서는 다음이 필요합니다.

* Adobe Experience Platform에 대해 구성된 데이터스트림 설정. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR)
* 웹 SDK 또는 모바일 SDK을 사용하여 코드에서 이벤트 컬렉션 구현.
* 콘텐츠를 표시하거나 클릭할 때 디스플레이 및 상호 작용 이벤트 전송.

[구현 사전 요구 사항에 대해 자세히 알아보기](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**추적되는 내용:** 구현되면 모든 디지털 접점(웹 사이트, 모바일 앱, IoT 장치 등)에서 디스플레이, 클릭 수, 클릭스루 비율 및 요소 수준 성능을 추적합니다. [캠페인 보고서](../reports/campaign-global-report-cja-code.md) | [여정 보고서](../reports/journey-global-report-cja-code.md)

+++

+++컨텐츠 카드 추적

컨텐츠 카드는 사용자 상호 작용을 자동으로 추적합니다. 추적 동작을 제어할 콘텐츠 및 표시 규칙을 구성합니다.

**구현 방법:**

* **추적된 콘텐츠 디자인** - 콘텐츠 카드에 단추와 링크를 추가합니다. 각 대화형 요소는 레이블과 URL을 사용하여 자동으로 추적됩니다.

* **지속성 구성** - 콘텐츠 카드는 앱 세션 간에 유지되므로 장기 참여 패턴을 추적할 수 있습니다. 만료 규칙을 설정하여 카드를 추적할 수 있는 기간을 제어합니다.

* **표시 규칙 설정** - 표시와 상호 작용을 정확하게 추적할 수 있도록 카드가 표시되는 시기와 위치를 정의합니다.

[콘텐츠 카드를 구성하는 방법 알아보기](../content-card/create-content-card.md)

**참여 모니터링:** 여러 세션에서 디스플레이, 클릭 수, 클릭스루 비율 및 참여 패턴을 추적합니다. [캠페인 보고서](../reports/campaign-global-report-cja-content.md) | [여정 보고서](../reports/journey-global-report-cja-content.md)

+++

+++랜딩 페이지 추적

랜딩 페이지에는 추가 설정이 필요 없는 내장 추적이 제공됩니다. Journey Optimizer은 방문, 전환 및 바운스 비율을 자동으로 캡처합니다.

**자동으로 추적되는 항목:**

* **방문 횟수** - 도달 범위를 측정하기 위한 총 방문 횟수 및 고유 방문 횟수
* **전환** - 양식 제출, 구독 확인 또는 기타 정의된 작업
* **바운스 비율** - 상호 작용하지 않고 나가는 방문자의 비율입니다.
* **성능 트렌드** - 지표가 발전하는 방식을 보여 주는 시계열 데이터

[랜딩 페이지 구성 방법 알아보기](../landing-pages/create-lp.md)

**성능 모니터링:** 시간에 따른 방문 패턴, 전환율 및 바운스 비율을 추적하여 사용자가 양식과 상호 작용하는 방법을 이해하고 개선할 영역을 식별합니다. [캠페인 보고서](../reports/lp-report-global-cja.md)

+++

## 여정 및 캠페인 활동 추적 {#journey-campaign-tracking}

채널 수준 추적을 넘어 추적을 구성하여 전반적인 성능을 측정하고 마케팅 이니셔티브 전반에 걸친 고객 행동을 이해합니다.

* **사용자 지정 성공 지표 정의** - 표준 참여 지표 외에 비즈니스 목표(구매, 등록, 갱신 등)에 맞게 특정 KPI를 구성합니다. [자세히 알아보기](../building-journeys/success-metrics.md)

* **여정 단계 이벤트 사용** - 고객이 여정을 진행할 때 취하는 모든 작업에 대한 자세한 추적을 활성화합니다. 이를 통해 시작/종료 지점, 경로 선택 및 드롭오프 위치에 대한 세분화된 가시성을 제공합니다. [자세히 알아보기](../reports/journey-step-events-overview.md)

* **예약 설정** - 전송 시간 최적화를 구성하여 다양한 타이밍 전략의 성능을 추적하고 최적의 전송 기간을 식별합니다. [자세히 알아보기](../building-journeys/send-time-optimization.md)

* **사용자 지정 작업 모니터링 구성** - API 호출, 응답 시간 및 오류 패턴을 모니터링하도록 외부 시스템과의 통합에 대한 추적을 설정합니다. [자세히 알아보기](../action/reporting.md)

* **사용자 지정 보고서를 만들고 데이터를 내보냅니다** - 더 자세한 분석을 위해 맞춤 보고서를 만들고 추적 데이터를 외부 시스템으로 내보냅니다. [자세히 알아보기](../reports/sharing-overview.md)

* **통합 성능 보기:** 캠페인과 여정 모두에 대한 포괄적인 보고서에 액세스하여 이메일, 푸시, SMS 및 기타 채널 간 성능을 비교하고 최상의 결과를 도출하는 조합을 파악합니다. [캠페인 보고서](../reports/campaign-global-report-cja.md) | [여정 보고서](../reports/journey-global-report-cja.md)

## 최적화 및 의사 결정 성능 추적 {#optimization-decisioning-tracking}

Journey Optimizer은 최적화 실험, 타기팅 전략 및 의사 결정 성능을 자동으로 추적합니다. 적절한 데이터 수집을 위해 설정을 구성합니다.

### 최적화 추적 설정 {#optimization-tracking}

* **캠페인 및 여정의 최적화**:

   * 실험을 생성할 때 추적할 지표(전환, 클릭 수, 사용자 지정 이벤트)를 정의합니다. Journey Optimizer은 각 치료에 대한 성능 데이터를 자동으로 수집합니다. [자세히 알아보기](../campaigns/optimization-experimentation.md)

   * 타깃팅 규칙을 만들어 다른 콘텐츠를 다른 대상 세그먼트에 전달합니다. Journey Optimizer은 타깃팅된 각 그룹에 대한 참여 지표를 자동으로 추적하므로 세그먼트 간에 성능을 비교할 수 있습니다. [자세히 알아보기](../campaigns/optimization-targeting.md)

* **여정 경로 최적화**: 여정에 **최적화** 활동을 추가하고 여러 경로를 구성합니다. Journey Optimizer은 프로필이 취하는 경로를 자동으로 추적하고 성능을 측정합니다. [자세히 알아보기](../building-journeys/optimize.md)

결과를 분석하려면: 실험 보고서에서 전환율, 통계적 중요도 및 처리 간 상승도를 보거나 타겟팅된 세그먼트 간의 참여 지표를 비교하십시오. [실험 캠페인 보고서](../reports/campaign-global-report-cja-experimentation.md) | [실험 여정 보고서](../reports/journey-global-report-cja-experimentation.md) | [여정 타깃팅 보고서](../reports/journey-global-report-cja.md#targeting)

### 의사 결정 성능 추적 {#decisioning-tracking}

Decisioning을 사용하여 콘텐츠를 개인화할 때 Journey Optimizer은 추가 구성 없이도 의사 결정 이벤트, 노출 횟수 및 클릭 수를 자동으로 추적합니다.

* **자동 이벤트 캡처** - Journey Optimizer은 프로필에 대한 결정 항목이 선택될 때마다 결정 이벤트를 자동으로 캡처합니다.
* **노출 추적** - 전자 메일의 경우 노출 수가 자동으로 추적됩니다. 코드 기반 경험의 경우 코드에 제안 표시 이벤트를 구현해야 합니다. [자세히 알아보기](../code-based/code-based-implementation-samples.md#client-side-how)
* **클릭 추적** - 결정 항목에 대한 클릭은 자동으로 이메일에서 추적됩니다. 코드 기반 경험에서는 클릭 이벤트를 구현해야 합니다.

>[!NOTE]
>
>**코드 기반 경험**&#x200B;에서 의사 결정을 추적하려면 구현에서 Web SDK 또는 Mobile SDK을 사용하여 Adobe Experience Platform에 제안 상호 작용 이벤트(디스플레이 및 클릭 수)를 전송하는지 확인하십시오. [자세히 알아보기](../experience-decisioning/data-collection/schema-requirement.md)

성과 모니터링: 보고서에서 의사 결정 KPI를 보고, 의사 결정 항목을 비교하고, 선택 전략을 분석하고, AI 모델 성과를 모니터링합니다. [자세히 알아보기](../experience-decisioning/cja-reporting.md)

## 추적 데이터 사용 제어 {#data-governance}

데이터 거버넌스 정책을 사용하면 조직 전체에서 추적 데이터가 사용되는 방법을 제어할 수 있습니다.

* **중요 추적 데이터에 레이블 지정** - 추적된 동작 데이터(예: 상태 콘텐츠 클릭, 금융 제품 상호 작용)에 거버넌스 레이블을 적용하여 중요 또는 규제 대상으로 표시합니다.

* **데이터 사용 제한** - 레이블이 지정된 추적 데이터를 특정 채널에서 사용하거나 서드파티 시스템으로 내보내거나 특정 개인화 시나리오에 사용할 수 없도록 하는 정책을 만듭니다.

* **자동 적용** - Journey Optimizer은 여정 및 캠페인을 만들 때 거버넌스 정책을 자동으로 확인하여 정의된 정책을 위반하여 추적된 데이터가 사용되는 경우 게시를 차단합니다.

데이터 거버넌스는 GDPR 및 CCPA와 같은 규정을 준수하는 동시에 승인된 경계 내에서 고객 행동을 추적하고 분석할 수 있도록 합니다. [자세히 알아보기](../action/action-privacy.md)

## 전달성 및 시스템 상태 모니터링 {#monitoring-capabilities}

참여 추적 외에, 메시지가 받은 편지함에 도달하고 시스템이 최적의 성능을 발휘하도록 모니터링을 구성하십시오.

게재 가능성 모니터링은 주요 지표를 추적하여 메시지가 수신자의 받은 편지함에 도달하고 올바른 발신자 평판을 유지할 수 있도록 도와줍니다.

* **금지 목록을 정기적으로 검토**&#x200B;하여 주소가 차단된 이유를 파악하고 목록 안전 상태를 유지하십시오. [자세히 알아보기](../reports/suppression-list.md)

* **게재 오류를 분석**&#x200B;하여 오류를 진단하고 수정 작업을 수행합니다. [자세히 알아보기](../configuration/email-error-types.md)

* 받은 편지함 배치를 최대화하려면 DMARC, SPF 및 DKIM의 **모범 사례를 따르세요**. [자세히 알아보기](../reports/deliverability.md)

중요한 이벤트 및 시스템 문제에 대한 실시간 알림을 받도록 사전 모니터링을 설정하여 고객 경험에 영향을 미치기 전에 신속하게 대응할 수 있습니다.

* **경고 구성** - 여정 오류, 사용자 지정 작업 오류 및 중요한 문제에 대한 실시간 알림을 설정하여 문제에 신속하게 대처합니다. [자세히 알아보기](../reports/alerts.md)

* **감사 로그 사용** - 감사 로깅을 활성화하여 규정 준수 및 문제 해결을 위해 리소스에 대한 모든 작업을 추적합니다. [자세히 알아보기](../privacy/audit-logs.md)

* **통합 모니터링** - 사용자 지정 작업 성능 및 외부 시스템 연결을 추적하여 통합 문제를 조기에 식별합니다. [자세히 알아보기](../action/reporting.md)

