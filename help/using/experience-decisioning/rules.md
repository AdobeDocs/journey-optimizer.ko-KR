---
title: 의사 결정 규칙
description: 의사 결정 규칙 작업 방법 알아보기
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 16%

---

# 의사 결정 규칙 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="의사 결정 규칙 만들기"
>abstract="의사 결정 규칙을 사용하면 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한 사항을 적용하여 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 어떤 대상에게 제공할지 정확하게 제어할 수 있습니다."

>[!BEGINSHADEBOX &quot;이 설명서 안내서에서 확인할 수 있는 사항&quot;]

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 의사 결정 항목 관리: [항목 카탈로그 구성](catalogs.md) - [의사 결정 항목 만들기](items.md) - [항목 컬렉션 관리](collections.md)
* 항목의 선택 사항 구성: **[의사 결정 규칙 만들기](rules.md)** - [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

의사 결정 규칙을 사용하면 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한 사항을 적용하여 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 어떤 대상에게 제공할지 정확하게 제어할 수 있습니다.

예를 들어, 여성을 위해 디자인된 요가 관련 제품을 갖춘 의사 결정 항목이 있는 시나리오를 생각해 보자. 의사 결정 규칙을 사용하여 이러한 항목이 성별이 &#39;여성&#39;이고 &#39;요가&#39;에서 &#39;관심 영역&#39;을 표시한 프로필에만 표시되도록 지정할 수 있습니다.

>[!NOTE]
>
>항목 및 선택 전략 수준 결정 규칙 외에도 캠페인 수준에서 의도한 대상자를 정의할 수도 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#audience)

의사 결정 규칙 목록은 **[!UICONTROL 구성]** / **[!UICONTROL 의사 결정 규칙]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](assets/decision-rules-list.png)

## 의사 결정 규칙 만들기 {#create}

의사 결정 규칙을 만들려면 다음 단계를 수행합니다.

1. 다음으로 이동 **[!UICONTROL 구성]** / **[!UICONTROL 의사 결정 규칙]** 그런 다음 을 클릭합니다. **[!UICONTROL 규칙 만들기]** 단추를 클릭합니다.

1. 의사 결정 규칙 만들기 화면이 열립니다. 규칙에 이름을 지정하고 설명을 제공합니다.

1. Adobe Experience Platform 세그먼트 빌더를 사용하여 필요에 따라 의사 결정 규칙을 만듭니다. 이렇게 하려면 프로필 속성, 대상 또는 Adobe Experience Platform에서 제공되는 컨텍스트 데이터와 같은 다양한 데이터 소스를 활용할 수 있습니다. [의사 결정 규칙에서 컨텍스트 데이터를 활용하는 방법 알아보기](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >의사 결정 규칙을 만들기 위해 제공된 세그먼트 빌더는 Adobe Experience Platform 세그먼테이션 서비스와 함께 사용되는 세그먼트 빌더와 비교하여 몇 가지 특성을 제공합니다.  그러나 설명서에 설명된 전역 프로세스는 의사 결정 규칙을 작성하는 데 여전히 유효합니다. [세그먼트 정의를 작성하는 방법 알아보기](../audience/creating-a-segment-definition.md)

1. 작업 영역에서 새 필드를 추가하고 구성할 때 **[!UICONTROL 대상 속성]** 창에는 대상자에 속한 예상 프로필에 대한 정보가 표시됩니다. 클릭 **[!UICONTROL 예상 새로 고침]** 을 클릭하여 데이터를 업데이트합니다.

   >[!NOTE]
   >
   >규칙 매개 변수에 컨텍스트 데이터와 같이 프로필에 없는 데이터가 포함되어 있으면 프로필 추정치를 사용할 수 없습니다.

1. 결정 규칙이 준비되면 **[!UICONTROL 저장]**. 생성된 규칙은 목록에 표시되며 의사 결정 항목 및 선택 전략에서 사용하여 프로필에 대한 의사 결정 항목 표시를 제어할 수 있습니다.

## 의사 결정 규칙의 컨텍스트 데이터 활용 {#context-data}

Experience Decisioning 규칙 만들기 화면에서는 Adobe Experience Platform에서 사용할 수 있는 정보를 활용하여 의사 결정 규칙을 만들 수 있습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 의사 결정 규칙을 디자인할 수 있습니다.

이를 위해서는 먼저 Experience Decisioning에서 사용할 수 있도록 할 데이터를 정의해야 합니다. 완료되면 이 데이터는 의 Experience Decisioning에 원활하게 통합됩니다. **[!UICONTROL 컨텍스트 데이터]** 의사 결정 규칙을 만들 때 사용할 수 있는 탭입니다.

![](assets/decision-rules-context.png)

Adobe Experience Platform 데이터를 사용하여 Experience Decisioning에 데이터를 제공하는 단계는 다음과 같습니다.

1. 만들기 **경험 이벤트 스키마**  Adobe Experience Platform 및 관련 항목 **데이터 세트**. [스키마를 만드는 방법 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 새 Adobe Experience Platform 데이터스트림 만들기:

   1. 다음 위치로 이동 **[!UICONTROL 데이터스트림]** 메뉴 및 선택 **[!UICONTROL 새 데이터스트림]**.

   1. 다음에서 **[!UICONTROL 이벤트 스키마]** 드롭다운 목록에서 앞에서 만든 경험 이벤트 스키마를 선택한 다음 를 클릭합니다. **[!UICONTROL 저장]**.

      ![](assets/decision-rule-context-datastream.png)

   1. 클릭 **[!UICONTROL 서비스 추가]** 서비스로 &quot;Adobe Experience Platform&quot;를 선택합니다. 다음에서 **[!UICONTROL 이벤트 데이터 세트]** 드롭다운 목록에서 이전에 만든 이벤트 데이터 세트를 선택하고 **[!UICONTROL Adobe Journey Optimizer]** 옵션을 선택합니다.

      ![](assets/decision-rules-context-datastream-service.png)

데이터 스트림이 저장되면 선택한 데이터 세트의 정보를 자동으로 가져와 Experience Decisioning에 통합합니다. 일반적으로 약 24시간 이내에 사용할 수 있습니다.

Adobe Experience Platform을 사용하여 작업하는 방법에 대한 추가 지침을 보려면 다음 리소스를 살펴보십시오.

* [XDM(경험 데이터 모델) 스키마](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [데이터 세트](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [데이터스트림](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
