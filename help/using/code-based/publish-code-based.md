---
title: Publish 및 코드 기반 경험 관리
description: Journey Optimizer에서 코드 기반 경험을 게시하고 중지하는 방법에 대해 알아봅니다
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# 코드 기반 경험 관리 {#publish-code-based}

## 코드 기반 경험 라이브로 만들기 {#code-based-experience-live}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 코드 기반 경험을 활성화하려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

코드 기반 경험을 정의하고 [코드 기반 편집기](create-code-based.md#edit-code)를 사용하여 원하는 대로 콘텐츠를 편집한 후에는 여정 또는 캠페인을 활성화하여 변경 내용을 대상자에게 표시할 수 있습니다.

코드 기반 경험 콘텐츠를 라이브로 만들기 전에 미리 볼 수도 있습니다. [자세히 알아보기](test-code-based.md)

>[!NOTE]
>
>이미 라이브 상태인 다른 여정 또는 캠페인과 동일한 페이지에 영향을 주는 코드 기반 여정/캠페인을 활성화하면 모든 변경 사항이 콘텐츠에 적용됩니다.
>
>여러 코드 기반 여정 또는 캠페인이 콘텐츠의 동일한 요소를 업데이트하는 경우, 우선 순위가 가장 높은 여정/캠페인이 우선합니다.

코드 기반 여정 또는 캠페인이 실행되면 앱 구현 팀이 명시적 API 또는 SDK 호출을 수행하여 선택한 [코드 기반 경험 구성](code-based-configuration.md)에 정의된 표면에 대한 콘텐츠를 가져옵니다. [이 섹션](code-based-implementation-samples.md)에서 다양한 고객 구현에 대해 자세히 알아보세요.

### Publish a 코드 기반 여정 {#publish-code-based-journey}

여정에서 코드 기반 경험을 라이브로 만들려면 아래 단계를 따르십시오.

1. 여정이 유효하고 오류가 없는지 확인합니다. [자세히 알아보기](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. 여정에서 오른쪽 상단 드롭다운 메뉴에 있는 **[!UICONTROL Publish]** 옵션을 선택합니다.

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >[이 섹션](../building-journeys/publishing-the-journey.md)에서 여정 게시에 대해 자세히 알아보세요.

코드 기반 여정은 **[!UICONTROL Live]** 상태를 사용하며 이제 선택한 대상자에게 표시됩니다. 여정의 각 수신자는 수정 사항을 볼 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Publish]**&#x200B;을(를) 클릭하면 변경 내용을 실시간으로 사용할 수 있게 되는 데 최대 15분이 걸릴 수 있습니다.

### 코드 기반 캠페인 활성화 {#activate-code-based-campaign}

1. 코드 기반 캠페인에서 **[!UICONTROL 활성화 검토]**&#x200B;를 선택합니다.

   ![](assets/code-based-campaign-review.png)

1. 필요한 경우 컨텐츠, 속성, 구성, 대상자 및 일정을 확인하고 편집합니다.

1. **[!UICONTROL 활성화]**&#x200B;를 선택합니다.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >[이 섹션](../campaigns/review-activate-campaign.md)에서 캠페인을 활성화하는 방법에 대해 자세히 알아보세요.

코드 기반 캠페인은 **[!UICONTROL Live]** 상태를 사용하며 이제 선택한 대상자에게 표시됩니다. 캠페인의 각 수신자는 콘텐츠에 추가한 수정 사항을 볼 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL 활성화]**&#x200B;를 클릭하면 변경 내용을 실시간으로 사용할 수 있게 되는 데 최대 15분이 걸릴 수 있습니다.
>
>코드 기반 캠페인에 대한 일정을 정의한 경우 시작 날짜 및 시간에 도달할 때까지 **[!UICONTROL 예약됨]** 상태가 됩니다.

## 코드 기반 여정 또는 캠페인 중지 {#stop-code-based-experience}

코드 기반 환경이 라이브 상태일 때 이를 중지하여 대상자가 수정 사항을 보지 못하도록 할 수 있습니다. 아래 단계를 수행합니다.

1. 해당 목록에서 라이브 여정 또는 캠페인을 선택합니다.

1. 사용 사례에 따라 관련 작업을 수행합니다.

   * 캠페인 상단 메뉴에서 **[!UICONTROL 캠페인 중지]**&#x200B;를 선택합니다.

     ![](assets/code-based-campaign-stop.png)

   * 여정 상단 메뉴에서 **[!UICONTROL 자세히]** 단추를 클릭하고 **[!UICONTROL 중지]**&#x200B;를 선택합니다.

     ![](assets/code-based-journey-stop.png)

1. 추가한 수정 사항은 정의한 대상자에게 더 이상 표시되지 않습니다.

>[!NOTE]
>
>코드 기반 여정 또는 캠페인이 중지되면 다시 편집하거나 활성화할 수 없습니다. 복제하고 복제된 여정/캠페인만 활성화할 수 있습니다.

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report-cja.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

-->

