---
title: 받은 편지함 만들기
description: Adobe Journey Optimizer에서 받은 편지함을 만들고 구성하여 지속적이고 방해받지 않는 메시지를 사용자에게 전달하는 방법을 알아봅니다.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 3%

---

# 받은 편지함 만들기 {#inbox-create}

받은 편지함을 만들기 전에 [받은 편지함 구성](inbox-configuration.md)의 단계를 완료하십시오. 채널 구성은 대상 애플리케이션이나 웹 사이트, 페이지나 규칙 및 받은 편지함이 렌더링되는 위치를 식별합니다.

캠페인을 통해 메시지 받은 편지함을 만들려면 다음 단계를 수행합니다.

1. 캠페인을 만듭니다. [자세히 알아보기](../campaigns/create-campaign.md)

1. 실행할 캠페인 유형 선택:

   * **[!UICONTROL 예약됨 - 마케팅]**: 캠페인을 즉시 또는 지정한 날짜에 실행합니다. 예약된 캠페인은 **마케팅** 메시지를 보내는 것을 목표로 합니다. 사용자 인터페이스에서 구성 및 실행됩니다.

   * **[!UICONTROL API 트리거됨 - 마케팅/트랜잭션]**: API 호출을 사용하여 캠페인을 실행하십시오. API 트리거 캠페인은 **마케팅** 또는 **트랜잭션** 메시지(예: 암호 재설정, 장바구니 구매 등 개인이 수행한 작업 후 발송된 메시지)를 보내는 것을 목표로 합니다. [API를 사용하여 캠페인을 트리거하는 방법을 알아봅니다](../campaigns/api-triggered-campaigns.md)

1. **[!UICONTROL 속성]** 탭에서 캠페인의 이름과 설명을 지정합니다.

1. **[!UICONTROL 작업]** 탭에서 **[!UICONTROL 받은 편지함]** 작업을 선택합니다.

   ![](assets/inbox-create-1.png)

1. [받은 편지함 구성](inbox-configuration.md)을 선택하거나 새로 만드세요.

   ![](assets/inbox-create-2.png)

1. 콘텐츠 디자이너를 사용하여 메시지를 디자인하려면 콘텐츠 탭에 액세스합니다. [자세히 알아보기](inbox-design.md)

1. **[!UICONTROL 대상]** 탭에서 **[!UICONTROL 대상 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 대상 목록을 표시합니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md)

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

1. 캠페인을 특정 날짜로 예약하거나 정기적으로 반복되도록 설정할 수 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#schedule)

1. 캠페인을 검토하고 활성화하여 받은 편지함으로 메시지를 보낼 수 있습니다.

이제 [콘텐츠 카드 캠페인](../content-card/create-content-card.md)을 만들 때 이 받은 편지함을 선택할 수 있습니다.
