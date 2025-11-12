---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 메시지 만들기
description: Journey Optimizer에서 라이브 활동을 만드는 방법을 알아봅니다
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 1%

---

# 라이브 활동 만들기 {#create-mobile-live}

>[!BEGINSHADEBOX]

* [라이브 활동 시작](get-started-mobile-live.md)
* [라이브 활동 구성](mobile-live-configuration.md)
* [Adobe Experience Platform Mobile SDK과 라이브 활동 통합](mobile-live-configuration-sdk.md)
* **[라이브 활동 만들기](create-mobile-live.md)**
* [자주 묻는 질문](mobile-live-faq.md)
* [라이브 활동 캠페인 보고서](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

모바일 구성을 구성하고 Adobe Experience Platform mobile SDK을 구현한 후 Journey Optimizer에서 라이브 활동을 만들 수 있습니다.

1. **[!UICONTROL 캠페인]** 메뉴에 액세스한 다음 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

1. **API 트리거됨** 캠페인 유형을 선택하십시오.

   * 대상 기반 캠페인에 대해 **API 트리거된 마케팅** 선택

   * 개별 캠페인에 대해 **API 트리거 트랜잭션**&#x200B;을(를) 선택하십시오.

   >[!IMPORTANT]
   >
   > **API 트리거 트랜잭션**&#x200B;의 경우 **[!UICONTROL 높은 처리량]** 옵션을 사용할 수 없습니다.


   ![](assets/create-live-1.png)

1. **[!UICONTROL 속성]** 섹션에서 Campaign의 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**&#x200B;을(를) 편집합니다.

1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 라이브 활동]**&#x200B;을 선택하고 새 구성을 선택하거나 만드십시오.

   [이 페이지](mobile-live-configuration.md)에서 실시간 활동 구성에 대해 자세히 알아보세요.

   ![](assets/create-live-2.png)

1. 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 대상 대상에 가장 적합한 옵션을 식별하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하십시오. [자세히 알아보기](../content-management/content-experiment.md)

1. **[!UICONTROL 대상자]** 탭에서 **[!UICONTROL ID 유형]**&#x200B;을 선택합니다. [자세히 알아보기](../audience/about-audiences.md).

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. **[!UICONTROL 이 섹션]**&#x200B;에서 캠페인의 [일정](../campaigns/create-campaign.md#schedule)을 구성하는 방법을 알아보세요.

1. 구성이 완료되면 **[!UICONTROL 활성화 검토]**&#x200B;를 클릭한 다음 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

1. 캠페인이 활성화되면 제공된 **cURL 요청**&#x200B;을(를) 템플릿으로 사용하여 라이브 활동 시작, 업데이트 또는 종료 이벤트를 트리거합니다. 실행 전에 특정 데이터로 샘플 페이로드를 업데이트합니다.

   페이로드에 포함할 **[!UICONTROL 캠페인 ID]** 식별자도 복사하십시오.

   ➡️ OAuth 토큰 및 API 키를 포함한 인증 요구 사항은 [API 트리거된 캠페인 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/)를 참조하십시오.

   ![](assets/create-live-3.png)

   +++ 개별 페이로드의 예

   다음 페이로드 예제의 필드 대부분은 필수이므로 `requestId`, `dismissal-date` 및 `alert`만 선택 사항입니다.

       &quot;json
       &lbrace;
       &quot;requestId&quot;: &quot;your-request-id&quot;,
       &quot;campaignId&quot;: &quot;your-campaign-id&quot;,
       &quot;수신자&quot;: &lbrack;
       &lbrace;
       &quot;type&quot;: &quot;aep&quot;,
       &quot;userId&quot;: &quot;testemail@gmail.com&quot;,
       &quot;namespace&quot;: &quot;email&quot;,
       &quot;컨텍스트&quot;: &lbrace;
       &quot;requestPayload&quot;: &lbrace;
       &quot;aps&quot;: &lbrace;
       &quot;콘텐츠 사용 가능&quot;: 1,
       &quot;timestamp&quot;: 1756984054,              // 현재 epoch 시간
       &quot;dismission-date&quot;: 1756984084,         // 선택 사항 - event=&quot;end&quot;
일 때 자동 제거       &quot;event&quot;: &quot;update&quot;,                    // 시작 | 업데이트 | end
       
   FoodDeliveryLiveActivityAttributes의     // 필드
       &quot;content-state&quot;: &lbrace;
       &quot;orderStatus&quot;: &quot;배달됨&quot;
       ,
       
       &quot;attributes-type&quot;: &quot;FoodDeliveryLiveActivityAttributes&quot;,
       &quot;attributes&quot;: &lbrace;
       &quot;restaurantName&quot;: &quot;피자&quot;,
       &quot;liveActivityData&quot;: &lbrace;
       &quot;liveActivityID&quot;: &quot;orderId1&quot;       // 고객 참조 ID
       
       ,
       
       &quot;경고&quot;: &lbrace;
       &quot;title&quot;: &quot;배달된 주문!&quot;,
       &quot;body&quot;: &quot;피자가 도착했습니다.&quot;
       
       
       
       
       &rbrace;
       &rbrack;
       
       &quot;
   +++

라이브 활동을 디자인한 후 [기본 제공 보고서](../reports/campaign-global-report-cja-activity.md)를 통해 라이브 활동의 영향을 측정하는 방법을 추적할 수 있습니다.
