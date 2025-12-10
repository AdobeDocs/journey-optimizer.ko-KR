---
solution: Journey Optimizer
product: journey optimizer
title: 활동을 탐색하여 고객 참여
description: 활동을 탐색하여 고객 참여
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# 활동을 탐색하여 고객 참여 {#engage-customers-uc}

>[!BEGINSHADEBOX]

이 사용 사례는 Experience Platform에 이미 존재하는 대상, 특히 발생한 검색 활동을 수집하는 실시간 웹 비헤이비어 대상으로 시작됩니다. [Adobe Experience Platform에서 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**이 사용 사례에 필요한 스키마:**

* **받는 사람**: `email`, `churnprop` 필드가 있는 타겟팅 차원으로 사용됨
* **위시리스트**: 필드: `description`, `priceref`, `imageurl`

➡️ [모델 기반 스키마를 구성하는 방법 알아보기](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

이 캠페인은 운동 장비 범주를 검색한 고객을 대상으로 합니다. 대상자는 이탈 위험에 의해 중복 제거되며 세그먼트화되며, 이는 누군가가 참여하거나 구매하는 것을 중단할 가능성이 얼마나 높은지 나타냅니다.

고위험 고객은 별도의 새로운 대상자로 수집되어 나중에 특정 커뮤니케이션에 사용되며, 저위험 및 중간 위험 고객은 개인화된 이메일과 후속 조치를 통해 여러 단계의 여정을 거칩니다.

1. **위시리스트 재참여**&#x200B;를 목표로 하는 새 캠페인을 설정하는 것으로 시작합니다. 이렇게 하면 제품을 위시리스트에 저장하여 이미 구매 의향을 보인 고객에게 메시지를 집중할 수 있습니다.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. 캠페인 이름, 설명, 시작 및 종료 날짜, 관련 태그 등 **[!UICONTROL 캠페인 설정]**&#x200B;을 입력합니다.

1. **[!UICONTROL 대상자 읽기]** 활동을 추가하여 Adobe Experience Platform에서 사전 정의된 대상자를 선택합니다. 여기서는 웹 사이트에서 운동 장비 범주를 검색한 고객을 선택합니다.

   받는 사람은 **[!UICONTROL 엔터티]** 필드에서 선택한 전자 메일 주소로 식별됩니다.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. **[!UICONTROL 중복 제거]** 활동을 추가하여 대상자에서 중복 이메일 주소를 제거하고 각 고객에게 하나의 메시지만 받도록 합니다.

1. **[!UICONTROL 특성 추가]**&#x200B;를 클릭하고 중복 제거의 특성으로 이메일을 선택합니다.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. 그런 다음 이탈 가능성별로 고객을 세그먼트화하는 **[!UICONTROL 분할]** 활동을 추가하여 각 고객 그룹에 맞는 개인화된 경험을 제공할 수 있습니다.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. 세 개의 그룹을 만들려면 **[!UICONTROL 세그먼트 추가]**&#x200B;를 클릭하십시오.

   * 낮은 위험

   * Medium 위험

   * 고위험

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하여 각 그룹의 이탈 확률을 정의합니다.

   **조건 편집기**&#x200B;를 사용하여 각 고객의 이탈 위험을 결정하는 특정 값을 설정하십시오.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. 각 세그먼트는 다르게 처리됩니다.

   * [낮은/중간 위험](#low-medium-risk)
   * [고위험](#high-risk)

1. 캠페인을 테스트하여 준비가 완료되면 **[!UICONTROL 게시]**&#x200B;를 클릭하여 라이브로 만듭니다.

캠페인이 실행되면 보고 대시보드를 탐색하여 성능 지표와 주요 통찰력을 검토하십시오.

➡️ [보고에 대한 자세한 정보](../reports/campaign-global-report-cja.md)

## 고위험 세그먼트 {#high-risk}

이탈 위험이 높은 것으로 식별된 고객의 경우 전용 대상 세그먼트를 만듭니다. 이 대상자는 나중에 별도의 타겟팅된 커뮤니케이션에 사용됩니다.

1. **[!UICONTROL 대상자 저장]**&#x200B;을(를) 추가합니다.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. 대상자에 **[!UICONTROL 레이블]**&#x200B;을(를) 추가하고 **[!UICONTROL 프로필 매핑 필드]**&#x200B;을(를) 선택합니다. 여기서 **수신자-이메일**&#x200B;입니다.

   ![](assets/uc-interest-8.png){zoomable="yes"}

그러면 이 대상자는 Experience Cloud에 저장되며, 여기에서 나중에 특정 타겟팅된 캠페인에 사용할 수 있습니다.

## 낮은/중간 위험 세그먼트 {#low-medium-risk}

이탈 위험이 낮거나 중간 수준인 고객의 경우 참여를 강화하기 위한 다단계 캠페인을 설정하십시오.

1. 낮은 위험과 Medium 위험을 **[!UICONTROL 결합]** 활동과 결합하십시오.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. **[!UICONTROL 데이터 보강]** 활동을 추가하여 위시리스트 및 제품 정보를 사용하여 캠페인을 개인화합니다.

1. 다음 세 가지 특성을 만들려면 **[!UICONTROL 특성 추가]**&#x200B;를 클릭하십시오.

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   이를 통해 자세한 위시리스트 정보로 메시지를 더욱 풍성하게 만들 수 있습니다.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. 이메일에 대한 참여를 기반으로 리타겟팅할 새 대상자를 만듭니다.

   여기에서는 이메일 클릭 이벤트를 기반으로 대상자를 만들어 이전에 전송된 이메일과 상호 작용한 모든 사람, 특히 해당 메시지 내의 링크를 클릭한 사람을 재타겟팅합니다.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. 참여를 균등하게 분할하여 SMS나 푸시 알림을 통해 후속 내용을 전송하여 전환을 유도합니다.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. 위시리스트 항목과 같은 데이터 보강 데이터와 함께 수신자의 이름과 같은 프로필 속성을 포함하는 각 채널의 메시지 콘텐츠를 만들어 각 메시지를 개인화합니다.

   ![](assets/uc-interest-13.png){zoomable="yes"}
