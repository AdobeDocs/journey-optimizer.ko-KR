---
title: 코드 기반 경험 사전 요구 사항
description: Journey Optimizer 코드 기반 기능을 사용하여 앱 및 웹 페이지를 편집하려면 이 페이지의 사전 요구 사항을 따르십시오
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 3c9952f2e57c45d5bbd78d70ae7d401bc4555abe
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# 보호 기능 및 사전 요구 사항 {#web-prerequisites}

에서 코드 기반 경험 작업을 사용하려면 [!DNL Journey Optimizer] 애플리케이션에서 사용할 수 있는 코드 컨텐츠 페이로드를 전달하려면 아래 사전 요구 사항을 따르십시오.

* 응용 프로그램에 수정 사항을 추가하려면 특정 구현이 있어야 합니다. [자세히 알아보기](#implementation-prerequisites)

* 코드 기반 경험이 올바로 제공되도록 하려면 Adobe Experience Platform 설정 을 자세히 정의해야 합니다 [여기](#delivery-prerequisites).


## 주의 사항 {#caution-notes-web}

* 현재 위치 [!DNL Journey Optimizer] 에서는 코드 기반 경험만 만들 수 있습니다. **캠페인**. [자세히 알아보기](../campaigns/create-campaign.md#configure)

>[!AVAILABILITY]
>
>현재 Adobe을 구입한 조직에서는 코드 기반 경험 채널을 사용할 수 없습니다 **헬스케어 실드** 및 **개인 정보 보호 및 보안 보호** 추가 기능 제공.

## 구현 사전 요구 사항 {#implementation-prerequisites}

코드 기반 경험은 아래 옵션에 표시된 대로 모든 유형의 고객 구현을 지원합니다. 속성에 클라이언트측, 서버측 또는 하이브리드 구현 방법을 사용할 수 있습니다.

* 클라이언트측 전용 - 웹 페이지 또는 모바일 앱에 수정 사항을 추가하려면 다음 중 하나를 구현해야 합니다. [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 모바일 앱에서.

* 하이브리드 모드 - 다음을 사용할 수 있습니다. [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=ko-KR){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* 서버측 - 다음을 사용할 수 있습니다. [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 을 입력하여 서버측에 개인화를 요청합니다. 개발 팀은 응답을 처리하고 앱 구현에서 클라이언트측에서 수정 사항을 렌더링해야 합니다.

위의 각 구현 방법에 대한 샘플은에서 찾을 수 있습니다. [이 섹션](code-based-implementation-samples.md).

## 게재 사전 요구 사항 {#delivery-prerequisites}

코드 기반 경험을 올바르게 전달하려면 다음 설정을 정의해야 합니다.

* 다음에서 [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}와 같은 데이터 스트림이 아래에 정의되어 있는지 확인합니다. **[!UICONTROL Adobe Experience Platform]** 서비스 보유: **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되었습니다.

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 위치 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  이 병합 정책은 다음 사용자가 사용합니다. [!DNL Journey Optimizer] 인바운드 채널을 통해 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

## 콘텐츠 실험 사전 요구 사항 {#experiment-prerequisites}

코드 기반 채널에 대해 콘텐츠 실험을 활성화하려면 다음을 확인해야 합니다 [데이터 세트](../data/get-started-datasets.md) 앱 구현에 사용됨 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 는 보고 구성에도 포함됩니다.

즉, 실험 보고를 구성할 때 앱 데이터 스트림에 없는 데이터 세트를 추가하면 앱 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다.

에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아봅니다. [이 섹션](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템이며, 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.
