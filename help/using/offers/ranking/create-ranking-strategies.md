---
product: experience platform
solution: Experience Platform
title: AI 모델 만들기
description: AI 모델을 만들어 오퍼의 등급을 매기는 방법을 알아봅니다
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 23%

---

# AI 모델 만들기 {#ai-rankings}

[!DNL Journey Optimizer]을(를) 사용하면 **AI 모델**&#x200B;을(를) 만들어 비즈니스 목표에 따라 오퍼의 등급을 지정할 수 있습니다.

>[!CAUTION]
>
>AI 모델을 만들거나 편집하거나 삭제하려면 **순위 전략 관리** 권한이 있어야 합니다. [자세히 알아보기](../../administration/high-low-permissions.md#manage-ranking-strategies)

## AI 모델 만들기 {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_metric"
>title="최적화 지표"
>abstract="[!DNL Journey Optimizer]는 **전환율**(전환율 = 총 전환 이벤트 수 / 총 노출 이벤트 수)을 기준으로 오퍼의 순위를 매깁니다. 전환율은 다음 두 가지 유형의 지표를 사용하여 계산됩니다. **노출 이벤트**(표시되는 오퍼)와 **전환 이벤트**(이메일이나 웹을 통해 클릭을 유도하는 오퍼). 이러한 이벤트는 제공된 Web SDK 또는 Mobile SDK를 사용하여 자동으로 캡처됩니다."

AI 모델을 만들려면 아래 단계를 수행합니다.

1. 전환 이벤트가 수집될 데이터 세트를 만듭니다. [방법 알아보기](../data-collection/create-dataset.md)

1. **[!UICONTROL 구성 요소]** 메뉴에서 **[!UICONTROL 순위]** 탭에 액세스한 다음 **[!UICONTROL AI 모델]**&#x200B;을(를) 선택합니다.

   ![](../assets/ai-ranking-list.png)

   지금까지 만든 모든 AI 모델이 나열됩니다.

1. **[!UICONTROL AI 모델 만들기]** 단추를 클릭합니다.

1. AI 모델의 고유한 이름과 설명을 지정한 다음 만들려는 AI 모델의 유형을 선택합니다.

   * **[!UICONTROL 자동 최적화]**&#x200B;은(는) 이전 오퍼 성능을 기반으로 오퍼를 최적화합니다. [자세히 알아보기](auto-optimization-model.md)
   * **[!UICONTROL 개인화된 최적화]**&#x200B;은(는) 대상 및 오퍼 성능을 기반으로 오퍼를 최적화하고 개인화합니다. [자세히 알아보기](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >**[!UICONTROL 최적화 지표]** 섹션에서는 오퍼의 순위를 계산하기 위해 AI 모델이 사용하는 전환 이벤트에 대한 정보를 제공합니다.
   >
   >[!DNL Journey Optimizer]는 **전환율**(전환율 = 총 전환 이벤트 수 / 총 노출 이벤트 수)을 기준으로 오퍼의 순위를 매깁니다. 전환율은 두 가지 유형의 지표를 사용하여 계산됩니다.
   >* **노출 이벤트**(표시되는 오퍼)
   >* **전환 이벤트**(전자 메일 또는 웹을 통해 클릭을 발생시키는 오퍼).
   >
   >이러한 이벤트는 제공된 웹 SDK 또는 모바일 SDK을 사용하여 자동으로 캡처됩니다. [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)에서 이에 대해 자세히 알아보세요.

1. 전환 및 노출 이벤트가 수집되는 데이터 세트를 선택합니다. [이 섹션](../data-collection/create-dataset.md)에서 이러한 데이터 세트를 만드는 방법을 알아봅니다. <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >**[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹(이전 이름: mixin)과 연결된 스키마에서 만든 데이터 세트만 드롭다운 목록에 표시됩니다.

1. **[!UICONTROL 개인화된 최적화]** AI 모델을 만드는 경우 AI 모델을 교육하는 데 사용할 세그먼트를 선택하십시오.

   ➡️ [비디오에서 이 기능 살펴보기](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >최대 5개의 대상을 선택할 수 있습니다.

1. AI 모델을 저장하고 활성화합니다.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

이제 오퍼가 표시 및/또는 클릭될 때마다 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 또는 Mobile SDK을 사용하여 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹에 의해 해당 이벤트가 자동으로 캡처되도록 합니다.

이벤트 유형(표시된 오퍼 또는 클릭한 오퍼)을 보낼 수 있으려면 Adobe Experience Platform으로 전송되는 경험 이벤트의 각 이벤트 유형에 대해 올바른 값을 설정해야 합니다. [방법 알아보기](../data-collection/schema-requirement.md)

## 사용 방법 비디오 {#video}

개인화된 최적화 모델을 만드는 방법과 이 모델을 의사 결정에 적용하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3419954?quality=12)
