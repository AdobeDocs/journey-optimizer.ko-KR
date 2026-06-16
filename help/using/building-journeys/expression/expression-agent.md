---
solution: Journey Optimizer
product: journey optimizer
title: 표현식 어시스턴트를 사용하여 표현식 생성
description: Adobe Journey Optimizer에서 표현식 도우미를 사용하여 자연어 프롬프트를 사용하여 여정 고급 표현식 편집기에서 직접 표현식을 생성하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="공개 베타" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: d90f0ac22c107a51967316f078f359f067b70431
workflow-type: tm+mt
source-wordcount: 661
ht-degree: 13%

---


# 표현식 어시스턴트를 사용하여 표현식 생성 {#expression-agent}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="표현식 어시스턴트를 사용하여 표현식 생성"
>abstract="표현식 어시스턴트는 생성형 AI를 사용하여 여정 고급 표현식 편집기에서 직접 표현식을 작성하고 생성하는 데 도움이 됩니다. 예를 들어 조건에서는 사용자 정의 날짜를 사용하는 **최적화** 활동 또는 **대기** 활동을 사용합니다. 필요한 사항을 일반 언어로 설명하면 어시스턴트가 해당 표현식을 생성합니다."

>[!AVAILABILITY]
>
>이 기능은 현재 **공개 베타**&#x200B;에 있습니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](../../rn/releases.md)를 참조하십시오.
>
>Expression Assistant를 사용하기 전에 Journey Optimizer의 생성 AI 기능에 적용되는 관련 [보호 기능 및 제한 사항](../../content-management/gs-generative.md#generative-guardrails)을 읽어 보십시오.

표현식 도우미는 여정 고급 표현식 편집기에 내장된 AI 기반 기능입니다. 일반 언어 프롬프트에서 유효한 표현식을 생성하는 데 도움이 됩니다.

여정 **[!UICONTROL 고급 표현식 편집기]**&#x200B;가 열리는 모든 곳에서 사용할 수 있습니다. 예를 들어 **[활동 최적화](../optimize.md)** 내에서 조건 및 라우팅을 구성하거나 사용자 지정 날짜를 사용하는 [**[!UICONTROL 대기&#x200B;]**활동](../wait-activity.md)을 구성할 때 `dateTimeOnly` 식이 필요합니다.

## 표현식 생성 {#generate}

표현식 도우미를 사용하여 표현식을 생성하려면 다음을 수행합니다.

1. 분기 조건, **[!UICONTROL 최적화]** 활동 또는 사용자 지정 날짜가 포함된 **[!UICONTROL 대기]** 활동 등을 사용하여 여정에서 **[!UICONTROL 고급 표현식 편집기]**&#x200B;를 엽니다.

   ![](../assets/expression-assistant-pane.png)

1. 텍스트 필드에 생성할 표현식을 일반 언어로 설명합니다. 예:

   * *&quot;미국 사용자 및 18&quot;* 이상
   * *&quot;지난 30일 동안 구매한 고객&quot;*

   아이디어는 이 페이지 끝에 있는 [예제 프롬프트](#example-prompts)를 참조하십시오.

1. 프롬프트를 제출하려면 **[!UICONTROL 생성]**&#x200B;을 클릭하세요.

   도우미는 해당 표현식의 생성을 시작하고 생성이 진행되는 동안 진행 상태 메시지를 표시합니다.

   >[!NOTE]
   >
   >도우미가 유효한 표현식을 생성할 수 없는 경우(예: 프롬프트가 사용 가능한 데이터 소스에 없는 필드를 참조하는 경우) 오류 메시지가 나타납니다. 이런 경우 여정 구성에서 사용할 수 있는 필드 이름 및 데이터 소스를 사용하도록 프롬프트를 수정한 다음 다시 생성합니다.

1. 표현식이 준비되면 패널에서 결과를 검토합니다.

   ![](../assets/expression-assistant-result.png)

   * 지원자가 요청한 시나리오에 대한 지원 도우미의 출력을 검토하려면 적용하기 전에 ![미리 보기 아이콘](../assets/do-not-localize/generation-preview.svg) 아이콘을 클릭하십시오.

   * 생성된 표현식을 고급 표현식 편집기에 직접 삽입하려면 **[!UICONTROL 적용]**&#x200B;을 클릭합니다(수동으로 붙여넣는 것과 동일한 배치).
   * 복사 컨트롤을 사용하여 제안된 표현식 텍스트를 선택하고 필요한 경우 다른 곳에 붙여넣습니다.

## 프롬프트 예 {#example-prompts}

아래 목록은 신속한 아이디어일 뿐입니다. 생성된 표현식 구문은 표시되지 않으며 정확한 출력은 여정에 정의된 필드 및 활동에 따라 다릅니다.

### 여정 이벤트 및 사용자 지정 작업 {#example-prompts-event-action}

* 주문 가격 합계가 100&quot;*보다 큰*&quot;이벤트
* *&quot;주문이 지난 7일 동안 만들어진 이벤트&quot;*
* *&quot;이벤트 유형이 상거래 구매인 이벤트&quot;*
* *&quot;지난 시간에 만들어진 순서가 있는 이벤트&quot;*
* 주문 가격 합계가 200을 초과하는 이벤트 및 작업 응답에 상태 코드가 있는 *&quot;*

### 대기 활동 표현식 {#example-prompts-datetime}

**[!UICONTROL 대기]** 활동에서 사용자 지정 날짜를 사용하는 경우 **[!UICONTROL 고급 표현식 편집기]**&#x200B;에서 `dateTimeOnly` 표현식을 만들어 프로필을 계속할 시기를 정의합니다. 예를 들어 프로필 속성, 이벤트 타임스탬프, 세그먼트 자격 데이터 또는 현재 시간으로부터 계산된 오프셋에서 가져온 데이터가 있습니다. 사용자 지정 대기 및 적용 가능한 제한을 구성하는 방법은 [사용자 지정 대기](../wait-activity.md#custom)를 참조하십시오.

* *&quot;고객의 마지막 주문 날짜를 날짜 시간으로만 사용&quot;*
* *&quot;동의 전자 메일 시간을 날짜 시간으로만 사용&quot;*
* *&quot;세그먼트 멤버십 마지막 자격 시간을 날짜 시간으로만 변환&quot;*
* *&quot;대기 노드: 2024년 크리스마스부터 1주일 후에 날짜 시간으로만&quot;*
* *&quot;대기 노드: 지금부터 30일 후 오후 10시 이후에만 날짜 시간으로&quot;*
* *&quot;UTC 시간대로 오늘 오전 9시까지 기다린 후 날짜 시간으로만 반환&quot;*

## 관련 리소스 {#related}

* [고급 표현식 편집기 작업](expressionadvanced.md) — 표현식 편집기 인터페이스와 지원되는 구문에 대한 개요입니다.
* [Journey Optimizer에서 AI Assistant 시작하기](../../content-management/gs-generative.md) - 일반 보호, 액세스 및 생성 AI 기능 설정.
