---
solution: Journey Optimizer
product: journey optimizer
title: 타겟팅 차원 만들기
description: 고객 프로필에 관계형 스키마를 매핑하는 방법에 대해 알아봅니다
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: ac80d1cec351a3029c8b2bf862275ffe7fd5c86d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---


# 타겟팅 차원 구성 {#configuration}

**[!UICONTROL 오케스트레이션된 캠페인]**&#x200B;을 통해 Adobe Experience Platform의 관계형 스키마 기능을 활용하여 엔터티 수준에서 타깃팅된 커뮤니케이션을 디자인하고 제공할 수 있습니다. Experience Platform은 스키마를 사용하여 데이터의 구조를 일관되고 재사용 가능한 방식으로 설명합니다. 데이터가 Experience Platform에 수집되면 XDM 스키마에 따라 구조화됩니다.

**[!UICONTROL 오케스트레이션된 캠페인]**&#x200B;의 세그먼테이션은 주로 관계형 스키마에서 작동하지만 실제 메시지 게재는 항상 **프로필** 수준에서 발생합니다.

타깃팅을 구성할 때는 두 가지 주요 측면을 정의합니다.

* **타깃팅 가능한 스키마**

  타겟팅에 적합한 관계형 스키마를 지정합니다. 기본적으로 이름이 `Recipient`인 스키마가 사용되지만 `Visitors`, `Customers` 등과 같은 대체 요소를 구성할 수 있습니다.

  >[!IMPORTANT]
  >
  > 대상 스키마에 :1 스키마와 1`Profile` 관계가 있어야 합니다. 예를 들어 `Purchases`은(는) 일반적으로 일대다 관계를 나타내므로 대상 스키마로 사용할 수 없습니다.

* **프로필 연결**

  대상 스키마가 `Profile` 스키마에 매핑되는 방식을 이해해야 합니다. 대상 스키마와 `Profile` 스키마에 모두 존재하며 ID 네임스페이스로 구성된 공유 ID 필드를 통해 수행됩니다.

➡️ [Adobe Experience Platform 설명서에서 관계형 스키마에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## 타겟팅 차원 만들기 {#targeting-dimension}

먼저 고객 프로필에 관계형 스키마를 매핑하여 캠페인 오케스트레이션을 설정합니다.

1. **[!UICONTROL 관리]**&#x200B;에서 **[!UICONTROL 구성]** 메뉴에 액세스하고 **[!UICONTROL Campaign Target Dimension]**&#x200B;를 선택하세요.

   ![](assets/target-dimension-1.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하여 **[!UICONTROL 타깃팅 차원]**&#x200B;을(를) 만듭니다.

1. 드롭다운에서 [이전에 구성된 스키마](gs-schemas.md)&#x200B;을(를) 선택합니다.

   모든 관계형 스키마가 표시되지만 **프로필**&#x200B;과(와) 직접적인 ID 관계가 있는 스키마만 선택할 수 있습니다.

1. 타깃팅할 엔터티를 나타내는 **[!UICONTROL ID 값]**&#x200B;을(를) 선택하십시오.

   이 예제에서 고객 프로필은 `crmID` 스키마에서 각각 고유한 `Recipient`(으)로 표시되는 여러 구독에 연결됩니다. **[!UICONTROL 스키마와 해당]** ID를 사용하도록 `Recipient`Target Dimension`crmID`을(를) 설정하여 기본 고객 프로필이 아닌 구독 수준에서 메시지를 보내어 각 계약 또는 줄이 개인화된 메시지를 받도록 할 수 있습니다.

   [Adobe Experience Platform 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. 설정을 완료하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요. **[!UICONTROL 대상 차원]**&#x200B;을(를) 만든 후에는 제거하거나 편집할 수 없습니다.

**[!UICONTROL Target Dimension]**&#x200B;을 구성한 후 계속 **[!UICONTROL 채널 구성]**&#x200B;을 만들고 설정하고 해당 **[!UICONTROL 실행 세부 정보]**&#x200B;를 정의합니다.