---
solution: Journey Optimizer
product: journey optimizer
title: 주요 용어
description: Adobe Journey Optimizer의 필수 용어 및 개념
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 9%

---

# 주요 용어 {#key-terminology}

이 참조 안내서는 Adobe Journey Optimizer을 사용할 때 접하게 되는 필수 용어를 정의합니다. 이러한 개념을 이해하면 자신 있게 플랫폼을 탐색하고 팀과 효과적으로 공동 작업을 수행할 수 있습니다.

>[!TIP]
>
>기능 및 워크플로에 대한 자세한 설명은 이 안내서 전체에 연결된 특정 설명서 섹션을 참조하십시오.

## 핵심 플랫폼 약관 {#core-terms}

| 용어 | 정의 |
|------|------------|
| **Adobe Journey Optimizer** | 여러 채널(이메일, SMS, 푸시 알림, 웹)에서 고객에게 개인화된 메시지를 만들고 게재하기 위한 애플리케이션입니다. 실시간 고객 행동에 대응하는 고객 여정을 디자인할 수 있습니다. |
| **Adobe Experience Platform** | 모든 고객 데이터를 한 곳에서 수집하고 구성하는 Adobe Journey Optimizer의 기반. Journey Optimizer이 개인화에 사용하는 통합 고객 프로필을 만듭니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=ko){target="_blank"} |
| **실시간 고객 프로필** | 온라인, 오프라인, CRM 및 서드파티 데이터를 비롯한 여러 채널의 데이터를 결합하는 각 고객에 대한 통합된 실시간 보기입니다. 고객이 브랜드와 상호 작용할 때 각 프로필은 동적으로 업데이트됩니다. [자세히 알아보기](../audience/get-started-profiles.md) |
| **샌드박스** | 라이브 고객 커뮤니케이션에 영향을 주지 않고 테스트 및 실험을 위한 별도의 작업 영역입니다. Adobe Journey Optimizer은 개발, 테스트 및 프로덕션 환경을 위한 여러 샌드박스를 제공합니다. [자세히 알아보기](../administration/sandboxes.md) |

## 여정 및 캠페인 약관 {#journey-campaign-terms}

| 용어 | 정의 |
|------|------------|
| **여정** | 시간이 지남에 따라 브랜드를 사용한 경험을 고객에게 안내하는 일련의 연결된 단계입니다. 각 단계는 고객 작업 또는 시간 트리거를 기반으로 발생하며 순차적인 개인화된 상호 작용을 가능하게 합니다. [자세히 알아보기](../building-journeys/journey.md) |
| **Campaign** | 특정 대상에게 전송된 단일 커뮤니케이션 또는 커뮤니케이션 세트입니다. 시간이 지남에 따라 전개되는 여정과 달리, 캠페인은 즉시 또는 특정 시간에 예약이나 트리거에 따라 메시지를 전달합니다. [자세히 알아보기](../campaigns/get-started-with-campaigns.md) |
| **이벤트** | 여정을 트리거하거나 전달하는 작업 또는 발생 횟수입니다. 이벤트는 고객 작업(구매, 장바구니 포기) 또는 시스템 이벤트(날짜/시간, 데이터 변경)일 수 있습니다. [자세히 알아보기](../event/about-events.md) |
| **채널** | 고객과 통신하는 데 사용되는 방법: 이메일, SMS, 푸시 알림, 인앱 메시지, 웹 또는 DM. 각 채널에는 특정 구성이 필요합니다. [자세히 알아보기](../configuration/get-started-configuration.md) |

## 고객 및 대상 약관 {#customer-audience-terms}

| 용어 | 정의 |
|------|------------|
| **대상자** | &quot;최근 30일 동안 구매한 고객&quot; 또는 &quot;충성도 프로그램 회원&quot;과 같이 일반적인 특성이나 행동을 공유하는 고객 그룹입니다. 대상은 특정 고객 세그먼트를 타깃팅하는 데 사용됩니다. [자세히 알아보기](../audience/about-audiences.md) |
| **대상 자격** | 고객이 대상을 참여하거나 탈퇴할 때 발생하는 자동 프로세스입니다. Journey Optimizer은 누군가가 대상자를 들어오거나 나갈 때 작업을 트리거하여 시기적절하고 적절한 커뮤니케이션을 보장할 수 있습니다. [자세히 알아보기](../building-journeys/audience-qualification-events.md) |
| **참여 가능한 대상** | 라이선스 계약에 따라 Adobe Journey Optimizer을 통해 적극적으로 연락할 수 있는 고객 프로필 수입니다. 이는 일반적으로 지난 12개월 내에 관여한 프로필을 나타냅니다. |
| **테스트 프로필** | 실제 고객에게 보내기 전에 메시지를 테스트하고 미리 보는 데 사용되는 가상 프로필입니다. 테스트 프로필은 개인화, 콘텐츠 및 여정 논리를 확인하는 데 도움이 됩니다. [자세히 알아보기](../audience/creating-test-profiles.md) |

## 컨텐츠 및 Personalization 약관 {#content-terms}

| 용어 | 정의 |
|------|------------|
| **개인화** | 프로필 데이터, 환경 설정 및 비헤이비어를 사용하여 개별 고객에게 콘텐츠를 맞춤화하는 프로세스입니다. 예를 들어 고객의 이름을 삽입하거나 검색 기록을 기반으로 제품 추천을 표시할 수 있습니다. [자세히 알아보기](../personalization/personalize.md) |
| **콘텐츠 템플릿** | 여러 캠페인 및 여정에서 브랜드 일관성을 유지하고 컨텐츠 생성을 가속화하는 데 사용할 수 있는 재사용 가능한 메시지 디자인입니다. [자세히 알아보기](../content-management/content-templates.md) |
| **조각** | 일관성을 보장하고 중앙 집중식 업데이트를 가능하게 하기 위해 여러 메시지에서 사용할 수 있는 재사용 가능한 콘텐츠 블록(예: 머리글, 바닥글 또는 홍보 배너). [자세히 알아보기](../content-management/fragments.md) |
| **랜딩 페이지** | 고객이 커뮤니케이션에서 옵트인 또는 옵트아웃하거나, 서비스에 가입하거나, 온라인 양식을 통해 정보를 제공할 수 있는 독립 실행형 웹 페이지입니다. [자세히 알아보기](../landing-pages/get-started-lp.md) |

## 의사 결정 및 오퍼 조건 {#decision-terms}

| 용어 | 정의 |
|------|------------|
| **의사 결정 관리** | 실시간 프로필 데이터, 컨텍스트 및 비즈니스 규칙을 기반으로 각 고객에 대해 최상의 콘텐츠 또는 오퍼를 자동으로 선택하는 기능입니다. [자세히 알아보기](../offers/get-started/starting-offer-decisioning.md) |
| **오퍼** | 고객에게 제공할 수 있는 마케팅 메시지, 할인 또는 프로모션. 오퍼에는 오퍼를 받을 수 있는 고객을 결정하는 자격 규칙이 포함됩니다. [자세히 알아보기](../offers/offer-library/creating-personalized-offers.md) |
| **결정 정책** | 자격 조건, 우선 순위 및 한도 규칙과 같은 제약 조건을 기반으로 어떤 시간에 어떤 고객에게 어떤 오퍼를 표시할지 결정하는 규칙 및 전략 세트입니다. [자세히 알아보기](../experience-decisioning/create-decision.md) |

## 데이터 및 구성 용어 {#data-config-terms}

| 용어 | 정의 |
|------|------------|
| **스키마** | 필드 이름, 데이터 유형 및 관계를 포함하여 Adobe Experience Platform에서 데이터가 구성되는 방식을 정의하는 구조입니다. 스키마는 시스템 간에 데이터 일관성을 보장합니다. [자세히 알아보기](../data/get-started-schemas.md) |
| **데이터 집합** | 특정 스키마를 따르는 데이터 컬렉션(일반적으로 테이블)입니다. 데이터 세트는 고객 데이터, 상호 작용 이벤트 및 개인화에 사용되는 기타 정보를 저장합니다. [자세히 알아보기](../data/get-started-datasets.md) |

>[!NOTE]
>
>Adobe Experience Platform 용어에 대한 포괄적인 용어집은 [Adobe Experience Platform 용어집](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}을 참조하세요.

## 관련 항목 {#related-topics}

* [Journey Optimizer 작동 방식 이해](understanding-ajo.md)
* [사용자 인터페이스 시작](user-interface.md)
* [역할 및 학습 경로 선택](quick-start.md)

