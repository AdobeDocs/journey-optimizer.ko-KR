---
title: 웹 채널 전제 조건
description: Journey Optimizer 사용자 인터페이스에서 웹 페이지에 액세스하고 페이지를 작성하려면 이 페이지의 사전 요구 사항을 따르십시오
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 2%

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

* 하이브리드 모드 - 다음을 사용할 수 있습니다. [AEP Edge Network 서버 API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 개인화 서버측을 요청합니다. 응답은 수정 클라이언트측을 렌더링하도록 Adobe Experience Platform Web SDK에 제공됩니다. Adobe Experience Platform에서 자세히 알아보기 [Edge Network 서버 API 설명서](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. 하이브리드 모드에 대한 자세한 내용은에서 확인하고 일부 구현 샘플을 확인할 수 있습니다. [이 블로그 게시물](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

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

1. 클릭 **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 추가]**.

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
> * 웹 사이트에는 엄격한 보안 정책이 있습니다.
> * 웹 사이트가 iframe으로 되어 있습니다.
> * 고객의 QA 또는 스테이지 사이트를 외부 세계(사이트가 내부적임)에서 사용할 수 없습니다.

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

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 위치 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}을(를) 사용하여 하나의 병합 정책을 **[!UICONTROL Active-On-Edge 병합 정책]** 옵션이 활성화되었습니다. 이렇게 하려면 **[!UICONTROL 고객]** > **[!UICONTROL 프로필]** > **[!UICONTROL 병합 정책]** Experience Platform 메뉴. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  이 병합 정책은 다음 사용자가 사용합니다. [!DNL Journey Optimizer] 인바운드 채널을 통해 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Journey Optimizer 웹 경험의 전달 문제를 해결하려면 다음을 사용할 수 있습니다. **Edge 게재** 다음 범위 내 보기 **Adobe Experience Platform 보증**. 이 플러그인을 사용하면 요청 호출을 자세히 검사하고, 예상 Edge 호출이 예상대로 발생하는지 확인하고, ID 맵, 세그먼트 멤버십 및 동의 설정을 포함한 프로필 데이터를 검사할 수 있습니다. 또한 요청이 자격을 부여한 활동을 검토하고 자격이 없는 활동을 식별할 수 있습니다.

  사용 **Edge 게재** 플러그인은 인바운드 구현을 효과적으로 이해하고 문제를 해결하는 데 필요한 인사이트를 얻을 수 있도록 도와줍니다.

  [Edge 게재 보기에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## 콘텐츠 실험 사전 요구 사항 {#experiment-prerequisites}

웹 채널에 대해 콘텐츠 실험을 활성화하려면 [데이터 세트](../data/get-started-datasets.md) 웹 구현에 사용됨 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 는 보고 구성에도 포함됩니다.

즉, 실험 보고를 구성할 때 웹 데이터 스트림에 없는 데이터 세트를 추가하면 웹 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다.

에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아봅니다. [이 섹션](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템이며, 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

다음과 같은 경우 **아님** 다음 사전 정의 사용 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"} 데이터 세트 스키마의 경우: `AEP Web SDK ExperienceEvent` 및 `Consumer Experience Event` (에 정의됨) [이 페이지](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}) 다음 필드 그룹을 추가해야 합니다. `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, 및 `Web Details`. 이러한 요구 사항은 [!DNL Journey Optimizer] 콘텐츠 실험 보고는 각 프로필이 참여하고 있는 실험 및 처리를 추적합니다.

>[!NOTE]
>
>이러한 필드 그룹을 추가해도 일반 데이터 수집에는 영향을 주지 않습니다. 실험이 실행 중인 페이지에만 추가되며 다른 모든 추적은 그대로 유지됩니다.

## 에셋용 브랜드 도메인 {#branded-domains-for-assets}

웹 경험을 작성할 때에서 오는 콘텐츠를 추가하는 경우 [Adobe Experience Manager Assets](../content-management/assets.md) 라이브러리에서는 이 콘텐츠를 게시하는 데 사용할 하위 도메인을 설정해야 합니다. [자세히 알아보기](web-delegated-subdomains.md)
