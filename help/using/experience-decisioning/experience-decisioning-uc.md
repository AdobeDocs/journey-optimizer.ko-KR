---
title: 결정 사용 사례
description: 코드 기반 채널을 사용한 실험을 사용하여 의사 결정을 만드는 방법에 대해 알아봅니다
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: bfc16476f525328b2b8451bfdd57b6b2027db916
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 5%

---

# 결정 사용 사례 {#experience-decisioning-uc}

이 사용 사례에서는 [!DNL Journey Optimizer] 코드 기반 채널에서 Decisioning을 사용하는 데 필요한 모든 단계를 제공합니다.

이 예에서는 특정 순위 공식이 사전 할당된 오퍼 우선 순위보다 더 나은 성과를 낼지 확신할 수 없습니다.

대상 대상에 가장 적합한 성과를 측정하려면 두 개의 게재 처리를 정의하는 [콘텐츠 실험](../content-management/content-experiment.md)을 사용하여 캠페인을 만드십시오.

* 첫 번째 처리에서는 우선 순위를 순위 방법으로 사용합니다.
* 두 번째 처리에서는 순위 방법을 사용합니다.

## 선택 전략 만들기

먼저 우선 순위를 순위 방법으로 하는 전략과 공식을 순위 방법으로 하는 전략, 이렇게 두 가지 선택 전략을 구축해야 합니다.

>[!NOTE]
>
>선택 전략을 실행하지 않고도 단일 결정 항목을 만들 수도 있습니다. 각 항목에 대해 설정된 우선 순위가 적용됩니다.

### 첫 번째 선택 전략 만들기

우선 순위를 순위 방법으로 사용하여 첫 번째 선택 전략을 작성하려면 아래 단계를 수행합니다.

1. 의사 결정 항목을 만듭니다. [방법 알아보기](items.md)

1. 다른 항목과 비교하여 결정 항목의 **[!UICONTROL 우선 순위]**&#x200B;를 설정하십시오. 프로필이 여러 항목에 적격인 경우 우선순위가 더 높을수록 항목이 다른 항목에 우선합니다.

   ![](assets/exd-uc-item-priority.png){width="80%"}

   >[!NOTE]
   >
   >우선 순위는 정수 데이터 형식입니다. 정수 데이터 유형인 모든 속성에는 정수 값(소수점 없음)이 포함되어야 합니다.

1. 결정 항목의 적격성을 설정합니다.

   * 항목을 특정 프로필로만 제한하도록 대상 또는 규칙을 정의합니다. [자세히 알아보기](items.md#eligibility)

   * 최대 가용량 규칙을 설정하여 오퍼를 표시할 수 있는 최대 횟수를 정의합니다. [자세히 알아보기](items.md#capping)

1. 필요한 경우 위의 단계를 반복하여 추가 결정 항목을 만듭니다.

1. 결정 항목이 포함될 **컬렉션**&#x200B;을 만듭니다. [자세히 알아보기](collections.md)

1. [선택 전략](selection-strategies.md#create-selection-strategy)을(를) 만들고 고려할 오퍼가 포함된 [컬렉션](collections.md)을(를) 선택하십시오.

1. 각 프로필에 가장 적합한 오퍼를 선택하는 데 사용할 [등급 메서드를 선택](#select-ranking-method)합니다. 이 경우 **[!UICONTROL 오퍼 우선 순위]**&#x200B;를 선택하십시오. 여러 오퍼가 이 전략에 적합한 경우 Decisioning 엔진은 오퍼에서 **[!UICONTROL 우선 순위]**(으)로 설정된 값을 사용합니다. [자세히 알아보기](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png){width="80%"}

### 두 번째 선택 전략 만들기

순위 방법으로 공식을 선택하여 두 번째 선택 전략을 작성하려면 아래 단계를 수행합니다.

1. 의사 결정 항목을 만듭니다. [방법 알아보기](items.md)

   <!--Do you need to set the same **[!UICONTROL Priority]** as for the first decision item, or it won't be considered at all?-->

1. 결정 항목의 적격성을 설정합니다.

   * 항목을 특정 프로필로만 제한하도록 대상 또는 규칙을 정의합니다. [자세히 알아보기](items.md#eligibility)

   * 최대 가용량 규칙을 설정하여 오퍼를 표시할 수 있는 최대 횟수를 정의합니다. [자세히 알아보기](items.md#capping)

1. 필요한 경우 위의 단계를 반복하여 추가 결정 항목을 만듭니다.

1. 결정 항목이 포함될 **컬렉션**&#x200B;을 만듭니다. [자세히 알아보기](collections.md)

1. [선택 전략](selection-strategies.md#create-selection-strategy)을(를) 만들고 고려할 오퍼가 포함된 [컬렉션](collections.md)을(를) 선택하십시오.

1. [각 프로필에 가장 적합한 오퍼를 선택하는 데 사용할 순위 방법을 선택하십시오](#select-ranking-method). 이 경우 **[!UICONTROL 공식]**&#x200B;을 선택하여 게재할 적격 오퍼를 결정할 특정 계산된 점수를 사용하십시오. [자세히 알아보기](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

## 코드 기반 경험 캠페인 구축

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

두 선택 전략을 구성하고 나면 성과가 가장 좋은 전략을 비교하기 위해 각 전략에 대해 서로 다른 처리를 정의하는 코드 기반 경험 캠페인을 만듭니다.

1. 캠페인을 만들고 **[!UICONTROL 코드 기반 경험]** 작업을 선택하십시오. [자세히 알아보기](../code-based/create-code-based.md)

1. 캠페인 요약 페이지에서 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하여 콘텐츠 실험 구성을 시작합니다. [자세히 알아보기](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png){width="80%"}

1. 캠페인 요약 페이지에서 코드 기반 구성을 선택하고 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭합니다.

   ![](assets/exd-uc-edit-cbe-content.png){width="80%"}

1. 콘텐츠 편집 창에서 **처리 A**&#x200B;의 개인화를 시작하려면 **[!UICONTROL 코드 편집]**&#x200B;을 클릭하세요.

   ![](assets/exd-uc-experiment-treatment-a.png){width="80%"}

1. [코드 편집기](../code-based/create-code-based.md#edit-code)에서 **[!UICONTROL 의사 결정 정책]**&#x200B;을 선택하고 **[!UICONTROL 의사 결정 정책 추가]**&#x200B;를 클릭한 다음 의사 결정 세부 정보를 입력하십시오. [자세히 알아보기](create-decision.md#add)

   ![](assets/decision-code-based-create.png)

1. **[!UICONTROL 전략 시퀀스]** 섹션에서 **[!UICONTROL 추가]** 단추를 클릭하고 **[!UICONTROL 선택 전략]**&#x200B;을 선택하세요. [자세히 알아보기](create-decision.md#select)

   ![](assets/decision-code-based-strategy-sequence.png){width="80%"}

   >[!NOTE]
   >
   >선택 전략을 실행하지 않고도 **[!UICONTROL 결정 항목]**&#x200B;을 선택하여 단일 항목을 추가할 수도 있습니다. 각 항목에 대해 설정된 우선 순위가 적용됩니다.

1. 생성한 첫 번째 전략을 선택합니다.

   ![](assets/exd-uc-experiment-strategy-priority.png){width="80%"}

1. 변경 내용을 저장하고 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 새 결정은 **[!UICONTROL 결정 정책]**&#x200B;에 추가됩니다.

1. **[!UICONTROL 정책 삽입]** 단추를 클릭합니다. 결정 정책에 해당하는 코드가 추가됩니다. 그런 다음 프로필 속성을 포함하여 코드에 원하는 모든 속성을 추가합니다. [자세히 알아보기](create-decision.md#use-decision-policy)

   ![](assets/exd-uc-experiment-insert-policy.png){width="80%"}

1. 변경 내용을 저장합니다.

1. 콘텐츠 편집 창으로 돌아가서 + 단추를 선택하여 **처리 B**&#x200B;를 추가하고 선택한 다음 **[!UICONTROL 코드 편집]**&#x200B;을 클릭합니다.

   ![](assets/exd-uc-experiment-treatment-b.png){width="80%"}

1. 위의 단계를 반복하여 다른 결정 정책을 만들고 만든 두 번째 선택 전략을 선택합니다. <!--Do you need to create exactly the same content to compare only the ranking method?-->

1. 변경 내용을 저장하고 [코드 기반 경험 캠페인을 게시](../code-based/publish-code-based.md)합니다.

[실험 캠페인 보고서](../reports/campaign-global-report-cja-experimentation.md) 및 [의사 결정에 대한 보고서](cja-reporting.md)(으)로 캠페인의 성과를 추적할 수 있습니다. <!--TBC how to check which treatment performs best-->