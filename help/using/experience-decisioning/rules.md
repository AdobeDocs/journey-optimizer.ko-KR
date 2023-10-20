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
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 15%

---

# 의사 결정 규칙 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="의사 결정 규칙 만들기"
>abstract="의사 결정 규칙을 사용하면 의사 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한을 적용하여 의사 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 누구에게 제시해야 하는지 정확하게 제어할 수 있습니다."

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 결정 항목 관리
   * [항목 카탈로그 구성](catalogs.md)
   * [결정 항목 만들기](items.md)
   * [항목 컬렉션 관리](collections.md)
* 항목 선택 구성
   * **[의사 결정 규칙 만들기](rules.md)**
   * [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

의사 결정 규칙을 사용하면 의사 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한을 적용하여 의사 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 누구에게 제시해야 하는지 정확하게 제어할 수 있습니다.

예를 들어, 여성을 위해 디자인된 요가 관련 제품을 갖춘 의사 결정 항목이 있는 시나리오를 생각해 보자. 의사 결정 규칙을 사용하면 이러한 항목이 성별이 &#39;여성&#39;이고 &#39;요가&#39;에서 &#39;관심 영역&#39;을 표시한 프로필에만 표시되도록 지정할 수 있습니다.

>[!NOTE]
>
>항목 및 선택 전략 수준 결정 규칙 외에도 캠페인 수준에서 의도한 대상자를 정의할 수도 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#audience)


의사 결정 규칙 목록은 **[!UICONTROL 구성]** / **[!UICONTROL 의사 결정 규칙]** 메뉴 아래의 제품에서 사용할 수 있습니다.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>현재 의사 결정 규칙은 Journey Optimizer의 **의사 결정 관리** 메뉴 아래의 제품에서 사용할 수 있습니다. 그 결과 **[!UICONTROL 의사 결정 규칙]** experience Decisioning의 목록은 두 Journey Optimizer 모두에서 만든 규칙을 포함합니다 **[!UICONTROL 의사 결정 관리]** 또는 **[!UICONTROL 경험 의사 결정]** 메뉴 아래의 제품에서 사용할 수 있습니다.

규칙을 만들려면 다음 단계를 수행합니다.

1. 다음으로 이동 **[!UICONTROL 구성]** / **[!UICONTROL 의사 결정 규칙]**.
1. Journey Optimizer의 의사 결정 관리 사용자 인터페이스가 중앙 영역에 표시됩니다. 다음에 설명된 단계를 수행합니다. [의사 결정 관리 설명서](../offers/offer-library/creating-decision-rules.md) 를 사용하여 필요에 따라 규칙을 빌드할 수 있습니다.

1. 규칙이 만들어지면 목록에 나타나고 프로필에 대한 결정 항목 표시를 제어하는 결정 항목 및 선택 전략에 사용할 수 있습니다.
