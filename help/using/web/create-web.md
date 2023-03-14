---
title: 웹 경험 만들기
description: Journey Optimizer에서 웹 페이지를 작성하고 콘텐츠를 편집하는 방법에 대해 알아봅니다
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
badge: label="Beta" type="정보"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 8%

---

# 웹 경험 만들기  {#create-web}

>[!BEGINSHADEBOX]

이 설명서에서 찾을 수 있는 내용:

* [웹 채널 시작하기](get-started-web.md)
* **[웹 경험 만들기](create-web.md)**
* [웹 페이지 작성 ](author-web.md)
* [Visual Editing Helper 확장 기능](visual-editing-helper.md)
* [웹 보고 ](web-report.md)

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] 인바운드 웹 캠페인을 통해 고객에게 제공하는 웹 경험을 개인화할 수 있습니다.

>[!CAUTION]
>
>현재 위치 [!DNL Journey Optimizer] 다음을 사용해서만 웹 경험을 만들 수 있습니다. **캠페인**.

## 전제 조건 {#prerequesites}

에서 웹 페이지에 액세스하고 웹 페이지를 작성하려면 [!DNL Journey Optimizer] 사용자 인터페이스에서 아래 사전 요구 사항을 따르십시오.

* 웹 사이트에 수정 사항을 추가하려면 다음을 구현해야 합니다 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"} 웹 사이트에서.

* 에 액세스하려면 [!DNL Journey Optimizer] 웹 디자이너에서 [Adobe Experience Cloud Visual Edit Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} chrome의 브라우저 확장 프로그램. [자세히 알아보기](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome은에서 웹 페이지 작성을 지원하는 유일한 브라우저입니다. [!DNL Journey Optimizer].

웹 경험을 올바르게 전달하려면 다음 설정을 정의해야 합니다.

* 다음에서 [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}와 같은 데이터 스트림이 아래에 정의되어 있는지 확인합니다. **[!UICONTROL Adobe Experience Platform]** 서비스 두 가지 모두 **[!UICONTROL Edge 세그멘테이션]** 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되었습니다.

   이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >다음 **[!UICONTROL Adobe Journey Optimizer]** 옵션은 다음 경우에만 활성화할 수 있습니다. **[!UICONTROL Edge 세그멘테이션]** 옵션이 이미 활성화되어 있습니다.

* 위치 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   이 병합 정책은 다음 사용자가 사용합니다. [!DNL Journey Optimizer] 인바운드 채널을 통해 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## 웹 캠페인 만들기 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="웹 표면 정의"
>abstract="웹 표면은 단일 페이지 URL 또는 여러 페이지를 일치시킬 수 있으므로 하나 또는 여러 웹 페이지에서 콘텐츠 수정 사항을 전달할 수 있습니다."

캠페인을 통해 웹 경험을 구축하려면 아래 단계를 따르십시오.

1. 캠페인 만들기. [자세히 알아보기](../campaigns/create-campaign.md)

1. 다음 항목 선택 **[!UICONTROL 웹]** 작업.

   ![](assets/web-create-campaign.png)

1. 웹 표면을 정의합니다.

   >[!NOTE]
   >
   >웹 표면은 콘텐츠가 전달될 URL로 식별되는 웹 속성입니다. 단일 페이지 URL 또는 여러 페이지를 일치시킬 수 있으므로 하나 또는 여러 웹 페이지에서 수정 사항을 전달할 수 있습니다.

   다음을 입력할 수 있습니다. **[!UICONTROL 페이지 URL]** 변경 사항을 단일 페이지에만 적용하려면

   ![](assets/web-campaign-surface.png)

1. 또는 다음을 빌드할 수 있습니다 **[!UICONTROL 페이지 일치 규칙]** 동일한 규칙과 일치하는 여러 URL을 타겟팅하려면, 예를 들어 전체 웹 사이트에 걸쳐 히어로 배너에 변경 사항을 적용하거나 웹 사이트의 모든 제품 페이지에 표시되는 상위 이미지를 추가합니다.

   이렇게 하려면 을(를) 선택합니다 **[!UICONTROL 페이지 일치 규칙]** 및 클릭 **[!UICONTROL 규칙 만들기]**.

   ![](assets/web-campaign-matching-rule.png)

1. 기준에 대한 정의 **[!UICONTROL 도메인]** 및 **[!UICONTROL 페이지]** 필드.

   예를 들어 Luma 웹 사이트의 모든 여성 제품 페이지에 표시되는 요소를 편집하려면 다음을 선택합니다. **[!UICONTROL 도메인]** > **[!UICONTROL 다음으로 시작]** > `luma` 및 **[!UICONTROL 페이지]** > **[!UICONTROL 다음 포함]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 변경 내용을 저장합니다. 규칙이에 표시됩니다. **[!UICONTROL 캠페인 만들기]** 화면.

   ![](assets/web-pages-matching-rule-example.png)

1. 웹 서피스를 정의한 후 다음을 선택합니다. **[!UICONTROL 만들기]**. 이제 캠페인 속성 및 설정을 구성할 수 있습니다.

## 웹 캠페인 구성 {#configure-web-campaign}

1. 다음에서 **[!UICONTROL 속성]** 탭에서는 캠페인 이름을 편집하고 필요한 경우 설명을 추가할 수 있습니다.

   ![](assets/web-campaign-properties.png)

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 웹 캠페인에 할당하려면 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md)

1. 다음을 선택할 수 있습니다. **[!UICONTROL 콘텐츠 실험]** 특정 지표와 관련하여 성과가 가장 좋은 처리를 결정하기 위해 대상자의 일부와 콘텐츠 처리를 테스트합니다. [자세히 알아보기](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >다음 **콘텐츠 실험** 기능은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.

1. 다음에서 **[!UICONTROL 작업]** 캠페인의 탭에서 **[!UICONTROL 콘텐츠 편집]** 을 클릭하여 웹 캠페인 작성을 시작합니다. [자세히 알아보기](author-web.md)

   ![](assets/web-edit-content.png)

1. 다음에서 **[!UICONTROL 대상자]** 탭에서 웹 캠페인을 볼 수 있는 사용자를 정의합니다. 기본적으로 웹 캠페인은 모든 방문자에게 표시됩니다.

   ![](assets/web-campaign-audience.png)

   특정 대상자를 선택할 수도 있습니다. 사용 **[!UICONTROL 대상자 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시합니다. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

   >[!NOTE]
   >
   >API 트리거 캠페인의 경우, API 호출을 통해 대상자를 설정해야 합니다. [자세히 알아보기](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. 다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

1. 정의 **[!UICONTROL 예약]** 웹 캠페인에 사용됩니다. [자세히 알아보기](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   기본적으로 수동으로 활성화하면 시작되고 수동으로 중지하면 종료되지만, 수정 사항을 표시할 특정 날짜 및 시간을 정의할 수도 있습니다.

   ![](assets/web-campaign-schedule-start.png)

## 웹 캠페인 활성화 {#activate-web-campaign}

을(를) 정의한 후 [웹 캠페인 설정](#configure-web-campaign) 을(를) 사용하여 원하는 대로 콘텐츠를 편집했습니다. [웹 디자이너](author-web.md), 웹 캠페인을 검토하고 활성화할 수 있습니다. 아래 단계를 수행합니다.

>[!NOTE]
>
>웹 캠페인 콘텐츠를 활성화하기 전에 미리 볼 수도 있습니다. [자세히 알아보기](author-web.md#test-web-campaign)

1. 웹 캠페인에서 다음을 선택합니다. **[!UICONTROL 활성화하려면 검토]**.

   ![](assets/web-campaign-review.png)

1. 필요한 경우 콘텐츠, 속성, 표면, 대상자 및 일정을 검토하고 편집합니다.

1. 선택 **[!UICONTROL 활성화]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >을(를) 클릭한 후 **[!UICONTROL 활성화]**&#x200B;웹 캠페인 변경 사항을 웹 사이트에서 라이브로 제공하는 데 최대 15분이 걸릴 수 있습니다.

웹 캠페인은 **[!UICONTROL 라이브]** 상태 및 가 이제 선택한 대상자에게 표시됩니다. 캠페인의 각 수신자는 다음을 사용하여 웹 사이트에 추가한 수정 사항을 볼 수 있습니다. [!DNL Journey Optimizer] 웹 디자이너.

>[!NOTE]
>
>웹 캠페인에 대한 일정을 정의한 경우 다음과 같이 표시됩니다. **[!UICONTROL 예약됨]** 시작 날짜 및 시간에 도달할 때까지의 상태.
>
>이미 라이브 상태인 다른 캠페인과 동일한 페이지에 영향을 주는 웹 캠페인을 활성화하면 모든 변경 사항이 웹 페이지에 적용됩니다.

에서 캠페인 활성화에 대해 자세히 알아보기 [이 섹션](../campaigns/review-activate-campaign.md).

## 웹 캠페인 중지 {#stop-web-campaign}

웹 캠페인이 라이브일 때 이를 중지하여 대상자가 수정 사항을 보지 못하도록 할 수 있습니다. 아래 단계를 수행합니다.

1. 목록에서 라이브 캠페인을 선택합니다.

1. 상단 메뉴에서 을 선택합니다. **[!UICONTROL 캠페인 중지]**.

   ![](assets/web-campaign-stop.png)

1. 추가한 수정 사항은 정의한 대상자에게 더 이상 표시되지 않습니다.

>[!NOTE]
>
>웹 캠페인이 중지되면 다시 편집하거나 활성화할 수 없습니다. 복제하고 복제된 캠페인을 활성화할 수만 있습니다.
