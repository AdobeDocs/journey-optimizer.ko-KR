---
product: experience platform
solution: Experience Platform
title: 등급 전략 만들기
description: Adobe Experience Platform에서 등급 전략을 만드는 방법을 알아봅니다.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 5%

---

# AI 등급 {#ai-rankings}

## AI 등급 시작

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use an trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>현재 AI 등급을 사용하여 사용자를 선택하기만 하면 조기 액세스에서 사용할 수 있습니다.

이 기능을 사용하면 비즈니스 목표를 기반으로 다른 **순위 전략**&#x200B;을 만들 수 있습니다. 의사 결정(이전의 오퍼 활동)에 이러한 다양한 목표 기반 전략을 사용하여, 다양한 등급 전략이 목표에 미치는 영향을 이해하는 데 도움이 됩니다.

예를 들어 이메일 채널에 대한 등급 전략과 푸시 채널에 대한 등급 전략을 선택할 수 있습니다. 각 채널에 대해, 훈련된 모델 시스템은 여러 데이터 포인트를 활용하여 오퍼의 우선 순위 점수 또는 [등급 공식](create-ranking-formulas.md)을 고려하지 않고, 지정된 배치에 대해 먼저 제시해야 하는 오퍼를 결정합니다.

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

등급 전략이 만들어지면 결정에서 배치에 할당합니다. [결정](../offer-activities/configure-offer-selection.md)에서 오퍼 선택을 구성합니다.

## 등급 전략 만들기 {#create-ranking-strategy}

등급 전략을 만들려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Components]** 메뉴에 액세스한 다음 **[!UICONTROL AI rankings]** 탭을 선택합니다.

   ![](../../assets/ai-ranking-list.png)

   지금까지 생성된 모든 순위 전략들이 나열됩니다.

1. **[!UICONTROL Create strategy]** 단추를 클릭합니다.

1. 다음 필드를 채웁니다.

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**: 입력해야 하는 고유한 이름입니다.

   * **[!UICONTROL Model type]**: 현재 유일하게 지원되는 모델 유형은  **[!UICONTROL Auto-optimization]**&#x200B;입니다.<!--More will be supported in the future so the drop-down list will be enabled.-->

   * **[!UICONTROL Optimization metric]**:

      이 옵션을 통해 마케터는 시스템 학습 모델을 만들고 교육하는 방법을 선택할 수 있습니다. 표시된 오퍼, 이메일을 클릭한 오퍼 및/또는 웹에서 클릭한 오퍼를 기반으로 합니다.

      >[!NOTE]
      >
      >필요한 경우 모든 지표 유형을 선택할 수 있습니다.

      다음과 같은 두 가지 유형의 최적화 지표가 있습니다.
      * **[!UICONTROL Impression]**: 현재 노출 이벤트는 표시되는 모든 오퍼에 해당합니다.
      * **[!UICONTROL Conversion]**: 전환 이벤트는 이메일 또는 웹을 통해 클릭을 생성하는 모든 오퍼에 해당합니다.

      선택한 모든 노출 이벤트 및/또는 전환 이벤트는 제공된 Web SDK 또는 Mobile SDK를 사용하여 자동으로 캡처됩니다. 자세한 내용은 [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en)를 참조하십시오.

   * **[!UICONTROL Dataset ID]**: 전환의 경우 드롭다운 목록에서 이벤트를 선택하여 이벤트를 수집할 데이터 세트를 제공해야 합니다. [이 섹션](#create-dataset)에서 이러한 데이터 집합을 만드는 방법을 알아봅니다. <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >**[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹과 연결된 스키마에서 생성된 데이터 세트(이전에 mixin이라고 함)만 드롭다운 목록에 표시됩니다.

1. 등급 전략을 저장하고 활성화합니다.

   ![](../../assets/ai-ranking-save-activate.png)

이제 배치에 적합한 오퍼의 등급을 매기는 결정에 사용할 준비가 되었습니다. 자세한 내용은 [이 섹션](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->을 참조하십시오.

## 이벤트를 수집할 데이터 세트 만들기 {#create-dataset}

전환 이벤트를 수집할 데이터 세트를 만들어야 합니다. 먼저 데이터 세트에 사용할 스키마를 만듭니다.

1. **[!UICONTROL Data Management]** 메뉴에서 **[!UICONTROL Schema]** 를 선택하고 **[!UICONTROL Browse]** 탭으로 이동한 다음 **[!UICONTROL Create schema]** 를 클릭합니다.

   ![](../../assets/ai-ranking-create-schema.png)

1. **[!UICONTROL XDM ExperienceEvent]**&#x200B;을 선택합니다.

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    [XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)의 XDM 스키마 및 필드 그룹에 대해 자세히 알아보십시오.


1. **[!UICONTROL Search]** 필드에 &quot;제안 상호 작용&quot;을 입력하고 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹을 선택합니다.

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    데이터 집합에 사용할 스키마에 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹이 연결되어 있어야 합니다. 그렇지 않으면 순위 전략에서 사용할 수 없습니다.

1. **[!UICONTROL Add field groups]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >필드 그룹은 이전에 mixin이라고 불렀습니다.


1. 이름을 입력하고 스키마를 저장합니다.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    스키마 구성](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas)의 기본 사항에서 스키마 빌드에 대해 자세히 알아보십시오.[

이제 이 스키마를 사용하여 데이터 세트를 만들 준비가 되었습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. **[!UICONTROL Data Management]** 메뉴에서 **[!UICONTROL Datasets]** 를 선택하고 **[!UICONTROL Browse]** 탭으로 이동한 다음 **[!UICONTROL Create dataset]** 를 클릭합니다.

   ![](../../assets/ai-ranking-create-dataset.png)

1. **[!UICONTROL Create dataset from schema]**&#x200B;를 선택합니다.

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. 목록에서 방금 만든 스키마를 선택합니다.

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Name]** 필드에 데이터 세트에 대한 고유한 이름을 입력하고 **[!UICONTROL Finish]** 를 클릭합니다.

   ![](../../assets/ai-ranking-dataset-name.png)

이제 [등급 전략](#create-ranking-strategy)을 만들 때 전환 이벤트를 수집하도록 데이터 세트를 선택할 준비가 되었습니다.

<!--## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).-->

