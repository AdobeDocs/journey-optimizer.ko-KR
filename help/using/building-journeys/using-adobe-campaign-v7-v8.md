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
source-git-commit: a068d3a4005d8f2247755f56ffb70665dc4c957f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 25%

---

# Adobe Campaign v7/v8 작업 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="사용자 정의 액션"
>abstract="Adobe Campaign v7 또는 v8이 있는 경우 통합을 사용할 수 있습니다. Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림, SMS를 전송할 수 있습니다."

Adobe Campaign v7 또는 v8이 있는 경우 통합을 사용할 수 있습니다. Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림, SMS를 전송할 수 있습니다.

Journey Optimizer 인스턴스와 Campaign 인스턴스 간의 연결은 프로비저닝 시 Adobe에 의해 설정됩니다. Adobe에 문의하십시오.

**사용 시기**: 메시징이 Campaign 트랜잭션 템플릿, Campaign별 데이터 모델 또는 기존 Campaign 게재 워크플로우에 의존하는 경우 Campaign v7/v8 작업을 사용하십시오.

**전제 조건**

* Adobe Campaign v7/v8 인스턴스가 프로비저닝되고 Adobe에서 Journey Optimizer에 연결합니다.
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

![Adobe Campaign v7/v8 작업 구성 및 통합 설정](assets/accintegration2.png)
