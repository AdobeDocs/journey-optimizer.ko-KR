---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 사용 사례 개요 | ADOBE JOURNEY OPTIMIZER
description: 각 시나리오에 가장 적합한 AJO 기능에 대한 지침을 통해 Adobe Journey Optimizer이 설계된 핵심 사용 사례를 살펴보십시오.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: 여정 최적화 도구, 사용 사례, 의사 결정 안내서, 기능, 시작, 실무자 목표, 자습서
source-git-commit: 054de625361914e217c27782b487db1933c3230f
workflow-type: tm+mt
source-wordcount: '2821'
ht-degree: 36%

---

# 목표에 적합한 Journey Optimizer 기능 찾기 {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**이 페이지에서:** 수행할 작업을 시작한 다음 기능 이름을 먼저 알 필요 없이 이를 해결하는 Adobe Journey Optimizer 기능으로 이동하십시오.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]은(는) 다양한 기능을 제공하며 올바른 기능은 달성하려는 작업에 따라 다릅니다. 이 안내서는 제품 기능보다는 비즈니스 목표를 중심으로 구성되어 있습니다. 필요에 맞는 목표를 찾은 다음 링크를 따라 권장 기능으로 시작하십시오.

이 페이지를 빠른 라우터로 사용 — 목표를 검색하고 올바른 기능으로 바로 이동합니다. 지금 시작하는 경우 [Journey Optimizer으로 시작](../../rp_landing_pages/get-started-landing-page.md)하여 역할에 맞는 시작 지점을 찾으십시오.

>[!NOTE]
>
>단계별 구현 샘플은 [여정 사용 사례 라이브러리](../building-journeys/jo-use-cases.md)를 참조하세요.

특정 시나리오에 종단간 튜토리얼을 사용할 수 없는 경우 이 링크를 클릭하면 현재 가장 적합한 시작점으로 이동하여 기능을 배우고 시작할 수 있습니다.

AI는 이러한 많은 기능에 내장되어 있습니다. 아래 표에서 **(AI)** 태그를 찾으십시오. 대화형 [AI Assistant](ai-features.md#ai-assistant)는 언제든지 제품 질문에 답변하고 여정에 대한 운영 통찰력을 제공할 수 있습니다. 전체 지능형 기능 집합을 보려면 [AI 및 지능형 기능](ai-features.md)을 참조하세요.

>[!TIP]
>
>Journey Optimizer을 처음 사용하십니까? [Journey Optimizer으로 시작](../../rp_landing_pages/get-started-landing-page.md)하여 역할에 적합한 경로를 선택한 다음 필수 요소에 대한 [Journey Optimizer 소개](get-started.md)를 읽어 보세요. 실습형 자신감을 높이려면 [Journey Optimizer 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}을 탐색하고 전문가가 큐레이션한 [비디오 재생 목록](https://experienceleague.adobe.com/ko/playlists?solution=Journey+Optimizer){target="_blank"}을 따라 [교육 샌드박스](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"}에서 또는 [실습형 과제](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}를 통해 연습하세요.

## 팀을 위한 Journey Optimizer 설정 {#setup-admin}

여정 또는 캠페인을 빌드하기 전에 환경을 구성해야 하는 관리자 및 기술 사용자의 경우

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 보내기 전에 이메일, SMS 또는 푸시 채널 구성 | 채널 구성 | [채널 구성 시작](../configuration/get-started-configuration.md) |
| 이메일 전송을 위한 새 IP 주소 준비 | IP 준비 계획 | [IP 준비 시작](../configuration/ip-warmup-gs.md) |
| 역할, 권한 및 액세스 제어 설정 | 액세스 제어 | [액세스 제어 시작](../administration/permissions-overview.md) |
| 여러 환경 또는 지역에서 작업 | 샌드박스 | [샌드박스 작업](../administration/sandboxes.md) |

## 실시간으로 고객 참여 {#engage-real-time}

발생한 고객 작업 또는 이벤트에 반응하는 시나리오의 경우.

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 새 고객 또는 구독자를 자동으로 시작합니다. | 이벤트 트리거된 여정 | [여정 시작](../building-journeys/journey-gs.md) · [여정 작성 소개](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |
| 포기한 장바구니 복구 또는 세션 찾아보기 | 이벤트 트리거된 여정 | [여정 시작](../building-journeys/journey-gs.md) · [찾아보기 자습서 중단](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |
| 웹 사이트 양식 제출에서 여정 트리거 | 이벤트 트리거된 여정 | [여정 시작](../building-journeys/journey-gs.md) · [자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| 인앱 비헤이비어 반응(앱 열기, 화면 보기) | 여정 + 인앱 | [인앱 시작](../in-app/get-started-in-app.md) |
| 주문, 배송 또는 약속 확인 보내기 | API 트리거된 캠페인 | [API 트리거 캠페인 작업](../campaigns/api-triggered-campaigns.md) |
| 비활성화 또는 종료된 고객 재참여 | 여정 + 대상 | [프로필 및 대상자 시작](../audience/get-started-profiles.md) · [규칙 빌더를 사용하여 대상자 만들기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |
| 활성화하기 전에 실제 데이터로 여정 테스트 | 여정 시험 실행 | [시험 실행으로 여정 테스트](../building-journeys/journey-dry-run.md) |
| 진행 중인 프로필을 중지하지 않고 편집하려면 라이브 여정 일시 중지 | 여정 일시 중지 및 다시 시작 | [여정 일시 중지 및 다시 시작](../building-journeys/journey-pause.md) |
| 자연어 프롬프트에서 여정 빌드 또는 최적화 | Journey Agent **(AI)** | [AI 에이전트](ai-features.md#ai-agents) · [Journey Agent 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## 규모에 맞게 대상에게 도달 {#reach-at-scale}

정의된 대상에 대한 일대다 전달을 예약하는 경우.

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 뉴스레터 또는 프로모션을 세그먼트에 전송 | 예약된 캠페인 | [캠페인 시작](../campaigns/get-started-with-campaigns.md) |
| A/B 테스트로 제품 실행 | 콘텐츠 실험 **(AI)** | [콘텐츠 실험 시작](../content-management/experiment-accelerator-gs.md) · [이메일 캠페인에 대한 콘텐츠 실험 만들기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| 고객에게 중단 또는 서비스 업데이트 알림 | 예약된 캠페인 + 대상자 | [대상자 정보](../audience/about-audiences.md) |
| 분기 논리를 사용하여 여러 단계 캠페인 디자인 | 오케스트레이션된 캠페인 | [오케스트레이션된 캠페인 시작](../orchestrated/gs-orchestrated-campaigns.md) |
| 마지막 캠페인 실행 이후 변경된 프로필만 타겟팅 | 오케스트레이션된 캠페인 — 증분 쿼리 | [오케스트레이션된 캠페인에서 쿼리 빌드](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| 시작하기 전에 내 대상자와 일치하는 프로필 수 확인 | 대상 미리 보기 | [대상자 정보](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| 규모에 맞게 여러 채널에서 메시징 조정 | 오케스트레이션 | [오케스트레이션을 옴니채널 참여로 확장](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| 각 고객에게 최적의 시간에 각 메시지 보내기 | 전송 시간 최적화 **(AI)** | [전송 시간 최적화](../building-journeys/send-time-optimization.md) |

## 각 고객에게 표시되는 항목 개인화 {#personalize}

각 개인에 대한 오퍼 및 콘텐츠를 맞춤화할 수 있습니다.

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 각 고객에 대한 최상의 오퍼 표시 | 결정 | [Offer Decisioning 시작하기](../offers/get-started/starting-offer-decisioning.md) · [웹 오퍼 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |
| 공식을 사용하여 오퍼 순위 지정(우편 번호, 수입, 날씨) | Decisioning — 등급 공식 | [순위 공식 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [날씨 데이터 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| 외부 제품 또는 CRM 데이터를 사용하여 오퍼 개인화 | Decisioning — AEP 데이터 세트 조회 | [의사 결정 시 데이터 세트 조회 사용](../experience-decisioning/context-data.md) |
| 프로필 데이터를 사용하여 메시지 콘텐츠 맞춤화 | 개인화 | [콘텐츠 개인화](../personalization/personalize.md) |
| 사본, 이미지 및 메시지 변형 생성 | AI 콘텐츠 생성 **(AI)** | [AI 콘텐츠 생성](../content-management/gs-generative.md) · [자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| 디자인 이미지를 편집 가능한 이메일 템플릿으로 변환 | HTML으로 이미지 변환기 **(AI)** | [이미지를 전자 메일 서식 파일로 변환](../content-management/image-to-html.md) |
| 자동으로 오퍼 순위 지정 및 개인화 | AI 순위 모델 **(AI)** | 의사 결정을 위한 [AI 모델](../experience-decisioning/ranking/ai-models.md) |
| 항시적 컨텍스트 콘텐츠 제공(캠페인 없음) | 콘텐츠 카드 | [콘텐츠 카드 시작](../content-card/get-started-content-card.md) · [콘텐츠 카드 만들기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| API를 통해 모든 앱 또는 표면에 개인화된 콘텐츠 제공 | 코드 기반 경험 | [코드 기반 경험 시작](../code-based/get-started-code-based.md) |
| 내 팀이 편집할 수 있는 이메일 템플릿 부분 제어 | 컨텐츠 잠금 | [전자 메일 서식 파일에서 콘텐트 잠금](../content-management/content-locking.md) |

## 게재 조정 및 관리 {#coordinate-govern}

여러 채널에서 고객과 연락하는 방법, 시기 및 빈도를 제어합니다.

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 채널 간 메시지 피로도 방지 | 빈도 상한 설정 | [채널별 빈도 제한 설정](../conflict-prioritization/channel-capping.md) |
| 충돌하거나 경쟁하는 메시지 해결 | 충돌 우선 순위 | [잠재적인 충돌 확인](../conflict-prioritization/conflicts.md) · [자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| 우선 순위를 사용할 여정 결정 | 여정 중재 | [수식을 사용하여 여정의 등급을 매기십시오](../conflict-prioritization/journey-ranking-formulas.md) |
| 조용한 시간 및 동의 준수 | 업무 시간/개인 정보 보호 | [자동 설정 시간](../conflict-prioritization/quiet-hours.md) |
| 채널 전반에 동의 정책 및 데이터 사용 레이블 적용 | 동의 및 데이터 거버넌스 | [개인 정보 보호 시작](../privacy/get-started-privacy.md) |
| 여정에 높은 오류 또는 폐기 비율이 있는 경우 경고 받기 | 여정 경고 | [여정 알림 설정](../reports/alerts.md) |

## 게재할 채널 선택 {#choose-channel}

| 전송... | 채널 | 여기서 시작 |
| --- | --- | --- |
| 이메일 뉴스레터, 프로모션 또는 트랜잭션 메시지 | 이메일 | [전자 메일 시작](../email/get-started-email.md) |
| 모바일 푸시 알림(iOS 및 Android) | 푸시 | [푸시 알림 시작](../push/get-started-push.md) |
| SMS, MMS 또는 RCS 텍스트 메시지 | SMS/MMS/RCS | [SMS/MMS/RCS 시작하기](../mobile/get-started-mobile.md) · [모바일 학습 허브](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| Meta Cloud API를 통한 WhatsApp 메시지 | WhatsApp | [WhatsApp 시작](../whatsapp/get-started-whatsapp.md) |
| 인브라우저 또는 인앱 오버레이 및 배너 | 인앱 | [인앱 시작](../in-app/get-started-in-app.md) |
| 개인화된 웹 페이지 콘텐츠 | 웹 | [웹 채널 시작](../web/get-started-web.md) |
| API를 통한 모든 표면(키오스크, 연결된 장치, 헤드리스 앱) | 코드 기반 경험 | [코드 기반 경험 시작](../code-based/get-started-code-based.md) |
| 여정에서 트리거된 실제 메일 부분 | DM | [DM 시작](../direct-mail/get-started-direct-mail.md) |

## 측정 및 최적화 {#measure-optimize}

성능 추적, 문제 진단 및 시간 경과에 따른 결과 향상

| 난... | 권장 기능 | 여기서 시작 |
| --- | --- | --- |
| 라이브 여정 또는 캠페인에 대한 성능 지표 보기 | 라이브 보고서 | [실시간 보고서](../reports/live-report.md) · [실시간 보고서로 여정 모니터링 및 분석](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| 종료 후 전체 캠페인 또는 여정 성과에 대해 보고합니다. | 전반적 보고서 | [보고 시작하기](../reports/gs-reports.md) |
| 실험 분석 및 다음 단계 추천 받기 | Experimentation Agent **(AI)** | [Experimentation Agent](ai-features.md#experimentation-agent) · [자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| 내 여정에서 사용자 지정 작업의 상태 및 대기 시간 모니터링 | 사용자 정의 액션 모니터링 | [사용자 지정 작업 사용](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| 여정 오류 또는 폐기 비율이 임계값을 초과하는 경우 경고 받기 | 여정 경고 | [여정 알림 설정](../reports/alerts.md) |

## 스타터 플로우 {#starter-flows}

아래의 각 시작 흐름은 여러분이 무엇을 구축할 것인지, 누구에게 적합한지, 거기에 어떻게 도달해야 하는지에 대한 짧고 결과 지향적인 단계 세트입니다. 첫 번째 프로젝트와 일치하는 목표를 선택하고 세부 설명서에 대한 링크를 따르십시오.

### 새 고객 시작 {#flow-welcome}

**다음 환영 시리즈를 만듭니다.** 모든 신규 가입자를 환영하고 비활성 가입자를 찾아내는 자동화된 환영 시리즈입니다.
**우수 사례:** 마케터 · **기능:** 이벤트 트리거 여정

1. [통합 프로필 및 대상자](../audience/get-started-profiles.md)가 등록 이벤트를 받고 있는지 확인합니다.
1. [첫 번째 여정을 만들고](../building-journeys/journey-gs.md) 등록 이벤트를 항목으로 사용합니다.
1. 환영 [이메일](../email/get-started-email.md)을 추가한 다음 대기 단계 및 참여하지 않은 프로필에 대한 후속 [푸시 알림](../push/get-started-push.md)을 추가합니다.
1. [이름 및 등록된 관심 분야와 같은 프로필 속성을 사용하여 콘텐츠를 개인 설정](../personalization/personalize.md)합니다.

➡️ [여정 시작](../building-journeys/journey-gs.md)

### 포기한 장바구니 복구 {#flow-cart}

**다음 항목을 만듭니다.** 고객에게 남아 있는 항목을 상기시키는 실시간 복구 흐름입니다.
**우수 사례:** 마케터 · **기능:** 이벤트 트리거 여정

1. 장바구니 중단 이벤트가 Journey Optimizer에 도달하는지 확인하십시오(필요한 경우 [데이터 팀](../data/gs-data.md)과(와) 협력).
1. 중단 이벤트로 트리거된 [여정 빌드](../building-journeys/journey-gs.md).
1. 개인화된 알림 메시지를 보냅니다. 24시간 내에 클릭이 없으면 [푸시](../push/get-started-push.md) 후속 작업으로 분기하세요.
1. 포기한 항목 및 충성도 상태로 [개인 설정](../personalization/personalize.md).

➡️ [여정 시작](../building-journeys/journey-gs.md)

### 트랜잭션 메시지 보내기 {#flow-transactional}

**외부 시스템에 의해 트리거된 주문형 주문, 배송 또는 약속 확인을 빌드합니다.**
**마케터 및 개발자를 위한 최적의 솔루션:** · **기능:** 외부 시스템에 의해 트리거된 캠페인

1. [외부 시스템에서 트리거된 캠페인](../campaigns/api-triggered-campaigns.md)의 작동 방식과 예상되는 페이로드를 검토합니다.
1. 메시지 템플릿을 디자인하고 트랜잭션 세부 정보를 사용하여 [개인화](../personalization/personalize.md)합니다.
1. 개발자가 주문 또는 이행 시스템에서 Campaign 엔드포인트를 호출하도록 합니다.

➡️ [외부 시스템에서 트리거된 캠페인 작업](../campaigns/api-triggered-campaigns.md)

### 콘텐츠 테스트를 사용하여 캠페인 시작 {#flow-campaign}

**다음 빌드를 수행합니다.** 가장 성과가 좋은 콘텐츠를 자동으로 선택하는 예약된 프로모션입니다.
**우수 사례:** 마케터 · **기능:** 예약된 캠페인 + 콘텐츠 실험

1. [캠페인을 시작하고](../campaigns/get-started-with-campaigns.md) 대상자를 정의합니다.
1. [콘텐츠 생성](../content-management/gs-generative.md)을 사용하여 제목란을 작성하고 변형을 복사합니다.
1. [콘텐츠 실험](../content-management/experiment-accelerator-gs.md)을 설정하여 샘플에서 변형을 테스트한 다음 우승자를 나머지 사람에게 보냅니다.

➡️ [캠페인 시작](../campaigns/get-started-with-campaigns.md)

### 고객별 오퍼 개인화 {#flow-offers}

**다음 결정을 만듭니다.** 각 고객에게 최상의 단일 오퍼를 표시하는 결정을 만듭니다.
**우수 사례:** 마케터 · **기능:** 의사 결정

1. [Offer Decisioning을 시작하고](../offers/get-started/starting-offer-decisioning.md) 오퍼 및 자격 규칙을 만듭니다.
1. [여정](../building-journeys/journey-gs.md) 또는 캠페인 메시지에 결정을 추가합니다.
1. 오퍼의 등급을 자동으로 지정하고 최적화하기 위해 [지능형 기능](ai-features.md)에 레이어를 적용하세요.

➡️ [Offer Decisioning 시작](../offers/get-started/starting-offer-decisioning.md)

## 예제 시나리오 {#example-scenarios}

다양한 역할, 업계, 채널에서 Journey Optimizer의 여러 기능이 함께 작동하는 방식을 보여 주는 예시입니다.

### 배송 지연 후 회복 조치 {#scenario-delayed-shipment}

**역할:** 마케터 | **핵심 기능:** [통합 프로필 + 대상 제외](../audience/get-started-profiles.md)

어느 의류 매장에서는 일반적으로 지난주에 제품을 구매한 모든 고객에게 구매 후 설문 조사를 보냅니다. 악천후 때문에 몇 개의 배송이 지연되었습니다. 배송을 받지 않은 고객을 확인하면 의류 매장에서는 예정된 고객 만족도 조사 전송 대상에서 해당 고객을 제외하고 지연에 대해 사과한 후 할인 코드를 제공하며 고객의 과거 구매 내역을 기반으로 제품을 추천할 수 있습니다.

[캠페인 시작](../campaigns/get-started-with-campaigns.md)

### 실시간 매장 내 참여 {#scenario-instore}

**역할:** 마케터 | **핵심 기능:** [Geofence 트리거 + 푸시](../push/get-started-push.md)

동일한 가게에서 고객이 매장 주차장에 들어올 때 실시간으로 재입고된 해당 고객 사이즈 스웨터에 대한 푸시 알림을 보내어 단골 고객의 관심을 사로잡을 수 있습니다.

[푸시 알림 시작](../push/get-started-push.md)

### 장바구니 포기 후 회복 조치 {#scenario-cart}

**역할:** 마케터 | **핵심 기능:** [이벤트로 트리거되는 단계 여정](../building-journeys/journey-gs.md)

고객이 온라인 장바구니에 항목을 추가했지만 구매를 완료하지 않고 떠나면 Journey Optimizer가 실시간으로 이벤트를 감지하고 자동으로 회복 여정을 시작합니다. 고객은 구매하지 않고 남긴 제품을 알려 주는 개인화된 이메일을 받게 됩니다. 24시간 이내에 클릭스루하지 않으면 브라우징 기록 및 충성도 상태에 따라 개인화된 후속 푸시 알림이 전송됩니다.

[첫 번째 여정 작성](../building-journeys/journey-gs.md)

### 스트리밍 서비스 환영 시리즈 {#scenario-welcome}

**역할:** 마케터 | **핵심 기능:** [이벤트로 트리거되는 환영 여정](../building-journeys/journey-gs.md)

고객이 스트리밍 서비스에 가입하면 Journey Optimizer가 가입 이벤트를 감지하여 즉시 여러 단계 환영 여정을 시작합니다. 고객은 앱을 처음으로 열어 보라고 추천하는 환영 이메일을 수신합니다. 48시간 이내에 로그인 활동이 감지되지 않으면 등록할 때 명시한 관심사를 기반으로 개인화된 콘텐츠 추천이 포함된 후속 푸시 알림이 전송되어 첫날부터 수동적인 구독자를 능동적으로 참여하는 사용자로 전환할 수 있습니다.

[첫 번째 여정 작성](../building-journeys/journey-gs.md)

### 지침이 포함된 예약 미리 알림 {#scenario-reservation}

**역할:** 마케터 | **핵심 기능:** [예약된 + 위치 인식형 메시지](../campaigns/get-started-with-campaigns.md)

어느 호스피탈리티 브랜드에서는 예약 한 시간 전에 각 고객에게 적시 미리 알림을 보냅니다. 알림에는 게스트의 이름, 예약 시간, 장소에 대한 위치 기반 안내가 포함되어 있으며, 이 내용은 마케팅 팀의 수작업 없이 고객 프로필 및 예약 데이터 자동으로 조합됩니다.

[캠페인 시작](../campaigns/get-started-with-campaigns.md)

### 서비스 중단 사전 알림 {#scenario-outage}

**역할:** 운영 | **핵심 기능:** [자동화된 대규모 대상자 선택](../audience/about-audiences.md)

서비스가 중단되면 Journey Optimizer는 계정 데이터 및 사용 패턴을 기반으로 영향을 받는 고객을 자동으로 식별합니다. 해당 고객은 문제에 대해 알리고 다음 단계를 요약하는 사전 알림을 받게 됩니다. 이를 통해 부정적일 수 있는 경험을 투명성과 신뢰의 순간으로 전환하여 대규모로 할 수 있습니다.

[첫 번째 여정 작성](../building-journeys/journey-gs.md)

### 지능형 홍보 캠페인 {#scenario-ai-campaign}

**역할:** 마케터 | **핵심 기능:** [콘텐츠 생성 + 실험](ai-features.md)

제품 출시를 계획하는 소매 브랜드에서 Journey Optimizer의 AI 어시스턴트를 사용하여 자연어 프롬프트 및 업로드된 브랜드 지침에 기반한 여러 제목 및 본문 카피 베리에이션을 몇 분만에 생성합니다. 기본 제공 콘텐츠 실험은 초기 대상자 샘플 중에서 가장 성과가 좋은 변형을 자동으로 식별합니다. 그런 다음 우수성이 검증된 메시지가 나머지 수신자에게 배포되어 추가적인 카피라이팅 노력 없이 참여도를 극대화할 수 있습니다.

[지능형 기능 살펴보기](ai-features.md) | [콘텐츠 실험에 대해 알아보기](../content-management/experiment-accelerator-gs.md)

### 모바일 앱을 통한 유지 관리 경고 {#scenario-maintenance}

**역할:** 운영 | **핵심 기능:** [비마케팅 여정 오케스트레이션](../building-journeys/journey-gs.md)

운영 팀 및 고객 지원 센터 등 마케터가 아닌 사용자는 [!DNL Adobe Journey Optimizer]을(를) 사용하여 운영 알림을 관리하거나 온보딩 프로세스를 모니터링할 수 있습니다. 예를 들어 방문자가 경험의 일부로 모바일 앱을 다운로드하는 놀이공원의 경우, 유지 관리 직원은 Journey Optimizer를 사용하여 공원 방문자에게 유지 관리 작업으로 인해 현재 운행하지 않는 놀이기구에 대해 알릴 수 있습니다.

[첫 번째 여정 작성](../building-journeys/journey-gs.md)

## 비디오 라이브러리 {#videos}

주제별로 선별된 비디오 콘텐츠를 찾아봅니다. 각 탭은 Experience League의 관련 튜토리얼 및 플레이리스트로 연결됩니다.

>[!BEGINTABS]

>[!TAB 시작]

* [Journey Optimizer 소개](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} - 핵심 개념 및 제품 둘러보기.
* [Journey Optimizer 자습서 개요](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - 안내식 비디오의 전체 카탈로그입니다.

>[!TAB 여정 및 캠페인]

* [여정 작성 소개](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — 첫 번째 이벤트가 트리거된 여정을 작성합니다.
* [Journey Agent을 사용하여 여정 작성](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} - 자연어 프롬프트에서 여정을 만듭니다.

>[!TAB Personalization 및 인텔리전스]

* [콘텐츠 생성을 위한 AI 도우미](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} - 복사본, 이미지 및 변형을 생성합니다.
* [의사 결정을 사용하여 웹 오퍼를 개인화합니다](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — 고객별로 오퍼를 사용자 지정합니다.

>[!TAB 보고 및 최적화]

* [실시간 보고서로 여정 모니터링 및 분석](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} - 실시간으로 성능을 추적합니다.
* [이메일 캠페인에 대한 콘텐츠 실험 만들기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} - 콘텐츠를 테스트하고 최적화합니다.

>[!ENDTABS]

## 여정, 캠페인 및 오케스트레이션된 캠페인 중 선택 {#choosing}

| 시나리오 | 사용 |
|----------|-----|
| 행동 중심의 여러 단계로, 각 고객은 각자의 속도에 맞게 움직입니다. | 여정 |
| 대상자에 대한 간단한 예약 또는 API 트리거 메시지 | 캠페인 |
| 다중 엔티티 세그먼테이션을 사용하는 복잡한 일괄 처리 워크플로 | 오케스트레이션된 캠페인 |

## 확실하지 않습니까? {#not-sure}

목표가 익숙하지 않은 용어에 매핑되거나 표가 가리키는 기능이 무엇인지 확실하지 않은 경우 [Journey Optimizer 주요 용어](terminology.md) 페이지로 시작하여 각 기능의 개념을 명확히 설명하십시오.

또한 [Journey Optimizer 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}에서 종합적인 연습을 통해 실습 자신감을 높일 수 있습니다.
