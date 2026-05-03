---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에서 변수 사용
description: 오케스트레이션된 캠페인에서 이벤트 변수를 사용하여 조건 및 타깃팅 규칙을 작성하는 방법을 알아봅니다.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
source-git-commit: 8175f63d4e1055d285d2f3f12a498a9dbd3fa1ba
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 오케스트레이션된 캠페인에서 변수 사용 {#variables-oc}

## 변수를 설정하는 방법 {#set}

오케스트레이션된 캠페인에서는 타깃팅을 유도하는 변수, **[!UICONTROL 테스트]** 조건 및 기타 캔버스 논리를 사용하여 작업할 수 있습니다. 이러한 값은 다음 두 위치에서 제공될 수 있습니다.

* **신호** — 캠페인 일정이 **[!UICONTROL 신호에 의해 트리거됨]**&#x200B;인 경우 캠페인을 실행할 때 매개 변수를 전달할 수 있습니다. 이러한 매개 변수는 해당 실행을 위해 트리거된 오케스트레이션된 캠페인에서 변수로 사용할 수 있습니다. [신호를 사용하여 오케스트레이션된 캠페인을 트리거하는 방법을 알아봅니다](trigger-orchestrated-campaign.md)

* **전역 변수** — **[!UICONTROL 변수 편집]** 메뉴를 사용하여 캠페인에 직접 이름-값 쌍을 정의할 수 있습니다. API 또는 신호가 필요하지 않습니다. [오케스트레이션된 캠페인에서 전역 변수를 정의하는 방법을 알아봅니다](global-variables.md)

>[!NOTE]
>
>지금은 변수에서 **text** 값만 지원합니다.
>
>변수는 **캔버스 논리**(규칙, 조건)을 구동하며 메시지 개인화에 사용할 수 없습니다.

## 캔버스에서 변수 사용 {#use}

변수는 캔버스의 다음 위치에서 사용할 수 있습니다.

* **규칙 빌더** — 규칙에 대한 표현식 편집기를 열고 **이벤트 변수** 선택기를 사용하여 변수를 선택하고 해당 참조를 표현식에 삽입합니다. [표현식을 편집하는 방법 알아보기](edit-expressions.md)

  아래 예에서는 이름이 `brand`인 변수가 전달되었으며 규칙이 이 변수를 필터 조건으로 사용합니다.

  ![이벤트 변수의 브랜드 변수를 사용하는 규칙 빌더 조건](assets/variables-rule.png){zoomable="yes"}

* **[!UICONTROL 테스트] 활동** — 조건을 정의할 때 **[!UICONTROL 조건 유형]** 드롭다운에 **[!UICONTROL 모집단 수]**&#x200B;와(과) 함께 범위의 모든 변수가 나열됩니다. 테스트 분기의 기반으로 사용할 변수를 선택하십시오. [**[!UICONTROL 테스트]** 활동을 구성하는 방법을 알아봅니다](activities/test.md)

  아래 예제에서는 `channel` 변수를 사용하여 해당 값에 따라 흐름을 다른 전환으로 라우팅합니다.

  ![채널 변수를 나열하는 테스트 활동 조건 유형 드롭다운](assets/variables-test.png){zoomable="yes"}
