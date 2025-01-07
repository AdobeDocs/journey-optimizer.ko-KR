---
title: 선택 전략 만들기
description: 선택 전략을 만드는 방법을 알아봅니다
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 1b73b398-050a-40bb-a8ae-1c66e3e26ce8
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 21%

---

# 선택 전략 만들기 {#selection-strategies}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_strategies"
>title="선택 전략 정의"
>abstract="선택 전략은 재사용 가능하며, 결정 정책에서 선택 시 표시할 제안을 결정하기 위한 자격 조건 및 순위 지정 방법과 관련된 컬렉션으로 구성됩니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision.html" text="결정 정책 만들기"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_eligibility"
>title="적격 프로필 제한"
>abstract="이 선택 전략에 대한 오퍼 선택을 제한할 수 있습니다. 기본적으로 모든 프로필이 적격하지만 대상자 또는 규칙을 사용하여 특정 프로필로만 오퍼 선택을 제한할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="대상자 사용"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/selection/rules.html" text="의사 결정 규칙 사용"

선택 전략은 다시 사용할 수 있으며, [의사 결정 정책](create-decision.md)에서 선택할 때 표시할 오퍼를 결정하는 자격 제한 및 순위 방법과 관련된 컬렉션으로 구성됩니다.

## 선택 전략 액세스 및 관리

1. **[!UICONTROL Decisioning]** > **[!UICONTROL 전략 설정]** > **[!UICONTROL 선택 전략]**(으)로 이동합니다.

1. 지금까지 만든 모든 선택 전략이 나열됩니다. 필터를 사용하여 등급 방법에 따라 전략을 검색할 수 있습니다.

   ![](assets/strategy-list-filters.png)

1. 편집할 선택 전략 이름을 클릭합니다.

1. 각 전략에 대해 선택한 컬렉션, 등급 방법 및 자격 조건도 표시됩니다. 각 컬렉션 이름 옆에 있는 아이콘을 클릭하여 컬렉션을 직접 편집할 수 있습니다.

   ![](assets/strategy-list-edit-collection.png)

## 선택 전략 만들기 {#create-selection-strategy}

선택 전략을 만들려면 아래 단계를 수행합니다.

1. **[!UICONTROL 선택 전략]** 인벤토리에서 **[!UICONTROL 선택 전략 만들기]**&#x200B;를 클릭합니다.

   ![](assets/strategy-create-button.png)

1. 전략의 이름을 추가합니다.

   >[!NOTE]
   >
   >현재 기본 **[!UICONTROL 오퍼]** 카탈로그만 사용할 수 있습니다.

1. 이름부터 시작하여 선택 전략에 대한 세부 정보를 입력합니다.

   ![](assets/strategy-create-screen.png)

1. 고려할 오퍼가 포함된 [컬렉션](collections.md)을(를) 선택하십시오.

1. 이 선택 전략에 대한 오퍼 선택을 제한하려면 **[!UICONTROL 자격]** 필드를 사용하십시오.

   ![](assets/strategy-create-eligibility.png)

   * Experience Platform 대상의 구성원으로 오퍼 선택을 제한하려면 **[!UICONTROL 대상]**&#x200B;을(를) 선택하고 목록에서 대상을 선택하십시오. [대상자를 사용한 작업 방법 알아보기](../audience/about-audiences.md)

   * 결정 규칙과 함께 선택 제한을 추가하려면 **[!UICONTROL 결정 규칙]** 옵션을 사용하고 선택한 규칙을 선택하십시오. [규칙을 만드는 방법 알아보기](rules.md)

1. 각 프로필에 가장 적합한 오퍼를 선택하는 데 사용할 순위 방법을 정의합니다. [자세히 알아보기](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * 기본적으로 여러 오퍼가 이 전략에 적합한 경우 [오퍼 우선 순위](#offer-priority) 메서드는 오퍼에 정의된 값을 사용합니다.

   * 특정 계산된 점수를 사용하여 게재할 적격 오퍼를 선택하려면 [공식](#ranking-formula) 또는 [AI 모델](#ai-ranking)을 선택하십시오.

1. Click **[!UICONTROL Create]**. 이제 [결정 정책](create-decision.md)에서 사용할 준비가 되었습니다.

## 순위 지정 방법 선택 {#select-ranking-method}

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_ranking"
>title="오퍼 순위 지정하는 방법에 대한 정의"
>abstract="특정 선택 전략에 여러 오퍼가 적합한 경우 선택 전략을 만들 때 각 프로필에 가장 적합한 오퍼를 선택하는 방법(우선순위 또는 순위 공식)을 선택합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision.html" text="결정 정책 만들기"

여러 오퍼가 주어진 선택 전략에 적합한 경우 선택 전략을 생성할 때 각 프로필에 가장 적합한 오퍼를 선택하는 방법을 선택할 수 있습니다. 오퍼의 순위를 지정할 수 있는 기준:

* [오퍼 우선 순위](#offer-priority)
* [공식](#ranking-formula)
* [AI 등급](#ai-ranking)

### 오퍼 우선 순위 {#offer-priority}

기본적으로 의사 결정 정책에서 일부 오퍼가 지정된 배치에 적합한 경우 **우선 순위**&#x200B;가 가장 높은 항목이 먼저 고객에게 전달됩니다.

![](assets/item-priority.png)

[결정 항목](items.md)을 만들 때 오퍼의 우선 순위 점수가 할당됩니다.

### 순위 공식 {#ranking-formula}

Journey Optimizer에서는 오퍼 우선 순위 외에도 **등급 수식**&#x200B;을 만들 수 있습니다. 오퍼의 우선 순위 점수를 고려하지 않고, 주어진 배치에 대해 먼저 제시해야 할 오퍼를 결정하는 수식입니다.

예를 들어 종료 날짜가 지금부터 24시간 미만인 모든 오퍼의 우선순위를 늘리거나, 프로필의 관심 지점이 &quot;실행 중&quot;인 경우 &quot;실행 중&quot; 카테고리의 오퍼를 늘릴 수 있습니다. [이 섹션](ranking.md)에서 순위 공식을 만드는 방법을 알아봅니다.

만든 후에는 이 공식을 선택 전략에 사용할 수 있습니다. 이 선택 전략을 사용할 때 여러 오퍼를 표시할 수 있는 경우, 의사 결정은 선택한 공식을 사용하여 먼저 게재할 오퍼를 계산합니다.

### AI 등급 {#ai-ranking}

AI 모델을 선택하여 주어진 프로필에 대해 표시할 오퍼에 자동으로 등급을 지정하는 교육된 모델 시스템을 사용할 수도 있습니다. [이 섹션](ranking.md)에서 AI 모델을 만드는 방법을 알아봅니다.

AI 모델이 만들어지면 선택 전략에 사용할 수 있습니다. 여러 오퍼가 적합한 경우 교육된 모델 시스템은 이 선택 전략에 대해 먼저 제시해야 하는 오퍼를 결정합니다.
