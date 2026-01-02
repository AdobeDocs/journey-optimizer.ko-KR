---
solution: Journey Optimizer
product: journey optimizer
title: 여정 시작
description: 여정 시작 - Adobe Journey Optimizer에서 개인화된 고객 경험을 만들기 위한 여정 유형, 워크플로우, 기능 및 모범 사례에 대해 알아봅니다.
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 여정, 검색, 시작, 단일, 대상자 읽기, 대상자 자격, 비즈니스 이벤트, 실시간, 예약됨, 배치, 이벤트 트리거, 워크플로우, 오케스트레이션, 개인화, 멀티채널
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 3%

---


# 여정 시작{#jo-general-principle}

Adobe Journey Optimizer을 사용하면 대상의 비헤이비어와 요구에 실시간으로 적응하는 개인화된 여러 단계 고객 여정을 만들 수 있습니다. 직관적인 드래그 앤 드롭 캔버스를 사용하여 컨텍스트 기반 데이터와 대상 타겟팅을 활용하여 여러 채널에서 메시지와 작업을 오케스트레이션할 수 있으므로 최대의 효과를 얻을 수 있습니다.

이 안내서에서는 여정 기본 사항을 이해하고 사용 사례에 적합한 여정 유형을 선택하며 의미 있고 시기 적절한 고객 경험을 제공하는 여정을 자신 있게 설계하는 데 도움이 되는 명확한 로드맵을 제공합니다.

## 여정 소개

**여정**&#x200B;은(는) 고객 행동, 비즈니스 이벤트 또는 예약된 캠페인에 응답하여 채널 간에 개인화된 상호 작용을 오케스트레이션하는 자동화된 여러 단계의 고객 경험입니다.

[!DNL Journey Optimizer]을(를) 사용하여 다음을 수행합니다.

* 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 사용하여 **실시간 오케스트레이션** 사용 사례를 빌드합니다.
* 고객 행동 및 비즈니스 이벤트에 동적으로 응답하는 **여러 단계의 고급 시나리오**&#x200B;를 디자인합니다.
* 이메일, 푸시, SMS, 인앱, 웹 등에서 규모에 맞게 **1:1 개인화된 경험 제공**

![팔레트, 캔버스 및 속성 창이 있는 여정 디자이너 인터페이스](assets/journey38.png)

➡️ **빌드를 시작할 준비가 되셨습니까?** [5분 후에 첫 번째 여정 만들기](journey-gs.md).

### 여정과 캠페인: 각각 사용해야 하는 경우 {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer에서는 고객에게 도달하기 위한 세 가지 접근 방식을 제공합니다. **여정**(1:1 실시간 오케스트레이션), **캠페인**(단순 일괄 처리 또는 API 트리거 게재) 및 **오케스트레이션된 캠페인**(다중 엔티티 데이터가 있는 일괄 처리 캔버스 워크플로).

**빠른 결정:**

* 각 고객이 원하는 속도로 진행하는 여러 단계의 동작 중심의 경험에 **여정**&#x200B;을(를) 사용합니다.
* 대상자에 대한 단순, 예약 또는 트리거된 메시지 게재에 **Action/API 캠페인**&#x200B;을(를) 사용합니다.
* 다중 엔티티 세분화 및 정확한 사전 전송 카운트가 필요한 복잡한 일괄 처리 워크플로에 **오케스트레이션된 캠페인**&#x200B;을(를) 사용합니다.

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## 여정 유형 선택 {#journey-types}

Adobe Journey Optimizer은 서로 다른 시작 메커니즘 및 비즈니스 시나리오에 맞게 디자인된 4가지 여정 유형을 지원합니다.

* **단일 여정**: 이벤트가 트리거된 실시간 경험(주문 확인, 환영 이메일)
* **대상 여정 읽기**: 대상 세그먼트에 예약된 일괄 통신(뉴스레터, 프로모션 캠페인)
* **대상 자격 여정**: 대상 멤버십 변경(VIP 업그레이드, 재참여)에 대한 실시간 응답
* **비즈니스 이벤트 여정**: 여러 고객에게 영향을 주는 비즈니스 상태(인벤토리 알림, 플래시 판매)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## 여정 디자이너를 사용하여 빌드 {#journey-designer}

**[여정 디자이너](using-the-journey-designer.md)**&#x200B;은(는) 고객 경험을 만들기 위한 시각적 캔버스입니다. 직관적인 드래그 앤 드롭 인터페이스에서 코드를 작성하지 않고도 여정의 모든 단계를 오케스트레이션할 수 있습니다.

![팔레트, 캔버스 및 속성 창이 있는 여정 디자이너 인터페이스](assets/journey38.png)

### 디자이너에서 수행할 수 있는 작업:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=ko)

**진입점 정의**

이벤트, 대상 세그먼트 또는 대상 자격을 통해 고객이 입장하는 방법을 선택합니다.

[항목 관리에 대해 알아보기](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=ko)

**메시지 보내기**

Journey Optimizer에서 설계된 이메일, 푸시, SMS/MMS, 인앱, 웹 등에 기본 제공 채널 작업을 사용합니다.

[여정으로 메시지 보내기](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=ko)

**논리 및 조건 추가**

프로필 속성, 대상자 멤버십 또는 실시간 이벤트를 기반으로 여정을 분기합니다.

[조건 사용](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=ko)

**데이터 활용**

이벤트, Adobe Experience Platform 또는 서드파티 API 서비스의 컨텍스트 데이터를 사용합니다.

[데이터 소스 작업](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=ko)

**외부 시스템 연결**

메시지를 보내거나 워크플로우를 트리거하기 위해 서드파티 시스템을 통합하는 사용자 지정 작업을 만듭니다.

[사용자 정의 액션 구성](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=ko)

**오케스트레이션 활동 추가**

대기 시간, 점프, 프로필 업데이트 및 대상자 관리를 사용하여 정교한 흐름을 만듭니다.

[모든 활동 살펴보기](about-journey-activities.md)
:::

::::

➡️ **실습 학습:** [여정 디자이너 비디오 보기](#video) 또는 [엔드 투 엔드 사용 사례 탐색](jo-use-cases.md)

## 여정 생성 워크플로 {#workflow}

성공적인 여정 구축은 명확하고 반복 가능한 프로세스를 따릅니다. 다음은 단계별 워크플로입니다.

**1. 플랜** → **2. 디자인** → **3. 테스트** → **4.** 5→ **을(를) 게시합니다.** 6→ **모니터링** 최적화

### &#x200B;1. 여정 계획 {#plan}

디자이너를 열기 전에 목표를 명확히 하십시오.

* **목표가 무엇입니까?**(예: 신규 고객 온보딩, 비활성 사용자 다시 참여)
* **대상자가 누구입니까?**(특정 세그먼트, 이벤트 기반 개인)
* **어떤 여정 유형에 적합합니까?**(위의 [여정 형식](#journey-types) 참조)
* **어떤 채널을 사용하시겠습니까?**(전자 메일, 푸시, SMS 등)

### &#x200B;2. 캔버스에 디자인 {#design}

여정 디자이너를 사용하여 플로우를 빌드합니다.

* **시작 조건 설정** - 프로필이 입력하는 방법(이벤트, 대상, 자격)을 정의합니다.
* **오케스트레이션 논리 추가** - 대기 시간, 조건 및 결정 지점 포함
* **메시지 구성** - 커뮤니케이션 디자인 또는 기존 템플릿 활용
* **작업 설정** - 실행할 기본 제공 작업 또는 사용자 지정 작업을 구성합니다.
* **종료 조건 정의** - 프로필이 여정을 완료하는 시기와 방법을 지정합니다.

[여정 디자이너 → 사용 방법 알아보기](using-the-journey-designer.md)

### &#x200B;3. 라이브로 전환되기 전에 테스트 {#test}

고객이 문제를 경험하기 전에 항상 여정을 테스트하여 문제를 파악하십시오.

* **테스트 모드**&#x200B;를 사용하여 테스트 프로필로 여정 시뮬레이션
* 실제 데이터나 메시지 전송에 영향을 주지 않고 여정 실행을 미리 보려면 **시험 실행**&#x200B;을 사용하십시오.
* 모든 조건, 메시지 및 작업이 예상대로 작동하는지 확인
* 타이밍, 데이터 흐름 및 개인화 확인

[여정 테스트 →](testing-the-journey.md) | [시험 실행 →에 대해 알아보기](journey-dry-run.md)

### &#x200B;4. 여정 게시 {#publish}

테스트가 완료되면 을 게시하여 여정을 라이브로 만듭니다.

* 최종 설정 및 속성 검토
* 실제 고객을 위해 활성화하려면 게시
* 참고: 라이브 여정은 중지할 수 있지만 편집할 수는 없습니다(새 버전을 만들어야 함).

[여정 → 게시](publish-journey.md)

### &#x200B;5. 성능 모니터링 {#monitor}

여정이 실제 환경에서 어떻게 수행되는지 추적합니다.

* 여정 보고서 및 분석 보기
* 입력, 완료 및 오류율 모니터링
* 중요한 문제에 대한 경고 설정

[모니터링 및 보고 →](report-journey.md) | [알림 설정 →](../reports/alerts.md)

### &#x200B;6. 최적화 및 반복 {#optimize}

인사이트를 사용하여 다음을 개선합니다.

* 참여 지표 및 전환율 분석
* 전송 시간 최적화 테스트
* 향상된 기능을 통해 새 여정 버전 만들기
* AI 기반 권장 사항 사용

[여정 최적화 →](optimize.md) | [전송 시간 최적화 →](send-time-optimization.md)

➡️ **시작할 준비가 되셨습니까?** [지금 첫 번째 여정 만들기 →](journey-gs.md)

## 실제 사용 사례 {#use-cases}

일반적인 마케팅 문제를 해결하기 위해 여정 개념을 적용하는 방법을 보여 주는 실용적인 예제를 통해 알아보십시오.

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=ko)

**새 구독자 시작**

고객이 서비스에 가입하면 온보딩 단계를 완료하도록 유도하는 시작 여정을 트리거합니다.

[사용 사례 → 보기](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=ko)

**전송 시간 최적화**

각 고객이 참여할 가능성이 가장 높은 경우 AI를 사용하여 이메일을 전달하여 오픈률과 클릭률을 극대화합니다.

[사용 사례 → 보기](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=ko)

**게재 램프 업**

메시지 볼륨을 점차 늘려 전송 평판을 개선하고 게재 가능성 문제를 방지합니다.

[사용 사례 → 보기](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=ko)

평일별 **타겟**

고객이 여정에 입력하여 더 나은 관련성을 위해 요일을 기준으로 다양한 콘텐츠를 보냅니다.

[사용 사례 → 보기](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=ko)

**멀티채널 캠페인**

이메일, 푸시, SMS 및 웹 여정 전반에 걸쳐 원활한 경험을 단일 채널로 오케스트레이션할 수 있습니다.

[사용 사례 → 보기](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=ko)

**모든 사용 사례**

단계별 구현을 통해 여정 사용 사례의 전체 라이브러리를 살펴보십시오.

[모든 → 찾아보기](jo-use-cases.md) | [사용 사례 라이브러리 →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 여정 기능 살펴보기 {#capabilities}

여정 구축에 익숙해지면 다음과 같은 강력한 기능을 활용하여 정교한 고객 경험을 구축할 수 있습니다.

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=ko)

**고급 표현식**

데이터 조작 및 복잡한 논리를 위해 표현식 편집기를 사용하여 동적 조건 및 개인화를 빌드합니다.

[표현식에 대해 알아보기](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=ko)

**표준 시간대 관리**

자동 시간대 조정과 최적의 전송 시간을 사용하여 글로벌 대상을 처리합니다.

[표준 시간대 관리](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=ko)

**테스트 모드 및 시험 실행**

라이브로 전환하기 전에 테스트 프로필로 여정의 유효성을 검사하고 실제 데이터에 영향을 주지 않고 실행을 미리 봅니다.

[시험 실행 사용](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=ko)

**샌드박스로 복사**

샌드박스 간 여정을 복제하여 테스트 및 배포 워크플로를 간소화합니다.

[여정 복사](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=ko)

**태그 및 조직**

태그를 사용하여 여정을 분류하고 필터링하여 크기를 효율적으로 관리할 수 있습니다.

[태그로 구성](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=ko)

**처리량 제어**

전송 평판을 관리하고 압도적인 시스템을 피하기 위해 메시지 처리량을 제한합니다.

[제어 처리량](limit-throughput.md)
:::

::::

[모든 여정 기능 보기 →](/help/rp_landing_pages/manage-journey-landing-page.md)

## 시청하여 알아보기 {#video}

여정 구성 요소를 시각적으로 살펴보고 캔버스에서 여정을 작성하는 기본 사항에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **더 많은 비디오를 원하십니까?** [여정 비디오 튜토리얼 살펴보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## 일반적인 질문 {#common-questions}

+++ 캠페인과 여정 간의 차이점은 무엇입니까?

Adobe Journey Optimizer에서는 다음 세 가지 접근 방식을 제공합니다.

* **여정**: 1:1 실시간 오케스트레이션을 통해 각 프로필이 각자의 속도로 단계를 진행합니다. 조건부 논리(예: 온보딩, 장바구니 포기)를 사용하는 비헤이비어 기반 다중 단계 경험에 가장 적합합니다.

* **캠페인(작업 및 API 트리거)**: 일정에 따라 또는 API 트리거를 통해 모든 프로필에 동시에 실행되는 간단한 메시지를 대상자에게 전달합니다. 프로모션 캠페인, 뉴스레터, 트랜잭션 메시지에 적합합니다.

* **오케스트레이션된 캠페인**: 관계형 데이터(프로필 + 제품/스토어/예약)를 사용하여 복잡한 세분화를 사용하는 여러 단계 일괄 처리 워크플로우입니다. 모든 프로필이 정확한 사전 전송 카운트와 함께 처리되었습니다. 여러 엔티티 데이터가 필요한 계절 프로모션, 제품 출시, 캠페인에 가장 적합합니다.

**주요 차이점**: 여정은 실시간 작업에 대한 개별 고객 상태를 유지 관리합니다. 작업/API 캠페인은 간단한 메시지를 일괄적으로 전달합니다. 오케스트레이션된 캠페인은 다중 엔티티 세그멘테이션 기능이 있는 일괄 워크플로우 캔버스를 제공합니다.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[오케스트레이션된 캠페인에 대해 알아보기](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ 라이브 여정을 편집할 수 있습니까?

제한된 요소(이름, 메시지 콘텐츠)를 편집할 수 있지만 구조를 변경하려면 새 버전을 만들어야 합니다. [여정 버전에 대해 알아보기](publish-journey.md#journey-versions)

+++

➡️ **개 질문 더?** [전체 여정 FAQ 보기](journey-faq.md) 및 40개 이상의 세부 답변

## 도움이 필요하십니까? {#help}

### 일반적인 작업에 대한 빠른 링크

* **[첫 번째 여정 만들기](journey-gs.md)** - 초보자용 단계별 안내서
* **[여정 FAQ](journey-faq.md)** - 답변된 일반적인 질문
* **[문제 해결](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - 문제 진단 및 해결
* **[오류 코드 참조](error-codes-reference.md)** - 오류 메시지 이해
* **[보호 기능 및 제한 사항](../start/guardrails.md)** - 기술 경계 및 모범 사례

### 문제에 대한 알림 받기

여정에게 오류 또는 비정상적인 패턴이 발생할 때 실시간 알림을 받도록 **[여정 알림](../reports/alerts.md)**&#x200B;을 설정하십시오.

### 추가 리소스

* **[여정 관리 허브](/help/rp_landing_pages/manage-journey-landing-page.md)** - 필터링, 최적화 및 프로필 관리를 위한 도구
* **[여정 활동 참조](/help/rp_landing_pages/about-journey-building-landing-page.md)** - 모든 활동 유형에 대한 전체 안내서
* **[실행 문제 해결](troubleshooting-execution.md)** - 디버그 여정 실행 문제
* **[인바운드 활동 문제 해결](troubleshooting-inbound.md)** - 입력 및 자격 문제 해결

**첫 번째 여정을 빌드할 준비가 되셨습니까?** [지금 시작 →](journey-gs.md)
