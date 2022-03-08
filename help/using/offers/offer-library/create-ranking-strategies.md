---
product: experience platform
solution: Experience Platform
title: 등급 전략 만들기
description: AI 모델을 만들어 오퍼의 등급을 지정하는 방법을 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: dcadbbcf8b2cd8422a189b8d02f222f32dd12c54
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 5%

---

# AI 모델 만들기 {#ai-rankings}

## 등급 전략 만들기 {#create-ranking-strategy}

등급 전략을 만들려면 아래 단계를 수행하십시오.

1. 액세스 권한 **[!UICONTROL Components]** 메뉴를 선택한 다음 **[!UICONTROL AI rankings]** 탭.

   ![](../../assets/ai-ranking-list.png)

   지금까지 생성된 모든 순위 전략들이 나열됩니다.

1. **[!UICONTROL Create strategy]** 단추를 클릭합니다.

1. 다음 필드를 채웁니다.

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**: 입력해야 하는 고유한 이름입니다.

   * **[!UICONTROL Model type]**: 현재 [!DNL Journey Optimizer] 유일하게 지원되는 모델 유형은 다음과 같습니다. **[!UICONTROL Auto-optimization]**. [자세히 알아보기](ai-ranking.md#auto-optimization)

   * **[!UICONTROL Optimization metric]**:

      이 옵션을 통해 마케터는 시스템 학습 모델을 만들고 교육하는 방법을 선택할 수 있습니다. 표시된 오퍼, 이메일을 클릭한 오퍼 및/또는 웹에서 클릭한 오퍼를 기반으로 합니다.

      >[!NOTE]
      >
      >필요한 경우 모든 지표 유형을 선택할 수 있습니다.

      다음과 같은 두 가지 유형의 최적화 지표가 있습니다.
      * **[!UICONTROL Impression]**: 현재 노출 이벤트는 표시되는 모든 오퍼에 해당합니다.
      * **[!UICONTROL Conversion]**: 전환 이벤트는 이메일 또는 웹을 통해 클릭을 생성하는 모든 오퍼에 해당합니다.

      선택한 모든 노출 이벤트 및/또는 전환 이벤트는 제공된 Web SDK 또는 Mobile SDK를 사용하여 자동으로 캡처됩니다. 자세한 내용은 [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

   * **[!UICONTROL Dataset ID]**: 전환의 경우 드롭다운 목록에서 이벤트를 선택하여 이벤트를 수집할 데이터 세트를 제공해야 합니다. 에서 이러한 데이터 세트를 만드는 방법을 알아봅니다 [이 섹션](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >스키마에서 생성된 데이터 세트만 과 연결됩니다 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹(이전에 mixin이라고 함)이 드롭다운 목록에 표시됩니다.

1. 등급 전략을 저장하고 활성화합니다.

   ![](../../assets/ai-ranking-save-activate.png)

이제 배치에 적합한 오퍼의 등급을 매기는 결정에 사용할 준비가 되었습니다. 추가 정보 [이 섹션](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## 이벤트를 수집할 데이터 세트 만들기 {#create-dataset}

전환 이벤트를 수집할 데이터 세트를 만들어야 합니다. 먼저 데이터 세트에 사용할 스키마를 만듭니다.

1. 에서 **[!UICONTROL Data Management]** 메뉴, 선택 **[!UICONTROL Schema]**&#x200B;로 이동합니다. **[!UICONTROL Browse]** 탭을 클릭하고 **[!UICONTROL Create schema]**.

   ![](../../assets/ai-ranking-create-schema.png)

1. 선택 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    XDM 스키마 및 필드 그룹의 [XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko).


1. 에서 **[!UICONTROL Search]** 필드를 입력하고 &quot;제안 상호 작용&quot;을 입력하고 을 선택합니다 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹.

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    데이터 집합에 사용할 스키마에는 **[!UICONTROL Experience Event - Proposition Interactions]** 연결된 필드 그룹입니다. 그렇지 않으면 순위 전략에서 사용할 수 없습니다.

1. **[!UICONTROL Add field groups]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >필드 그룹은 이전에 mixin이라고 불렀습니다.

1. 이름을 입력하고 스키마를 저장합니다.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    스키마 빌드에 대한 자세한 내용 [스키마 작성 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

이제 이 스키마를 사용하여 데이터 세트를 만들 준비가 되었습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 에서 **[!UICONTROL Data Management]** 메뉴, 선택 **[!UICONTROL Datasets]**&#x200B;로 이동합니다. **[!UICONTROL Browse]** 탭을 클릭하고 **[!UICONTROL Create dataset]**.

   ![](../../assets/ai-ranking-create-dataset.png)

1. **[!UICONTROL Create dataset from schema]**&#x200B;를 선택합니다.

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. 목록에서 방금 만든 스키마를 선택합니다.

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. 에서 데이터 세트에 대한 고유한 이름을 제공합니다 **[!UICONTROL Name]** 필드를 입력하고 **[!UICONTROL Finish]**.

   ![](../../assets/ai-ranking-dataset-name.png)

이제 데이터 세트를 선택하여 이벤트 데이터를 수집할 준비가 되었습니다. [등급 전략 생성](#create-ranking-strategy).

## 오퍼 스키마 요구 사항 {#schema-requirements}

이 시점에서 다음을 수행해야 합니다.

* 순위 전략,
* 캡처할 이벤트 유형, 즉 표시된 오퍼(노출) 및/또는 클릭한 오퍼(전환)를 정의합니다.
* 및 이벤트 데이터를 수집할 데이터 세트에 포함되어 있습니다.

이제 오퍼가 표시되고/또는 클릭할 때마다 해당 이벤트가 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹을 사용하여 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} 또는 Mobile SDK입니다.

이벤트 유형(표시된 오퍼 또는 클릭한 오퍼)을 보낼 수 있으려면 Adobe Experience Platform으로 전송되는 경험 이벤트의 각 이벤트 유형에 대해 올바른 값을 설정해야 합니다. 다음은 JavaScript 코드에 구현해야 하는 스키마 요구 사항입니다.

### 표시된 오퍼 시나리오

**이벤트 유형:** `decisioning.propositionDisplay`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 배치 수집
+++**샘플 페이로드:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### 클릭한 오퍼 시나리오

**이벤트 유형:** `decisioning.propositionInteract`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 배치 수집
+++**샘플 페이로드:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->

