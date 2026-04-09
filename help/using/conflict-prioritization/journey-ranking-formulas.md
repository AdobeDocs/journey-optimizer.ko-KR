---
title: 여정 중재 등급 수식
description: 규칙과 컨텍스트를 기반으로 프로필별로 최상의 여정을 선택하도록 중재용 여정의 등급을 지정하는 공식을 만드는 방법을 알아봅니다.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="제한 공개" type="Informative"
exl-id: b172e0e1-b78e-4d96-ab88-254507b55f48
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 2%

---

# 공식을 사용하여 여정 등급 지정 {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>이 기능은 현재 제한된 가용성입니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

[!DNL Adobe Journey Optimizer]을(를) 사용하면 프로필이 시스템에서 허용하는 것보다 더 많은 여정에 대한 자격이 있을 때 프로필이 입력할 수 있는 프로필을 제어할 수 있습니다. 이렇게 하려면 [규칙 집합](rule-sets.md)을 사용하여 여정 항목 또는 동시 사용에 대한 제한을 정의할 수 있습니다. 여정이 상한선이 허용하는 것보다 더 많은 여정에 적격인 경우, 각 프로필에 할당된 우선순위에 따라 선택되는 여정이 결정됩니다.

우선 순위를 사용하는 대신 **순위 수식**&#x200B;을 사용하여 여정 특성, 프로필 특성 또는 AI 모델 점수를 기반으로 여정 순위를 동적으로 조정할 수도 있습니다.

수식을 사용하면 정적 우선 순위보다 더 유연합니다. 예를 들어 gold 충성도 멤버에 대한 여정을 높일 수 있습니다.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).
-->

## 순위 공식 만들기 {#create-journey-ranking-formula}

여정에 대한 순위 공식을 만들려면 아래 단계를 수행합니다.

1. **[!UICONTROL 오케스트레이션 등급]** 섹션에 액세스한 다음 **[!UICONTROL 등급 수식]** 탭을 선택하십시오. 이전에 만든 수식의 목록이 표시됩니다.

1. **[!UICONTROL 수식 만들기]**&#x200B;를 클릭합니다.

1. 수식 이름을 지정하고 원하는 경우 설명을 추가합니다.

   ![이름 및 설명 필드가 있는 수식 세부 정보 창](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >순위 객체는 순위 공식이 적용될 엔티티입니다. 기본적으로 순위 개체는 **[!UICONTROL 여정]**(으)로 설정됩니다.

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.
-->

1. 선택적으로 **[!UICONTROL AI 모델 선택]**&#x200B;을 클릭하여 순위 공식을 만드는 데 참조로 사용할 모델을 설정합니다. [자세히 알아보기](journey-ai-models.md)

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)
-->

1. **[!UICONTROL 기준 1]** 섹션에서 다음을 수행하여 순위 점수를 적용할 여정을 지정합니다.

   * [여정 특성](../building-journeys/journey-properties.md)(예: 여정 이름, 태그, 우선 순위 또는 기타 여정 속성)을 선택하십시오.
   * 논리 연산자를 선택합니다.
   * 일치하는 조건 추가 - 값을 입력/선택하거나 프로필 속성을 선택할 수 있습니다.

   ![여정 특성, 연산자 및 일치하는 조건이 있는 기준 1 섹션](assets/journey-formula-criterion-1.png){width="70%"}

1. 선택적으로 추가 요소를 지정하여 기준이 true가 되도록 일치하는 조건을 구체화할 수 있습니다.

   ![일치하는 기준을 구체화하는 추가 조건](assets/journey-formula-additional-condition.png){width="70%"}

   예를 들어, *여정 태그*&#x200B;에 *충성도*&#x200B;가 포함되어 있는 것과 같은 *기준 1*&#x200B;을(를) 정의했습니다. 또한 *충성도 상태*&#x200B;가 *골드*&#x200B;인 경우 *기준 1*&#x200B;이 참인 경우와 같은 다른 조건을 추가할 수 있습니다.

1. 위에 정의된 조건을 충족하는 여정에 등급 점수를 지정할 표현식을 만듭니다. 다음 중 하나를 참조할 수 있습니다.
   * 변수:
      * 여정 우선 순위는 [여정을 만들 때](../building-journeys/journey-gs.md) 여정에 할당된 수동 값입니다.
      * 위에서 선택적으로 선택한 AI 모델에서 나온 점수
   * 속성:
      * 외부에서 파생된 성향 점수와 같이 프로필에 있을 수 있는 모든 속성
      * 여정 속성;
   * 자유 형식으로 할당할 수 있는 정적 값
   * 위의 모든 조합을 구성합니다.

   ![변수, 특성 또는 정적 값을 사용하여 순위 점수를 할당하는 식 작성기](assets/journey-formula-expression.png){width="70%"}

1. 하나 이상의 기준을 필요한 횟수만큼 추가하려면 **[!UICONTROL 기준 추가]**&#x200B;를 클릭하십시오. 논리는 다음과 같습니다.
   * 주어진 결정 항목에 대해 첫 번째 기준이 참인 경우 다음 기준보다 우선합니다.
   * true가 아닌 경우 의사 결정 엔진이 두 번째 기준으로 이동합니다.

1. 모든 기준을 정의하고 나면 마지막 필드에서 위의 기준을 충족하지 않는 모든 여정에 지정할 표현식을 작성할 수 있습니다.

   조건을 충족하지 않는 여정에 대한 ![식 필드](assets/journey-formula-criteria-not-met.png){width="70%"}

1. 순위 공식을 완료하려면 **[!UICONTROL 만들기]**&#x200B;를 클릭하세요.

이제 목록에서 이 공식을 선택하여 세부 정보를 보고 편집하거나 삭제할 수 있습니다. 그런 다음 규칙 세트를 구성할 때 사용할 수 있습니다. [방법 알아보기](#assign-formula-to-ruleset)

### 순위 공식 예 {#journey-ranking-formula-example}

아래 예를 참조하십시오.

+++예제 1: 여정 태그를 기반으로 여정 우선 순위 또는 AI 스코어 사용

![순위 공식: 마케팅 태그에서 여정 우선 순위를 사용](assets/journey-formula-ex-1.png){width="60%"}

여정에 &quot;마케팅&quot; 태그가 있는 경우 순위 점수가 여정 우선 순위입니다.

![순위 공식: 프로모션 태그가 AI 모델 점수를 사용함](assets/journey-formula-ex-2.png){width="60%"}

여정에 &quot;프로모션&quot; 태그가 있는 경우 순위 점수는 AI 모델 점수입니다.

+++

+++예제 2: 프로필 상태별 충성도 여정 증폭


![순위 공식: Gold 상태의 충성도 태그에서 여정 우선 순위 + 5](assets/journey-formula-ex-3.png){width="60%"}을(를) 사용합니다.

여정에 &quot;충성도&quot; 태그가 있고 프로필의 충성도 상태가 Gold인 경우 사용되는 순위 점수는 여정 우선 순위와 5를 더한 것입니다.

![순위 공식: Silver 상태의 충성도 태그에서 여정 우선 순위 + 2](assets/journey-formula-ex-4.png){width="60%"}를 사용합니다.

여정에 &quot;충성도&quot; 태그가 있고 프로필의 충성도 상태가 실버인 경우 순위 점수가 여정 우선 순위에 2를 더한 값입니다.

위의 조건 중 어느 하나도 충족되지 않는 경우 사용되는 순위 점수가 여정 우선순위가 된다.

+++

### 코드 편집기 사용 {#journey-ranking-formula-code-editor}

**PQL 구문**&#x200B;에서 등급 수식을 표현하려면 화면 오른쪽 상단의 전용 단추를 사용하여 코드 편집기로 전환하십시오. PQL 구문을 사용하는 방법에 대한 자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=ko)를 참조하세요.

>[!CAUTION]
>
>이 작업을 수행하면 이 수식의 기본 빌더 보기로 되돌아 가는 것이 방지됩니다.

그런 다음 여정 속성, 프로필 속성 및 정적 값을 활용하여 등급 공식을 작성할 수 있습니다.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## 규칙 세트에 공식 지정 {#assign-formula-to-ruleset}

공식을 사용하여 규칙의 등급을 지정하려면 여정 세트에 지정해야 합니다.

>[!NOTE]
>
>공식은 개별 여정이 아닌 규칙 세트 수준에서 지정됩니다.

1. **[!UICONTROL 비즈니스 규칙]** 메뉴에서 여정 중재에 사용할 규칙 집합을 만듭니다. [방법 알아보기](rule-sets.md#Create)

1. **[!UICONTROL 여정]** 도메인을 선택하십시오.

   여정 도메인이 선택된 ![규칙 집합 속성](assets/journey-formula-rule-set-journey.png){width="60%"}

1. 규칙 집합 속성에서 **[!UICONTROL 순위 메서드]**&#x200B;을(를) 기본 **[!UICONTROL 우선 순위]** 대신 **[!UICONTROL 수식]**(으)로 설정합니다.

1. 드롭다운 목록에서 생성한 순위 공식을 선택합니다.

   ![드롭다운 목록에서 등급 수식을 선택한 규칙 집합](assets/journey-rule-set-formula.png){width="60%"}

1. 규칙 세트에 추가할 여정 한도 규칙을 만듭니다. [방법 알아보기](journey-capping.md#create-rule)

1. 규칙 세트를 저장합니다.

이제 공식이 규칙 세트에 지정됩니다. 그런 다음 해당 규칙 세트를 여정에 적용할 수 있습니다.

## 여정에 규칙 세트 적용 {#assign-rule-set-to-journey}

여정에 규칙 세트를 지정하려면 아래 단계를 따르십시오.

1. 규칙 세트를 할당할 여정을 만들거나 엽니다. [여정 만드는 방법 알아보기](../building-journeys/journey-gs.md)

1. 여정 속성의 드롭다운 목록에서 규칙 세트를 선택합니다.  [방법을 알아보세요](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >한 번에 하나의 여정 세트만 규칙에 적용할 수 있습니다.

1. 여정을 저장합니다.

이 여정 세트를 사용하는 모든 규칙은 상한선이 적용될 때 선택한 수식으로 순위가 지정됩니다.

규칙 집합 및 등급 수식의 수행 방식을 모니터링하려면 개요 보고서의 [여정 제한 및 충돌](../reports/channel-report-cja.md#rule-sets) 섹션을 참조하십시오.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.
-->
