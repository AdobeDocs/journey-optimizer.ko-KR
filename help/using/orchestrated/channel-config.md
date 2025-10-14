---
solution: Journey Optimizer
product: journey optimizer
title: 채널 구성
description: 채널 구성을 구성하는 방법을 알아봅니다
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 채널 구성 {#channel-configuration}

[Target Dimension](target-dimension.md)을 설정한 후에는 **[!UICONTROL 채널 구성]**&#x200B;을 구성하고 적절한 **[!UICONTROL 실행 세부 정보]**&#x200B;를 정의해야 합니다. 이를 통해 을(를) 정의할 수 있습니다.

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
