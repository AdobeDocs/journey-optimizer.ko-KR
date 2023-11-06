---
solution: Journey Optimizer
product: journey optimizer
title: 구독 목록 만들기
description: Journey Optimizer에서 구독 목록을 설정하는 방법 알아보기
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 랜딩, 랜딩 페이지, 목록, 구독, 서비스
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: f63f9d6ffd28d276f8a3dadbf8dc6b947b8331e7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 13%

---

# 구독 목록 {#create-subscription-list}

## 구독 목록이란? {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="구독 목록 설정"
>abstract="구독 목록을 만들어 특정 주제 또는 이벤트에 대한 커뮤니케이션을 수신하도록 옵트인한 프로필을 수집합니다. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html#define-subscription-list" text="구독 목록 만들기"

구독 서비스는 특정 주제/이벤트/관심 분야 등에 대한 커뮤니케이션을 수신하도록 선택한 고객에게 제공되는 마케팅 상품 및 서비스를 의미합니다. 지속적으로. 위치 [!DNL Journey Optimizer], 이러한 옵트인 고객은 구독 목록으로 수집됩니다.

구독 서비스는 다음과 같을 수 있습니다.

* 뉴스레터(예: &quot;시리즈 실행 중&quot;)
* 예: &quot;Summit 2021&quot;
* 웨비나(예: &quot;암호에 대해 자세히 알아보기&quot;)
* 특정 제품/스포츠/서비스 등에 대한 관심 분야(예: &quot;향후 12개월 이내에 주택을 구입하는 데 관심 있음&quot;)
* 알림 방법에 대한 환경 설정(예: &quot;이메일로 새 노래 알림 수신&quot;)

프로필을 통해 구독 목록에 추가할 수 있습니다. [랜딩 페이지](create-lp.md). 예는에 나와 있습니다. [이 섹션](lp-use-cases.md#subscription-to-a-service).

## 구독 목록 만들기 {#define-subscription-list}

구독 목록을 만들려면 아래 단계를 수행하십시오.

1. 구독 목록에 액세스하려면 다음을 선택합니다. **[!UICONTROL 고객]** > **[!UICONTROL 구독 목록]**.

   ![](assets/lp_subscription-lists.png)

1. 다음 항목 선택 **[!UICONTROL 구독 목록 만들기]** 단추를 클릭합니다.

   ![](assets/lp_create-subscription-list.png)

1. 제목 및 설명을 추가합니다. 이러한 필드는 필수입니다.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >현재 의 다른 구독 목록에 대해 공백을 사용하거나 이미 존재하는 이름을 입력할 수 없습니다. **[!UICONTROL 제목]** 필드.

1. 시작 날짜와 종료 날짜를 정의할 수 있습니다.

   ![](assets/lp_subscription-list-dates.png)

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **[!UICONTROL 태그]** 검색을 개선하기 위해 랜딩 페이지를 분류하는 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이 목록에는 생성된 모든 가입 목록이 표시됩니다. 만든 날짜 또는 수정 날짜 및 해당 상태를 기준으로 필터링할 수 있습니다.

![](assets/lp_subscription-filters.png)

가능한 상태는 다음과 같습니다.

* **[!UICONTROL 시작되지 않음]**: 현재 날짜보다 늦은 시작 날짜를 정의했습니다. 구독한 프로필은 아직 이 구독 목록과 관련된 커뮤니케이션을 받지 않습니다.
* **[!UICONTROL 라이브]**: 현재 날짜가 구독 목록 시작 날짜와 종료 날짜 사이에 포함되어 있거나 종료/시작 날짜를 정의하지 않았습니다. 즉 구독 목록이 항상 활성 상태입니다.
* **[!UICONTROL 만료됨]**: 종료 날짜가 경과되므로 구독 목록이 더 이상 유효하지 않습니다. 구독한 프로필은 이 구독 목록과 관련된 더 이상 커뮤니케이션을 받지 않습니다.

구독 목록이 생성되면 랜딩 페이지에서 사용할 수 있습니다. 랜딩 페이지 양식을 통해 옵트인하는 프로필이 목록에 추가됩니다. [자세히 알아보기](design-lp.md)

다음과 같은 경우 구독 목록을 대상으로 사용할 수도 있습니다. [여정 작성](../building-journeys/journey-gs.md#jo-build) 개인화 추가.

>[!NOTE]
>
>특정 보고서를 통해 구독 목록이 미치는 영향을 모니터링할 수 있습니다. [자세히 알아보기](../reports/subscription-report-live.md)
