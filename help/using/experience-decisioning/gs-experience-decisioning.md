---
title: Experience Decisioning 시작
description: Experience Decisioning에 대한 자세한 내용
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 7%

---

# Experience Decisioning 시작 {#get-started-experience-decisioning}

>[!BEGINSHADEBOX &quot;이 설명서 안내서에서 확인할 수 있는 사항&quot;]

* **[Experience Decisioning 시작하기](gs-experience-decisioning.md)**
* 의사 결정 항목 관리: [항목 카탈로그 구성](catalogs.md) - [의사 결정 항목 만들기](items.md) - [항목 컬렉션 관리](collections.md)
* 항목의 선택 사항 구성: [의사 결정 규칙 만들기](rules.md) - [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

## Experience Decisioning 소개 {#about}

>[!AVAILABILITY]
>
>Experience Decisioning 기능은 현재 사용자를 선택하는 베타 버전으로 사용할 수 있습니다. Beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주십시오.

Experience Decisioning은 &#39;의사 결정 항목&#39;이라고 하는 마케팅 오퍼의 중앙 집중식 카탈로그와 정교한 의사 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 등급 기준을 활용하여 각 개인에게 가장 관련성이 높은 결정 항목을 선택하고 제공합니다.

이러한 의사 결정 항목은 이제 Journey Optimizer 캠페인 내에서 액세스할 수 있는 새로운 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다.

**제한 사항:**

* 의사 결정 정책은 코드 기반 경험 캠페인에서만 사용할 수 있습니다.
* 현재 Experience Decisioning에서는 빈도 제한 기능을 사용할 수 없습니다.

## Experience Decisioning 주요 단계 {#steps}

Experience Decisioning을 사용하는 주요 단계는 다음과 같습니다.

1. **사용자 지정 속성 구성**: 사용자 지정 특성을 카탈로그의 스키마에 설정하여 결정 항목의 카탈로그를 특정 요구 사항에 맞게 조정할 수 있습니다.

1. **의사 결정 항목 만들기** 을 입력하여 타깃팅된 대상자에게 표시할 수 있습니다.

1. **컬렉션으로 구성**: 컬렉션을 사용하여 속성 기반 규칙에 따라 결정 항목을 분류합니다. 컬렉션을 선택 전략에 통합하여 고려해야 하는 결정 항목의 컬렉션을 결정합니다.

1. **의사 결정 규칙 만들기**: 의사 결정 규칙은 의사 결정 항목 및/또는 선택 전략에서 의사 결정 항목을 표시할 수 있는 대상을 결정하는 데 사용됩니다.

1. **등급 메서드 구현**: 등급 메서드를 만들고 의사 결정 전략 내에 적용하여 의사 결정 항목 선택의 우선 순위를 결정합니다.

1. **선택 전략 만들기**: 컬렉션, 의사 결정 규칙 및 등급 방법을 활용하여 프로필에 표시하는 데 적합한 의사 결정 항목을 식별하는 선택 전략을 수립합니다.

1. **코드 기반 캠페인에 의사 결정 정책 포함**: 의사 결정 정책은 여러 선택 전략을 결합하여 의도한 대상자에게 표시할 적합한 의사 결정 항목을 결정합니다.
