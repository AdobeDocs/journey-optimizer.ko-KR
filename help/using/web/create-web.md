---
title: 웹 경험 만들기
description: Journey Optimizer에서 웹 페이지를 작성하고 해당 컨텐츠를 편집하는 방법을 알아봅니다
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 14%

---

# 웹 경험 만들기  {#create-web}

[!DNL Journey Optimizer] 인바운드 웹 캠페인을 통해 고객에게 전달하는 웹 경험을 개인화할 수 있습니다.

>[!CAUTION]
>
>현재 [!DNL Journey Optimizer] 를 사용하여 웹 경험만 만들 수 있습니다. **캠페인**.

[이 비디오에서 웹 캠페인을 만드는 방법을 알아봅니다](#video)

## 웹 캠페인 만들기 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="웹 표면 정의"
>abstract="웹 표면이 단일 페이지 URL 또는 여러 페이지와 일치하면 하나 또는 여러 웹 페이지에 콘텐츠 수정 내용을 전달할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="페이지 일치 규칙 작성"
>abstract="페이지 일치 규칙을 사용하면 전체 웹 사이트의 히어로 배너에 변경 사항을 적용하거나 웹 사이트의 모든 제품 페이지에 표시되는 상단 이미지를 추가하려는 경우와 같이 동일한 규칙과 일치하는 여러 URL을 대상으로 지정할 수 있습니다."

캠페인을 통해 웹 경험 작성을 시작하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>웹 경험을 처음 만드는 경우에는 다음에 설명된 전제 조건을 따라야 합니다. [이 섹션](web-prerequisites.md).

1. 캠페인 만들기. [자세히 알아보기](../campaigns/create-campaign.md)

1. 을(를) 선택합니다 **[!UICONTROL 웹]** 작업.

1. 웹 표면 정의.

   >[!NOTE]
   >
   >웹 서피스는 컨텐츠가 전달될 URL로 식별되는 웹 속성입니다. 단일 페이지 URL 또는 여러 페이지를 일치시킬 수 있으므로 하나 또는 여러 웹 페이지에서 수정 사항을 전달할 수 있습니다.

   을(를) 입력할 수 있습니다. **[!UICONTROL 페이지 URL]** 변경 사항을 단일 페이지에만 적용하려면

   ![](assets/web-campaign-surface.png)

1. 또는 **[!UICONTROL 페이지 일치 규칙]** 동일한 규칙과 일치하는 여러 URL을 타깃팅하려면, 예를 들어 전체 웹 사이트에 히어로 배너에 변경 사항을 적용하거나 웹 사이트의 모든 제품 페이지에 표시되는 최상위 이미지를 추가하십시오.

   이렇게 하려면 을(를) 선택합니다. **[!UICONTROL 페이지 일치 규칙]** 을(를) 클릭합니다. **[!UICONTROL 규칙 만들기]**.

   ![](assets/web-campaign-matching-rule.png)

1. 에 대한 기준을 정의합니다 **[!UICONTROL 도메인]** 및 **[!UICONTROL 페이지]** 필드.

   예를 들어, Luma 웹 사이트의 모든 여성 제품 페이지에 표시되는 요소를 편집하려면 을(를) 선택합니다 **[!UICONTROL 도메인]** > **[!UICONTROL 다음으로 시작]** > `luma` 및 **[!UICONTROL 페이지]** > **[!UICONTROL 다음 포함]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 변경 내용을 저장합니다. 규칙이 **[!UICONTROL 캠페인 만들기]** 화면.

   ![](assets/web-pages-matching-rule-example.png)

1. 웹 서피스를 정의했으면 다음을 선택합니다 **[!UICONTROL 만들기]**.

1. 캠페인 속성과 같은 웹 캠페인을 만드는 단계를 완료합니다. [대상자](../segment/about-segments.md), 및 [예약](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

캠페인 구성 방법에 대한 자세한 내용은 [이 페이지](../campaigns/get-started-with-campaigns.md).

## 웹 캠페인 활성화 {#activate-web-campaign}

을(를) 정의했으면 [웹 캠페인 설정](#configure-web-campaign) 원하는 대로 컨텐츠를 편집한 다음 [웹 디자이너](author-web.md), 웹 캠페인을 검토하고 활성화할 수 있습니다. 아래 절차를 따르십시오.

>[!NOTE]
>
>웹 캠페인 콘텐츠를 활성화하기 전에 미리 볼 수도 있습니다. [자세히 알아보기](author-web.md#test-web-campaign)

1. 웹 캠페인에서 를 선택합니다 **[!UICONTROL 활성화 검토]**.

1. 필요한 컨텐츠, 속성, 서피스, 대상 및 일정을 확인하고 편집합니다.

1. 선택 **[!UICONTROL 활성화]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >을 클릭한 후 **[!UICONTROL 활성화]**&#x200B;웹 캠페인 변경 사항을 웹 사이트에서 실시간으로 사용할 수 있도록 하려면 최대 15분이 걸릴 수 있습니다.

웹 캠페인이 **[!UICONTROL 라이브]** 이제 선택한 대상자에게 상태 및 가 표시됩니다. 캠페인의 각 수신자는 [!DNL Journey Optimizer] 웹 디자이너

>[!NOTE]
>
>웹 캠페인에 대한 일정을 정의한 경우 해당 웹 캠페인에 가 있습니다 **[!UICONTROL 예약됨]** 시작 날짜 및 시간에 도달할 때까지의 상태입니다.
>
>이미 사용 중인 다른 캠페인과 동일한 페이지에 영향을 주는 웹 캠페인을 활성화하면 웹 페이지에 모든 변경 사항이 적용됩니다.

에서 캠페인 활성화에 대해 자세히 알아보십시오 [이 섹션](../campaigns/review-activate-campaign.md).

## 웹 캠페인 중지 {#stop-web-campaign}

웹 캠페인이 라이브 상태일 때 이를 중지하여 대상자가 수정 사항을 보지 못하도록 할 수 있습니다. 아래 절차를 따르십시오.

1. 목록에서 라이브 캠페인을 선택합니다.

1. 상단 메뉴에서 **[!UICONTROL 캠페인 중지]**.

   ![](assets/web-campaign-stop.png)

1. 추가한 수정 사항은 정의한 대상에 더 이상 표시되지 않습니다.

>[!NOTE]
>
>웹 캠페인이 중지되면 다시 편집하거나 활성화할 수 없습니다. 복제하고 복제된 캠페인만 활성화할 수 있습니다.

## 방법 비디오{#video}

아래 비디오에서는 웹 캠페인을 만들고, 속성을 구성하고, 검토하고, 게시하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)