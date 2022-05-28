---
product: experience platform
solution: Experience Platform
title: AI 모델 만들기
description: AI 모델을 만들어 오퍼의 등급을 지정하는 방법을 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# AI 모델 만들기 {#ai-rankings}

[!DNL Journey Optimizer] 다음을 수행할 수 있습니다. **AI 모델** 비즈니스 목표에 따라 오퍼의 등급을 매깁니다.

>[!CAUTION]
>
>AI 모델을 만들거나, 편집하거나, 삭제하려면 **등급 전략 관리** 권한. [자세히 보기](../../administration/high-low-permissions.md#manage-ranking-strategies)

## AI 모델 만들기 {#create-ranking-strategy}

AI 모델을 만들려면 아래 단계를 수행하십시오.

1. 에서 **[!UICONTROL Components]** 메뉴에서 **[!UICONTROL Ranking]** 탭을 선택하고 **[!UICONTROL AI models]**.

   ![](../assets/ai-ranking-list.png)

   지금까지 만든 모든 AI 모델이 나열됩니다.

1. **[!UICONTROL Create AI model]** 단추를 클릭합니다.

1. AI 모델의 고유 이름과 설명을 지정합니다.

   <!--* **[!UICONTROL Auto-optimization]** optimizes offers based on past offer performance. [Learn more](auto-optimization-model.md)
    * **[!UICONTROL Personalized]** optimizes and personalizes offers based on segments and offer performance. [Learn more](personalized-optimization-model.md)-->

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >다음 **[!UICONTROL Optimization metric]** 섹션에서 AI 모델에서 오퍼의 등급을 계산하는 데 사용되는 전환 이벤트에 대한 정보를 제공합니다.
   >
   >[!DNL Journey Optimizer] 오퍼를 기반으로 등급 지정 **전환율** (전환율 = 총 전환 이벤트 수 / 총 노출 이벤트 수). 전환율은 다음 두 가지 유형의 지표를 사용하여 계산됩니다.
   >* **노출 이벤트** (표시되는 오퍼)
   >* **전환 이벤트** (이메일 또는 웹을 통해 클릭을 발생시키는 오퍼).

   >
   >이러한 이벤트는 제공된 Web SDK 또는 Mobile SDK를 사용하여 자동으로 캡처됩니다. 자세한 내용은 [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

1. 전환 및 노출 이벤트가 수집되는 데이터 세트를 선택합니다. 에서 이러한 데이터 세트를 만드는 방법을 알아봅니다 [이 섹션](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >스키마에서 생성된 데이터 세트만 과 연결됩니다 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹(이전에 mixin이라고 함)이 드롭다운 목록에 표시됩니다.

<!--1. If you are creating a **[!UICONTROL Personalization]** AI model, select the segment(s) to use to train the AI model.

    ![](../assets/ai-ranking-segments.png)

    >[!NOTE]
    >
    >You can select up to 5 segments.-->

1. AI 모델을 저장하고 활성화합니다.

   ![](../assets/ai-ranking-save-activate.png)
