---
solution: Journey Optimizer
product: Journey Optimizer
title: 테스트 및 승인
description: 테스트 및 승인
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# 테스트 및 승인{#section-overview}

품질 보증은 탁월한 고객 경험을 제공하는 데 매우 중요합니다. Adobe Journey Optimizer은 포괄적인 테스트 및 승인 기능을 제공하여 콘텐츠를 검증하고, 여정 논리를 확인하고, 캠페인이 대상에 도달하기 전에 품질 표준을 충족하는지 확인하는 데 도움이 됩니다. 테스트 프로필로 개인화된 메시지를 미리 보는 것에서부터 복잡한 여정 흐름을 시뮬레이션하는 것에 이르기까지 이러한 도구를 사용하여 문제를 조기에 식별 및 해결하고, 위험을 줄이며, 브랜드 무결성을 유지할 수 있습니다. 장치 간에 이메일 렌더링을 테스트하거나, 여러 단계 여정의 유효성을 검사하거나, 공식 승인 워크플로를 설정하는 경우 이 섹션에서는 캠페인 및 여정에 대한 신뢰도를 구축하기 위한 모범 사례 및 단계별 프로세스를 안내합니다. 철저한 테스트와 체계적인 승인을 구현하면 오류를 최소화하고, 전달성을 향상시키며, 고객과 공감하는 원활한 경험을 만들 수 있습니다.

## 테스트 및 승인이 중요한 이유

테스트 및 승인 프로세스는 브랜드 평판을 보호하고 캠페인 성공을 보장하는 필수적인 품질 게이트 역할을 합니다. 이것이 중요한 이유입니다.

* **오류가 고객에게 도달하기 전에 오류를 catch** - 수정 사항이 빠르고 위험이 없는 제어된 환경에서 끊어진 링크, 잘못된 개인화, 렌더링 문제 및 논리 결함을 식별합니다.

* **전달성 향상** - 스팸 점수를 테스트하고, 전자 메일 인증을 확인하고, 전자 메일 클라이언트 간의 렌더링을 확인하여 받은 편지함 배치 및 참여 비율을 최대화합니다.

* **브랜드 일관성 보장** - 다양한 테스트 프로필로 콘텐츠를 미리 보고 다양한 고객 세그먼트에 대해 개인화가 올바르게 표시되고 브랜드 표준이 유지되는지 확인합니다.

* **복잡한 여정의 유효성을 검사합니다** - 여러 단계 여정 흐름을 시뮬레이션하여 트리거가 올바르게 실행되고, 조건이 올바르게 평가되며, 고객이 적절한 시간에 올바른 메시지를 수신하는지 확인하십시오.

* **책임 설정** - 이해 당사자의 승인을 필요로 하는 공식 승인 워크플로를 구현하여 명확한 소유권을 만들고 승인되지 않은 캠페인 시작 또는 미숙한 캠페인 시작을 줄입니다.

* **시간 및 리소스 절약** - 수정 사항이 더 저렴하고 빨라져 비용이 많이 드는 출시 후 수정 또는 고객 서비스 에스컬레이션을 방지하는 개발 주기 초기에 문제를 감지합니다.

## 모범 사례 테스트

테스트 노력의 효과를 극대화하려면 다음 권장 사례를 따르십시오.

1. **일찍 테스트하고 자주 테스트합니다** - 캠페인이 완전히 빌드될 때까지 기다리지 마십시오. 콘텐츠, 개인화 및 논리를 개발하면서 점진적으로 테스트하십시오.

1. **실제 테스트 프로필 사용** - [에지 사례 및 다양한 개인화 시나리오를 포함하여 대상 대상 세그먼트를 정확하게 나타내는 테스트 프로필 만들기](../using/audience/creating-test-profiles.md).

1. **장치 및 클라이언트 간 테스트** - 일관된 표시를 위해 자주 사용하는 전자 메일 클라이언트(Gmail, Outlook, Apple Mail) 및 장치(데스크톱, 모바일, 태블릿)에서 [전자 메일 렌더링](../using/content-management/rendering.md)을 확인합니다.

1. **개인화를 철저히 확인** - 다른 특성 값을 가진 여러 [테스트 프로필](../using/content-management/test-profiles.md)을 사용하여 테스트하여 개인화 토큰이 올바르게 렌더링되고 대체 값이 작동하는지 확인합니다.

1. **여정 경로 시뮬레이션** - 여러 분기가 있는 복잡한 여정의 경우 [테스트 모드](../using/building-journeys/testing-the-journey.md)를 사용하여 다양한 시작 조건 및 프로필 특성을 테스트하여 가능한 모든 경로의 유효성을 검사하십시오.

1. **게재 가능성 지표 확인** - 대량 전송 전에 [스팸 점수](../using/content-management/spam-report.md), 인증 상태 및 전자 메일 상태 지표를 검토합니다.

1. **테스트 결과 문서** - 테스트 결과, 발견된 문제 및 해결 방법을 기록하여 향후 테스트 프로세스를 개선하고 팀과 학습을 공유할 수 있습니다.

1. **이해 당사자를 일찍 참여시키세요** - [정식 승인](../using/test-approve/gs-approval.md) 전에 미리 보기 및 테스트 결과를 이해 당사자와 공유하여 피드백을 수집하고 기대치를 조정합니다.

## 권장 테스트 워크플로우

철저한 테스트와 원활한 승인을 보장하기 위해 다음과 같은 체계적인 접근 방식을 따르십시오.

### &#x200B;1. 콘텐츠 개발 및 미리보기

먼저 콘텐츠를 만들고 미리보기 기능을 사용하여 초기 디자인 및 개인화를 확인합니다.

* [이메일](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [푸시 알림](../using/push/create-push.md) 또는 기타 채널 콘텐츠 디자인
* **[콘텐츠 시뮬레이션](../using/content-management/preview-test.md)** 기능을 사용하여 테스트 프로필로 미리 보기
* [개인화 토큰](../using/personalization/personalization-syntax.md), 다이내믹 콘텐츠 및 대체 값 확인
* 다양한 화면 크기 및 전자 메일 클라이언트에서 [렌더링](../using/content-management/rendering.md) 확인

### &#x200B;2. 기술 검증

전달성 및 기능에 영향을 주는 기술적 측면의 유효성 검사:

* [스팸 점수 확인](../using/content-management/spam-report.md)을 실행하여 잠재적인 게재 가능성 문제를 식별하십시오.
* 링크가 손상되지 않고 제대로 추적되는지 테스트합니다.
* [전자 메일 인증](../using/configuration/dmarc-record.md)(SPF, DKIM, DMARC) 구성 유효성 검사
* HTML 렌더링 검토 및 CSS 호환성 문제 확인
* 모바일 및 데스크톱 장치에서 [응답형 디자인](../using/email/content-from-scratch.md) 테스트

### &#x200B;3. 여정 테스트

여정의 경우 오케스트레이션 논리의 유효성을 검사합니다.

* **[테스트 모드](../using/building-journeys/testing-the-journey.md)**&#x200B;를 활성화하여 여정 전체에 걸쳐 프로필 진행률을 시뮬레이션하세요.
* 다른 [시작 조건](../using/building-journeys/entry-management.md) 및 대상 자격 테스트
* [대기 활동](../using/building-journeys/wait-activity.md), [조건](../using/building-journeys/condition-activity.md) 및 분기 논리가 올바르게 작동하는지 확인
* 메시지를 보내지 않고 실행 경로를 분석하려면 복잡한 여정에 **[시험 실행](../using/building-journeys/journey-dry-run.md)**&#x200B;을 사용하세요.
* [events](../using/event/about-events.md)이(가) 올바르게 트리거되고 [사용자 지정 작업](../using/action/about-custom-action-configuration.md)이(가) 예상대로 실행되는지 확인

### &#x200B;4. 승인 제출

테스트가 완료되고 문제가 해결되면:

* 조직의 [승인 여정](../using/test-approve/approval-policies.md)에 따라 승인을 위해 캠페인이나 정책을 제출하세요.
* [승인 요청](../using/test-approve/request-approval.md)과 함께 테스트 결과 및 문서 포함
* [승인자](../using/test-approve/review-approve-request.md)의 피드백 또는 변경 요청 처리
* 필요한 수정 작업을 수행하고 변경 사항이 중요한 경우 다시 테스트합니다.

### &#x200B;5. 출시 전 확인

캠페인 또는 여정 활성화 전:

* 모든 설정, 대상 및 [일정](../using/building-journeys/journey-properties.md)에 대한 최종 검토를 수행합니다.
* 모든 승인이 적소에 있고 문서화되어 있는지 확인합니다.
* 전송 시간과 [표준 시간대](../using/building-journeys/timezone-management.md)가 올바른지 확인
* 실행 후 성능을 추적하려면 [모니터링 및 알림](../using/reports/alerts.md)을 사용하도록 설정하십시오.

### &#x200B;6. 모니터링 및 반복

시작 후 모니터링을 계속 진행하여 문제를 조기에 포착합니다.

* 여정 오류, 높은 바운스 비율 또는 낮은 참여에 대해 [시스템 경고](../using/reports/alerts.md)를 설정합니다.
* [실시간 보고서](../using/building-journeys/report-journey.md)를 검토하여 예상과 다르게 성과를 추적하세요.
* 중요한 문제가 발생하면 여정을 [일시 중지 또는 수정](../using/building-journeys/journey-pause.md)할 준비를 하십시오
* 향후 테스트 프로세스를 개선하기 위해 학습한 문서화 교육

## 작동 중인 테스트: 사용 사례

테스트 개념이 실제 시나리오에 어떻게 적용되는지 알아보십시오.

* **[다중 채널 메시지 보내기](../using/building-journeys/journeys-uc.md)** - 이 사용 사례에서는 대상자 읽기, 반응 이벤트 및 전자 메일/푸시 메시지를 결합하는 여정을 테스트하는 방법을 보여 줍니다. 대상 타기팅에서 메시지 게재에 이르기까지 전체 흐름의 유효성을 검사하는 방법을 알아보고 테스트 및 게시 단계가 작동하는지 확인합니다.

* **[구독자에게 메시지 보내기](../using/building-journeys/message-to-subscribers-uc.md)** - 동적 전자 메일 주소 지정으로 구독 목록을 대상으로 하는 여정을 테스트하는 방법을 알아봅니다. 이 예에서는 개인화 표현식의 유효성을 검사하고 메시지가 올바른 구독자에게 도달하는지 확인하는 방법을 보여 줍니다.

* **[시간 제한 메시지 보내기](../using/building-journeys/weekday-email-uc.md)** - 특정 날짜에 메시지가 전송될 수 있도록 시간 기반 조건으로 여정을 테스트하는 방법을 이해합니다. 대기 활동 및 예약 논리의 유효성을 검사하는 방법을 참조하십시오.

* **[더 많은 여정 사용 사례 탐색](../using/building-journeys/jo-use-cases.md)** - 경험 이벤트, 다중 채널 메시징 및 외부 시스템 통합에 대한 포괄적인 실제 예제 컬렉션에 액세스합니다.

## 콘텐츠 테스트 및 승인

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=ko)

콘텐츠 미리 보기, 테스트 및 유효성 검사

테스트 프로필, 이메일 렌더링 테스트, 스팸 점수 평가 등을 사용하여 개인화된 콘텐츠를 미리 보고, 테스트하며, 확인하는 방법을 알아봅니다.

[콘텐츠 미리 보기 및 테스트 살펴보기](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=ko)

여정과 캠페인을 위한 승인 워크플로우

여정과 캠페인의 품질 관리를 보장하기 위해 승인 프로세스를 설정, 관리 및 실행하는 방법을 이해합니다.

[승인 워크플로우에 대해 알아보기](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=ko)

여정 테스트

여정을 게시하기 전에 이벤트, 조건, 액션이 예상대로 작동하는지 확인하기 위해 특정 프로필로 테스트하여 여정을 검증합니다.

[여정 테스트](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=ko)

여정 시험 실행

시험 실행을 통해 여정의 실행 경로를 시뮬레이션하고 확인하여 실제로 실행하기 전에 잠재적 문제를 식별합니다.

[시험 실행에 대해 알아보기](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=ko)

모니터링 및 문제 해결

포괄적인 문제 해결 리소스, 시스템 경고, 오류 코드에 액세스하여 여정 실행 및 성능 문제를 해결할 수 있습니다.

[모니터링 및 문제 해결 보기](troubleshoot-journey-landing-page.md)
:::

::::

## 추가 리소스

### 필수 테스트 및 유효성 검사 가이드

* [여정의 실시간 보고서](../using/building-journeys/report-journey.md) - 실시간으로 여정 지표를 모니터링하여 성능을 추적하고 실행 중 문제를 식별합니다. 프로필 진행, 이벤트 트리거 및 작업 완료율의 세부 분류에 액세스합니다.

* [테스트 프로필 만들기](../using/audience/creating-test-profiles.md) - 테스트 프로필을 만들고 관리하여 실제 고객 시나리오를 시뮬레이션하고 개인화를 확인합니다. 테스트를 위해 프로필에 플래그를 지정하고, 속성 값을 설정하고 테스트 프로필 세그먼트를 구성하는 방법을 알아봅니다.

* [전자 메일 스팸 보고서](../using/content-management/spam-report.md) - 보내기 전에 전자 메일 스팸 점수를 확인하여 배달 가능성 및 받은 편지함 배치를 개선합니다. 스팸 필터가 콘텐츠를 평가하는 방법을 이해하고 개선을 위한 권장 사항을 얻을 수 있습니다.

* [여정 FAQ](../using/building-journeys/journey-faq.md) - 여정 만들기, 테스트, 실행 및 문제 해결에 대한 일반적인 질문에 대한 답변을 찾을 수 있습니다. 빈번한 문제 해결 및 여정 동작 이해를 위한 빠른 참조.

### 관련 항목

* [콘텐츠 관리](content-management-landing-page.md) - 템플릿, 조각 및 전자 메일 Designer을 사용하여 콘텐츠를 디자인하고 미리 보고 관리하는 방법에 대해 알아봅니다. 일관된 브랜딩을 위한 기본 콘텐츠 생성 모범 사례

* [보고 및 분석](reporting-landing-page.md) - 포괄적인 보고서, 대시보드 및 지표를 사용하여 캠페인 및 여정 성과를 분석합니다. 데이터 중심의 의사 결정을 내려 고객 경험을 최적화합니다.

* [여정 구성](configure-journeys-landing-page.md) - 정교한 여정 오케스트레이션을 사용하도록 데이터 원본, 이벤트 및 사용자 지정 작업을 구성합니다. 여정 생성을 위한 기술적 토대를 설정합니다.

* [캠페인 관리](../using/campaigns/get-started-with-campaigns.md) - 다양한 캠페인 유형을 탐색하고 최대의 효과를 위해 일괄 처리 및 실시간 캠페인을 만들고, 예약하고, 최적화하는 방법을 알아봅니다.
