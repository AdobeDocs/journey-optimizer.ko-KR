---
solution: Journey Optimizer
product: journey optimizer
title: 타겟팅 차원 만들기
description: 고객 프로필에 관계형 스키마를 매핑하는 방법에 대해 알아봅니다
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---


# 타겟팅 차원 구성 {#configuration}

**[!UICONTROL 오케스트레이션된 캠페인]**&#x200B;을 통해 Adobe Experience Platform의 관계형 스키마 기능을 활용하여 엔터티 수준에서 타깃팅된 커뮤니케이션을 디자인하고 제공할 수 있습니다.

**[!UICONTROL 오케스트레이션된 캠페인]**&#x200B;의 세그먼테이션은 주로 관계형 스키마에서 작동하지만 실제 메시지 게재는 항상 **프로필** 수준에서 발생합니다.

타깃팅을 구성할 때는 두 가지 주요 측면을 정의합니다.

* **타깃팅 가능한 스키마**

  타겟팅에 적합한 관계형 스키마를 지정합니다. 기본적으로 이름이 `Recipient`인 스키마가 사용되지만 `Visitors`, `Customers` 등과 같은 대체 요소를 구성할 수 있습니다.

  >[!IMPORTANT]
  >
  > 대상 스키마에 :1 스키마와 1`Profile` 관계가 있어야 합니다. 예를 들어 `Purchases`은(는) 일반적으로 일대다 관계를 나타내므로 대상 스키마로 사용할 수 없습니다.

* **프로필 연결**

  대상 스키마가 `Profile`에 매핑되는 방식을 이해해야 합니다. 대상 스키마와 `Profile` 스키마에 모두 존재하며 ID 네임스페이스로 구성된 공유 ID 필드를 통해 수행됩니다.

## 타겟팅 차원 만들기 {#targeting-dimension}

먼저 고객 프로필에 관계형 스키마를 매핑하여 캠페인 오케스트레이션을 설정합니다.

1. **[!UICONTROL 관리]**&#x200B;에서 **[!UICONTROL 구성]** 메뉴에 액세스하고 **[!UICONTROL Campaign Target Dimension]**&#x200B;를 선택하세요.

   ![](assets/target-dimension-1.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하여 **[!UICONTROL 타깃팅 차원]**&#x200B;을(를) 만듭니다.

1. 드롭다운에서 [이전에 구성된 스키마](gs-schemas.md)&#x200B;을(를) 선택합니다.

   모든 관계형 스키마가 표시되지만 **프로필**&#x200B;과(와) 직접적인 ID 관계가 있는 스키마만 선택할 수 있습니다.

1. 타깃팅할 엔터티를 나타내는 **[!UICONTROL ID 값]**&#x200B;을(를) 선택하십시오.

   이 예제에서 고객 프로필은 `crmID` 스키마에서 각각 고유한 `Recipient`(으)로 표시되는 여러 구독에 연결됩니다. **[!UICONTROL 스키마와 해당]** ID를 사용하도록 `Recipient`Target Dimension`crmID`을(를) 설정하여 기본 고객 프로필이 아닌 구독 수준에서 메시지를 보내어 각 계약 또는 줄이 개인화된 메시지를 받도록 할 수 있습니다.

   [Adobe Experience Platform 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. 설정을 완료하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요. **[!UICONTROL 대상 차원]**&#x200B;을(를) 만든 후에는 제거하거나 편집할 수 없습니다.

**[!UICONTROL Target Dimension]**&#x200B;을 구성한 후 계속 **[!UICONTROL 채널 구성]**&#x200B;을 만들고 설정하고 해당 **[!UICONTROL 실행 세부 정보]**&#x200B;를 정의합니다.

## 채널 구성 {#channel-configuration}

**[!UICONTROL Target Dimension]**&#x200B;을 설정한 후에는 전자 메일 또는 SMS를 **[!UICONTROL 채널 구성]**&#x200B;을 구성하고 적절한 **[!UICONTROL 실행 세부 정보]**&#x200B;를 정의해야 합니다. 이를 통해 을(를) 정의할 수 있습니다.

* **메시지 게재 수준**: 예를 들어, 개인당 하나의 전자 메일과 같이 받는 사람당 하나의 메시지를 보내는 경우입니다.

* **실행 주소**: 전자 메일 주소 또는 전화 번호와 같이 보낼 때 사용할 특정 연락처 필드입니다.

채널 구성을 구성하려면 다음 작업을 수행하십시오.

1. 먼저 **[!UICONTROL 채널 구성]**&#x200B;을 만들고 구성하세요.

   기존 **[!UICONTROL 채널 구성]**&#x200B;을 업데이트할 수도 있습니다.

   ➡️ [이 페이지에 설명된 단계를 따릅니다](../email/surface-personalization.md)

1. **[!UICONTROL 채널 구성]**&#x200B;의 **[!UICONTROL 실행 세부 정보]** 섹션에서 **[!UICONTROL 오케스트레이션된 캠페인]** 탭에 액세스합니다.

   ![](assets/target-dimension-3.png)

1. 오케스트레이션된 캠페인과 호환되도록 하려면 **[!UICONTROL 사용]**&#x200B;을 클릭하세요.

1. 게재 방법 선택:

   * **[!UICONTROL 대상 Dimension]**: 기본 엔터티(예: 수신자)로 보냅니다.

   * **[!UICONTROL Target + 보조 Dimension]**: 기본 및 보조 엔터티(예: 수신자 + 계약)를 모두 사용하여 보냅니다.

1. 드롭다운에서 [이전에 만든 Target Dimension](#targeting-dimension)을 선택합니다.

   ![](assets/target-dimension-4.png)

1. **[!UICONTROL Target + 보조 Dimension]**&#x200B;을(를) 게재 방법으로 선택한 경우 **[!UICONTROL 보조 Dimension]**&#x200B;을(를) 선택하여 메시지 게재의 컨텍스트를 정의합니다.

1. **[!UICONTROL 실행 주소]** 섹션에서 전자 메일 주소 또는 전화 번호와 같은 게재 주소를 가져오는 데 사용할 **[!UICONTROL Source]**&#x200B;을(를) 선택하십시오.

   * **[!UICONTROL 프로필]**: 게재 주소(예: 이메일)가 기본 고객 프로필에 직접 저장되어 있는 경우 이 옵션을 선택합니다.

     특정 관련 엔티티가 아니라 기본 고객에게 메시지를 보낼 때 유용합니다.

   * **[!UICONTROL 대상 Dimension]**: 게재 주소가 기본 엔터티(예: 받는 사람)에 저장되어 있는 경우 선택하십시오.

     각 수신자에게 다른 전자 메일 또는 전화 번호와 같은 고유한 게재 주소가 있는 경우 유용합니다.

   * **[!UICONTROL 보조 Dimension]**: **[!UICONTROL Target + 보조 Dimension]**&#x200B;을(를) 배달 방법으로 사용할 때 이전에 구성한 관련 **[!UICONTROL 보조 Dimension]**&#x200B;을(를) 선택하십시오.

     예를 들어 보조 차원이 예약 또는 구독을 나타내는 경우 이메일과 같은 실행 주소를 해당 수준에서 가져올 수 있습니다. 이 기능은 서비스를 예약하거나 구독할 때 프로필에서 다른 연락처 세부 정보를 사용하는 경우에 유용합니다.

1. **[!UICONTROL 게재 주소]** 필드에서 ![편집 아이콘](assets/do-not-localize/edit.svg)을 클릭하여 메시지 게재에 사용할 특정 필드를 선택합니다.

   ![](assets/target-dimension-4.png)

1. 구성이 완료되면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

이제 채널을 **오케스트레이션된 캠페인**&#x200B;에서 사용할 준비가 되었으며 선택한 대상 차원에 따라 메시지가 전달됩니다.
