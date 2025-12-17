---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer API 사용
description: Journey Optimizer에서는 애플리케이션에서 주요 작업을 프로그래밍 방식으로 수행할 수 있는 RESTful API를 제공합니다. 액세스 및 사용 방법에 대해 알아봅니다.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: cbfebeaaa3ef6e55d48457012fd94bd74afc91de
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# [!DNL Journey Optimizer] API 작업 {#apis-gs}

## 빠른 액세스 {#quick-access}

>[!IMPORTANT]
>
>**Journey Optimizer API 시작:**
>
>* **[전체 API 참조 찾아보기](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** - 모든 Journey Optimizer API에 액세스하고 직접 테스트합니다.
>* **[인증 설정](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** - API 사용을 시작하는 데 필요한 자격 증명을 수집합니다.
>* **[의사 결정 관리 API](../offers/api-reference/getting-started.md)** - 오퍼와 의사 결정을 프로그래밍 방식으로 관리합니다.
>* **[Experience Decisioning API](../experience-decisioning/api-reference/deliver.md)** - 코드 기반 경험을 사용하여 개인화된 결정 항목 전달

## 개요 {#overview}

Adobe Journey Optimizer API를 사용하면 모든 앱, 장치 또는 채널에서 개인화되고, 연결되며, 시기적절한 고객 경험을 제공할 수 있으며, 결과적으로 엔드 투 엔드 고객 여정을 효과적으로 관리할 수 있습니다. 고객 여정은 고객과 브랜드 간의 상호 작용을 위한 전체 프로세스로서, 연락 시작부터 고객이 떠난 시점까지 진행됩니다. 브랜드에 대해 알아보고 높이고 참여를 유도하는 인지도 단계로 시작합니다. 그런 다음 고객은 브랜드와 상호 작용하고, 온라인 및 물리적 사이트를 방문하거나, 구매를 하거나, 메시지를 보내거나, 리뷰를 게시합니다.

Adobe Journey Optimizer은 기본적으로 Adobe Experience Platform을 기반으로 빌드되었으며 개인화 및 최적화를 위한 통합 실시간 고객 프로필, API 우선 오픈 프레임워크, 중앙 집중식 Offer Decisioning 및 AI(인공 지능) 및 ML(머신 러닝)을 결합합니다. Journey Optimizer API와 통합함으로써 브랜드는 전체 고객 여정에서 규모, 속도 및 유연성과 차세대 상호 작용을 지능적으로 결정할 수 있습니다.

## 인증 {#authentication}

Journey Optimizer API를 사용하기 전에 API 끝점에 액세스하기 위해 인증을 설정해야 합니다.

모든 Journey Optimizer API에 필요한 인증 자격 증명을 수집하려면 [인증 안내서](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}를 따르십시오.

## API 설명서 {#api-documentation}

전체 Adobe Journey Optimizer API 설명서에는 사용 가능한 모든 엔드포인트, 요청/응답 형식 및 대화형 테스트 기능에 대한 자세한 정보가 포함되어 있습니다.

[Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}에 액세스하고 **API 참조** 메뉴를 탐색하여 사용 가능한 모든 API를 살펴보십시오.

## 의사 결정 관리 API {#decision-management-apis}

Journey Optimizer은 의사 결정 관리에 대한 전용 API를 제공하므로 오퍼, 의사 결정 및 배치를 프로그래밍 방식으로 관리할 수 있습니다.

Offer Decisioning API를 시작하려면 [의사 결정 관리 API 개발자 안내서](../offers/api-reference/getting-started.md)를 참조하십시오.

## Experience Decisioning API {#experience-decisioning-apis}

Journey Optimizer은 또한 코드 기반 경험을 통해 개인화된 의사 결정 항목을 전달하기 위한 Experience Decisioning API를 제공합니다. Experience Decisioning은 의사 결정 항목, 자격 규칙 및 선택 전략을 사용하여 개인화에 대한 간소화된 접근 방식을 제공합니다.

**사용 가능한 API 작업:**

* **결정 항목** - 결정 항목 만들기, 읽기, 업데이트 및 삭제
* **선택 전략** - 결정 항목을 선택하고 등급을 매기는 방법을 정의합니다.
* **자격 규칙** - 항목 자격 조건을 설정합니다.
* **항목 컬렉션** - 결정 항목을 컬렉션에 구성
* **등급 수식** - 사용자 지정 등급 논리 구성
* **배치** - 결정 항목을 표시할 위치를 정의합니다.

[Experience Decisioning API 참조](../experience-decisioning/api-reference/deliver.md)에서 자세히 알아보고 [코드 기반 경험을 사용하여 오퍼 게재](../experience-decisioning/api-reference/deliver.md)하는 방법을 알아봅니다.
