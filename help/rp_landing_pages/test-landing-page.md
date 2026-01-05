---
solution: Journey Optimizer
product: Journey Optimizer
title: 테스트, 유효성 검사 및 승인
description: Journey Optimizer의 모든 테스트 및 승인 기능을 살펴보십시오. 시작하기 전에 컨텐츠 미리 보기, 여정 시뮬레이션, 이메일 유효성 검사, 실험 실행, 충돌 감지 및 승인 워크플로우 설정.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 테스트, 유효성 검사, 승인, 승인, 품질 보증, qa, 테스트 프로필, 개인화, 렌더링, 스팸 확인, 콘텐츠 실험, a/b 테스트, 충돌 감지, 시드 목록, 증명, 샘플 데이터, 승인 워크플로우, 이메일 테스트, 유효성 검사 워크플로우
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: fb13aee243757de7fe47bdd9d9ebad47069e24ba
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 4%

---

# 테스트, 유효성 검사 및 승인{#section-overview}

이 섹션에서는 Journey Optimizer의 모든 테스트 및 승인 기능을 다룹니다. 테스트 프로필로 콘텐츠를 미리 보고, 여정 논리를 확인하고, 이메일 렌더링 및 스팸 점수를 확인하고, A/B 실험을 실행하고, 충돌을 감지하고, 승인 워크플로를 설정하는 도구를 찾을 수 있습니다.

이 랜딩 페이지는 작성 중인 테스트(캠페인 대 여정)에 따라 올바른 테스트 접근 방식을 선택하고, 권장 테스트 워크플로를 안내하고, 모든 테스트 및 승인 리소스에 대한 빠른 액세스를 제공합니다. 사용 사례에 적용되는 도구를 확인하려면 [테스트 방법을 선택하세요](#choose-your-testing-approach).

## 테스트 기능 개요

**사용 가능한 테스트 형식:**

* 콘텐츠 테스트: [캠페인 테스트](#testing-campaigns), →2}개인화 테스트[를 보내기 전에 메시지 콘텐츠를 미리 보고 확인합니다.](#testing-personalization)
* 여정 논리 테스트: [테스트 여정](#testing-journeys)→ 여정 경로를 통해 고객 진행률을 시뮬레이션합니다.
* 기술 테스트: [기술 유효성 검사](#2-technical-validation)→ 렌더링, 게재 가능성 및 인증 유효성 검사
* 성능 테스트: A/B 실험을 사용하여 콘텐츠 변형 비교 → [콘텐츠 실험](#content-experiments--ab-testing)
* 충돌 테스트: 캠페인 및 여정이 [충돌 검색](#conflict-detection)→ 겹칩니다.
* 승인 테스트: 활성화 → [승인 워크플로](#approval-workflows-for-journeys-and-campaigns)의 구조화된 검토 워크플로

컨텍스트별 **주요 기능:**

| 기능 | 적용 대상 | 채널 제한 사항 | 전제 조건 | 주요 목적 | 설명서 |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [테스트 프로필](../using/content-management/test-profiles.md) | 캠페인, 여정 | 모든 채널 | 테스트 프로필 생성됨 | 개인화된 콘텐츠 미리보기 | [안내서](#testing-campaigns) |
| [샘플 입력 데이터](../test-approve/simulate-sample-input.md) | 캠페인, 여정 | 이메일, SMS, 푸시, 웹, 코드 기반, 인앱, 콘텐츠 카드 | CSV/JSON 파일 | 여러 개인화 변형 테스트 | [안내서](#simulate-content-variations) |
| [테스트 모드](../using/building-journeys/testing-the-journey.md) | 여정 전용 | N/A | 초안 여정, 네임스페이스 구성됨 | 프로필 진행률 시뮬레이션 | [카드](#test-your-journey) |
| [시험 실행](../using/building-journeys/journey-dry-run.md) | 여정 전용 | N/A | 여정 생성됨 | 실행 경로 분석 | [카드](#journey-dry-run) |
| [이메일 렌더링](../using/content-management/rendering.md) | 캠페인, 여정 | 이메일만 | 리트머스 통합 | 클라이언트 간 디스플레이 확인 | [워크플로](#2-technical-validation) |
| [스팸 점수](../using/content-management/spam-report.md) | 캠페인, 여정 | 이메일만 | None | 게재 가능성 유효성 검사 | [워크플로](#2-technical-validation) |
| [시드 목록](../using/configuration/seed-lists.md) | 캠페인, 여정 | 이메일만 | 시드 목록 구성됨 | 관련자 모니터링 | [카드](#seed-lists-for-stakeholder-monitoring) |
| [콘텐츠 실험](../using/content-management/get-started-experiment.md) | 캠페인만 | 모든 채널 | None | A/B 및 multi-armed bandit 테스트 | [카드](#content-experiments--ab-testing) |
| [충돌 검색](../using/conflict-prioritization/conflicts.md) | 캠페인, 여정(제한적) | 모든 채널 | None | 고객 과대 메시지 방지 | [카드](#conflict-detection) |
| [승인 워크플로](../using/test-approve/gs-approval.md) | 캠페인, 여정 | 모든 채널 | 승인 정책이 생성됨 | 구조화된 검토 프로세스 | [카드](#approval-workflows-for-journeys-and-campaigns) |
| [Personalization 플레이그라운드](../using/personalization/personalize.md#playground) | 모두 | 모든 채널 | None | 개인화 구문 학습 및 테스트 | [카드](#personalization-playground) |

**일반적인 테스트 워크플로:**

1. 사전 개발: [개인화 플레이그라운드](#testing-personalization)를 사용하여 구문을 알아보세요.
2. 개발 중: [테스트 프로필](#testing-campaigns)로 미리 보고 [샘플 입력 데이터](#simulate-content-variations)로 확인
3. 시작 전: [기술 테스트 실행](#2-technical-validation)(렌더링, 스팸), [충돌 확인](#conflict-detection), [승인](#approval-workflows-for-journeys-and-campaigns) 제출
4. 시작 후: 실시간 보고서로 모니터링([모니터링 및 문제 해결](#monitoring--troubleshooting) 참조), 결과를 기반으로 반복


## 테스트 및 승인이 중요한 이유

테스트 및 승인 프로세스는 브랜드 평판을 보호하고 캠페인 성공을 보장하는 필수적인 품질 게이트 역할을 합니다. 이것이 중요한 이유입니다.

* **오류가 고객에게 도달하기 전에 오류를 catch** - 수정 사항이 빠르고 위험이 없는 제어된 환경에서 끊어진 링크, 잘못된 개인화, 렌더링 문제 및 논리 결함을 식별합니다.

* **전달성 향상** - 스팸 점수를 테스트하고, 전자 메일 인증을 확인하고, 전자 메일 클라이언트 간의 렌더링을 확인하여 받은 편지함 배치 및 참여 비율을 최대화합니다.

* **브랜드 일관성 보장** - 다양한 테스트 프로필로 콘텐츠를 미리 보고 다양한 고객 세그먼트에 대해 개인화가 올바르게 표시되고 브랜드 표준이 유지되는지 확인합니다.

* **복잡한 여정의 유효성을 검사합니다** - 여러 단계 여정 흐름을 시뮬레이션하여 트리거가 올바르게 실행되고, 조건이 올바르게 평가되며, 고객이 적절한 시간에 올바른 메시지를 수신하는지 확인하십시오.

* **책임 설정** - 이해 당사자의 승인을 필요로 하는 공식 승인 워크플로를 구현하여 명확한 소유권을 만들고 승인되지 않은 캠페인 시작 또는 미숙한 캠페인 시작을 줄입니다.

* **시간 및 리소스 절약** - 수정 사항이 더 저렴하고 빨라져 비용이 많이 드는 출시 후 수정 또는 고객 서비스 에스컬레이션을 방지하는 개발 주기 초기에 문제를 감지합니다.

## 주요 용어

**[테스트 프로필](../using/content-management/test-profiles.md)** = 개인화된 콘텐츠를 미리 보는 데 사용되는 가상 고객 프로필(실제 고객이 아님)입니다. 실시간 고객 프로필 서비스에 플래그가 지정되었습니다. 테스트 모드 및 컨텐츠 미리 보기에 필요합니다. [테스트 프로필을 만드는 방법을 알아봅니다](../using/audience/creating-test-profiles.md)

**[테스트 모드](../using/building-journeys/testing-the-journey.md)** = 여정 경로를 통해 테스트 프로필을 전송하는 여정 시뮬레이션 기능입니다. 제한 사항: 초안 여정 전용, 네임스페이스 필요, 테스트 프로필만 해당. [테스트 모드 설명서 보기](../using/building-journeys/testing-the-journey.md)

**[시험 실행](../using/building-journeys/journey-dry-run.md)** = 메시지를 보내거나 API 호출을 하지 않고 경로를 추적하는 여정 실행 분석 도구입니다. 사용 사례: 리소스를 사용하지 않고 논리를 확인합니다. [시험 실행에 대해 알아보기](../using/building-journeys/journey-dry-run.md)

**[입력 데이터 샘플](../test-approve/simulate-sample-input.md)** = 개인화 테스트를 위한 프로필 속성 값이 들어 있는 CSV 또는 JSON 파일. 최대 30개의 변형을 지원합니다. 테스트 프로필을 만드는 대신 사용할 수 있습니다. [콘텐츠 변형을 시뮬레이션하는 방법](../test-approve/simulate-sample-input.md)

**[시드 목록](../using/configuration/seed-lists.md)** = 내부 관련자의 전자 메일 주소가 실제 게재에 자동으로 포함됩니다(테스트 전송 아님). 이메일 채널만. 사용 사례: 품질 모니터링 및 규정 준수. [시드 목록 구성](../using/configuration/seed-lists.md)

**[콘텐츠 실험](../using/content-management/get-started-experiment.md)** = 콘텐츠 변형을 비교하는 A/B 테스트 또는 multi-armed bandit 실험. 캠페인만 해당되며, 여정에서 사용할 수 없습니다. [실험 시작](../using/content-management/get-started-experiment.md) | [실험 만들기](../using/content-management/content-experiment.md)

**[증명](../using/content-management/proofs.md)** = 테스트 프로필 데이터를 사용하여 특정 이메일 주소로 전송된 테스트 이메일 게재. 시드 목록과 다릅니다(증명은 수동 테스트 전송이며 시드 목록은 자동 이해 관계자 사본). [증명 보내기](../using/content-management/proofs.md)

**[충돌 감지](../using/conflict-prioritization/conflicts.md)** = 동일한 대상을 타깃팅하는 겹치는 캠페인과 여정을 식별하는 도구입니다. 제한된 여정 지원: 단일, 대상 자격 및 대상 읽기 유형만 지원합니다. [충돌 관리에 대해 알아보기](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[승인 워크플로](../using/test-approve/gs-approval.md)** = 활성화하기 전에 관련자 승인이 필요한 다단계 검토 프로세스입니다. 승인 정책 구성이 필요합니다. [승인 설정](../using/test-approve/gs-approval.md) | [정책 만들기](../using/test-approve/approval-policies.md)

**[테스트 렌더링](../using/content-management/rendering.md)** = 이메일 클라이언트(Gmail, Outlook, Apple Mail) 및 장치 간 이메일 표시 유효성 검사 Litmus 통합이 필요합니다. [전자 메일 렌더링 테스트](../using/content-management/rendering.md)

**[Personalization playground](../using/personalization/personalize.md#playground)** = 개인화 구문을 실험하고 샘플 데이터를 사용하여 식을 테스트하는 대화형 학습 환경입니다. 라이브 데이터 세트가 필요하지 않습니다. [플레이그라운드 액세스](../using/personalization/personalize.md#playground)

## 테스트 방법 선택을 위한 의사 결정 트리

이 진단트리를 사용하여 특정 시나리오에 적합한 테스트 도구를 신속하게 식별할 수 있습니다. 컨텍스트에 따라 각 질문에 답변하여 관련 기능 및 설명서로 직접 이동합니다(작성 중인 항목, 유효성 검사가 필요한 항목 및 사용 중인 채널).

+++ **질문 1: 무엇을 테스트하고 있습니까?**

* 캠페인 → [캠페인 테스트](#testing-campaigns)
* 여정 → [여정 테스트](#testing-journeys)
* Personalization 표현식 → [Personalization 플레이그라운드](#testing-personalization)
+++

+++**질문 2: 유효성 검사가 필요한 측면은 무엇입니까?**

* 콘텐츠 및 개인화 → [테스트 프로필](#testing-campaigns) 또는 [샘플 입력 데이터](#simulate-content-variations)
* 전자 메일 표시 → [전자 메일 렌더링 테스트](#2-technical-validation)
* 전달성 → [스팸 점수 확인](#2-technical-validation)
* 여정 논리 및 흐름 → [테스트 모드](#testing-journeys) 또는 [시험 실행](#journey-dry-run)
* 성능 비교 → [콘텐츠 실험](#content-experiments--ab-testing)(캠페인만 해당)
* 시간 충돌 → [충돌 검색](#conflict-detection)
* 관련자 검토 → [승인 워크플로](#approval-workflows-for-journeys-and-campaigns)
+++

+++**질문 3: 채널을 선택하십시오.**

* 전자 메일 → 사용 가능한 모든 테스트 방법([캠페인 테스트](#testing-campaigns) 참조)
* SMS, 푸시 → [콘텐츠 테스트](#testing-campaigns), [샘플 입력 데이터](#simulate-content-variations), [승인 워크플로](#approval-workflows-for-journeys-and-campaigns)
* 웹, 인앱, 코드 기반 → [콘텐츠 테스트](#testing-campaigns), [샘플 입력 데이터](#simulate-content-variations), [승인 워크플로](#approval-workflows-for-journeys-and-campaigns)
* 여러 채널 → 각 채널을 개별적으로 테스트
+++

+++**질문 4: 워크플로에 있을 때?**

* 학습을 위해 →[Personalization 플레이그라운드](#personalization-playground)를 빌드하기 전
* 유효성 검사→ 위해 [테스트 프로필](#testing-campaigns) 및 [샘플 입력 데이터](#simulate-content-variations)를 작성하는 동안
* 시작 전 →[테스트 렌더링](#2-technical-validation), [스팸 확인](#email-spam-report), [충돌 검색](#conflict-detection), [승인](#approval-workflows-for-journeys-and-campaigns)
* 시작 후 →0}실시간 보고서[ 및 ](../using/building-journeys/report-journey.md)모니터링[](#monitoring--troubleshooting)
+++


## 테스트 접근 방식 선택

올바른 테스트 접근 방식은 구축 중인 내용과 유효성 검사에 필요한 사항에 따라 다릅니다. 이 안내서를 사용하여 시나리오와 가장 관련성이 높은 테스트 도구를 식별합니다.

### 캠페인 테스트

**모든 캠페인에 대해:**

* [테스트 프로필](../using/content-management/test-profiles.md) 또는 [샘플 입력 데이터](../test-approve/simulate-sample-input.md)를 사용하여 콘텐츠 미리 보기 및 테스트
* 장치 및 클라이언트에서 [전자 메일 렌더링](../using/content-management/rendering.md) 확인(전자 메일 채널만 해당)
* [스팸 점수 확인](../using/content-management/spam-report.md) 실행(전자 메일 채널만)
* 다른 캠페인 및 여정과의 [충돌](../conflict-prioritization/conflicts.md) 검토
* 관련자 모니터링을 위해 [시드 목록](../configuration/seed-lists.md) 설정(전자 메일 채널만 해당)
* 활성화하기 전에 [승인](../using/test-approve/gs-approval.md)을 제출하세요.

**A/B 테스트 및 최적화를 위한**

* [콘텐츠 실험](../using/content-management/get-started-experiment.md)을 만들어 여러 처리를 테스트하고 성능을 측정합니다.

**API 트리거 캠페인의 경우:**

* 프로그래밍 방식으로 증명 작업을 트리거하려면 [Campaign 시뮬레이션 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}를 사용하십시오.

### 테스트 여정

**모든 여정:**

* [여정 모드](../using/building-journeys/testing-the-journey.md)를 사용하여 프로필 진행률(초안 테스트만 해당, 네임스페이스 필요)을 시뮬레이션하거나 [시험 실행](../using/building-journeys/journey-dry-run.md)을 사용하여 메시지를 보내지 않고 실행 경로를 분석하십시오
* [미리 보기 및 증명](../using/content-management/preview-test.md)을 사용하여 개별 메시지 테스트
* 다른 여정 및 캠페인과의 [충돌](../conflict-prioritization/conflicts.md) 확인
* 게시하기 전에 [승인](../using/test-approve/gs-approval.md)을 제출하세요.

**복잡한 여정의 경우:**

* 테스트 모드 및 시험 실행을 함께 사용하여 분기 논리 및 실행 경로를 철저히 확인합니다
* 다양한 항목 조건 및 프로필 속성을 체계적으로 테스트합니다.

**참고:** 충돌 검색 및 여정 한도는 단일 대상 자격 조건 및 대상 여정 읽기에만 사용할 수 있습니다.

### 개인화 테스트

**콘텐츠를 빌드하기 전:**

* [개인화 플레이그라운드](../using/personalization/personalize.md#playground)에서 테스트하여 샘플 데이터가 있는 구문 및 테스트 표현식을 알아보십시오

**콘텐츠를 만드는 중:**

* 개인화 렌더링을 올바르게 확인하기 위해 [테스트 프로필](../using/content-management/test-profiles.md)(으)로 미리 보기
* CSV/JSON 파일의 [샘플 입력 데이터](../test-approve/simulate-sample-input.md)를 사용하여 여러 시나리오를 테스트합니다(최대 30개의 변형 지원).

## 모범 사례 테스트

테스트 노력의 효과를 극대화하려면 다음 권장 사례를 따르십시오.

1. **일찍 테스트하고 자주 테스트합니다** - 캠페인이 완전히 빌드될 때까지 기다리지 마십시오. 콘텐츠, 개인화 및 논리를 개발하면서 점진적으로 테스트하십시오.

1. **실제 테스트 프로필 사용** - [에지 사례 및 다양한 개인화 시나리오를 포함하여 대상 대상 세그먼트를 정확하게 나타내는 테스트 프로필 만들기](../using/audience/creating-test-profiles.md).

1. **장치 및 클라이언트 간 테스트** - 일관된 표시(전자 메일 채널만)를 위해 인기 있는 전자 메일 클라이언트(Gmail, Outlook, Apple Mail) 및 장치(데스크톱, 모바일, 태블릿)에서 [전자 메일 렌더링](../using/content-management/rendering.md)을 확인합니다.

1. **개인화를 철저히 확인** - 다른 특성 값을 가진 여러 [테스트 프로필](../using/content-management/test-profiles.md)을 사용하여 테스트하여 개인화 토큰이 올바르게 렌더링되고 대체 값이 작동하는지 확인합니다. [개인화 플레이그라운드](../using/personalization/personalize.md#playground)를 사용하여 개인화 표현식과 샘플 데이터로 테스트 코드를 실험한 후 캠페인에 적용하십시오.

1. **샘플 데이터가 있는 콘텐츠 변형을 테스트합니다** - CSV 또는 JSON 파일의 [샘플 입력 데이터](../test-approve/simulate-sample-input.md)를 사용하여 수많은 테스트 프로필을 만들지 않고도 최대 30개의 개인화 시나리오를 테스트하여 시간을 절약하고 포괄적인 적용 범위를 보장합니다. 이메일, SMS, 푸시, 웹, 코드 기반 경험, 인앱 및 콘텐츠 카드 채널을 지원합니다.

1. **관련자 모니터링에 시드 목록 사용** - 품질 모니터링 및 준수 확인을 위해 실행 시 모든 게재 복사본을 받는 내부 관련자를 자동으로 포함하도록 [시드 목록 구성](../configuration/seed-lists.md)(전자 메일 채널만 해당).

1. **여정 경로 시뮬레이션** - 여러 분기가 있는 복잡한 여정의 경우 [테스트 모드](../using/building-journeys/testing-the-journey.md)를 사용하여 다양한 시작 조건 및 프로필 특성을 테스트하여 가능한 모든 경로의 유효성을 검사하십시오. 네임스페이스를 사용하는 초안 여정에 사용할 수 있습니다.

1. **게재 가능성 지표 확인** - 대량 전송 전 [스팸 점수](../using/content-management/spam-report.md), 인증 상태 및 이메일 상태 지표 검토(이메일 채널만 해당).

1. **테스트 결과 문서** - 테스트 결과, 발견된 문제 및 해결 방법을 기록하여 향후 테스트 프로세스를 개선하고 팀과 학습을 공유할 수 있습니다.

1. **이해 당사자를 일찍 참여시키세요** - [정식 승인](../using/test-approve/gs-approval.md) 전에 미리 보기 및 테스트 결과를 이해 당사자와 공유하여 피드백을 수집하고 기대치를 조정합니다.

## 권장 테스트 워크플로우

철저한 테스트와 원활한 승인을 보장하기 위해 다음과 같은 체계적인 접근 방식을 따르십시오.

### &#x200B;1. 콘텐츠 개발 및 미리보기

먼저 콘텐츠를 만들고 미리보기 기능을 사용하여 초기 디자인 및 개인화를 확인합니다.

* [이메일](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [푸시 알림](../using/push/create-push.md) 또는 기타 채널 콘텐츠 디자인

* **[콘텐츠 시뮬레이션](../using/content-management/preview-test.md)** 기능을 사용하여 테스트 프로필로 미리 보기

* [개인화 토큰](../using/personalization/personalization-syntax.md), 다이내믹 콘텐츠 및 대체 값 확인

* **[개인화 플레이그라운드](../using/personalization/personalize.md#playground)**&#x200B;에서 개인화 표현식을 실험하여 라이브 콘텐츠에 적용하기 전에 샘플 데이터로 코드를 테스트하고 세분화합니다

* CSV/JSON 파일의 **[샘플 입력 데이터](../test-approve/simulate-sample-input.md)**&#x200B;를 사용하여 여러 변형을 테스트하여 다양한 프로필 시나리오에서 개인화의 유효성을 검사합니다.

* 다양한 화면 크기 및 전자 메일 클라이언트에서 [렌더링](../using/content-management/rendering.md) 확인

### &#x200B;2. 기술 검증

전달성 및 기능에 영향을 주는 기술적 측면의 유효성 검사:

* [스팸 점수 확인](../using/content-management/spam-report.md)을 실행하여 잠재적인 게재 가능성 문제를 식별하십시오.

* 링크가 손상되지 않고 제대로 추적되는지 테스트합니다.

* [전자 메일 인증](../using/configuration/dmarc-record.md)(SPF, DKIM, DMARC) 구성 유효성 검사

* HTML 렌더링 검토 및 CSS 호환성 문제 확인

* 모바일 및 데스크톱 장치에서 [응답형 디자인](../using/email/content-from-scratch.md) 테스트

* 고객 메시지 피로도 및 시간 문제를 방지하기 위해 다른 캠페인 및 여정과 [잠재적 충돌](../conflict-prioritization/conflicts.md)을 확인합니다.

### &#x200B;3. 여정 테스트(여정 전용)

여정을 테스트하는 경우 오케스트레이션 논리의 유효성을 검사합니다.

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

| 사용 사례 | 학습 내용 | 주요 테스트 포커스 |
|----------|-------------------|-------------------|
| **[다중 채널 메시지 보내기](../using/building-journeys/journeys-uc.md)** | 대상자 읽기, 반응 이벤트 및 이메일/푸시 메시지를 결합하는 여정을 테스트합니다. 대상 타기팅에서 메시지 게재까지의 전체 흐름을 확인합니다. | 멀티채널 조정, 반응 이벤트, 엔드 투 엔드 플로우 유효성 검사, 테스트 및 게시 단계 |
| **[구독자에게 메시지 보내기](../using/building-journeys/message-to-subscribers-uc.md)** | 동적 이메일 주소 지정으로 구독 목록을 타겟팅하는 여정을 테스트합니다. 올바른 구독자 타겟팅을 위해 개인화 표현식의 유효성을 검사합니다. | Personalization 표현식, 동적 주소 지정, 구독 목록 타기팅 |
| **[시간 제한 메시지 보내기](../using/building-journeys/weekday-email-uc.md)** | 특정 날짜에 메시지가 전송되도록 시간 기반 조건으로 여정을 테스트합니다. 대기 활동 및 예약 논리의 유효성을 검사합니다. | 시간 기반 조건, 대기 활동, 유효성 검사 예약 |
| **[더 많은 여정 사용 사례 살펴보기](../using/building-journeys/jo-use-cases.md)** | 경험 이벤트, 다중 채널 메시징 및 외부 시스템 통합에 대한 포괄적인 실제 예제 컬렉션에 액세스합니다. | 다양한 시나리오, 고급 패턴, 통합 테스트 |

## 콘텐츠 테스트 및 승인

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

콘텐츠 미리 보기, 테스트 및 유효성 검사

테스트 프로필, 이메일 렌더링 테스트, 스팸 점수 평가 등을 사용하여 개인화된 콘텐츠를 미리 보고, 테스트하며, 확인하는 방법을 알아봅니다.

[콘텐츠 미리 보기 및 테스트 살펴보기](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

여정과 캠페인을 위한 승인 워크플로우

여정과 캠페인의 품질 관리를 보장하기 위해 승인 프로세스를 설정, 관리 및 실행하는 방법을 이해합니다.

[승인 워크플로우에 대해 알아보기](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

여정 테스트

여정, 조건 및 작업이 예상대로 작동하는지 확인하기 위해 특정 프로필을 사용하여 테스트하여 게시하기 전에 이벤트의 유효성을 검사합니다. 네임스페이스를 사용하는 초안 여정에 사용할 수 있습니다.

[여정 테스트](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

여정 시험 실행

시험 실행을 통해 여정의 실행 경로를 시뮬레이션하고 확인하여 실제로 실행하기 전에 잠재적 문제를 식별합니다.

[시험 실행에 대해 알아보기](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

모니터링 및 문제 해결

포괄적인 문제 해결 리소스, 시스템 경고, 오류 코드에 액세스하여 여정 실행 및 성능 문제를 해결할 수 있습니다.

[모니터링 및 문제 해결 보기](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization 플레이그라운드

안전한 환경에서 개인화 표현식을 실험해 보십시오. 캠페인 및 여정에 적용하기 전에 샘플 데이터로 코드를 테스트하고 결과를 미리 봅니다.

[Personalization 플레이그라운드에 대해 알아보기](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

콘텐츠 실험 및 A/B 테스트

여러 콘텐츠 변형을 테스트하고 성능을 측정하여 최상의 성과를 내는 처리를 식별하여 캠페인을 최적화합니다. 캠페인에만 사용할 수 있습니다(A/B 및 multi-armed bandit 실험 지원).

[콘텐츠 실험에 대해 알아보기](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

관련자 모니터링을 위한 시드 목록

게재에 내부 관련자 주소를 자동으로 포함시켜 품질 보증 및 규정 준수를 위해 고객에게 전송된 실제 메시지를 모니터링합니다. 이메일 채널에만 사용할 수 있습니다.

[시드 목록 구성](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

충돌 감지

캠페인과 여정 간의 잠재적 중복을 식별하여 동시 커뮤니케이션이 너무 많은 압도적인 고객을 방지합니다. 캠페인 및 단일, 대상 검증, 대상 읽기 여정에 사용할 수 있습니다.

[충돌 감지](../using/conflict-prioritization/conflicts.md)
:::

::::

## 추가 리소스

### 필수 테스트 및 유효성 검사 가이드

* [콘텐츠 변형 시뮬레이션](../test-approve/simulate-sample-input.md) - CSV 또는 JSON 파일을 사용하여 최대 30개의 개인화 시나리오를 테스트합니다. 여러 테스트 프로필을 만들지 않고 다국어 콘텐츠 테스트에 이상적입니다. 이메일, SMS, 푸시, 웹, 코드 기반, 인앱 및 콘텐츠 카드를 지원합니다.

* [테스트 프로필 만들기](../using/audience/creating-test-profiles.md) - 테스트 프로필을 만들고 관리하여 고객 시나리오를 시뮬레이션합니다. 프로필에 테스트를 플래그 지정하고, 속성을 설정하고 테스트 세그먼트를 구성하는 방법을 알아봅니다.

* [전자 메일 스팸 보고서](../using/content-management/spam-report.md) - 보내기 전에 스팸 점수를 확인하여 배달 가능성 및 받은 편지함 배치를 개선합니다. 콘텐츠 최적화를 위한 실행 가능한 권장 사항을 얻을 수 있습니다.

* [여정 FAQ](../using/building-journeys/journey-faq.md) - 여정 테스트, 실행 및 문제 해결에 대한 일반적인 질문에 대한 빠른 참조입니다.

### 종속성 및 관계

테스트 기능이 서로 및 광범위한 Journey Optimizer 워크플로우와 연결되는 방식을 이해합니다. 이 섹션에서는 사전 요구 사항, 업스트림/다운스트림 종속성 및 공통 기능 조합을 매핑합니다.

+++**필수 구성 요소(테스트하기 전에 필요)**

* 테스트 모드 또는 콘텐츠 미리보기를 사용하기 전에 테스트 프로필을 만들어야 합니다.
* 승인을 위해 제출하기 전에 승인 정책을 구성해야 합니다.
* 캠페인/여정에 추가하기 전에 시드 목록을 만들어야 합니다.
* 이메일 렌더링 테스트에 필요한 Litmus 통합
* 테스트 모드를 사용하려면 여정이 초안 상태여야 합니다.
* 여정은 테스트 모드를 사용하도록 구성된 네임스페이스가 있어야 합니다.

+++

+++**테스트가 종속되는 사항(업스트림)**

* 콘텐츠 만들기: 테스트할 캠페인 또는 여정 필요
* 테스트 프로필: 테스트 모드 및 컨텐츠 미리 보기에 필요
* 승인 정책: 승인 워크플로에 필요
* 구성: 채널 구성, 이메일 인증, 도메인 설정

+++

+++**테스트에 따라 달라지는 사항(다운스트림)**

* 캠페인/여정 활성화: 오류를 해결하지 않으면 활성화할 수 없습니다.
* 게시: 게시 전에 승인이 필요할 수 있습니다.
* 라이브 모니터링: 출시 후 모니터링 및 보고
* 최적화: 테스트 결과를 사용하여 향후 캠페인 구체화

+++

+++**관련 기능**

* 테스트 + 승인 워크플로우 = 품질 보증 프로세스
* 테스트 + 충돌 감지 = 고객 과대 메시지 방지
* 테스트 + 콘텐츠 실험 = 성능 최적화
* 테스트 + 보고 = 지속적인 개선 주기
* 테스트 프로필 + Personalization = 컨텐츠 유효성 검사
* 시험 실행 + 여정 모드 = 포괄적인 테스트 유효성 검사

+++

+++**일반적인 기능 조합**

* 컨텐츠 테스트: 테스트 프로필 + 샘플 입력 데이터 + Personalization 플레이그라운드
* 이메일 유효성 검사: 테스트 렌더링 + 스팸 점수 + 테스트 프로필 + 증명
* 여정 유효성 검사: 테스트 모드 + 시험 실행 + 테스트 프로필
* 출시 전 확인 목록: 모든 기술 테스트 + 충돌 감지 + 승인 워크플로

+++

### 일반적인 질문

+++**Q: 캠페인을 시작하기 전에 필요한 테스트는 무엇입니까?**

**최소:** 테스트 프로필 + 스팸 점수 확인(이메일)이 포함된 콘텐츠 미리 보기
**권장:** + 전자 메일 렌더링 + 충돌 감지 + 승인 워크플로
**모범 사례:** + 샘플 입력 데이터 테스트 + 시드 목록 + A/B 실험(최적화하는 경우)

+++

+++**Q: 테스트 프로필을 많이 만들지 않고 개인화를 테스트하려면 어떻게 합니까?**

**기본 솔루션:** CSV/JSON 파일과 함께 [샘플 입력 데이터 사용](../test-approve/simulate-sample-input.md)(최대 30개의 변형 지원)
**대체 요소:** 주요 세그먼트를 다루는 3~5개의 대표 [테스트 프로필](../using/audience/creating-test-profiles.md) 만들기
**학습 도구:** [개인화 플레이그라운드](../using/personalization/personalize.md#playground)에서 먼저 실험

+++

+++**Q: 여정의 테스트 모드와 시험 실행 간의 차이점은 무엇입니까?**

**테스트 모드:** 여정을 통해 테스트 프로필을 보내고 실제 작업을 트리거하며 테스트 메시지를 생성합니다. 초안 여정 + 네임스페이스가 필요합니다.
**시험 실행:** 아무것도 보내지 않고 실행 경로를 추적합니다. 모든 여정 상태에서 작동합니다. 보낸 메시지가 없고 실행된 액션이 없습니다.
**함께 사용:** 메시지 테스트를 위한 테스트 모드 + 논리 유효성 검사를 위한 시험 실행 = 포괄적인 적용 범위.

+++

+++**Q: 프로덕션/라이브 상태에서 여정을 테스트할 수 있습니까?**

**테스트 모드:** 아니요 - 초안 여정 전용
**시험 실행:** 예 - 모든 여정 상태에서 작동합니다.
**콘텐츠 미리 보기:** 예 - 언제든지 개별 메시지 미리 보기
**해결 방법:** 전체 여정 모드 유효성 검사를 위해 라이브 테스트를 초안으로 복제

+++

+++**Q: 외부 통합이 필요한 테스트 기능은 무엇입니까?**

**전자 메일 렌더링:** Litmus 통합(별도의 라이선스)이 필요합니다.
**다른 모든 기능:** Journey Optimizer에 내장되어 있으며 추가 통합이 필요하지 않습니다.
**참고:** 테스트 프로필에는 실시간 고객 프로필 서비스(포함)가 필요합니다.

+++

+++**Q: API 트리거 캠페인을 테스트하려면 어떻게 합니까?**

**옵션 1:** 프로그래밍 테스트에 [Campaign 시뮬레이션 API 사용](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}
**옵션 2:** UI에서 테스트 프로필로 콘텐츠 미리 보기
**옵션 3:** 테스트 전자 메일 주소로 증명 보내기
**모범 사례:** 포괄적인 유효성 검사를 위해 세 가지 모두를 결합

+++


### 관련 항목

* [콘텐츠 관리](content-management-landing-page.md) - 템플릿, 조각 및 전자 메일 Designer을 사용하여 콘텐츠를 디자인하고 미리 보고 관리하는 방법에 대해 알아봅니다. 일관된 브랜딩을 위한 기본 콘텐츠 생성 모범 사례

* [보고 및 분석](reporting-landing-page.md) - 포괄적인 보고서, 대시보드 및 지표를 사용하여 캠페인 및 여정 성과를 분석합니다. 데이터 중심의 의사 결정을 내려 고객 경험을 최적화합니다.

* [여정 구성](configure-journeys-landing-page.md) - 정교한 여정 오케스트레이션을 사용하도록 데이터 원본, 이벤트 및 사용자 지정 작업을 구성합니다. 여정 생성을 위한 기술적 토대를 설정합니다.

* [캠페인 관리](../using/campaigns/get-started-with-campaigns.md) - 다양한 캠페인 유형을 탐색하고 최대의 효과를 위해 일괄 처리 및 실시간 캠페인을 만들고, 예약하고, 최적화하는 방법을 알아봅니다.
