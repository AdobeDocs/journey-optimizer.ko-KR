---
solution: Journey Optimizer
product: journey optimizer
title: 사용자에게 제품 사용 가능 여부 알림
description: 사용자에게 제품 사용 가능 여부 알림
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# 사용자에게 제품 사용 가능 여부 알림 {#product-availability-uc}

>[!BEGINSHADEBOX]

이 사용 사례에서는 여러 수준의 전송 사례를 보여 줍니다. 수신자 레코드가 아닌 개별 항목과 함께 저장된 이메일 주소를 사용하여 각 위시리스트 항목에 대해 고유한 이메일을 생성합니다. 이렇게 하면 고객이 서로 다른 항목에 대해 서로 다른 이메일 주소를 사용하는 경우에도 위시리스트의 모든 제품에 대해 별도의 알림을 받을 수 있습니다.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

위시리스트의 항목을 다시 사용할 수 있게 되는 시기를 고객에게 알리기 위해 재고가 없는 알림을 설계합니다. 이 메시지는 관심 있는 고객을 다시 참여시키는 데 도움이 되며 재고가 보충되는 동안 구매를 완료하도록 장려합니다.

1. 위시리스트 재참여를 목표로 하는 새로운 캠페인을 설정하는 것부터 시작하십시오. 이렇게 하면 제품을 위시리스트에 저장하여 이미 구매 의향을 보인 고객에게 메시지를 집중할 수 있습니다.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. 캠페인 이름, 설명, 시작 및 종료 날짜, 관련 태그 등 **[!UICONTROL 캠페인 설정]**&#x200B;을 입력합니다.

1. 위시리스트를 **[!UICONTROL 타깃팅 차원]**(으)로 사용하는 **[!UICONTROL 대상자 빌드]** 활동을 추가합니다.

   ![](assets/notify-1.png){zoomable="yes"}

1. 지난 36개월 동안 만든 위시리스트만 포함하는 조건을 추가합니다.

   ![](assets/notify-2.png){zoomable="yes"}

1. **[!UICONTROL 차원 변경]** 활동을 추가하여 위시리스트에서 타깃팅을 위한 각 고객 집합으로 다시 이동합니다.

   ![](assets/notify-3.png){zoomable="yes"}

1. 초안 모드를 시작한 후 위시리스트 세부 정보로 대상자를 미리 봅니다. 자세한 정보를 보려면 출력 결과를 클릭하고 **[!UICONTROL 결과 미리 보기]**&#x200B;를 선택하십시오.

   여기에서 데이터에는 수신자와 위시리스트 항목이 모두 표시됩니다. 일부 고객은 위시리스트 항목을 여러 개 보유하고 있으며 다중 레벨 전송을 통해 각 항목에 대해 별도의 이메일을 수신합니다. 경우에 따라 고객은 별도의 재입고 요청에 대해 서로 다른 이메일 주소를 사용합니다.

   ![](assets/notify-4.png){zoomable="yes"}

1. 각 항목에 대해 별도의 전자 메일을 보내려면 [전자 메일 구성](../orchestrated/target-dimension.md)이(가) `Recipients - email`을(를) **[!UICONTROL 프로필 대상 Dimension]**(으)로, `Wishlistitems`을(를) **[!UICONTROL 보조 차원]**(으)로 설정되어 있는지 확인하십시오.

   그런 다음 **[!UICONTROL 실행 주소]** 메뉴에서 `wishlist.email`을(를) **[!UICONTROL 보조 차원]**(으)로 선택합니다. 각 위시리스트 항목은 위시리스트 데이터에 저장된 이메일 주소를 보조 차원으로 사용하여 개별 이메일을 트리거합니다.

   ![](assets/notify-5.png){zoomable="yes"}

1. **[!UICONTROL Email]** 활동을 추가하여 제품 가용성 메시지를 만듭니다. 콘텐츠 디자인을 시작하려면 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하세요.

   ➡️ [전자 메일 개인화에 대해 자세히 알아보기](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. 캠페인을 테스트하여 준비가 완료되면 **[!UICONTROL 게시]**&#x200B;를 클릭하여 라이브로 만듭니다.

이 오케스트레이션된 캠페인을 통해 고객은 각 위시리스트 항목에 대해 별도의 이메일을 수신합니다. 각 메시지는 해당 위시리스트와 연결된 특정 이메일 주소로 전송되며, 특정 위시리스트 항목의 세부 정보에서 수집한 개인화된 콘텐츠도 함께 제공됩니다.

