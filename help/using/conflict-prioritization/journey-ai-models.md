---
title: 여정 중재 AI 모델
description: AI 모델을 만들고 사용하여 중재에 사용할 여정의 등급을 매겨 AI 기반 점수를 기반으로 프로필별로 최상의 여정을 선택하는 방법에 대해 알아봅니다.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="제한 공개" type="Informative"
hide: true
hidefromtoc: true
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 4%

---

# AI 모델을 사용하여 여정 등급 지정 {#journey-ai-models}

>[!AVAILABILITY]
>
>이 기능은 현재 제한된 가용성입니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

[!DNL Adobe Journey Optimizer]을(를) 사용하면 프로필이 시스템에서 허용하는 것보다 더 많은 여정에 대한 자격이 있을 때 프로필이 입력할 수 있는 프로필을 제어할 수 있습니다. 이렇게 하려면 [규칙 집합](rule-sets.md)을 사용하여 여정 항목 또는 동시 사용에 대한 제한을 정의할 수 있습니다. 여정이 상한선이 허용하는 것보다 더 많은 여정에 적격인 경우, 각 프로필에 할당된 우선순위에 따라 선택되는 여정이 결정됩니다.

우선 순위를 사용하는 대신 순위 공식에 **AI 모델**&#x200B;을 사용하여 훈련된 모델 점수를 기반으로 여정의 등급을 동적으로 지정할 수도 있습니다.

## AI 모델 만들기 {#create-ai-model}

<!--
Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)
-->

여정 등급에 대한 AI 모델을 만들려면 아래 단계를 따르십시오.

1. 전환 이벤트가 수집될 데이터 세트를 만듭니다. [방법 알아보기](../experience-decisioning/data-collection/create-dataset.md)

1. **[!UICONTROL 오케스트레이션 순위]** 섹션에 액세스한 다음 **[!UICONTROL AI 모델]** 탭을 선택하십시오. 이전에 만든 AI 모델 목록이 표시됩니다.

1. **[!UICONTROL AI 모델 만들기]**&#x200B;를 클릭합니다.

1. 고유한 이름을 지정하고 필요한 경우 AI 모델에 대한 설명을 지정합니다.

   ![이름 및 설명 필드를 표시하는 AI 모델 세부 정보](assets/journey-model-details.png){width="85%"}

   >[!NOTE]
   >
   >순위 객체는 순위 공식이 적용될 엔티티입니다. 기본적으로 순위 개체는 **[!UICONTROL 여정]**(으)로 설정됩니다.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)
-->

1. **[!UICONTROL 최적화 지표]** 섹션에서 기본 [!DNL Customer Journey Analytics] [데이터 보기](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}의 모든 지표가 목록에 표시됩니다. 모델을 최적화할 지표를 선택합니다.

   AI 모델에 대한 Customer Journey Analytics 지표를 나열하는 ![최적화 지표 드롭다운](assets/journey-model-metrics.png){width="70%"}

   [!DNL Journey Optimizer]은(는) **전환율**&#x200B;을(를) 기반으로 순위를 지정합니다(전환율 = 총 전환 이벤트 수 / 총 노출 이벤트 수). 전환율은 다음을 사용하여 계산됩니다.

   * **노출 이벤트**(표시되는 항목)
   * **전환 이벤트**(클릭 또는 전환을 초래하는 항목)

   이러한 이벤트는 웹 SDK 또는 모바일 SDK을 사용하여 자동으로 캡처됩니다. [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 개요에서 자세히 알아보세요.

1. 전환 및 노출 이벤트가 수집되는 데이터 세트를 선택합니다. [이 섹션](../experience-decisioning/data-collection/create-dataset.md)에서 이러한 데이터 세트를 만드는 방법을 알아보세요.

   ![전환 및 노출 이벤트에 대한 데이터 집합 선택](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >**[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹과 연결된 스키마에서 만든 데이터 세트만 드롭다운 목록에 표시됩니다. 최대 5개의 데이터 세트를 선택할 수 있습니다.

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->AI 모델을 교육하는 데 사용할 세그먼트를 선택합니다.

   >[!NOTE]
   >
   >최대 50개의 대상을 선택할 수 있습니다.

1. AI 모델을 저장하고 활성화합니다.

이제 순위 공식을 만들 때 AI 모델을 선택할 수 있습니다.

## 여정의 등급을 지정하려면 공식에서 AI 모델을 참조하십시오 {#reference-ai-model}

이제 AI 모델을 참조로 설정하여 등급 공식을 작성한 후 공식을 여정 세트에 지정하고 규칙 세트를 규칙에 적용할 수 있습니다. 그 방법은 다음과 같습니다.

1. 순위 공식을 만듭니다. [방법 알아보기](journey-ranking-formulas.md#create-journey-ranking-formula)

1. **[!UICONTROL AI 모델 선택]** 단추를 사용하여 수식에 사용할 AI 모델을 선택합니다.

   ![AI 모델 선택 단추를 사용하여 여정 등급 수식 세부 정보](assets/journey-formula-ai-model.png){width="80%"}

1. **[!UICONTROL 기준]** 섹션 중 적어도 하나에서 조건을 정의하고 **[!UICONTROL AI 모델 점수]**&#x200B;를 순위 지정 방법으로 선택합니다. 예를 들어 여정에 &quot;프로모션&quot; 태그가 있는 경우 순위 점수는 AI 모델 점수입니다.

   ![프로모션 태그 기준이 AI 모델 점수를 등급 방법으로 사용하는 등급 수식 예](assets/journey-formula-ex-2.png){width="60%"}

1. 순위 공식을 완료하려면 **[!UICONTROL 만들기]**&#x200B;를 클릭하세요.

1. 이제 규칙 세트를 만들고 순위 방법으로 만든 공식을 선택합니다. [방법 알아보기](journey-ranking-formulas.md#assign-formula-to-ruleset)

1. 여정 최대 가용량 규칙을 만들고 규칙 세트를 저장합니다.

1. 원하는 여정에 규칙 세트를 적용하고 저장합니다. [방법 알아보기](journey-ranking-formulas.md#assign-rule-set-to-journey)

   >[!NOTE]
   >
   >한 번에 하나의 여정 세트만 규칙에 적용할 수 있습니다.

이 여정 세트를 사용하는 모든 규칙은 상한이 적용될 때 선택한 AI 모델을 참조하는 공식으로 순위가 지정됩니다.
