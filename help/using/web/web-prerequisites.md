---
title: 웹 채널 전제 조건
description: Journey Optimizer 사용자 인터페이스에서 웹 페이지에 액세스하고 페이지를 작성하려면 이 페이지의 사전 요구 사항을 따르십시오
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: a20e01e66138ea5bb7be4d36c0d55b24ab9426db
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 11%

---

# 사전 요구 사항 및 보호 기능 {#web-prerequisites}

에서 웹 페이지에 액세스하고 웹 페이지를 작성하려면 [!DNL Journey Optimizer] 사용자 인터페이스에서 아래 사전 요구 사항을 따르십시오.

* 웹 사이트에 수정 사항을 추가하려면 특정 구현이 있어야 합니다. [자세히 알아보기](#implementation-prerequisites)

* 에 액세스하려면 [!DNL Journey Optimizer] 웹 디자이너에는 특정 Google Chrome 브라우저 확장 프로그램이 설치되어 있어야 합니다. [자세히 알아보기](#visual-authoring-prerequesites)

* 웹 경험이 제대로 제공되도록 하려면 Adobe Experience Platform 설정을 자세히 정의해야 합니다 [여기](#delivery-prerequisites).

## 주의 사항 {#caution-notes-web}

* 현재 위치 [!DNL Journey Optimizer] 다음에서만 웹 경험을 만들 수 있습니다. **캠페인**. [자세히 알아보기](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] 웹 캠페인은 다른 채널에서 이전에 참여하지 않은 새 프로필을 타겟팅합니다. 이렇게 하면 총 참여 가능 프로필 수가 증가하므로 구입한 계약 참여 가능 프로필 수를 초과하는 경우 비용이 발생할 수 있습니다. 각 패키지에 대한 라이선스 지표는 [Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} 페이지를 가리키도록 업데이트하는 중입니다.


>[!AVAILABILITY]
>
>현재 Adobe을 구입한 조직에서는 웹 채널을 사용할 수 없습니다 **헬스케어 실드** 및 **개인 정보 보호 및 보안 보호** 추가 기능 제공.

## 구현 사전 요구 사항 {#implementation-prerequisites}

현재 웹 속성에서 웹 채널 캠페인을 작성 및 게재할 수 있도록 두 가지 유형의 구현이 지원됩니다.

* 클라이언트측 전용 - 웹 사이트에 수정 사항을 추가하려면 다음을 구현해야 합니다 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"} 웹 사이트에서.

  >[!NOTE]
  >
  >AEP 웹 SDK 버전이 2.16 이상인지 확인하십시오.

* 하이브리드 모드 - 다음을 사용할 수 있습니다. [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=ko-KR){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>서버측 전용 구현은 현재 지원되지 않습니다.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 시각적 작성 사전 요구 사항 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

웹 페이지를 안정적으로 열고, 작성하고, 미리 보려면 [!DNL Journey Optimizer] 웹 디자이너에는 [Adobe Experience Cloud Visual Edit Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 웹 브라우저에 설치된 브라우저 확장 프로그램.

>[!CAUTION]
>
>Google Chrome 및 Microsoft Edge는에서 웹 페이지 작성을 지원하는 유일한 브라우저입니다. [!DNL Journey Optimizer].

### Visual Editing Helper 확장 기능 설치 {#install-visual-editing-helper}

Visual Editing Helper 브라우저 확장 기능을 다운로드하여 설치하려면 아래 단계를 수행하십시오.

1. 브라우저에서 새 탭(Google Chrome 또는 Microsoft Edge)을 엽니다.

1. 로 이동 [Google Chrome 웹 스토어](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Microsoft Edge를 사용하는 경우 **[!UICONTROL 다른 스토어의 확장 허용]** 상단 배너에서 이렇게 하면 Chrome 웹 스토어의 확장을 Microsoft Edge에 추가할 수 있습니다.

1. 검색 후 다음 위치로 이동 [Adobe Experience Cloud Visual Edit Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 브라우저 확장.

1. **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 기능 추가]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >Microsoft Edge를 사용하는 경우 버튼 레이블이 지정 되더라도 확장이 Edge에 추가됩니다 **[!UICONTROL Chrome에 추가]**.

1. 브라우저의 도구 모음에서 Visual Editing Helper 브라우저 확장 기능이 올바르게 활성화되어 있는지 확인합니다.

   ![](assets/web-visual-editing-extension-edge.png)

이제 웹 사이트에서 웹 사이트를 열 때 Adobe Experience Cloud Visual Editing Helper가 자동으로 활성화됩니다. [!DNL Journey Optimizer] [웹 디자이너](edit-web-content.md#work-with-web-designer) 작성 기능을 향상시킵니다.

확장 기능에는 조건부 설정이 없으며 SameSite 쿠키 설정을 포함하여 모든 설정을 자동으로 처리합니다.

>[!NOTE]
>
>일부 웹 사이트는 [!DNL Journey Optimizer] 다음 이유 중 하나로 인한 웹 디자이너:
>
> * 웹 사이트에 엄격한 보안 정책이 있습니다.
> * 웹 사이트가 iframe으로 되어 있습니다.
> * 고객의 QA 또는 스테이지 사이트는 외부에서 사용할 수 없습니다(사이트는 내부 사이트임).

### 웹 사이트 로드 문제 해결 {#troubleshooting}

Adobe 사용 시 [!DNL Journey Optimizer] 웹 디자이너 로드에 실패한 웹 사이트를 로드하려고 하면 다음을 설치하라는 메시지가 표시됩니다. [Visual Editing Helper 브라우저 확장 기능](#install-visual-editing-helper).

1. Visual Editing Helper 브라우저 확장 기능이 올바르게 설치되어 있는지 확인합니다.

1. 웹 사이트가 여전히 예기치 않게 작동하는 경우 브라우저에서 타사 쿠키가 허용되는지 확인하십시오. 그렇지 않으면 웹 페이지를 [!DNL Journey Optimizer] 웹 디자이너.

인증 중인 페이지의 경우 로그인 페이지가 로드되지 않거나 로그인을 시도한 후에도 여전히 로그인되지 않습니다.

1. 먼저 새 브라우저 탭에 로그인하고 원하는 페이지로 이동한 다음 URL을 복사하고 [!DNL Journey Optimizer] 웹 디자이너.

2. 에서 웹 사이트를 로드할 수 없는 경우 [!DNL Journey Optimizer] 웹 디자이너에서 Adobe 고객 지원 센터에 문의하여 문제를 보고하여 실패한 URL을 지정하십시오.

## 게재 사전 요구 사항 {#delivery-prerequisites}

웹 경험을 올바르게 전달하려면 다음 설정을 정의해야 합니다.

* 다음에서 [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}와 같은 데이터 스트림이 아래에 정의되어 있는지 확인합니다. **[!UICONTROL Adobe Experience Platform]** 서비스 보유: **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되었습니다.

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 위치 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  이 병합 정책은 다음 사용자가 사용합니다. [!DNL Journey Optimizer] 인바운드 채널을 통해 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## 콘텐츠 실험 사전 요구 사항 {#experiment-prerequisites}

웹 채널에 대해 콘텐츠 실험을 활성화하려면 [데이터 세트](../data/get-started-datasets.md) 웹 구현에 사용됨 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=ko-KR){target="_blank"} 는 보고 구성에도 포함됩니다.

즉, 실험 보고를 구성할 때 웹 데이터 스트림에 없는 데이터 세트를 추가하면 웹 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다.

에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아봅니다. [이 섹션](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템이며, 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

다음과 같은 경우 **아님** 다음 사전 정의 사용 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}) 다음 필드 그룹을 추가해야 합니다. `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, 및 `Web Details`. 이러한 요구 사항은 [!DNL Journey Optimizer] 콘텐츠 실험 보고는 각 프로필이 참여하고 있는 실험 및 처리를 추적합니다.

>[!NOTE]
>
>이러한 필드 그룹을 추가해도 일반 데이터 수집에는 영향을 주지 않습니다. 실험이 실행 중인 페이지에만 추가되며 다른 모든 추적은 그대로 유지됩니다.

## 에셋용 브랜드 도메인 {#branded-domains-for-assets}

웹 경험을 작성할 때에서 오는 콘텐츠를 추가하는 경우 [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) 라이브러리에서는 이 콘텐츠를 게시하는 데 사용할 하위 도메인을 설정해야 합니다. [자세히 알아보기](web-delegated-subdomains.md)
