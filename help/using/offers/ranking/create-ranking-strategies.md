---
product: experience platform
solution: Experience Platform
title: AI 모델 만들기
description: AI 모델을 만들어 오퍼의 등급을 매기는 방법을 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 4f331eff73991c32682ba2c1ca5f6b7341a561e1
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 6%

---

# AI 모델 만들기 {#ai-rankings}

[!DNL Journey Optimizer] 을(를) 통해 다음을 만들 수 있습니다. **AI 모델** 비즈니스 목표에 따라 오퍼의 등급을 지정합니다.

>[!CAUTION]
>
>AI 모델을 생성, 편집 또는 삭제하려면 **순위 전략 관리** 권한. [자세히 알아보기](../../administration/high-low-permissions.md#manage-ranking-strategies)

## AI 모델 만들기 {#create-ranking-strategy}

AI 모델을 만들려면 아래 단계를 수행합니다.

1. 전환 이벤트가 수집될 데이터 세트를 만듭니다. [방법 알아보기](../data-collection/create-dataset.md)

1. 다음에서 **[!UICONTROL 구성 요소]** 메뉴, 액세스 **[!UICONTROL 순위]** 탭을 선택한 다음 를 선택합니다 **[!UICONTROL AI 모델]**.

   ![](../assets/ai-ranking-list.png)

   지금까지 만든 모든 AI 모델이 나열됩니다.

1. 다음을 클릭합니다. **[!UICONTROL AI 모델 만들기]** 단추를 클릭합니다.

1. AI 모델의 고유한 이름과 설명을 지정한 다음 만들려는 AI 모델의 유형을 선택합니다.

   * **[!UICONTROL 자동 최적화]** 는 과거 오퍼 성능을 기반으로 오퍼를 최적화합니다. [자세히 알아보기](auto-optimization-model.md)
   * **[!UICONTROL 개인화된 최적화]** 세그먼트 및 오퍼 성능을 기반으로 오퍼를 최적화하고 개인화합니다. [자세히 알아보기](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >다음 **[!UICONTROL 최적화 지표]** 섹션에는 오퍼의 순위를 계산하기 위해 AI 모델이 사용하는 전환 이벤트에 대한 정보가 제공됩니다.
   >
   >[!DNL Journey Optimizer] 을 기반으로 오퍼 등급 지정 **전환율** (전환율 = 총 전환 이벤트 수 / 총 노출 이벤트 수). 전환율은 두 가지 유형의 지표를 사용하여 계산됩니다.
   >* **노출 이벤트** (표시되는 오퍼)
   >* **전환 이벤트** (이메일 또는 웹을 통해 클릭을 초래하는 오퍼).

   >
   >이러한 이벤트는 제공된 Web SDK 또는 Mobile SDK를 사용하여 자동으로 캡처됩니다. 에서 자세히 알아보기 [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko-KR).

1. 전환 및 노출 이벤트가 수집되는 데이터 세트를 선택합니다. 에서 이러한 데이터 세트를 만드는 방법 알아보기 [이 섹션](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >와(과) 연결된 스키마에서 생성된 데이터 세트만 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹(이전의 mixin)이 드롭다운 목록에 표시됩니다.

1. 다음을 만드는 경우 **[!UICONTROL 개인화된 최적화]** AI 모델, AI 모델을 교육하는 데 사용할 세그먼트를 선택합니다.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >최대 5개의 세그먼트를 선택할 수 있습니다.

1. AI 모델을 저장하고 활성화합니다.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

이제 오퍼가 표시 및/또는 클릭될 때마다 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 를 사용하는 필드 그룹 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 또는 Mobile SDK입니다.

이벤트 유형(표시된 오퍼 또는 클릭한 오퍼)을 보낼 수 있으려면 Adobe Experience Platform으로 전송되는 경험 이벤트의 각 이벤트 유형에 대해 올바른 값을 설정해야 합니다. [방법 알아보기](../data-collection/schema-requirement.md)