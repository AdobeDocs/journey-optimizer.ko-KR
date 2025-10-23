---
solution: Journey Optimizer
product: journey optimizer
title: 여정 단계 이벤트 작업
description: Adobe Journey Optimizer에서 여정 단계 이벤트로 작업하는 방법 - 이벤트 유형, 중요한 이유, 분석 및 최적화에 이를 사용하는 방법을 알아봅니다
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: 여정, 단계 이벤트, 분석, 보고, 모니터링, XDM
hide: true
hidefromtoc: true
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 1%

---

# 여정 단계 이벤트 작업 {#work-with-journey-step-events}

여정 단계 이벤트는 [profile](../audience/get-started-profiles.md)이(가) Adobe Journey Optimizer의 [여정](../building-journeys/journey.md)을(를) 진행할 때 취하는 각 단계에 대한 자세한 정보를 캡처하는 자동으로 생성된 이벤트입니다. 이러한 이벤트는 [여정 성능](../building-journeys/report-journey.md)에 대한 포괄적인 가시성을 제공하고 강력한 분석 기능을 활성화합니다.

## 여정 단계 이벤트란? {#what-are-step-events}

여정 단계 이벤트는 여정에서 프로필이 한 노드에서 다른 노드로 이동할 때마다 Adobe Journey Optimizer에서 자동으로 만들어 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}에 보내는 시스템 생성 [XDM(Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=ko){target="_blank"} 이벤트입니다. 각 이벤트는 고객의 여정 경험에서 특정 [여정 활동](../building-journeys/about-journey-activities.md) 또는 전환에 해당합니다.

여정 단계 이벤트에는 두 가지 주요 유형이 있습니다.

- **journeyStepEvent**: 여정 단계를 통한 개별 프로필 진행과 관련된 이벤트
- **journeyStepProfileEvent**: 추가 프로필 컨텍스트 정보를 포함하는 이벤트

### 여정 단계 이벤트를 트리거하는 것은 무엇입니까? {#event-triggers}

여정 단계 이벤트는 다양한 여정 활동에 대해 자동으로 생성됩니다.

- **시작 여정**: [ 프로필이 이벤트에 들어갈 때](../building-journeys/entry-management.md)
- **작업 실행**: [메시지를 보낼 때](../building-journeys/journeys-message.md) 또는 [사용자 지정 작업](../building-journeys/using-custom-actions.md)을 수행할 때
- **조건 평가**: 프로필이 [조건](../building-journeys/condition-activity.md) 및 결정 지점을 통과할 때
- **대기 활동**: 프로필이 [대기 노드](../building-journeys/wait-activity.md)를 시작하고 종료할 때
- **종료 이벤트**: 프로필이 완료될 때 또는 [여정 종료](../building-journeys/end-journey.md)
- **오류 처리**: 여정 실행 중에 오류가 발생하는 경우

>[!NOTE]
>
>여정 단계 이벤트는 기본적으로 모든 인스턴스에서 활성화됩니다. 단계 이벤트를 프로비전하는 동안 만든 [스키마 및 데이터 세트](sharing-overview.md)을(를) 수정하거나 업데이트할 수 없습니다. 이러한 스키마와 데이터 세트는 읽기 전용 모드에 있습니다.

[여정 단계 이벤트 스키마](sharing-field-list.md)에 대해 자세히 알아보세요.

## 여정 단계 이벤트가 중요한 이유 {#why-step-events-matter}

여정 단계 이벤트는 Adobe Journey Optimizer을 사용하는 조직에 중요한 가치를 제공합니다.

### 실시간 분석 및 모니터링 {#real-time-analytics}

- **여정 성능 추적**: [실시간 보고서](live-report.md)를 사용하여 프로필이 여정을 통해 흐르는 방식을 실시간으로 모니터링합니다.
- **전환 분석**: [여정 분석](journey-global-report-cja.md)을 통해 중단점 및 성공적인 전환 경로를 이해합니다.
- **오류 감지**: [모니터링 및 알림](alerts.md)을 통해 발생하는 문제를 식별하고 해결합니다.

### 데이터 통합 및 통찰력 {#data-integration}

- **플랫폼 간 분석**: 여정 데이터를 다른 [Adobe Experience Platform 데이터 원본](../datasource/adobe-experience-platform-data-source.md)과 결합
- **Customer 360 보기**: 여정 상호 작용을 포함하는 포괄적인 [고객 프로필](../audience/get-started-profiles.md) 만들기
- **속성 모델링**: [Customer Journey Analytics](cja-ajo.md)을(를) 사용하여 여정 터치 포인트를 다운스트림 비즈니스 결과에 연결

### 최적화 기회 {#optimization}

- **A/B 테스트 인사이트**: [실험](campaign-global-report-cja-experimentation.md)을 사용하여 다양한 여정 경로의 성능을 분석합니다.
- **Personalization 개선 사항**: 여정 동작 데이터를 사용하여 [다이내믹 콘텐츠](../personalization/dynamic-content.md)를 통해 향후 환경을 개선합니다.
- **운영 효율성**: 병목 현상을 식별하고 [여정 디자인을 최적화합니다](../building-journeys/using-the-journey-designer.md)

## 여정 단계 이벤트를 사용하는 방법 {#how-to-use-step-events}

### 여정 단계 이벤트 데이터 액세스 {#accessing-data}

여정 단계 이벤트 데이터는 자동으로 Adobe Experience Platform에 저장되고 다음을 통해 액세스할 수 있습니다.

1. **데이터 레이크 쿼리**: SQL을 사용하여 `journey_step_events`쿼리 서비스[로 ](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=ko){target="_blank"} 데이터 집합을 쿼리합니다.
2. **Customer Journey Analytics**: [고급 분석 도구](cja-ajo.md)를 통해 여정 데이터 분석
3. **실시간 보고**: Journey Optimizer의 [기본 제공 보고 기능을 통해 데이터에 액세스](gs-reports.md)
4. **API**: 사용자 지정 응용 프로그램의 이벤트 데이터에 프로그래밍 방식으로 액세스합니다.

[데이터 세트에 액세스](../data/datasets-query-examples.md)에 대해 자세히 알아보세요.

### 사용 가능한 주요 데이터 포인트 {#key-data-points}

여정 단계 이벤트는 다음을 포함한 포괄적인 정보를 캡처합니다.

- **여정 식별**: [여정 ID, 버전 및 이름](sharing-journey-fields.md)
- **프로필 정보**: [프로필 ID 및 관련 ID](sharing-identity-fields.md)
- **단계 세부 정보**: [노드 이름, 단계 유형 및 실행 상태](sharing-common-fields.md)
- **타임스탬프**: 각 여정 단계의 정확한 타이밍
- **작업 결과**: [성공/실패 상태 및 실행 세부 정보](sharing-execution-fields.md)
- **오류 정보**: 문제가 발생할 때 자세한 [오류 코드 및 설명](sharing-field-list.md#discarded-events)

[사용 가능한 모든 필드 정의](sharing-field-list.md)를 살펴보세요.

### 일반적인 사용 사례 {#common-use-cases}

**성능 모니터링**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**오류 분석**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**funnel 분석 여정**

- 각 여정 단계에서 전환율 추적
- 프로필이 여정을 가장 일반적으로 종료하는 위치 식별
- 다른 여정 단계에서 보낸 시간 측정

[funnel 분석을 위한 쿼리 기법](query-examples.md#common-queries)에 대해 자세히 알아보세요.

## 샘플 및 리소스 {#samples-resources}

### 쿼리 예제 및 템플릿 {#query-examples}

일반적인 여정 단계 이벤트 분석을 위한 포괄적인 쿼리 예제를 살펴보십시오.

- **[여정 단계 이벤트 쿼리 예제](query-examples.md)**: 일반적인 분석 시나리오에 사용할 준비가 되었습니다.
- **[데이터 집합 쿼리 샘플](../data/datasets-query-examples.md#journey-step-event)**: 여정 단계 이벤트 데이터 집합을 쿼리하는 예제
- **[프로필 기반 쿼리](query-examples.md#profile-based-queries)**: 개별 프로필 여정 및 상호 작용 추적

### 필드 설명서 {#field-documentation}

여정 단계 이벤트의 전체 데이터 구조를 이해합니다.

- **[여정 단계 이벤트 필드 목록](sharing-field-list.md)**: 사용 가능한 모든 필드에 대한 포괄적인 참조
- **[공통 필드](sharing-common-fields.md)**: journeyStepEvent 및 journeyStepProfileEvent에서 필드 공유
- **[작업 실행 필드](sharing-execution-fields.md)**: 작업 실행 추적에 관련된 필드
- **[여정 필드](sharing-journey-fields.md)**: 여정 관련 메타데이터 및 식별자

### 모범 사례 및 문제 해결 {#best-practices}

**성능 최적화**

- 쿼리 성능 향상을 위해 `journeyVersionID` 대신 `journeyVersionName`을(를) 사용합니다([여정 속성에 대해 자세히 알아보기](../building-journeys/expression/journey-properties.md)).
- 날짜 범위별로 필터링하여 큰 데이터 세트의 쿼리 속도 개선
- [여정 네임스페이스 구성](../building-journeys/entry-management.md)과(와) 일치하는 프로필 ID 활용

**데이터 품질**

- 데이터 문제를 식별하기 위해 [삭제된 이벤트](sharing-field-list.md#discarded-events)를 정기적으로 모니터링합니다.
- 이벤트 스키마가 분석 요구 사항과 일치하는지 확인
- 사용자 정의 쿼리에서 적절한 오류 처리 구현

**분석 전략**

- 전체 속성을 위해 여정 단계 이벤트를 [메시지 피드백 데이터](../data/datasets-query-examples.md#message-feedback-event-dataset)와(과) 결합
- 시간 기반 분석을 사용하여 여정 속도 및 병목 현상 파악

### 고급 분석 기능 {#advanced-analytics}

**Customer Journey Analytics 통합**
여정 단계 이벤트는 다음에 대해 [Customer Journey Analytics](cja-ajo.md)을(를) 사용하여 분석할 수 있습니다.

- 고급 속성 모델링
- 크로스 채널 여정 시각화
- 여정 결과에 대한 예측 분석

Journey Optimizer 데이터에 대해 [Customer Journey Analytics을 구성](report-gs-cja.md)하는 방법을 알아봅니다.

## 추가 리소스 {#additional-resources}

### 설명서 링크 {#documentation-links}

- **[여정 단계 공유 개요](sharing-overview.md)**: 여정 데이터가 Adobe Experience Platform으로 흐르는 방식 이해
- **[기본 제공 스키마 사전](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=ko){target="_blank"}**: 전체 XDM 스키마 참조
- **[Journey Optimizer 보고](report-gs-cja.md)**: Journey Optimizer의 보고 기능 개요

### 통합 안내서 {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: CJA에서 Journey Optimizer 데이터 분석
- **[데이터 관리](../data/export-datasets.md)**: 여정 데이터 내보내기 및 관리
- **[개인 정보 및 거버넌스](../privacy/audit-logs.md)**: 여정 이벤트에 대한 데이터 거버넌스 고려 사항


**다음 단계:**

- [첫 번째 여정 보고서 만들기](sharing-overview.md)(으)로 시작
- 특정 사용 사례에 대해 [쿼리 예제](query-examples.md) 살펴보기
- [여정 관리 모범 사례](../building-journeys/journey.md)에 대해 알아보기
