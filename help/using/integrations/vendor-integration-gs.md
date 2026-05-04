---
solution: Journey Optimizer
product: journey optimizer
title: 공급업체 통합
description: 유효한 API를 노출하는 외부 플랫폼과 Adobe Journey Optimizer 통합 및 설정을 디자인할 때 신뢰할 수 있도록 엔지니어링 테스트를 거친 공급업체 패턴을 사용합니다.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 통합, 공급업체, 서드파티
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# 공급업체 통합 {#vendor-integration}

각 시스템이 사용 사례에 적합하고 통합에서 요청을 처리하고 응답을 사용하는 방식과 호환되는 **API 끝점**&#x200B;을(를) 노출할 때 Adobe Journey Optimizer에서 **통합**&#x200B;을 사용하여 **HTTP를 통한 외부 시스템**&#x200B;을(를) 호출할 수 있습니다. 전체 워크플로를 보려면 [통합 작업](integrations.md)을 참조하십시오.

본 명세서에 기술된 타사 솔루션 목록은 예시적인 것이며, 완전한 것은 아니다. 제품 요구 사항을 충족하는 다른 플랫폼이 사용될 수도 있습니다.

## 작동 보호 기능 {#operational-guardrails}

이 안내서 또는 유사한 공급업체에서 통합을 구성할 때 다음을 적용합니다.

* **응답 형식:** 통합 맵 필드는 **JSON** 또는 **HTML** 응답에서 가져옵니다. 작성 시간에 API가 매핑에 적합한 JSON 또는 HTML을 반환하도록 디자인됩니다.
* **페이로드 및 필드:** 필요한 특성만 요청하고 매핑합니다. 응답 크기가 작을수록 대기 시간이 단축되고 중요한 데이터의 노출이 제한됩니다.
* **끝점 셰이프:** 제품이 대상 조회를 예상할 때 광범위한 목록 또는 페이지 매김 끝점보다 안정적인 **단일 리소스** 검색(예: 하나의 시작, 제품 또는 멤버)을 선호합니다. [제한 및 제외](#limitations-exclusions) 및 [통합 작업](integrations.md)을 참조하세요.
* **볼륨 및 안정성:** 공급업체의 **속도 제한**&#x200B;을 준수합니다. 채널에 대해 **시간 초과**, **다시 시도** 및 **캐시** 정책을 구성하고(예: 일괄 전자 메일과 트랜잭션 전송) 로드 중에 유효성을 검사하십시오.
* **보안:** 조직의 정책에 따라 토큰, API 키 및 OAuth 자격 증명을 저장하고 회전합니다. 메시지 콘텐츠에 비밀을 임베드하지 마십시오.


## 제한 사항 및 제외 {#limitations-exclusions}

타사 솔루션 목록은 완전하지 않은 **그림**&#x200B;입니다. 공급업체 API, 호스트, 속도 제한 및 JSON 또는 HTML 응답 모양이 변경될 수 있습니다. 공급업체의 현재 설명서 및 구독을 통해 엔드포인트, 인증 및 필드 매핑을 확인합니다. 여기에 있는 패턴은 개인화에 적합한 **읽기 지향** 호출을 가정합니다. 통합은 **JSON** 및 **HTML** 응답에서만 매핑을 지원합니다. **다시 쓰기**, **일괄 내보내기** 및 다른 형식의 응답은 지원되지 않습니다.

## 빠른 탐색 {#quick-navigation}

이러한 그룹화된 링크를 사용하여 관련 공급업체 패턴으로 빠르게 이동합니다.

* **콘텐츠 관리 시스템:** [콘텐츠화](vendor-integration.md#contentful), [사이트코어](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [콘텐츠스택](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [목련](vendor-integration.md#magnolia)
* **충성도 및 보상:** [Voucherify](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Salesforce 충성도](vendor-integration.md#salesforce-loyalty), [모세관](vendor-integration.md#capillary)
* **템플릿, 개인화 및 권장 사항:** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Adobe Target 권장 사항](vendor-integration.md#adobe-target-recommendations)
* **데이터, 날씨 및 작업:** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [데이터 집합](vendor-integration.md#databricks)
* **검토, 동의 및 소셜:** [바이더](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon(Epsilon3)](vendor-integration.md#epsilon)
