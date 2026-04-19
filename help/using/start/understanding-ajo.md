---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 이해
description: Adobe Journey Optimizer을 Adobe Experience Platform과 함께 사용하여 개인화된 고객 경험을 제공하는 방법에 대해 알아봅니다
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: 여정 최적화 도구, 작동 방식, 아키텍처, experience platform, 기능 영역
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
source-git-commit: 83a4b2d85866d5bbad607c6b84d0573f211fad89
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 3%

---

# Journey Optimizer 이해 {#understanding-ajo}

이 페이지에서는 Adobe Experience Platform과 Journey Optimizer이 함께 작동하는 방식을 설명하며 지속적인 데이터 경험 주기, 주요 기능 영역, 아키텍처 세부 정보 및 통합 지점에 대해 설명합니다.

Adobe Journey Optimizer과 Adobe Experience Platform은 함께 작동하여 규모에 맞게 데이터 기반 개인화를 활성화합니다. 이 페이지에서는 이러한 시스템의 작동 방식과 주요 기능 영역이 결합되어 탁월한 고객 경험을 제공하는 방법을 설명합니다. [주요 기능에 대해 알아보기](get-started.md) | [주요 용어 탐색](terminology.md)

## Journey Optimizer 작동 방식 {#how-it-works}

통합된 데이터 기반이 없으면 브랜드는 여러 채널별 도구에 의존해야 하므로 각 고객에 대한 일관된 관점을 유지하거나 고객의 행동에 실시간으로 대처하기 어렵습니다. Journey Optimizer은 Adobe Experience Platform을 기반으로 구축하여 고객 데이터, 콘텐츠 제작 및 여정 오케스트레이션을 하나의 연속적인 시스템에 연결하여 이를 해결합니다. 그 결과는 고객 충성도와 라이프타임 가치를 이끄는 의미 있는 브랜드 경험입니다.

Adobe Journey Optimizer은 개인화된 고객 여정을 만들기 위해 데이터를 수집, 분석 및 적용하는 연속 흐름으로 작동합니다.

![실시간 고객 프로필, 데이터 거버넌스 및 ID 확인과 같은 핵심 서비스를 공유하는 Real-Time CDP, Customer Journey Analytics 및 Adobe Mix Modeler과 함께 구축된 Journey Optimizer을 통해 Adobe Experience Platform을 기본 데이터 레이어로 표시하는 다이어그램입니다.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: The Foundation {#aep-foundation}

Adobe Experience Platform은 브랜드가 고객 데이터를 중앙 집중화하고 개인화된 경험에 대해 활성화할 수 있도록 하는 뼈대 역할을 합니다.

* **데이터 플랫폼** - 고객 데이터를 수집, 관리 및 구조화하여 시스템 전반에서 일관성을 보장하기 위한 중앙 허브입니다. [스키마 및 데이터 세트 알아보기](../data/get-started-schemas.md)
* **데이터 수집(소스)** - 미리 만들어진 커넥터를 사용하여 CRM 플랫폼, 웹 사이트, 모바일 앱 및 클라우드 저장소에서 데이터를 가져옵니다. [데이터 원본 탐색](get-started-sources.md)
* **실시간 고객 프로필** - 여러 소스의 데이터(이메일 상호 작용, 매장 내 구매, 웹 동작)를 병합하여 통합 프로필을 만듭니다. [프로필에 대해 알아보기](../audience/get-started-profiles.md)
* **거버넌스 계층** - 규정을 준수하면서 데이터 액세스, 개인 정보 보호 규정 준수 및 보안을 제어합니다. [개인 정보 보호 문서 보기](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: 오케스트레이션 엔진 {#ajo-orchestration}

Adobe Journey Optimizer은 Adobe Experience Platform의 데이터와 통찰력을 적용하여 지능적이고 개인화된 고객 경험을 제공합니다.

* **고객 이해** - 실시간 고객 프로필을 통해 대상 메시지를 세분화할 수 있습니다. [대상자 만들기](../audience/about-audiences.md)
* **콘텐츠 및 오퍼** - 내장된 비주얼 디자이너, 재사용 가능한 템플릿 및 중앙 집중식 자산 라이브러리를 통해 팀이 플랫폼을 떠나지 않고도 모든 채널에 대한 메시지를 작성하고 개인화할 수 있습니다. 동적 개인화는 고객 특성, 동작 및 컨텍스트를 기반으로 콘텐츠를 조정합니다. 그런 다음 실시간 의사 결정 논리는 각 개인에 대해 최상의 오퍼를 선택합니다. [콘텐츠 디자인](../../rp_landing_pages/content-management-landing-page.md) | [자산 관리](../integrations/assets.md) | [오퍼 관리](../offers/get-started/starting-offer-decisioning.md)
* **여정 및 캠페인 관리** - 상호 작용(여정) 시퀀스를 자동화하거나 일회성 타겟팅된 메시지(캠페인)를 예약합니다. [여정 작성](../building-journeys/journey-gs.md) | [캠페인 만들기](../campaigns/get-started-with-campaigns.md)
* **게재(연결)** - 이메일, SMS, 푸시 알림 및 DM과 같은 채널을 통해 메시지를 전달하고 외부 시스템으로 데이터를 내보냅니다. [채널 구성](../configuration/get-started-configuration.md)
* **측정 및 분석** - 지속적인 개선을 위한 보고서로 고객 참여 및 캠페인 성과를 추적합니다. [보고서 보기](../reports/campaign-global-report-cja.md)

### 지속적인 최적화 주기 {#optimization-cycle}

이 생태계는 지속적인 최적화 사이클로 작동합니다. 데이터는 고객 이해를 유도하여 개인화된 콘텐츠와 의사 결정을 알려줍니다. 이러한 기능은 여정으로 오케스트레이션되고, 여러 채널에 걸쳐 전달되며, 효과를 측정하고 시간이 지남에 따라 개선됩니다.

![Journey Optimizer의 지속적인 최적화 주기를 보여 주는 다이어그램: 데이터 수집은 고객 프로필을 피드합니다. 이 프로필은 콘텐츠와 오퍼 의사 결정을 알리고 여정으로 조정하며, 여러 채널에 걸쳐 전달되며, 성능을 측정하며, 시간에 따라 개선됩니다.](../assets/do-not-localize/get-started-flow.png)

## 주요 기능 영역 {#functional-areas}

Journey Optimizer에는 원활하게 함께 작동하는 7개의 주요 기능 영역이 포함되어 있습니다.

| 기능 영역 | 용도 | 주요 활동 |
|-----------------|---------|----------------|
| **데이터 관리** | 고객 데이터 구성 | 스키마를 정의하고, 데이터 세트를 만들고, 다양한 시스템에서 데이터를 가져옵니다. [자세히 알아보기](../data/get-started-schemas.md) |
| **고객 관리** | 고객이 누구인지 이해 | 통합 프로필 작성, ID 확인, 대상자 만들기 [자세히 알아보기](../audience/get-started-profiles.md) |
| **콘텐츠 관리** | 개인화된 메시지 만들기 | 이메일 디자인, 에셋 관리, 템플릿 및 조각 빌드, 콘텐츠 개인화 [자세히 알아보기](../../rp_landing_pages/content-management-landing-page.md) |
| **의사 결정 관리** | 실시간으로 최상의 오퍼 선택 | 오퍼 라이브러리 관리, 규칙 정의, 제한 적용, 순위 논리 설정. [자세히 알아보기](../offers/get-started/starting-offer-decisioning.md) |
| **여정 관리** | 자동화된 고객 경험 디자인 | 비주얼 디자이너를 사용하여 여정을 만들고, 트리거를 설정하고, 조건을 추가하고, 단계를 기다립니다. [자세히 알아보기](../building-journeys/journey-gs.md) |
| **연결** | 데이터 소스 및 채널 연결 | 소스 커넥터를 구성하고, 채널을 설정하고, 외부 플랫폼에 연결합니다. [자세히 알아보기](../configuration/get-started-configuration.md) |
| **관리 및 개인 정보** | 설정 및 규정 준수 제어 | 사용자 관리, 샌드박스 구성, 채널 설정, 개인 정보 보호 요청 처리. [자세히 알아보기](../administration/permissions.md) |

### 이러한 영역을 함께 사용하는 방법 {#working-together}

이러한 기능 영역은 연속적인 사이클에서 작동합니다.

1. **데이터 수집** - 데이터가 데이터 관리로 구성된 Adobe Experience Platform으로 이동합니다.
2. **고객 이해** - 실시간 고객 프로필은 데이터를 통합하고, 고객 관리는 대상을 만듭니다
3. **컨텐츠 및 오퍼 전략** - 컨텐츠 관리에서 메시지를 만들고 의사 결정 관리에서 오퍼 논리를 정의합니다.
4. **오케스트레이션** - 여정 관리에서 고객 데이터, 콘텐츠 및 의사 결정을 사용하여 채널 간 상호 작용을 매핑합니다.
5. **게재** - 연결을 통해 채널을 통해 메시지를 전달하거나 외부 시스템과 데이터를 공유할 수 있습니다.
6. **측정** - 성능 데이터 피드에서 대상, 콘텐츠, 의사 결정 및 여정을 세분화하기 위해 통찰력을 다시 가져옵니다.
7. **거버넌스** - 관리 및 개인 정보 보호 컨트롤을 통해 규정 준수 보장

## 아키텍처 세부 정보 {#architecture-details}

Journey Optimizer은 Real-Time CDP, Customer Journey Analytics 및 Adobe Mix Modeler과 함께 Adobe Experience Platform을 기반으로 기본적으로 구축된 4개의 애플리케이션 중 하나입니다. AEP의 핵심 서비스(실시간 고객 프로필, ID 그래프, 데이터 거버넌스 및 쿼리 서비스)를 공유하므로 별도의 통합 없이 통합 고객 데이터 파운데이션에 액세스할 수 있습니다. Journey Optimizer은 독립 실행형 애플리케이션으로 작동하거나 다른 AEP 기반 애플리케이션과 상호 작용할 수 있습니다.

통합 패턴, 사전 요구 사항 및 시스템 데이터 흐름을 포함한 기술 아키텍처에 대한 자세한 내용은 [Adobe Journey Optimizer 블루프린트](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}를 참조하십시오. 구현 고려 사항에 대해서는 [보호 기능 및 제한 사항을 검토하십시오](guardrails.md).

## 개인 정보 보호 및 보안 {#privacy-security}

Adobe Experience Cloud의 개인 정보 보호 및 보안 방침은 Adobe Journey Optimizer에 적용됩니다. 이러한 조치는 GDPR과 같은 개인 정보 보호 규정을 준수하도록 함으로써 고객 신뢰를 유지하면서 개인화된 경험을 제공할 수 있도록 합니다. [Journey Optimizer의 개인 정보 보호에 대해 자세히 알아보기](../privacy/get-started-privacy.md)
