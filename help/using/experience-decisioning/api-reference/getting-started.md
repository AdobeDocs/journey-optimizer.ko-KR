---
title: API 결정하기 시작
description: Decisioning API를 사용하여 시작함으로써 의사 결정 항목을 프로그래밍 방식으로 관리하고 개인화된 오퍼를 제공하는 방법을 알아봅니다.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 5%

---

# Decisioning API 개발자 안내서 {#decisioning-api-developer-guide}

Decisioning API를 사용하면 고객에게 개인화된 오퍼를 제공하는 데 사용되는 구성 요소를 프로그래밍 방식으로 만들고 관리할 수 있습니다. 이러한 RESTful API는 의사 결정 항목, 선택 전략, 자격 규칙 및 기타 의사 결정 구성 요소에 대한 전체 CRUD(만들기, 읽기, 업데이트, 삭제) 작업을 제공합니다.

## 인증 {#authentication}

Decisioning API를 사용하기 전에 API 끝점에 액세스할 수 있는 인증을 설정해야 합니다. 단계별 지침은 [Journey Optimizer 인증 안내서](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}를 참조하십시오.

## 사용 가능한 API 작업 {#available-operations}

Decisioning API는 의사 결정 구성 요소를 위한 포괄적인 관리 기능을 제공합니다. 다음과 같은 범주의 작업을 사용할 수 있습니다.

* **의사 결정 항목** - 고객에게 제공할 오퍼 또는 콘텐츠를 나타내는 의사 결정 항목을 만들고, 읽고, 업데이트하고, 삭제하고, 나열합니다.

  ➡️ [결정 항목을 관리하는 방법 알아보기](decisions-items/create.md)

* **항목 컬렉션** - 자격 규칙을 사용하여 보다 쉽게 관리하고 타깃팅할 수 있도록 의사 결정 항목을 컬렉션으로 구성합니다.

  ➡️ [항목 컬렉션을 관리하는 방법 알아보기](items-collections/create.md)

* **선택 전략** - 여러 항목이 배달될 수 있을 때 결정 항목을 선택하고 등급을 지정하는 방법을 정의합니다.

  ➡️ [선택 전략을 관리하는 방법 알아보기](selection-strategies/create.md)

* **자격 규칙** - 특정 결정 항목을 받을 수 있는 프로필을 결정하는 조건을 설정합니다.

  ➡️ [자격 규칙을 관리하는 방법 알아보기](eligibility-rules/create.md)

* **등급 수식** - 의사 결정 항목이 표시되는 순서를 결정하는 사용자 지정 등급 논리를 만듭니다.

  ➡️ [등급 수식 관리 방법 알아보기](ranking-formulas/create.md)

* **배치** - 경험에 결정 항목을 표시할 수 있는 위치 또는 컨텍스트를 정의합니다.

  ➡️ [배치 관리 방법 알아보기](exd-placements/create.md)

## 다음 단계 {#next-steps}

이제 Decisioning API의 기본 사항을 이해했으므로 특정 작업으로 진행할 수 있습니다.

* [결정 항목 만들기](decisions-items/create.md)
* [의사 결정 항목 나열](decisions-items/decision-items-list.md)
* [선택 전략 만들기](selection-strategies/create.md)
* [자격 규칙 만들기](eligibility-rules/create.md)

캠페인 및 여정에서 Decisioning 사용에 대한 자세한 내용은 [Decisioning 설명서](../gs-experience-decisioning.md)를 참조하세요.

>[!NOTE]
>
>기존 의사 결정 관리 개체를 Decisioning으로 마이그레이션해야 하는 경우 전용 [Decisioning 마이그레이션 API](../decisioning-migration-api.md)를 사용하십시오. 이 전문 API는 샌드박스 간 엔티티 마이그레이션을 결정하도록 특별히 설계된 자동 종속성 해결 및 롤백 기능을 제공합니다.
