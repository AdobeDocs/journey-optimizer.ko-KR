---
title: 코드 기반 경험 만들기
description: Journey Optimizer에서 코드 기반 경험을 만드는 방법을 알아봅니다
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 503bedc30c35305537c62f9452f4a2dc07424523
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 9%

---

# 코드 기반 경험 만들기 {#create-code-based}

[!DNL Journey Optimizer]에서 여정 또는 캠페인에서 코드 기반 경험을 만들 수 있습니다.

코드 기반 경험에 적용되는 가드레일 및 권장 사항은 [이 페이지](code-based-prerequisites.md)에서 자세히 설명합니다.

## 여정 또는 캠페인을 통해 코드 기반 경험 추가 {#create-code-based-experience}

여정 또는 캠페인을 통해 코드 기반 경험을 구축하려면 아래 단계를 따르십시오.

>[!BEGINTABS]

>[!TAB 여정에 코드 기반 경험 추가]

여정에 **코드 기반 경험** 활동을 추가하려면 다음 단계를 따르십시오.

1. [여정 만들기](../building-journeys/journey-gs.md).

1. [이벤트](../building-journeys/general-events.md) 또는 [대상자 읽기](../building-journeys/read-audience.md) 활동으로 여정을 시작하십시오.

1. 팔레트의 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 코드 기반 경험]** 활동을 끌어서 놓습니다.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >**코드 기반 경험**&#x200B;은(는) 인바운드 메시지 활동이므로 3일 **대기** 활동과 함께 제공됩니다. [자세히 알아보기](../building-journeys/wait-activity.md#auto-wait-node)

1. 메시지에 대해 **[!UICONTROL 레이블]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 사용할 [코드 기반 경험 구성](code-based-configuration.md)을 선택하거나 만드십시오.

   ![](assets/code-based-activity-config.png)

1. **[!UICONTROL 콘텐츠 편집]** 단추를 선택하고 개인화 편집기를 사용하여 원하는 대로 콘텐츠를 편집하십시오. [자세히 알아보기](#edit-code)

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. 코드 기반 경험이 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다. [자세히 알아보기](../building-journeys/publishing-the-journey.md)

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

>[!TAB 코드 기반 경험 캠페인 만들기]

캠페인을 통해 **코드 기반 경험** 빌드를 시작하려면 아래 단계를 따르십시오.

1. 캠페인을 만듭니다. [자세히 알아보기](../campaigns/create-campaign.md)

1. 실행할 캠페인 유형 선택

   * **[!UICONTROL 예약됨 - 마케팅]**: 캠페인을 즉시 또는 지정한 날짜에 실행합니다. 예약된 캠페인은 **마케팅** 메시지를 보내는 것을 목표로 합니다. 사용자 인터페이스에서 구성 및 실행됩니다.

   * **[!UICONTROL API 트리거됨 - 마케팅/트랜잭션]**: API 호출을 사용하여 캠페인을 실행하십시오. API 트리거 캠페인은 **마케팅** 또는 **트랜잭션** 메시지(예: 암호 재설정, 장바구니 구매 등 개인이 수행한 작업 후 발송된 메시지)를 보내는 것을 목표로 합니다. [API를 사용하여 캠페인을 트리거하는 방법을 알아봅니다](../campaigns/api-triggered-campaigns.md)

1. 캠페인 속성, [대상자](../audience/about-audiences.md) 및 [일정](../campaigns/create-campaign.md#schedule)과 같은 캠페인을 만드는 단계를 완료합니다. 캠페인을 구성하는 방법에 대한 자세한 내용은 [이 페이지](../campaigns/get-started-with-campaigns.md)를 참조하세요.

1. **[!UICONTROL 코드 기반 경험]** 작업을 선택하십시오.

1. 코드 기반 경험 구성을 선택하거나 만듭니다. [자세히 알아보기](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. 개인화 편집기를 사용하여 원하는 대로 콘텐츠를 편집합니다. [자세히 알아보기](#edit-code)

   <!--![](assets/code-based-campaign-edit-content.png)-->

캠페인을 구성하는 방법에 대한 자세한 내용은 [이 페이지](../campaigns/get-started-with-campaigns.md)를 참조하세요.

>[!ENDTABS]

## 코드 콘텐츠 편집 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="개인화 편집기 사용"
>abstract="이 코드 기반 경험 액션의 일부로 게재하려는 코드를 삽입하고 편집합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=ko" text="개인화 편집기 시작하기"

1. 여정 활동 또는 캠페인 버전 화면에서 **[!UICONTROL 코드 편집]**&#x200B;을 선택합니다.

   ![](assets/code-based-campaign-edit-code.png)

1. [개인화 편집기](../personalization/personalization-build-expressions.md)가 열립니다. 코드를 작성할 수 있는 비시각적 경험 만들기 인터페이스입니다.

1. 작성 모드를 HTML에서 JSON으로 전환하거나 그 반대로 전환할 수 있습니다.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >작성 모드를 변경하면 현재 코드가 모두 손실되므로 작성을 시작하기 전에 모드를 전환해야 합니다.

1. 필요에 따라 코드를 입력합니다. [!DNL Journey Optimizer] 개인화 편집기를 모든 개인화 및 작성 기능과 함께 활용할 수 있습니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

1. 필요한 경우 HTML 또는 JSON 표현식 조각을 추가할 수 있습니다. [방법 알아보기](../personalization/use-expression-fragments.md)

   코드 콘텐츠의 일부를 조각으로 저장할 수도 있습니다. [방법 알아보기](../content-management/fragments.md#save-as-expression-fragment)

1. 코드 기반 경험을 사용하면 experience decisioning 기능을 사용할 수 있습니다. 왼쪽 막대에서 **[!UICONTROL 결정 정책]** 아이콘을 선택하고 **[!UICONTROL 결정 정책 추가]**&#x200B;를 클릭합니다. [자세히 알아보기](../experience-decisioning/create-decision.md) <!--UI labels TBC + TBC for journeys (visible in UI so probably confirmed) -->

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 권한을 얻으려면 Adobe 담당자에게 문의하십시오.


1. 변경 내용을 확인하려면 **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭하십시오.

이제 개발자가 채널 구성에 정의된 표면에 대한 콘텐츠를 가져오기 위해 API 또는 SDK를 호출하는 즉시 변경 사항이 웹 페이지 또는 앱에 적용됩니다.

## 코드 기반 경험 테스트 {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="코드 기반 경험 미리보기"
>abstract="코드 기반 경험이 어떻게 시각화되는지 시뮬레이션을 수행합니다."

수정된 코드 기반 경험의 미리보기를 표시하려면 아래 단계를 따르십시오. 테스트 프로필을 선택하고 콘텐츠를 미리 보는 방법에 대한 자세한 내용은 [콘텐츠 페이지 미리 보기 및 테스트](../content-management/preview-test.md)를 참조하세요.

>[!CAUTION]
>
>게재할 오퍼를 시뮬레이션할 수 있는 테스트 프로필이 있어야 합니다. [테스트 프로필을 만드는](../audience/creating-test-profiles.md) 방법을 알아봅니다.

1. 여정 또는 캠페인의 개인화 편집기 또는 콘텐츠 편집 화면에서 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 선택합니다.

   ![](assets/code-based-campaign-simulate.png)

1. 하나 이상의 테스트 프로필을 선택하려면 **[!UICONTROL 테스트 프로필 관리]**&#x200B;를 클릭하십시오.

1. 수정된 코드 기반 경험의 미리보기가 표시됩니다.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## 코드 기반 경험 라이브로 만들기 {#code-based-experience-live}

>[!IMPORTANT]
>
>9월 릴리스부터 새로운 캠페인 및 여정 활성화 환경을 사용하면 전체 승인 프로세스를 관리할 수 있으므로 캠페인 및 여정이 시작하기 전에 해당 관련자로부터 철저하게 검토 및 승인되도록 합니다. 이 기능은 제한된 가용성으로 사용할 수 있습니다. [자세히 알아보기](../test-approve/gs-approval.md)

코드 기반 경험을 정의하고 [코드 기반 편집기](#edit-code)를 사용하여 원하는 대로 콘텐츠를 편집한 후에는 여정 또는 캠페인을 활성화하여 변경 내용을 대상자에게 표시할 수 있습니다.

코드 기반 경험 콘텐츠를 라이브로 만들기 전에 미리 볼 수도 있습니다. [자세히 알아보기](#test-code-based-experience)

>[!NOTE]
>
>이미 라이브 상태인 다른 여정 또는 캠페인과 동일한 페이지에 영향을 주는 코드 기반 여정/캠페인을 활성화하면 모든 변경 사항이 콘텐츠에 적용됩니다.
>
>여러 코드 기반 여정 또는 캠페인이 콘텐츠의 동일한 요소를 업데이트하는 경우, 우선 순위가 가장 높은 여정/캠페인이 우선합니다.

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

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report.md)

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

TBC video if existing

## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
