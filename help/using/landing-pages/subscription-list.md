---
title: 구독 목록 만들기
description: Journey Optimizer에서 구독 목록을 설정하는 방법 알아보기
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 구독 목록 만들기 {#create-subscription-list}

## 구독 목록이란 무엇입니까?

구독 서비스는 특정 제목/이벤트/관심사 등에서 커뮤니케이션 수신을 선택한 고객에게 제공되는 마케팅 상품 및 서비스를 의미합니다. 계속. in [!DNL Journey Optimizer]로 설정되면 이러한 옵트인 고객이 구독 목록에 수집됩니다.

구독 서비스는 다음과 같습니다.

* 뉴스레터(예: &quot;Running series&quot;)
* 예를 들어 &quot;Summit 2021&quot; 와 같은 이벤트
* 웨비나(예: &quot;crypto에 대해 자세히 알아보기&quot;)
* 특정 제품/스포츠/서비스 등에 대한 관심사(예: &quot;향후 12개월 내에 주택 구입에 관심&quot;)
* 알림 방법에 대한 기본 설정(예: &quot;이메일에 새 노래 알림 받기&quot;)

프로필을 [랜딩 페이지](create-lp.md). 예는 다음과 같습니다 [이 섹션](get-started-lp.md#subscription-to-a-service).

## 구독 목록 정의 {#define-subscription-list}

구독 목록을 만들려면 아래 단계를 수행하십시오.

1. 가입 목록에 액세스하려면 다음을 선택합니다 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. 구독 목록에서 **[!UICONTROL Create subscription]** 목록.

   ![](../assets/lp_create-subscription-list.png)

1. 이름과 설명을 추가합니다. 이러한 필드는 필수입니다.

1. 시작 날짜 및 종료 날짜를 정의할 수 있습니다.

   ![](../assets/lp_subscription-list-dates.png)

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

생성된 모든 구독 목록이 목록에 표시됩니다. 생성 날짜 또는 수정 날짜에 따라 필터링할 수 있습니다.

![](../assets/lp_subscription-filters.png)

가능한 상태는 다음과 같습니다.

* **[!UICONTROL Not started]**: 현재 날짜보다 늦은 시작 날짜를 정의했습니다. 이 목록을 구독한 프로필은 이 구독 목록과 관련된 메시지를 아직 받지 않습니다.
* **[!UICONTROL Live]**: 오늘이 구독 목록 시작 날짜와 종료 날짜 사이에 포함되거나, 종료/시작 날짜를 정의하지 않은 경우, 구독 목록이 항상 라이브됩니다.
* **[!UICONTROL Expired]**: 종료 날짜가 전달되면 구독 목록이 더 이상 유효하지 않습니다. 이 목록을 구독한 프로필은 이 구독 목록과 관련된 더 이상 통신을 받지 않습니다.

구독 목록이 만들어지면 랜딩 페이지에서 해당 프로필을 사용하여 양식을 통해 옵트인하고 목록에 추가할 수 있습니다. [자세히 알아보기](design-lp.md)

여정 및 개인화를 작성할 때 구독 목록을 세그먼트로 사용할 수도 있습니다.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->