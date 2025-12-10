---
solution: Journey Optimizer
product: journey optimizer
title: 설명서 업데이트
description: 설명서 업데이트에 대해 알아보기
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: c30a74ccdaec81cbbb28e3129d5c351a0fe64bfc
workflow-type: tm+mt
source-wordcount: '3762'
ht-degree: 94%

---

# 설명서 업데이트 {#latest-updates}

이 페이지에는 월별 릴리스 기능 및 개선 사항과 관련된 업데이트 외에도 [!DNL Journey Optimizer] 설명서의 모든 최신 변경 사항이 나와 있습니다.

## 2025년 12월 {#december-2025}

* 대상자 읽기 여정의 대기 활동에 파킹된 프로필이 UPS(통합 프로필 서비스)에서 속성을 자동으로 새로 고치는 방법을 설명하는 새 섹션을 대기 활동 설명서에 추가했습니다. 이렇게 하면 여정 실행 중에 여정 데이터가 대기 노드 이후에 변경될 수 있음을 명확하게 하며, 대기 노드 전체에서 일관된 스냅샷 데이터가 기대되는 경우 예상치 못한 결과가 발생할 수 있습니다. [자세히 보기](../building-journeys/wait-activity.md#profile-refresh)

* 경로 실험이 게시되면 실험 결과의 계산 및 보고에 지장을 주므로 사용자가 경로 실험의 메타데이터를 편집하지 말 것을 경고하는 주의 사항이 경로 실험 섹션에 추가되었습니다. [자세히 보기](../building-journeys/optimize.md#experimentation)

* 양식 사전 설정 만들기 섹션에 스트리밍 연결이 선택 드롭다운 목록에 표시되기 위한 요구 사항을 지정하는 메모가 추가되었습니다. [자세히 보기](../landing-pages/lp-forms.md#create-form-preset)

* 이제 Experience Decisioning 섹션에서 노출 횟수, 클릭 수 및 사용자 지정 이벤트 추적을 위한 데이터 수집을 구성하는 방법에 대한 새 페이지를 사용할 수 있습니다. [자세히 보기](../experience-decisioning/data-collection/schema-requirement.md)

* 명확성과 유용성을 개선하기 위해 AI 지원 설명서를 통한 콘텐츠 생성이 재구성되었습니다. 이전 5개의 채널별 페이지(이메일, 푸시, SMS, 웹 및 랜딩 페이지)는 [전체 콘텐츠 생성](../content-management/generative-full-content.md), [텍스트 생성](../content-management/generative-text.md) 및 [이미지 생성](../content-management/generative-image.md)의 세 가지 생성 유형 페이지로 통합되었습니다.

## 2025년 11월 {#november-2025}

* 이제 최대 가용량 규칙, AI 모델 구성, 트래픽 요구 사항 및 오퍼 최적화 전략과 같은 주제를 다루는 새로운 의사 결정 FAQ 페이지를 사용할 수 있습니다. [자세히 보기](../experience-decisioning/decisioning-faq.md)

* 이메일 디자이너에 액세스하는 방법을 명확히 설명하기 위해 이메일 디자인 시작하기 페이지를 업데이트하였습니다. [자세히 보기](../email/get-started-email-design.md)

* DMARC 레코드 페이지에 DNS 전파 지연을 해결하기 위한 문제 해결 섹션이 추가되었습니다. [자세히 보기](../configuration/dmarc-record.md#troubleshooting)

* GenStudio for Performance Marketing 작업 페이지가 주요 기능, 일반적인 사용 사례, 사전 요구 사항 및 자주 묻는 질문 등의 새로운 섹션으로 개선되었습니다. [자세히 보기](../integrations/genstudio.md)

* 인바운드 채널이 있는 익명 프로필 타기팅에 대한 가드레일을 가드레일 및 제한 사항 페이지에 추가했습니다. 인증되지 않은 방문자를 타기팅하면 총 참여 가능한 프로필 수가 증가하므로 Adobe에서는 자동 프로필 삭제에 대한 TTL(Time-To-Live)을 설정하여 관련 비용을 관리할 것을 권장합니다. [자세히 보기](../start/guardrails.md#profile-management-inbound)

* 의사 결정 및 코드 기반 경험을 위한 웹 SDK 구성에 대한 두 가지 튜토리얼이 이제 코드 기반 구현 방법 샘플 페이지에서 참조됩니다. [자세히 보기](../code-based/code-based-decisioning-implementations.md#tutorials)

* 자산 및 이미지에 처음 게시한 후 최대 2년(730일) 동안 액세스할 수 있는 상태가 유지되며 만료 후 다시 게시해야 한다는 메모가 추가되었습니다. [자세히 보기](../content-management/proofs.md)

* 이제 포괄적인 AI 어시스턴트 콘텐츠 프롬프트 안내서를 사용할 수 있습니다. 이 안내서에서는 높은 전환율과 브랜드 중심 마케팅 콘텐츠를 만들기 위해 효과적인 프롬프트를 만드는 방법을 설명합니다. 마케팅 목표 작성, 브랜드 자산 사용, 다양한 채널에 대한 콘텐츠 최적화를 위한 모범 사례에 대해 알아봅니다. [자세히 보기](../content-management/ai-assistant-prompting-guide.md)

* `frequencyMap` 속성은 세그먼트 정의에 사용할 수 없으며 대상 세분화 기준의 일부로 사용할 수 없다는 점을 명확히 하는 메모를 세그먼트 정의 문서에 추가했습니다. 빈도 기반 타겟팅의 경우 비즈니스 규칙에서 빈도 제한 규칙 사용을 고려하십시오. [자세히 보기](../audience/creating-a-segment-definition.md)
* 기본 채널에서 사용자 정의 액션 응답을 사용하는 방법을 보여주는 새로운 예시가 API 호출 응답 설명서에 추가되었습니다. 이 예에서는 이메일, 푸시, SMS 메시지에서 Handlebars 구문을 사용하여 사용자 정의 액션 응답에서 중첩된 배열을 반복하는 방법을 보여 줍니다. [자세히 보기](../action/action-response.md#response-in-channels)

* 실시간(RT) 엔드포인트가 변경될 때 기존 사용자 지정 작업을 업데이트하는 방법을 설명하는 새로운 섹션을 Campaign v7/v8 통합 설명서에 추가했습니다. 섹션에는 엔드포인트 URL 업데이트, 연결 테스트 및 저장 전 변경 사항 유효성 검사에 대한 단계별 지침이 포함되어 있습니다. [자세히 보기](../action/acc-action.md#update-action)

* 다이내믹 콘텐츠와 함께 잠금 해제된 다른 조각 내 다이내믹 콘텐츠가 포함되어 있고 조각이 지원되지 않는 중첩에 대해 사용자에게 경고하는 새로운 제한 사항 및 모범 사례 섹션이 시각적 조각 설명서에 추가되었습니다. 안내서에는 호환성 모드 문제에 대한 문제 해결 단계 및 적절한 이메일 구조 설계를 위한 권장 사항이 포함되어 있습니다. [자세히 보기](../email/use-visual-fragments.md#fragment-dynamic-content)

* 사용자가 누락된 보고 데이터 문제를 해결하는 데 도움이 되는 문제 해결 섹션이 여정 라이브 보고 설명서에 추가되었습니다. 이 섹션에서는 보고 데이터 세트와의 여정 이름 동기화, 데이터 새로 고침 시간, 액세스 권한 확인, 여정 상태 요구 사항에 대해 설명합니다. [자세히 보기](../building-journeys/report-journey.md#troubleshooting-missing-data)

* 에셋 만료 및 라이프사이클 관리를 설명하는 세 가지 새로운 FAQ 항목이 에셋 설명서에 추가되었습니다. 주요 내용은 AEM 에셋에 대한 TTL(Time-To-Live) 정책(730일), 에셋 만료로 인해 손상된 이미지를 해결하는 방법 및 에셋 만료 논리의 향후 개선 사항에 대한 정보 등입니다. [자세히 보기](../integrations/assets.md#faq-assets)

* 여정을 입력하는 예상 프로필과 실제 프로필 간의 대상 수 불일치를 해결하기 위해 대상 읽기 활동 설명서에 포괄적인 문제 해결 섹션이 추가되었습니다. 이 섹션에서는 타이밍 및 데이터 전파 문제, 데이터 유효성 검사 및 모니터링 기법, &quot;배치 대상자 평가 후 트리거&quot; 옵션 사용을 포함한 모범 사례에 대해 설명합니다. [자세히 보기](../building-journeys/read-audience.md#audience-count-mismatch)

* 스트리밍 세분화 지연 시간(최대 2시간)을 명확히 하고 시간에 민감한 여정에 대해 대기 활동 또는 버퍼 시간을 추가하는 것이 좋다는 메모가 대상자 선별 이벤트 설명서에 추가되었습니다. [자세히 보기](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* 백엔드 처리 오버헤드를 허용하기 위해 작성된 콘텐츠를 1MB 미만으로 유지하는 모범 사례를 포함하여 여정 게시에 대한 2MB 메시지 콘텐츠 크기 제한을 문서화한 이메일 가드레일에 새 섹션이 추가되었습니다. [자세히 보기](../start/guardrails.md#message-content-size)

* 스냅샷 타이밍 종속성 및 24시간 전환 확인 제한을 명확하게 하기 위해 대상 읽기 활동의 증분 읽기 옵션에 대한 설명서를 개선했습니다. 여기에는 누락된 프로필을 방지하기 위한 권장 사항이 포함됩니다. [자세히 보기](../building-journeys/read-audience.md)

* 여러 조회를 묶을 수 없음을 구체적으로 설명하는 메모가 데이터 세트 조회 가드레일에 추가되었습니다. [자세히 보기](../data/lookup-aep-data.md#guidelines)

* 이제 액션 캠페인에 WhatsApp 및 LINE 채널을 사용할 수 있습니다. [자세히 보기](../campaigns/campaign-content.md)

* 여정 처리 속도에 대한 새로운 종합 섹션이 입력 관리 설명서에 추가되었습니다. 프로필 진입률, 여정 내 이벤트 및 대상자 선별, 대기 활동 영향, 액션 활동 영향에 대해 다룹니다. [자세히 보기](../building-journeys/entry-management.md#journey-processing-rate)

* 이제 이메일 메시지를 디자인할 때 시스템에서 주요 설정을 확인하고 경고와 오류에 대한 알림을 표시합니다. 이메일 경고 및 유효성 검사 요구 사항에 대한 정보를 가드레일 페이지에 추가했습니다. [자세히 보기](../email/create-email.md#check-email-alerts)

* 오퍼 제한 추가 페이지에서 이전에 만든 오퍼에 대해 캡핑을 활성화하거나 비활성화할 수 없다는 주의 사항이 제거되었습니다. [자세히 보기](../offers/offer-library/add-constraints.md#capping)

* 여정 단계 이벤트로 작업하는 방법에 대한 설명서가 공개되었습니다. [자세히 보기](../reports/journey-step-events-overview.md)

* 여정에서 삭제된 이벤트를 식별하는 쿼리가 세그먼트 내보내기 작업 오류, Dispatcher 취소 및 상태 시스템 취소에 대한 적절한 필터를 포함하도록 수정되었습니다. [자세히 보기](../reports/query-examples.md#common-queries)

* SQL 코드를 제시하기 전에 더 나은 컨텍스트를 제공하고 각 쿼리가 수행하는 작업을 설명하기 위해 쿼리 예시 설명서의 37개 쿼리 예시 전체에 소개 문장이 추가되었습니다. 이를 통해 사용자의 이해도가 향상되고 각 쿼리를 사용해야 하는 경우에 대한 명확한 지침을 확보할 수 있게 되었습니다. [자세히 보기](../reports/query-examples.md)

## 2025년 10월 {#october-2025}

* 이제 이미지 HTML 전환기를 사용하여 이미지를 HTML 템플릿으로 전환할 수 있습니다. [자세히 보기](../email/image-to-html.md)

* Adobe Journey Optimizer 릴리스 주기에 대한 정보가 공개되었습니다. [자세히 보기](releases.md)

* 이제 새로운 여정 FAQ 페이지를 사용할 수 있습니다. [자세히 보기](../building-journeys/journey-faq.md)

* 이제 사용자 정의 액션 모니터링 기능을 사용할 수 있습니다. [자세히 보기](../action/reporting.md)

* 이제 API 트리거 캠페인의 높은 처리량 모드를 사용할 수 있습니다. [자세히 보기](../campaigns/api-triggered-high-throughput.md)

* 이제 여정에 대한 오류 코드 참조를 사용할 수 있습니다. [자세히 보기](../building-journeys/error-codes-reference.md)

* 이제 Journey Optimizer Experimentation Accelerator 설명서를 사용할 수 있습니다. [자세히 보기](../content-management/experiment-accelerator-gs.md)

* **formatDate** 도우미 함수 설명서에 새로운 섹션을 추가했습니다. 이 섹션에서는 y, Y, M, d, D와 같은 주요 패턴 기호의 의미를 명확히 설명합니다. [자세히 읽기](../personalization/functions/dates.md#pattern-characters)

* 결정 순위 수식 섹션에 프로필의 우편 번호 및 연간 소득을 기반으로 오퍼를 활성화하는 방법을 보여 주는 PQL 예제가 추가되었습니다. [자세히 보기](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* 테스트 모드 섹션에 테스트 모드가 사용자 정의 업로드 대상자 속성 강화를 지원하지 않는다는 제한을 추가했습니다. [자세히 보기](../building-journeys/testing-the-journey.md#important_notes)

* [의사 결정 관리 가드레일 및 제한 사항](../offers/decision-management-guardrails.md#configurations)과 [결정 가드레일 및 제한 사항](../experience-decisioning/decisioning-guardrails.md#configurations) 페이지에 지원되는 최대 구성 수(20,000개)를 명시하는 섹션을 새로 추가했습니다. 이는 샌드박스에 있는 총 캡핑 규칙 수에 해당합니다.

* 여정의 조건 활동 섹션에 두 개를 초과하는 크로스 디바이스 ID가 포함된 프로필에 대한 조건 평가가 실패한다는 메모를 추가했습니다. [자세히 보기](../building-journeys/condition-activity.md)

* 동의 정책을 사용하여 고객의 동의를 존중하면서 고객의 선택에 따라 고객의 선호를 적용하는 방법을 설명하는 새 페이지를 추가했습니다. [자세히 보기](../action/preference-center.md)

* 프로필 시작 페이지 및 가드레일 페이지에 데이터를 수집할 때 이메일이 대소문자를 구분하므로 해당 수신자를 타기팅할 때 중복 프로필을 만들고 사용할 수 있다는 메모를 추가했습니다. [자세히 보기](../audience/get-started-profiles.md)

* 개인화 편집기에 새 `render` 속성이 도입되었습니다. 표현식 조각의 콘텐츠를 숨기려는 경우 `false`(으)로 설정합니다. [자세히 보기](../personalization/use-expression-fragments.md#use-expression-fragment)

* 의사 결정 정책 내 의사 결정 항목에 첨부된 조각을 활용하는 방법을 설명하는 섹션에 가드레일 목록이 추가되었습니다. [자세히 보기](../experience-decisioning/create-decision.md#guardrails-limitations)

* 데이터 세트 조회에 대한 모범 사례 추가: 색인화 문제를 방지하기 위해 토글을 계속 켜 두고, 배치 삭제가 조회 데이터에 미치는 영향을 이해합니다. [자세히 보기](../data/lookup-aep-data.md#guidelines)

* 보조 식별자가 있는 대상자 읽기 여정을 사용할 때 통합 프로필 서비스 대상자만 지원된다는 제한 사항을 추가했습니다. [자세히 보기](../building-journeys/supplemental-identifier.md#guardrails)

* Experimentation Accelerator 설명서가 별도의 컬렉션으로 재배치되었습니다. [자세히 보기](https://experienceleague.adobe.com/ko/docs/experimentation-accelerator/using/overview)

## 2025년 9월 {#september-2025}

* 가드레일 및 제한 사항 페이지에 새로운 인바운드 채널 섹션을 추가해 웹, 인앱, 코드 기반 경험, 콘텐츠 카드 채널에 적용되는 제한 사항을 모두 모았습니다. 여기에는 모든 인바운드 요청에 대해 초당 인바운드 요청 5,000개라는 최대 볼륨 제한과 활성 인바운드 액션 최대 500개라는 제한이 포함됩니다. [자세히 보기](../start/guardrails.md#inbound-guardrails)

* 오케스트레이션된 캠페인에 대해 자주 묻는 질문 페이지가 릴리스되었습니다. [자세히 보기](../orchestrated/orchestrated-campaigns-faq.md)

* 여정 단계 이벤트 설명서에 자주 발생하는 삭제 이벤트 유형의 정의, 일반적인 원인, 문제 해결 단계가 포함된 문제 해결 섹션이 추가되었습니다. [자세히 보기](../reports/sharing-field-list.md#discarded-events)

* 여정에서 보조 식별자를 사용하는 방법에 대한 설명서에 이제 보조 ID를 사용하는 여정에서 종료 기준이 적용될 때 프로필이 어떻게 작동하는지 자세히 설명하는 표가 포함됩니다. [자세히 보기](../building-journeys/supplemental-identifier.md#exit-criteria)

* 일시 중지된 여정의 프로필 삭제에 대해 이해하기 위한 문제 해결 섹션이 추가되었습니다. [자세히 보기](../building-journeys/journey-pause.md#discards-troubleshoot)

* 스키마 개요 설명서에 오케스트레이션된 캠페인에 사용되는 표준 및 관계형 스키마를 구별하기 위한 정보를 추가했습니다. [자세히 보기](../data/gs-data.md)

* 결정 및 의사 결정 관리 설명서에 [자동 최적화](../experience-decisioning/ranking/auto-optimization-model.md) 및 [개인화된 최적화](../experience-decisioning/ranking/personalized-optimization-model.md) 모델을 성공적으로 교육하기 위한 요구 사항에 대한 정보를 추가했습니다.

* 대화형 메시지 실행 REST API 호출에 60초 시간 제한이 있으며, 전달을 보장하기 위한 내부 재시도가 있음을 명확히 설명했습니다. [자세히 보기](../campaigns/trigger-campaigns.md)

* 결정 항목 컬렉션 페이지에서 규칙을 정의할 때 **CONTAINS** 연산자의 동작을 명확하게 설명하도록 업데이트했습니다. [자세히 보기](../experience-decisioning/collections.md)

* 우선순위 점수 할당 페이지에 **액션** 활동 내의 인바운드 채널 작업에 대한 우선순위 점수를 정의하기 위한 구체적 단계를 업데이트했습니다. [자세히 보기](../conflict-prioritization/priority-scores.md#priority-action)

## 2025년 8월 {#august-2025}

* [!DNL Journey Optimizer]로 접근 가능한 이메일 및 랜딩 페이지 콘텐츠 디자인 모범 사례를 설명하는 새 페이지를 추가했습니다. [자세히 보기](../email/accessible-content.md)

* 여정의 보조 식별자 설명서에 다음 설명을 업데이트했습니다.

   * 스키마에 보조 식별자를 추가한 후 새 이벤트(이벤트 트리거 여정의 경우) 또는 새 필드 그룹(대상자 읽기 여정의 경우)을 만들어야 합니다. 기존 엔터티는 자동으로 새로 고쳐지지 않으며 새 식별자를 인식하지 않습니다.

   * 보조 식별자는 DULE(Data Usage Labeling &amp; Enforcement) 정책을 기준으로 확인되지 않으며, 여정의 데이터 거버넌스 검사 중에 고려되지 않습니다.

[자세히 보기](../building-journeys/supplemental-identifier.md)

* 캠페인의 최적화 페이지에 이제 여정에서도 최적화를 사용할 수 있다는 사실을 반영하여 업데이트했습니다. [자세히 보기](../campaigns/campaigns-message-optimization.md)

* 캠페인에서 메시지 최적화를 활용하는 방법을 설명하는 튜토리얼 비디오 링크를 추가했습니다. [자세히 보기](../campaigns/campaigns-message-optimization.md)

## 2025년 7월 {#july-2025}

* 이제 캠페인 인터페이스에는 두 가지 탭 즉, **액션** 및 **API 트리거**&#x200B;가 있습니다. 이에 따라 설명서도 업데이트되었으며, 각 캠페인 유형에 대한 정보가 전담 섹션으로 구성되어 명확성과 사용성이 향상되었습니다. [자세히 보기](../campaigns/get-started-with-campaigns.md)

* [하위 도메인 위임 시작](../configuration/about-subdomain-delegation.md) 및 [하위 도메인 위임](../configuration/delegate-subdomain.md) 페이지를 업데이트하여 다양한 위임 방법과 설정 단계를 보다 잘 보여 줍니다.

* 조각 섹션에 다음과 같은 메모가 추가되었습니다. 여정 또는 캠페인에서 추적을 활성화할 때 조각에 링크가 있고 이 조각을 메시지에 사용하는 경우 이러한 링크가 메시지에 포함된 다른 모든 링크와 같이 이러한 링크가 추적됩니다. [자세히 알아보기](../content-management/create-fragments.md#content)

* Journey Optimizer의 하위 도메인 위임에 적용되는 가드레일 및 제한 사항이 보강되어 하나의 전용 섹션으로 통합되었습니다. [자세히 보기](../configuration/delegate-subdomain.md#guardrails)

* 대체 오퍼 만들기 및 의사 결정 페이지 만들기에 대체 오퍼가 의사 결정 내에서 사용되는 모든 표현을 포함해야 한다는 메모가 추가되었습니다. [자세히 보기](../offers/offer-library/creating-fallback-offers.md)

* 조각에 적용되는 가드레일이 보강되었습니다. [자세히 보기](../start/guardrails.md#fragments-guardrails).

* 메시지에 추가된 링크는 25개월 후에 만료되고 미러 페이지에 연결된 링크는 90일 후에 만료된다는 메모가 추가되었습니다. [자세히 보기](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## 2025년 6월 {#june-2025}

* HTML 구성 요소를 사용하여 사용자 정의 가능한 조각에 줄 바꿈, 굵게, 기울임체 등 서식이 있는 텍스트를 추가하고 사용하는 방법에 대한 새 섹션을 추가했습니다. [자세히 보기](../content-management/customizable-fragments.md#rich-text)

* 결정 부분에 AI 모델 구축을 다루는 전용 섹션을 업데이트했습니다. [자세히 보기](../experience-decisioning/ranking/ai-models.md)

* journeyStep 이벤트 액션에서 `actionExecutionTime` 필드 사용에 대한 권장 사항을 추가했습니다. [자세히 보기](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* 개별 게재마다 고유하지 않을 수 있는 `messageID`에 대한 메모를 추가했습니다. [자세히 보기](../data/datasets-query-examples.md)

* 데이터 위생 작업의 지난 이벤트 관리에 대한 권장 사항을 추가했습니다. [자세히 보기](../privacy/data-hygiene.md#data-hygiene-recommendations)

* 랜딩 페이지에 샌드박스 간 마이그레이션이 지원되지 않는다는 가드레일을 추가했습니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#global)

* 사용자 정의 액션에 대한 사용자 정의 인증에서 중첩된 JSON 개체가 지원되지 않는다는 주의 사항을 추가했습니다. [자세히 보기](../datasource/external-data-sources.md)

* 이메일 디자이너의 조건부 콘텐츠 베리에이션 이름 지정에 대한 주의 사항을 추가했습니다. [자세히 보기](../personalization/create-conditions.md)

* “랜딩 페이지 하위 도메인 위임 취소” 섹션을 업데이트했습니다. [자세히 보기](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* 보조 식별자를 사용하는 경우의 여정 재입장 규칙을 명확히 설명했습니다. [자세히 보기](../building-journeys/supplemental-identifier.md#guardrails)

* 이벤트 구성 중에 보조 식별자 속성을 선택할 때는 고급 모드에서 표현식 편집기를 사용해야 한다고 명확히 설명하는 새 메모를 추가했습니다. [자세히 알아보기](../building-journeys/supplemental-identifier.md#add)

* 여정 재입장과 보조 식별자가 함께 작동하는 방식에 대한 설명을 추가했습니다. [자세히 알아보기](../building-journeys/supplemental-identifier.md#guardrails)

## 2025년 5월 {#may-2025}

* 이제 “시스템 및 환경 연결” 섹션에 Journey Optimizer에서 사용할 수 있는 Adobe 통합 목록이 표시됩니다. [자세히 보기](../integrations/ajo-integrations.md)

* 이제 콘텐츠 통합이 콘텐츠 관리 섹션에 그룹화되어 있습니다. [자세히 보기](../integrations/content-integrations.md)

* Adobe Experience Platform 및 Journey Optimizer에 대한 아키텍처 다이어그램이 업데이트되었습니다. [자세히 보기](../start/get-started.md#architecture)

* 샘플 데이터를 사용하여 개인화 코드를 작성하고 테스트하는 방법을 학습하는 데 도움이 되는 개인화 편집기 플레이그라운드에 대한 비디오를 추가했습니다. [자세히 보기](../personalization/personalize.md#video-perso)

* 시드 리스트의 최대 주소 수를 50개에서 300개로 늘렸습니다. [자세히 보기](../configuration/seed-lists.md#create-seed-list)

* 결정 정책 만들기 페이지에 결정 정책을 사용할 때 코드를 래핑하는 방법을 자세히 설명하는 새 단계를 추가했습니다. [자세히 보기](../experience-decisioning/create-decision.md#create-decision)

* 코드 기반 경험 설명서에 동일한 표면에서 여러 코드 기반 경험 액션 실행 시 최종 사용자가 두 개 이상의 액션에 적합한 경우 캠페인이나 여정의 우선순위 점수로 최종 사용자에게 무엇을 전달할지 결정한다는 메모를 추가했습니다. [자세히 보기](../code-based/code-based-surface.md#surface-definition)

* 여정의 인바운드 액션 문제 해결에 대한 새 페이지에서는 지원을 요청하기 전에 문제를 독립적으로 식별하고 해결하기 위한 단계별 안내서를 제공합니다. [자세히 보기](../building-journeys/troubleshooting-inbound.md)

* 코드 기반 환경에서 결정을 사용할 때 클라이언트 구현에 다음 플래그를 추가하는 방법을 설명하는 새 [페이지](../code-based/code-based-decisioning-implementations.md)를 추가했습니다.

   * 코드 기반 경험에서 결정을 테스트하기 위해 `dryRun` 플래그를 추가합니다. [자세히 보기](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * 코드 기반 경험에서 결정 요청에 중복 제거를 적용합니다. [자세히 보기](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## 2025년 4월 {#apr-2025}

* 구성 챕터를 [채널 구성](../configuration/get-started-configuration.md), [여정 구성](../configuration/about-data-sources-events-actions.md), [시스템 연결](../configuration/ajo-apis.md)이라는 세 챕터로 분할했습니다.
* 여정 표현식 및 조건에서 경험 이벤트를 사용할 때의 주의 사항을 추가했습니다. [자세히 보기](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* 다이렉트 메일 구성 페이지에 출력 파일의 임시 저장에 대한 메모를 추가했습니다. [자세히 보기](../direct-mail/direct-mail-configuration.md)
* 여정 고급 표현식 편집기 섹션에 조건문 형식 지침에 대한 팁을 추가했습니다. [자세히 보기](../building-journeys/expression/expressionadvanced.md)
* `inAudience` 함수 섹션에 대상자의 이름을 바꿀 때의 영향과 모범 사례에 대한 주의 메모를 추가했습니다. [자세히 보기](../building-journeys/functions/functioninaudience.md)
* 양방향 SMS 사용 시 기본 키워드 사용에 대한 권장 사항을 추가했습니다. [자세히 보기](../sms/sms-opt-out.md)
* 여정 테스트 페이지를 업데이트하여 사용하는 이벤트에 ID 네임스페이스를 포함할 필요성에 대한 메모를 추가했습니다. [자세히 보기](../building-journeys/testing-the-journey.md)
* 현재는 [!UICONTROL Journey Optimizer] 사용자 인터페이스를 통해 하위 도메인의 위임을 해제할 수 없습니다. Adobe 담당자에게 연락해야 합니다. 이제 [이메일](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [웹 경험](../web/web-delegated-subdomains.md#undelegate-subdomain), [랜딩 페이지](../landing-pages/lp-subdomains.md#undelegate-subdomain)에서 하위 도메인의 위임을 취소하는 단계를 자세히 설명합니다.<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* 여정 캡핑 API의 선택적 `maxHttpConnections` 매개 변수에 대한 설명을 추가했습니다. 여기에는 이 매개 변수를 동일한 엔드포인트에 대한 제한 구성과 함께 사용하는 방법에 대한 지침이 포함됩니다. [자세히 보기](../configuration/throttling.md)
* 경험 결정 섹션에 승인된 오퍼 항목을 컬렉션이나 결정에 사용할 경우 삭제할 수 없다는 안내를 추가했습니다. **[!UICONTROL 승인 실행 취소]** 옵션을 사용하여 상태를 “초안”으로 변경하는 단계를 포함했습니다. [자세히 보기](../experience-decisioning/items.md#manage)
* 샌드박스에 대한 정보를 새로운 “샌드박스 관리” 섹션으로 그룹화했습니다. 이 새로운 섹션에서는 샌드박스를 사용 및 할당하는 방법과 패키지 내보내기 및 가져오기 기능을 사용하여 여러 샌드박스 간에 여정, 콘텐츠 템플릿 또는 조각과 같은 오브젝트를 복사하는 방법에 대해 설명합니다. [자세히 보기](../administration/sandboxes.md)

## 2025년 3월 {#mar-2025}

* 대상자 선별 이벤트에 대한 페이지에 새로운 권장 사항을 업데이트했습니다. [자세히 보기](../building-journeys/audience-qualification-events.md)
* 이제 사용자 정의 작업 문제 해결 기능을 모든 고객이 사용할 수 있습니다(GA). [자세히 보기](../action/troubleshoot-custom-action.md)
* 이제 제품 사용자 인터페이스에서 [데이터 위생]의 이름이 [데이터 라이프사이클]로 변경되었습니다. 이 변경 사항을 반영하여 설명서를 업데이트했습니다. [자세히 보기](../privacy/data-hygiene.md)
* 누락된 [랜딩 페이지] 기본 제공 권한이 설명서에 추가되었습니다. [자세히 보기](../administration/ootb-permissions.md)
* 반복 캠페인 예약에 대한 메모가 추가되었습니다. [자세히 보기](../campaigns/create-campaign.md)
* 이메일 메시지에 링크를 삽입하고 추적을 활성화하는 작업에 대한 섹션을 업데이트 및 재구성했습니다. [자세히 보기](../email/message-tracking.md)
* Adobe Journey Optimizer의 개인화 기능에 대한 섹션을 재구성하고 개선했습니다. [자세히 보기](../personalization/personalize.md)
* 개인화된 오퍼를 나열하는 의사 결정 관리 API는 응답에서 여러 개인화된 오퍼가 누락된 경우 페이지 매김을 수행하는 샘플을 포함하도록 업데이트되었습니다. [자세히 보기](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* 명료성을 개선하기 위해 [목록 구독 취소] 기능에 대한 모든 정보를 모은 새 페이지를 만들었습니다. [자세히 보기](../email/list-unsubscribe.md)
* [빈도 캡핑] 섹션에서 Edge Decisioning API 외에도 Decisioning 및 Batch Decisioning API에 대한 빈도 캡핑 카운터가 어떻게 업데이트되는지에 대한 정보를 업데이트했습니다. [자세히 보기](../offers/offer-library/add-constraints.md#frequency-capping)

## 2025년 2월 {#feb-2025}

* [대상자 읽기] 활동 가드레일은 한 여정에서 하나의 활동만 사용할 수 있고 대상자 한 명만 타기팅할 수 있다는 점을 명시하여 업데이트했습니다. [자세히 보기](../building-journeys/read-audience.md)
* Adobe Campaign 활동 사용 시 여정 가드레일을 업데이트했습니다. [자세히 보기](../start/guardrails.md#ac-g)
* 첫 번째 여정을 만드는 단계가 자세히 설명되어 있으며 설명서 섹션에 대한 링크가 추가되었습니다. [자세히 보기](../building-journeys/journey-gs.md)
* 이제 새 페이지에서 여정 대시보드 및 필터링 사용자 인터페이스를 자세히 확인할 수 있습니다. [자세히 보기](../building-journeys/journey-ui.md)
* **[!UICONTROL 전송 시간 최적화]** 및 관련 FAQ에 대한 설명서를 업데이트 및 개선하고 새 전용 페이지로 이동했습니다. [자세히 보기](../building-journeys/send-time-optimization.md)
* 여정 이벤트에 대한 새 가드레일을 추가했습니다. [자세히 보기](../start/guardrails.md#events-g)
* 기본 제공 채널 액션 페이지를 재구성했습니다. [자세히 보기](../building-journeys/journeys-message.md)
* 의사 결정 및 의사 결정 관리 섹션에 가드레일과 제한 사항이 추가되었습니다.
   * [의사 결정 가드레일 및 제한 사항](../experience-decisioning/decisioning-guardrails.md)
   * [의사 결정 관리 가드레일 및 제한 사항](../offers/decision-management-guardrails.md)
* 의사 결정 관리 설명서에 컨텍스트 데이터에 대한 새 섹션이 추가되었습니다. 해당 섹션에서는 의사 결정 엔진에서 컨텍스트 데이터를 활용하는 방법에 대한 정보를 제공합니다. 예를 들어 의사 결정 요청이 이루어질 때 현재 날씨가 80도 이상이어야 하는 결정 규칙을 디자인하는 데 도움이 됩니다. [자세히 보기](../offers/context-data.md)

## 2025년 1월 {#jan-2025}

* 이메일 구성의 **[!UICONTROL 실행 주소]** 옵션에 대한 새로운 섹션을 추가했습니다. 기본 주소는 샌드박스 수준에서 정의되지만, 특정 이메일 구성에 대해 기본 설정을 재정의할 수 있습니다. [자세히 보기](../email/email-settings.md#execution-address)

* **전달성 시작** 페이지에 사용자 인터페이스에서 직접 IP 워밍업 워크플로를 만들 수 있다는 내용을 추가하여 업데이트했습니다. [자세히 보기](../reports/deliverability.md#reputation)

* **헤더 매개 변수** 섹션에 사용자 인터페이스의 새로운 레이블 및 변경 사항을 반영하여 업데이트했습니다. [자세히 보기](../email/email-settings.md#email-header)

* **이메일 전달** 섹션에 **발신자 이메일** 주소로 보낸 이메일은 모두 전달 이메일 주소로 전달한다는 점을 명시하여 업데이트했습니다. 전달 이메일을 지정하지 않은 경우 해당 이메일은 삭제됩니다. [자세히 보기](../email/email-settings.md#email-settings)

* API 트리거 캠페인 요청에 전달되는 상황별 속성의 최대 크기를 200kb로 업데이트했습니다. [자세히 보기](../campaigns/api-triggered-campaigns.md#contextual)

* 라이브 조각에 새 속성을 추가하는 방법을 설명하기 위해 **조각 관리** 페이지에 새로운 섹션을 추가했습니다. 전체적인 페이지도 개선했습니다. [자세히 보기](../content-management/manage-fragments.md#adding-new-attributes)

* 충돌 관리 및 우선 순위 지정 도구 설명서에 &quot;가드레일 및 제한 사항&quot; 섹션을 추가했습니다. [자세히 보기](../conflict-prioritization/gs-conflict-prioritization.md)

* [!DNL Journey Optimizer] 코드 기반 경험 채널을 사용하는 콘텐츠 실험에서 Decisioning을 사용하는 데 필요한 모든 단계를 제공하는 새로운 엔드투엔드 사용 사례를 추가했습니다. [자세히 보기](../experience-decisioning/experience-decisioning-uc.md)

* **이메일 설정 구성** 페이지의 가독성을 개선하기 위해 여러 하위 페이지로 나누고 [구독 취소 목록](../email/list-unsubscribe.md), [헤더 매개변수](../email/header-parameters.md), [URL 추적](../email/url-tracking.md)에 대한 새로운 독립형 페이지를 추가했습니다.

## 2024년 12월 {#nov-2024}

* Adobe Experience Platform 데이터를 사용하여 개인화할 데이터 세트를 활성화하기 위한 API 호출 수행 시 발생할 수 있는 오류 메시지를 해결하는 데 도움이 되는 메모가 추가되었습니다. [자세히 보기](../personalization/aep-data-perso.md)

## 2024년 10월 {#oct-2024}

* [!DNL Journey Optimizer] 2024년 10월 릴리스의 모든 새로운 기능 및 개선 사항은 설명서에 자세히 나와 있습니다. [자세히 보기](release-notes.md)
* [!DNL Journey Optimizer]에서 사용할 수 있는 모든 통신 채널이 이제 설명서의 전용 섹션에 그룹화되었습니다. [자세히 보기](../channels/gs-channels.md)
* 프로세스를 보다 명확하게 설명하도록 **코드 기반 경험 구성** 페이지를 개선했습니다. 표면 URI의 정의를 설명하는 섹션이 포함됩니다. [자세히 보기](../code-based/code-based-configuration.md)
* **웹 채널 구성 만들기** 페이지에서 페이지 일치 규칙을 만드는 단계를 명확하게 설명하도록 업데이트했습니다. 이는 코드 기반 경험 구성에도 적용됩니다. [자세히 보기](../web/web-configuration.md#web-page-matching-rule)
* 시스템 생성 데이터 세트에 적용될 예정인 TTL(Time-to-Live) 가드레일에 대한 메모를 추가했습니다. [자세히 보기](../data/get-started-datasets.md)
* 여정 또는 캠페인의 콘텐츠를 시뮬레이션할 때 **디바이스에서 미리 보기** 옵션을 사용하여 브라우저 또는 모바일 디바이스에서 바로 코드 기반의 개인화된 경험을 미리 보는 방법을 설명하는 새 섹션을 추가했습니다. [자세히 보기](../code-based/test-code-based.md#preview-on-device)
* 의사 결정에 사용자 정의 업로드 대상자를 활용하는 방법에 대한 새 페이지를 추가했습니다. [자세히 보기](../offers/custom-upload-decisioning.md)
* Journey Optimizer에서 사용할 수 있는 결정 기능을 소개하는 새 페이지가 추가되었습니다. [자세히 보기](../experience-decisioning/gs-decision.md)
* 결정 설명서에 가드레일 및 제한 사항이 추가되었습니다. [자세히 보기](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## 2024년 9월 {#sept-2024}

* [!DNL Journey Optimizer] 24년 9월 릴리스의 모든 새로운 기능 및 개선 사항은 설명서에서 자세히 설명합니다. [자세히 보기](release-notes.md)
* 여정 다시 시도 관리에 대한 섹션을 추가했습니다. [자세히 보기](../building-journeys/read-audience.md#read-audience-retry)
* 사용자 정의 액션의 캡핑/스로틀링 규칙에 대한 FAQ에서 기본 캡핑 규칙을 언급하도록 업데이트했습니다. [자세히 보기](../configuration/external-systems.md#faq)
* 액세스 제어 섹션에 AI 어시스턴트 콘텐츠 생성기와 관련된 권한에 대한 정보를 업데이트했습니다. [자세히 보기](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* 이메일 생성을 위한 AI 어시스턴트 콘텐츠 생성기에 대한 비디오를 추가했습니다. [자세히 보기](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision Management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision Management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behaviour of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision Management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behaviour. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision Management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision Management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md#uc-journey)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision Management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision Management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision Management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
