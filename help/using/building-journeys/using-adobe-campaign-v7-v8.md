---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign v7/v8 작업
description: Adobe Campaign v7/v8 작업에 대해 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: 여정, 통합, campaign, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 11%

---

# [!DNL Adobe Campaign] v7/v8 액션 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Campaign v7 및 v8 통합을 사용하여 Campaign 트랜잭션 메시지를 통해 여정에서 이메일, 푸시 알림 및 SMS를 보내는 방법을 알아봅니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="사용자 정의 액션"
>abstract="[!DNL Adobe Campaign] v7 또는 v8이 있는 경우 통합 기능을 사용할 수 있습니다. [!DNL Adobe Campaign] 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림, SMS를 전송할 수 있습니다."

[!DNL Adobe Campaign] v7 또는 v8이 있는 경우 통합 기능을 사용할 수 있습니다. [!DNL Adobe Campaign] 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림, SMS를 전송할 수 있습니다.

Journey Optimizer 인스턴스와 Campaign 인스턴스 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다. Adobe에 문의하십시오.

**사용 시기**: 메시징이 Campaign 트랜잭션 템플릿, Campaign별 데이터 모델 또는 기존 Campaign 게재 워크플로우에 의존하는 경우 Campaign v7/v8 작업을 사용하십시오.

**전제 조건**

* [!DNL Adobe Campaign] v7/v8 인스턴스가 프로비저닝되고 Adobe에서 Journey Optimizer에 연결합니다.
* 캠페인 트랜잭션 메시지에 대한 액세스 권한과 필요한 권한이 있습니다.

이를 수행하려면 전용 작업을 구성해야 합니다. 이 [섹션](../action/acc-action.md)을 참조하십시오.

이 [섹션](../building-journeys/ajo-ac.md)에 엔드 투 엔드 사용 사례가 표시됩니다.

1. 이벤트로 시작하여 여정을 디자인합니다. 이 [섹션](../building-journeys/journey.md)을 참조하세요.
1. 팔레트의 **작업** 섹션에서 캠페인 작업을 선택하고 여정에 추가합니다.
1. **작업 매개 변수**&#x200B;에 메시지 페이로드에 필요한 모든 필드가 표시됩니다. 이러한 각 필드를 이벤트 또는 데이터 소스에서 사용할 필드에 매핑해야 합니다. 이는 사용자 지정 작업과 유사합니다. 이 [섹션](../building-journeys/using-custom-actions.md)을 참조하십시오.

>[!NOTE]
>
>* Campaign v7/v8 작업은 동일한 여정에서 기본 채널 작업과 함께 사용할 수 있습니다. Campaign Standard 작업에는 적용되지 않습니다. [캠페인 활동 보호](../start/guardrails.md#ac-g)를 참조하세요.
>* Campaign v7/v8 작업은 대상 읽기 또는 대상 자격 활동과 함께 사용할 수 없습니다. 보호 기능 페이지에서 대상 및 대상 자격 보호 기능 읽기 를 참조하십시오.

![[!DNL Adobe Campaign] v7/v8 작업 구성 및 통합 설정](assets/accintegration2.png)

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 Adobe Campaign v7/v8을 Journey Optimizer 여정에서 Campaign 트랜잭션 메시지를 통해 이메일, 푸시 알림 및 SMS를 전송하는 작업을 설명합니다.

**의도:**

* 여정에 Campaign v7/v8 작업을 추가하여 트랜잭션 메시지 보내기
* 여정 이벤트 또는 데이터 소스 필드를 캠페인 메시지 페이로드 매개 변수에 매핑
* 동일한 여정에서 Campaign v7/v8 작업을 기본 Journey Optimizer 채널 작업과 결합
* Campaign v7/v8 통합에 필요한 전용 작업 구성

**용어집:**

* **Campaign 트랜잭션 메시지**: Journey Optimizer *(제품별)와 통합된 전용 작업을 통해 트리거된 메시지(이메일, SMS, 푸시)를 전송하는 Adobe Campaign v7/v8 기능*
* **작업 매개 변수**: 여정 데이터를 예상 캠페인 메시지 페이로드 *(제품별)에 매핑하는 여정 활동 창의 필드*

**보호 기능:**

* Journey Optimizer과 Campaign 인스턴스 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다. Adobe에 문의하여 활성화하십시오.
* 여정 팔레트에서 Campaign v7/v8 작업을 사용하려면 먼저 전용 작업을 구성해야 합니다.
* Campaign v7/v8 작업은 대상 읽기 또는 대상 자격 활동과 함께 사용할 수 없습니다.
* Campaign 트랜잭션 메시지에 대한 액세스와 Campaign에서 필요한 권한은 사전 요구 사항입니다.

**용어:**

* 정식 이름: Adobe Campaign v7/v8 — 약어: ACC — 변형: Campaign v7, Campaign v8, Campaign Classic
* 혼동하지 마십시오. &quot;Campaign v7/v8 작업&quot;(기본 작업과 함께 사용할 수 있음) ≠ &quot;Campaign Standard 작업&quot;(동일한 여정에서 기본 작업과 결합할 수 없음)

**FAQ:**

* **Q: 누가 Journey Optimizer과 Campaign v7/v8 간의 연결을 설정합니까?** — Adobe은 프로비저닝 시 연결을 설정합니다. Adobe에 문의하여 구성해야 합니다.
* **Q: Campaign v7/v8 작업을 동일한 여정에서 기본 Journey Optimizer 채널 작업과 결합할 수 있습니까?** — 예. 기본 채널 작업과 함께 Campaign v7/v8 작업을 사용할 수 있습니다. Campaign Standard 작업에는 해당되지 않습니다.
* **Q: Campaign v7/v8 작업을 대상 읽기 또는 대상 자격 활동과 함께 사용할 수 있습니까?** — 아니요. Campaign v7/v8 작업은 대상 읽기 또는 대상 자격 활동과 함께 사용할 수 없습니다.
* **Q: 여정 데이터를 Campaign 메시지 페이로드에 매핑하려면 어떻게 해야 합니까?** — 작업 매개 변수 창에서 사용자 지정 작업과 동일한 방식으로 각 예상 페이로드 필드를 여정 이벤트 또는 데이터 소스의 해당 필드에 매핑합니다.

+++
