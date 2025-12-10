---
solution: Journey Optimizer
product: journey optimizer
title: 위시리스트 항목 업데이트 보내기
description: 위시리스트 항목 업데이트 보내기
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# 위시리스트 항목 업데이트 보내기 {#wishist-uc}

>[!BEGINSHADEBOX]

이 예제에서는 **위시리스트** 스키마를 사용하지만 동일한 메서드가 **수신자**(예: **구매**, **구독**)와 일대다 관계에 있는 모든 엔터티 또는 각 수신자에게 여러 개의 연결된 레코드가 있을 수 있는 모든 사용자 지정 스키마에 적용됩니다.

**이 사용 사례에 필요한 스키마:**

* **수신자**: 타겟팅 차원으로 사용됨
* **WishlistItems**: 필드: `creationDate`, `product`, `Wishlistid`
* **제품**: 필드: `description`, `priceref`, `imageurl`
* **포기한 장바구니**(선택 사항): 필드: `lastmodified`

➡️ [모델 기반 스키마를 구성하는 방법 알아보기](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

이 오케스트레이션된 캠페인은 방문자에게 위시리스트에 저장된 제품을 상기시켜 방문자를 다시 유도하는 데 중점을 둡니다. Campaign Orchestration을 사용하여 위시리스트 활동을 기반으로 하는 조건으로 대상자를 정의함으로써 방문자가 다시 전환하도록 지원합니다.

1. 위시리스트 재참여를 목표로 하는 새 캠페인을 만드는 것부터 시작하십시오. 이렇게 하면 항목을 저장하여 구매 의도를 표시한 고객에게 메시지를 집중시키는 데 도움이 됩니다.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. **캠페인 설정**&#x200B;을 입력하십시오.

1. 위시리스트 동작을 기준으로 타깃팅할 고객 그룹을 식별하려면 **[!UICONTROL 대상자 빌드]** 활동을 추가하십시오.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. 이 대상자에 대해 설명하는 **[!UICONTROL 레이블]**&#x200B;을(를) 설정하고 **[!UICONTROL 수신자]**&#x200B;을(를) **[!UICONTROL 타깃팅 차원]**(으)로 선택합니다. 그런 다음 **[!UICONTROL 계속]**&#x200B;을 클릭하여 대상자를 구성합니다.

1. 다음 조건을 만들어 대상을 세분화하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하세요.

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
또는
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   이 대상은 위시리스트가 있거나, 제품 이미지가 있는 항목을 포함하거나, 정의된 기간 내에 장바구니를 포기한 수신자를 기반으로 합니다.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. **[!UICONTROL 계산]**&#x200B;을 클릭하여 이러한 조건의 영향을 받는 프로필 수를 확인하고 **[!UICONTROL 결과 보기]**&#x200B;를 클릭하여 각 조건에 대한 세부 정보를 검사하고 대상자가 대상 세그먼트와 일치하는지 확인하십시오.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 데이터 보강]** 활동을 추가하여 **위시리스트** 및 **제품 정보**&#x200B;를 사용하여 캠페인을 개인화합니다.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. **[!UICONTROL 보강 데이터 추가]**&#x200B;를 클릭합니다.

1. `Targeting dimension > Wishlistitems > Wishlistid`에 액세스합니다.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. 데이터를 수집하는 방법을 선택합니다. 이 경우 대상자에 대한 위시리스트 세부 정보를 수집하려면 **[!UICONTROL 데이터를 수집]**&#x200B;합니다.

1. 검색할 라인의 수를 선택합니다. 기본적으로 위시리스트당 3개의 항목이 검색되지만 캠페인 필요에 따라 더 많거나 더 적은 제품을 강조 표시해야 하므로 이를 조정할 수 있습니다.

1. 다음 세 가지 특성을 만들려면 **[!UICONTROL 특성 추가]**&#x200B;를 클릭하십시오.

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   이렇게 하면 자세한 제품 정보로 메시지를 강화하여 전환을 촉진할 수 있습니다.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. 이메일 활동을 추가하여 각 고객에 대해 개별적으로 개인화된 재참여 메시지를 만듭니다. 콘텐츠 디자인을 시작하려면 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하세요.

   ➡️ [전자 메일 개인화에 대해 자세히 알아보기](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. 이메일을 완료한 후 오케스트레이션된 캠페인에서 **[!UICONTROL 시작]**&#x200B;을(를) 클릭하여 초안 모드로 캠페인을 저장하고 실행하십시오.

1. 초안 모드를 시작한 후 위시리스트 세부 정보로 대상자를 미리 봅니다.

   자세한 정보를 보려면 출력 결과를 클릭하고 **[!UICONTROL 결과 미리 보기]**&#x200B;를 선택하십시오.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

캠페인이 실행되면 캠페인의 수행 방식에 대한 강력한 데이터 및 KPI 세트를 제공하는 보고서를 살펴볼 수 있습니다.

➡️ [보고에 대한 자세한 정보](../reports/campaign-global-report-cja.md)
