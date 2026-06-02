---
solution: Journey Optimizer
product: journey optimizer
title: 패키지별 Journey Optimizer 기능
description: 라이선스, 패키지 및 활성화된 채널에 따라 사용할 수 있는 Adobe Journey Optimizer 기능을 이해합니다.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: 여정 최적화 도구, 패키지, 라이선스, 선택, prime, ultimate, 기능, 기능, 모듈식, 채널
hide: true
source-git-commit: 5e9ffb790127aae281dd15ad0eac03dbe0bb05e2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 6%

---


# 내 [!DNL Adobe Journey Optimizer] 패키지에서 사용할 수 있는 항목 {#ajo-packages}

[!DNL Adobe Journey Optimizer] 기능은 사용권 계약, 사용 가능한 채널 및 사용자 권한에 따라 다릅니다. 이 안내서를 사용하여 패키지에서 일반적으로 사용할 수 있는 기능을 파악하고 각 기능에 대한 제품 설명서로 직접 이동합니다.

채널 구성, 구현 사전 요구 사항 및 구입한 추가 기능에 따라 사용 가능 여부가 달라질 수도 있습니다. 라이선스 모델과 일치하는 탭을 선택합니다.

>[!BEGINTABS]

>[!TAB 여정 및 캠페인]

이 탭은 현재 [!DNL Adobe Journey Optimizer] 모듈식 패키징 모델에 따라 라이선스가 부여된 고객(Journey Optimizer - 캠페인, Journey Optimizer - 여정 또는 Journey Optimizer - 캠페인 및 여정)에게 적용됩니다.

## 기본 패키지 {#current-packages}

| 패키지 | 포함 사항 |
|---------|----------------|
| **Journey Optimizer - 캠페인** | Campaign Orchestration: 일괄 처리를 위한 단일 또는 다중 단계 대상 워크플로 이메일, 푸시 및 SMS를 통한 트랜잭션 메시징이 포함되었습니다. |
| **Journey Optimizer - 여정** | 실시간 Journey Orchestration: 스트리밍 및 일괄 처리를 지원하는 이벤트에서 트리거된 여정. 이메일, 푸시 및 SMS를 통한 트랜잭션 메시징이 포함되었습니다. |
| **Journey Optimizer - 캠페인 및 여정** | Campaign Orchestration과 실시간 Journey Orchestration이 결합되었습니다. 이메일, 푸시 및 SMS를 통한 트랜잭션 메시징이 포함되었습니다. |

>[!NOTE]
>
>총 데이터 볼륨 권한 부여는 패키지별로 다릅니다. **캠페인** 고객은 주소 지정 프로필당 15KB의 권한을 갖습니다. **여정** 및 **캠페인 및 여정** 고객은 주소 지정 프로필당 75KB의 권한을 갖습니다.

다음 추가 기능은 모든 기본 패키지 위에 채널 범위를 확장합니다. **모든 채널** 추가 기능은 아웃바운드 게재, 모바일 및 웹을 함께 묶습니다.

| 추가 기능 | 채널 잠금 해제됨 |
|--------|----------------|
| **아웃바운드 게재** | 이메일, 푸시 알림, DM. 전달성 기본 사항이 포함되어 있습니다. |
| **모바일** | 모바일 표면에 대한 인앱 메시지, 푸시 알림, 콘텐츠 카드 및 코드 기반 채널 |
| **웹** | 웹 표면에 대한 웹 채널 및 코드 기반 채널 |
| **모든 채널** | 번들 아웃바운드 게재 + 모바일 + 웹 |
| **의사 결정** | 실시간 오퍼 의사 결정 및 AI 기반 최적화 |

## 기능 매트릭스 {#capability-matrix-current}

| 기능 | 수행 가능한 작업 | Journey Optimizer - 캠페인 | JOURNEY OPTIMIZER - 여정 | Journey Optimizer - 캠페인 및 여정 | 추가 기능 필요 | 자세히 알아보기 |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **트랜잭션 메시지** | 이메일, 푸시 또는 SMS를 통해 실시간 트리거 메시지 전송 | ✓ | ✓ | ✓ | — | [트랜잭션 메시지에 대해 알아보기](../building-journeys/journey-gs.md) |
| **이메일** | 개인화된 이메일 메시지 디자인 및 보내기 | ✓ | ✓ | ✓ | 아웃바운드 게재 | [전자 메일을 보내는 방법 알아보기](../email/get-started-email.md) |
| **푸시 알림** | 모바일 푸시 알림 보내기 | ✓ | ✓ | ✓ | 아웃바운드 게재 | [푸시 알림을 보내는 방법 알아보기](../push/get-started-push.md) |
| **다이렉트 메일** | 실제 메일 부분 만들기 및 보내기 | ✓ | ✓ | ✓ | 아웃바운드 게재 | [DM 사용 방법 알아보기](../direct-mail/get-started-direct-mail.md) |
| **SMS / MMS** | 텍스트 및 멀티미디어 메시지 보내기 | ✓ | ✓ | ✓ | 아웃바운드 게재 | [모바일 메시지를 보내는 방법 알아보기](../mobile/get-started-mobile.md) |
| **인앱 메시지** | 모바일 앱 내 메시지 표시 | ✓ | ✓ | ✓ | 모바일 | [인앱 메시지 사용 방법 알아보기](../in-app/get-started-in-app.md) |
| **콘텐츠 카드** | 지속적인 비간섭적 제품 내 메시지 전달 | ✓ | ✓ | ✓ | 모바일 | [콘텐츠 카드 사용 방법 알아보기](../content-card/get-started-content-card.md) |
| **웹 채널** | 실시간으로 웹 페이지 개인화 | ✓ | ✓ | ✓ | 웹 | [웹 채널 사용 방법 알아보기](../web/get-started-web.md) |
| **코드 기반 경험** | API 또는 SDK을 통해 모든 표면 개인화 | ✓ | ✓ | ✓ | 모바일 또는 웹 | [코드 기반 경험을 사용하는 방법 알아보기](../code-based/get-started-code-based.md) |
| **WhatsApp** | WhatsApp Business를 통해 메시지 보내기 | ✓ | ✓ | ✓ | WhatsApp | [WhatsApp 사용 방법 알아보기](../whatsapp/get-started-whatsapp.md) |
| **오케스트레이션된 캠페인** | 일괄 처리를 위한 여러 단계 대상 워크플로우를 디자인할 수 있습니다. 지원되는 채널: 이메일, SMS, 푸시 및 DM만 | ✓ | — | ✓ | — | [오케스트레이션된 캠페인을 사용하는 방법을 알아보세요](../orchestrated/gs-orchestrated-campaigns.md) |
| **자동화된 여정** | 이벤트가 트리거되는 실시간 고객 여정 디자인 | — | ✓ | ✓ | — | [여정 작성 방법 알아보기](../building-journeys/journey-gs.md) |
| **실시간 트리거** | 고객 이벤트 발생 시 대응 | — | ✓ | ✓ | — | [여정 이벤트에 대해 알아보기](../event/about-events.md) |
| **의사 결정** | 각 고객을 위한 최적의 오퍼를 실시간으로 선택 | 라이선스에 따라 다릅니다. | 라이선스에 따라 다릅니다. | 라이선스에 따라 다릅니다. | 결정 | [의사 결정 사용 방법 알아보기](../experience-decisioning/gs-experience-decisioning.md) |
| **AI 기반 순위** | 머신 러닝을 사용하여 오퍼 선택 최적화 | 라이선스에 따라 다릅니다. | 라이선스에 따라 다릅니다. | 라이선스에 따라 다릅니다. | 결정 | [AI 모델에 대해 알아보기](../offers/ranking/ai-models.md) |

>[!TAB 선택 / Prime / Ultimate]

이 탭은 Select, Prime 또는 Ultimate 패키징 용어를 사용하는 기존 라이선스 계약을 보유한 고객에게 적용됩니다.

## 패키지 요약 {#package-summaries}

+++**선택**

일괄 처리 및 트랜잭션 메시지 시작을 위한 조직에 가장 적합합니다.

- 예약된 일괄 캠페인 및 트랜잭션 메시지
- 핵심 캠페인 및 여정 실행
- 이메일, SMS, 푸시 및 사용자 정의 작업 채널 기초
- 표준 오케스트레이션 보호

+++

+++**Prime**

Select의 모든 기능과 실시간 오케스트레이션 및 인바운드 채널 포함:

- 이벤트가 트리거되는 실시간 여정 오케스트레이션
- 인바운드 채널: 웹, 인앱 메시지, 코드 기반 경험, 콘텐츠 카드 및 DM
- 고급 대상자 세분화 및 타겟팅

+++

+++**Ultimate**

Prime의 모든 기능과 더불어 의사 결정 및 고급 최적화를 포함합니다.

- 실시간 오퍼 의사 결정 및 개인화
- AI 기반 순위 및 최적화 모델
- 고급 보고 및 실험 기능

+++

## 기능 매트릭스 {#capability-matrix-legacy}

| 기능 | 수행 가능한 작업 | 선택 | Prime | Ultimate | 자세히 알아보기 |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **이메일** | 개인화된 이메일 메시지 디자인 및 보내기 | 포함됨 | 포함됨 | 포함됨 | [전자 메일을 보내는 방법 알아보기](../email/get-started-email.md) |
| **SMS / MMS** | 텍스트 및 멀티미디어 메시지 보내기 | 포함됨 | 포함됨 | 포함됨 | [모바일 메시지를 보내는 방법 알아보기](../mobile/get-started-mobile.md) |
| **푸시 알림** | 모바일 푸시 알림 보내기 | 포함됨 | 포함됨 | 포함됨 | [푸시 알림을 보내는 방법 알아보기](../push/get-started-push.md) |
| **일괄 캠페인** | 대상에게 메시지 예약 | 포함됨 | 포함됨 | 포함됨 | [캠페인을 만드는 방법 알아보기](../campaigns/get-started-with-campaigns.md) |
| **자동화된 여정** | 이벤트가 트리거되는 고객 여정 디자인 | 포함됨 | 포함됨 | 포함됨 | [여정 작성 방법 알아보기](../building-journeys/journey-gs.md) |
| **실시간 여정 트리거** | 고객 행동 발생 시 대응 | — | 포함됨 | 포함됨 | [여정 이벤트에 대해 알아보기](../event/about-events.md) |
| **인앱 메시지** | 모바일 앱 내 메시지 표시 | — | 포함됨 | 포함됨 | [인앱 메시지 사용 방법 알아보기](../in-app/get-started-in-app.md) |
| **웹 채널** | 실시간으로 웹 페이지 개인화 | — | 포함됨 | 포함됨 | [웹 채널 사용 방법 알아보기](../web/get-started-web.md) |
| **코드 기반 경험** | API 또는 SDK을 통해 모든 표면 개인화 | — | 포함됨 | 포함됨 | [코드 기반 경험을 사용하는 방법 알아보기](../code-based/get-started-code-based.md) |
| **콘텐츠 카드** | 지속적인 비간섭적 제품 내 메시지 전달 | — | 포함됨 | 포함됨 | [콘텐츠 카드 사용 방법 알아보기](../content-card/get-started-content-card.md) |
| **다이렉트 메일** | 실제 메일 부분 만들기 및 보내기 | — | Prime 이상에서 사용 가능 | 포함됨 | [DM 사용 방법 알아보기](../direct-mail/get-started-direct-mail.md) |
| **의사 결정** | 각 고객을 위한 최적의 오퍼를 실시간으로 선택 | — | — | 포함됨 | [의사 결정 사용 방법 알아보기](../experience-decisioning/gs-experience-decisioning.md) |
| **AI 기반 순위** | 머신 러닝을 사용하여 오퍼 및 콘텐츠 선택 최적화 | — | — | 포함됨 | [AI 모델에 대해 알아보기](../offers/ranking/ai-models.md) |
| **WhatsApp** | WhatsApp Business를 통해 메시지 보내기 | 라이선스 및 채널 구성에 따라 다름 | 라이선스 및 채널 구성에 따라 다름 | 라이선스 및 채널 구성에 따라 다름 | [WhatsApp 사용 방법 알아보기](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
