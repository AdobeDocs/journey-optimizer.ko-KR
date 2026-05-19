---
solution: Journey Optimizer
product: journey optimizer
title: 주요 용어
description: Adobe Journey Optimizer의 필수 용어 및 개념
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56id: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: d92b3c8475020b26a3f154b322374a05f7d41f29
workflow-type: tm+mt
source-wordcount: 1573
ht-degree: 7%

---

# 주요 용어 {#key-terminology}

이 참조 안내서는 Adobe Journey Optimizer을 사용할 때 접하게 되는 필수 용어를 정의합니다. 이러한 개념을 이해하면 자신 있게 플랫폼을 탐색하고 팀과 효과적으로 공동 작업을 수행할 수 있습니다.

**의사 결정과 의사 결정 관리** 또는 **콘텐츠 카드와 인앱 메시지**&#x200B;와 같이 종종 혼동되는 유사한 소리 용어 쌍에 대해서는 이 페이지 하단의 [용어가 비슷해 보이는 경우](#disambiguation)를 참조하십시오.

>[!NOTE]
>
>Adobe Journey Optimizer은 **Adobe Experience Platform**&#x200B;을 기반으로 빌드되었습니다. 실시간 고객 프로필, 샌드박스, 스키마 및 데이터 세트와 같이 사용자가 접할 수 있는 많은 기본 개념은 Journey Optimizer 관련 개념이 아닌 Adobe Experience Platform 개념입니다. 이러한 용어에 대한 정의는 [Adobe Experience Platform 용어집](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}을 참조하세요.

## 여정 및 캠페인 용어 {#journey-campaign-terms}

| 용어 | 정의 |
|------|------------|
| **여정** | 시간이 지남에 따라 브랜드를 사용한 경험을 고객에게 안내하는 일련의 연결된 단계입니다. 각 단계는 고객 작업 또는 시간 트리거를 기반으로 발생하며 순차적인 개인화된 상호 작용을 가능하게 합니다. [자세히 알아보기](../building-journeys/journey.md) |
| **Campaign** | 하나 이상의 채널에서 특정 대상에게 콘텐츠를 전달하는 조정된 마케팅 작업입니다. 캠페인은 여정과 달리 작업을 동시에 실행합니다. Journey Optimizer은 다음 세 가지 캠페인 유형을 지원합니다. **작업 캠페인**(예약된 일괄 전송), **API 트리거 캠페인**(API를 통한 실시간 이벤트 기반 메시징) 및 **오케스트레이션된 캠페인**(시각적 캔버스를 사용하는 복잡한 다단계 워크플로우). [자세히 알아보기](../campaigns/get-started-with-campaigns.md) |
| **이벤트** | 여정을 트리거하거나 전달하는 작업 또는 발생 횟수입니다. 이벤트는 고객 작업(구매, 장바구니 포기) 또는 시스템 이벤트(날짜/시간, 데이터 변경)일 수 있습니다. [자세히 알아보기](../event/about-events.md) |
| **채널** | 고객과 통신하는 데 사용되는 방법: 이메일, SMS, 푸시 알림, 인앱 메시지, 웹 또는 DM. 각 채널에는 특정 구성이 필요합니다. [자세히 알아보기](../configuration/get-started-configuration.md) |

## 고객 및 대상 약관 {#customer-audience-terms}

| 용어 | 정의 |
|------|------------|
| **대상자** | &quot;최근 30일 동안 구매한 고객&quot; 또는 &quot;충성도 프로그램 회원&quot;과 같이 일반적인 특성이나 행동을 공유하는 고객 그룹입니다. 대상은 특정 고객 세그먼트를 타깃팅하는 데 사용됩니다. [자세히 알아보기](../audience/about-audiences.md) |
| **대상 자격** | 고객이 대상을 참여하거나 탈퇴할 때 발생하는 자동 프로세스입니다. Journey Optimizer은 누군가가 대상자를 들어오거나 나갈 때 작업을 트리거하여 시기적절하고 적절한 커뮤니케이션을 보장할 수 있습니다. [자세히 알아보기](../building-journeys/audience-qualification-events.md) |
| **참여 가능한 대상** | 라이선스 계약에 따라 Adobe Journey Optimizer을 통해 적극적으로 연락할 수 있는 고객 프로필 수입니다. 이는 일반적으로 지난 12개월 내에 관여한 프로필을 나타냅니다. |
| **테스트 프로필** | 실제 고객에게 보내기 전에 메시지를 테스트하고 미리 보는 데 사용되는 가상 프로필입니다. 테스트 프로필은 개인화, 콘텐츠 및 여정 논리를 확인하는 데 도움이 됩니다. [자세히 알아보기](../audience/creating-test-profiles.md) |

## 콘텐츠 및 개인화 용어 {#content-terms}

| 용어 | 정의 |
|------|------------|
| **개인화** | 프로필 데이터, 환경 설정 및 비헤이비어를 사용하여 개별 고객에게 콘텐츠를 맞춤화하는 프로세스입니다. 예를 들어 고객의 이름을 삽입하거나 검색 기록을 기반으로 제품 추천을 표시할 수 있습니다. [자세히 알아보기](../personalization/personalize.md) |
| **콘텐츠 템플릿** | 여러 캠페인 및 여정에서 브랜드 일관성을 유지하고 컨텐츠 생성을 가속화하는 데 사용할 수 있는 재사용 가능한 메시지 디자인입니다. [자세히 알아보기](../content-management/content-templates.md) |
| **조각** | 일관성을 보장하고 중앙 집중식 업데이트를 가능하게 하기 위해 여러 메시지에서 사용할 수 있는 재사용 가능한 콘텐츠 블록(예: 머리글, 바닥글 또는 홍보 배너). [자세히 알아보기](../content-management/fragments.md) |
| **랜딩 페이지** | 고객이 커뮤니케이션에서 옵트인 또는 옵트아웃하거나, 서비스에 가입하거나, 온라인 양식을 통해 정보를 제공할 수 있는 독립 실행형 웹 페이지입니다. [자세히 알아보기](../landing-pages/get-started-lp.md) |
| **콘텐츠 실험** | 대상을 무작위 그룹으로 분할하고 다양한 메시지 변형(콘텐츠, 제목 줄 또는 오퍼)을 각 그룹에 전달한 다음, 정의된 성공 지표를 기반으로 최상의 성과를 보이는 변형을 식별하는 A/B 테스트 프레임워크입니다. [자세히 알아보기](../content-management/get-started-experiment.md) |
| **실험** | 의사 결정 테스트 및 최적화를 위한 Journey Optimizer의 광범위한 기능: 콘텐츠 실험은 캠페인 및 여정의 메시지 변형을 테스트하는 동시에 의사 결정 실험 테스트는 선택 전략을 제공합니다. 두 가지 모두 통계적 분석을 사용하여 우수성이 검증된 접근 방식을 식별합니다. [자세히 알아보기](../content-management/get-started-experiment.md) |

## 의사 결정 및 오퍼 조건 {#decision-terms}

| 용어 | 정의 |
|------|------------|
| **의사 결정** | 새로운 구현에 권장되는 Journey Optimizer의 현재 세대 의사 결정 프레임워크 스키마 기반 항목 카탈로그 관리, 유연한 수집 규칙, 재사용 가능한 의사 결정 구성 요소 및 실험 기능을 제공합니다. 코드 기반 경험, 푸시, SMS 및 이메일에 사용 가능(제한된 가용성). [자세히 알아보기](../experience-decisioning/gs-experience-decisioning.md) |
| **의사 결정 관리** | Journey Optimizer의 레거시 offer decisioning 기능. 마케팅 오퍼의 중앙 라이브러리와 실시간 고객 프로필에 제한을 적용하는 규칙 기반 의사 결정 엔진을 사용합니다. 기존 구현에 대해 여전히 지원되지만, 새로운 구현은 대신 Decisioning을 사용해야 합니다. 이메일, 인앱, 푸시, SMS 및 DM을 지원합니다. [자세히 알아보기](../offers/get-started/starting-offer-decisioning.md) |
| **오퍼** | 고객에게 제공할 수 있는 마케팅 메시지, 할인 또는 프로모션. 오퍼에는 오퍼를 받을 수 있는 고객을 결정하는 자격 규칙이 포함됩니다. [자세히 알아보기](../offers/offer-library/creating-personalized-offers.md) |
| **결정 정책** | 자격 조건, 우선 순위 및 한도 규칙과 같은 제약 조건을 기반으로 어떤 시간에 어떤 고객에게 어떤 오퍼를 표시할지 결정하는 규칙 및 전략 세트입니다. [자세히 알아보기](../experience-decisioning/create-decision.md) |

## 데이터 및 구성 용어 {#data-config-terms}

| 용어 | 정의 |
|------|------------|
| **채널 구성** | 보낸 사람 세부 정보, 하위 도메인, IP 풀 및 메시지 유형(마케팅 또는 트랜잭션)을 포함하여 특정 채널에 대해 메시지를 배달하는 방법을 정의하는 설정입니다. 이전 설명서에서는 &quot;표면&quot; 또는 &quot;사전 설정&quot;이라고 했습니다. [자세히 알아보기](../configuration/channel-surfaces.md) |
| **금지 목록** | 하드 바운스, 스팸 불만 또는 수동 추가로 인해 메시지 게재에서 자동으로 제외되는 이메일 주소 및 도메인 목록입니다. 숨겨진 주소로 보내는 것은 전달성과 발신자의 평판을 보호하기 위해 차단됩니다. [자세히 알아보기](../reports/suppression-list.md) |

## 충돌 및 우선 순위 지정 용어 {#conflict-terms}

| 용어 | 정의 |
|------|------------|
| **규칙 집합** | 메시징 동작을 제어하기 위해 여정 및 캠페인에 적용되는 비즈니스 규칙의 명명된 그룹입니다. 규칙 세트는 빈도 제한, 여정 시작 제한 및 중지 시간을 하나의 재사용 가능한 정책으로 결합할 수 있습니다. [자세히 알아보기](../conflict-prioritization/rule-sets.md) |
| **빈도 제한** | 채널 또는 통신 유형(판매, 프로모션 등)별로 지정된 기간 내에 프로필에서 받을 수 있는 메시지 수를 제한하는 규칙 세트 내의 규칙입니다. 한도를 초과하는 프로필은 자동으로 게재에서 제외됩니다. [자세히 알아보기](../conflict-prioritization/channel-capping.md) |

## 용어가 비슷할 때: 명확화 안내서 {#disambiguation}

Adobe Journey Optimizer은 몇 년에 걸쳐 성장했으며, 이는 일부 기능 영역이 유사한 이름을 공유한다는 것을 의미합니다. 아래 표를 사용하여 요구 사항에 맞는 기능을 신속하게 파악할 수 있습니다.

### 의사 결정과 의사 결정 관리 비교 {#decisioning-vs-dm}

두 기능 모두 오퍼를 선택하고 제공하지만 제품 라이프사이클의 여러 단계를 제공합니다.

| | 결정 | 의사 결정 관리 |
|---|---|---|
| **상태** | 현재 — 모든 새로운 구현에 권장됨 | **레거시** — 계속 지원되지만 새 구현에는 더 이상 권장되지 않습니다. |
| **항목 카탈로그** | 스키마 기반, 유연한 메타데이터 | 중앙 집중식 오퍼 라이브러리 |
| **지원되는 채널** | 코드 기반 경험, 푸시, SMS, 이메일(제한된 가용성) | 이메일, 인앱, 푸시, SMS, DM |
| **주요 차별화 요소** | 재사용 가능한 의사 결정 구성 요소, 실험, 광범위한 채널 로드맵 | 검증된 제약 조건 엔진, 새로운 프로젝트를 위한 의사 결정 (Decisioning) 으로의 마이그레이션 |
| **시작** | [의사 결정](../experience-decisioning/gs-experience-decisioning.md) | [의사 결정 관리](../offers/get-started/starting-offer-decisioning.md) |

현재 [의사 결정 관리]를 사용 중인데 전환하려면 [마이그레이션 안내서](../experience-decisioning/migrate-to-decisioning.md)를 참조하세요.

### 캠페인 유형 {#campaign-types-disambiguation}

Journey Optimizer에서는 다르게 활성화되고 고유한 사용 사례를 제공하는 세 가지 캠페인 유형을 제공합니다.

| | 작업 캠페인(예약된 캠페인) | API로 트리거되는 캠페인 | 오케스트레이션된 캠페인 |
|---|---|---|---|
| **활성화** | 수동 또는 예약됨 | 외부 API 호출 | 시각적 워크플로우 캔버스 |
| **추천 항목** | 일회성 또는 반복 배치 전송(뉴스레터, 프로모션) | 실시간 이벤트 기반 메시징(주문 확인, 암호 재설정) | 복잡한 여러 단계로 구성된 크로스 채널 프로그램 |
| **Personalization 소스** | 프로필 속성 | 프로필 속성 + API 페이로드 컨텍스트 | 프로필 속성 + 관계형 데이터 |
| **시작** | [액션 캠페인](../campaigns/create-campaign.md) | [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md) | [오케스트레이션된 캠페인](../orchestrated/gs-orchestrated-campaigns.md) |

모든 캠페인 유형에 대한 전체 개요와 각 캠페인 유형을 사용할 시기는 [캠페인 시작](../campaigns/get-started-with-campaigns.md)을 참조하세요.

### 빈도 제한 대 여정 중재 {#capping-vs-arbitration}

둘 다 충돌 및 우선 순위 지정 도구 세트 아래의 규칙 세트 메커니즘이지만 서로 다른 문제를 해결합니다.

| | 빈도 상한 설정 | 여정 중재 |
|---|---|---|
| **문제 해결** | 프로필에서 시간이 지남에 따라 너무 많은 메시지를 수신함 | 한 프로필이 여러 여정을 동시에 수행할 수 있습니다. |
| **범위** | 채널 및 커뮤니케이션 유형별 (판매, 프로모션 등) | 여정 등록 — 동시 여정 수 또는 우승한 여정 |
| **메커니즘** | 기간당 메시지 수를 제한합니다. 과도하게 요청된 프로필을 자동으로 제외합니다. | 우선 순위 점수 및 최대 가용량 규칙을 사용하여 프로필이 입력하는 여정 결정 |
| **구성 위치** | 규칙 집합 → 빈도 제한 | 규칙 세트 → 여정 한도 및 중재 |
| **자세히 알아보기** | [채널별 빈도 제한 설정](../conflict-prioritization/channel-capping.md) | [여정 한도 및 중재 관리](../conflict-prioritization/journey-capping.md) |

### 콘텐츠 카드와 인앱 메시지 비교 {#content-cards-vs-in-app}

두 채널 모두 모바일 또는 웹 애플리케이션 내에서 메시지를 전달하지만 렌더링 모델과 지속성 동작이 다릅니다.

| | 콘텐츠 카드 | 인앱 메시지 |
|---|---|---|
| **디스플레이 모델** | 앱 UI에 포함된 영구 카드(피드, 받은 편지함 또는 사용자 지정 표면) | 앱 상단에 표시되는 임시 오버레이, 배너 또는 모달 |
| **지속성** | 명시적으로 해제되거나 만료될 때까지 표시 | 사용자가 상호 작용하거나 닫으면 사라짐 |
| **트리거** | SDK이 로드되면 렌더링됩니다. 규칙은 표시 및 해제를 제어합니다. | 여정 또는 캠페인 트리거 게재의 실시간 이벤트 |
| **추천 항목** | 진행 중인 프로모션, 충성도 상태, 지속적인 경고 | 온보딩 팁, 제한 시간 오퍼, 임시 알림 |
| **시작** | [콘텐츠 카드](../content-card/create-content-card.md) | [인앱 메시지](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer과 Journey Optimizer B2B edition 비교:** 동일한 브랜드 제품군에 있는 두 개의 개별 제품입니다. Adobe Journey Optimizer(이 설명서)는 B2C 고객 여정을 타깃팅합니다. Journey Optimizer B2B edition은 계정 기반 마케팅을 위해 특별히 빌드되었으며 구매 그룹 및 계정 대상과 함께 사용됩니다. B2B edition 설명서를 찾으려면 [Journey Optimizer B2B edition 안내서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}를 방문하십시오.

## 관련 항목 {#related-topics}

* [Journey Optimizer 작동 방식 이해](understanding-ajo.md) - 제품 아키텍처에서 여정, 캠페인, 프로필 및 채널이 어떻게 서로 결합되는지 확인합니다.
* [의사 결정 기능 시작](../experience-decisioning/gs-decision.md) - 의사 결정 및 의사 결정 관리를 나란히 비교하고 구현에 적합한 접근 방식을 선택합니다.
* [여정 시작](../building-journeys/journey.md) - 이벤트가 트리거된 순차적 고객 경험을 빌드하는 방법을 단계별로 알아봅니다.
* [캠페인 시작](../campaigns/get-started-with-campaigns.md) - 세 가지 캠페인 유형(액션, API 트리거, 오케스트레이션)과 각 캠페인을 사용할 시기를 이해합니다.
* [충돌 관리 및 우선 순위 지정](../conflict-prioritization/gs-conflict-prioritization.md) - 규칙 집합, 빈도 제한, 우선 순위 점수 및 자동 체류 시간을 사용하여 과도한 메시징을 방지하는 방법을 알아봅니다.
* [통신 채널 시작](../channels/gs-channels.md) - 사용 가능한 모든 채널, 사전 요구 사항 및 구성 방법을 찾아봅니다.
