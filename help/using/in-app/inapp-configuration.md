---
title: 인앱 채널 사전 요구 사항 및 구성
description: Journey Optimizer을 사용하여 인앱 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
role: Admin
feature: In App
level: Intermediate
keywords: 인앱, 메시지, 구성, 플랫폼
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 9%

---

# 전제 조건 및 구성 {#inapp-configuration}

## 구성 단계 {#inapp-steps}

[!DNL Journey Optimizer]을(를) 사용하여 여정 및 캠페인에서 인앱 메시지를 보내려면 다음 구성 단계를 수행해야 합니다.

1. 시작하기 전에 적절한 Journey Optimizer 캠페인 권한이 있는지 확인해야 합니다. 인앱 메시지를 여정에서만 사용하려는 경우에도 마찬가지입니다. 이 경우에도 Campaign 권한이 필요합니다. [자세히 알아보기](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
Adobe Experience Platform 데이터 컬렉션의 **앱 표면** 메뉴에 액세스하려면 특정 권한을 부여해야 합니다. [이 비디오](#video)에서 자세히 알아보세요.
1. Adobe Experience Platform 데이터 수집 데이터스트림에서 Adobe Journey Optimizer을 사용하도록 설정하고, 아래 [게재 필수 구성 요소](#delivery-prerequisites)에 설명된 대로 Adobe Experience Platform에서 기본 병합 정책을 확인하십시오.
1. [이 섹션](#channel-prerequisites)에 자세히 설명된 대로 Adobe Experience Platform 데이터 수집에서 앱 표면을 만들고 구성합니다.
1. 콘텐츠 실험을 사용하는 경우 [이 섹션](#experiment-prerequisite)에 나열된 요구 사항을 따라야 합니다.

권한 부여가 완료되면 첫 인앱 메시지를 만들고 구성하고 전송할 수 있습니다. 방법은 [이 섹션](create-in-app.md)을 참조하십시오.

## 게재 사전 요구 사항 {#delivery-prerequisites}

인앱 메시지를 올바르게 배달하려면 다음 설정을 정의해야 합니다.

* [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}에서 **[!UICONTROL Adobe Experience Platform]** 서비스 아래에 Adobe Experience Platform Edge 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되어 있는지와 같이 데이터 스트림이 정의되어 있는지 확인합니다.

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}에서 **[!UICONTROL Active-On-Edge 병합 정책]** 옵션이 활성화된 기본 병합 정책이 있는지 확인하십시오. 이렇게 하려면 **[!UICONTROL 고객]** > **[!UICONTROL 프로필]** > **[!UICONTROL 정책 병합]** Experience Platform 메뉴에서 정책을 선택합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  [!DNL Journey Optimizer] 인바운드 채널이 이 병합 정책을 사용하여 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  >[!NOTE]
  >
  >사용자 지정 **[!UICONTROL 데이터 집합 환경 설정]** 병합 정책을 사용하는 경우 지정된 병합 정책 내에 **[!UICONTROL 여정 인바운드]** 데이터 집합을 추가해야 합니다.

  ![](assets/inapp_config_8.png)

* Journey Optimizer 모바일 경험의 배달 문제를 해결하려면 **Adobe Experience Platform Assurance** 내에서 **Edge Delivery** 보기를 사용할 수 있습니다. 이 플러그인을 사용하면 요청 호출을 자세히 검사하고, 예상 Edge 호출이 예상대로 발생하는지 확인하고, ID 맵, 세그먼트 멤버십 및 동의 설정을 포함한 프로필 데이터를 검사할 수 있습니다. 또한 요청이 자격을 부여한 활동을 검토하고 자격이 없는 활동을 식별할 수 있습니다.

  **Edge Delivery** 플러그인을 사용하면 인바운드 구현을 효과적으로 이해하고 문제를 해결하는 데 필요한 인사이트를 얻을 수 있습니다.

  [Edge Delivery 보기에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery)

## 채널 구성 사전 요구 사항 {#channel-prerequisites}

1. **[!UICONTROL 앱 표면]** 메뉴에 액세스하고 **[!UICONTROL 앱 표면 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 앱 표면]**&#x200B;에 이름을 추가하십시오.

   ![](assets/inapp_config_2b.png)

1. **[!UICONTROL Apple iOS]** 드롭다운에서 Apple iOS에 대한 모바일 애플리케이션을 구성합니다.

+++ 추가 정보

   1. **[!UICONTROL iOS 번들 ID]**&#x200B;를 입력하세요. **번들 ID**&#x200B;에 대한 자세한 내용은 [Apple 설명서](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids)를 참조하세요.

   1. (선택 사항) 푸시 알림을 전송할 **[!UICONTROL 샌드박스]**&#x200B;를 선택합니다. 특정 샌드박스를 선택하려면 필요한 액세스 권한이 필요합니다.

      샌드박스 관리에 대한 자세한 내용은 [이 페이지](../administration/sandboxes.md#assign-sandboxes)를 참조하세요.

   1. 필요한 경우 **[!UICONTROL 자격 증명 푸시]** 옵션을 사용하여 .p8 인증 키 파일을 끌어서 놓습니다.

      **[!UICONTROL 푸시 자격 증명 수동 입력]** 옵션을 활성화하여 APNs 인증 키를 직접 복사하여 붙여넣을 수도 있습니다.

   1. **[!UICONTROL 키 ID]** 및 **[!UICONTROL 팀 ID]**&#x200B;을(를) 입력하십시오.

      ![](assets/inapp_config_2.png)

+++

1. **[!UICONTROL Android]** 드롭다운에서 Android용 모바일 애플리케이션을 구성합니다.

+++ 추가 정보

   1. **[!UICONTROL Android 패키지 이름]**&#x200B;을(를) 입력하십시오. **패키지 이름**&#x200B;에 대한 자세한 내용은 [Android 설명서](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores)를 참조하세요.

   1. (선택 사항) 푸시 알림을 전송할 **[!UICONTROL 샌드박스]**&#x200B;를 선택합니다. 특정 샌드박스를 선택하려면 필요한 액세스 권한이 필요합니다.

      샌드박스 관리에 대한 자세한 내용은 [이 페이지](../administration/sandboxes.md#assign-sandboxes)를 참조하세요.

   1. 필요한 경우 **[!UICONTROL 자격 증명 푸시]** 옵션을 사용하여 .json 개인 키 파일을 끌어서 놓습니다.

      **[!UICONTROL 푸시 자격 증명을 수동으로 입력]** 옵션을 활성화하여 FCM 개인 키를 직접 복사하여 붙여넣을 수도 있습니다.

      ![](assets/inapp_config_7.png)

1. **[!UICONTROL 앱 표면]**&#x200B;의 구성을 마치면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![](assets/inapp_config_3.png)

   인앱 메시지를 사용하여 새 캠페인을 만들 때 **[!UICONTROL 앱 표면]**&#x200B;을 사용할 수 있습니다. [자세히 알아보기](create-in-app.md)

1. 앱 표면을 만든 후 이제 모바일 속성을 만들어야 합니다.

   자세한 절차는 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile)를 참조하세요.

   ![](assets/inapp_config_4.png)

1. 새로 만든 속성의 확장 메뉴에서 다음 확장을 설치합니다.

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP 보증
   * 동의
   * 신원
   * 모바일 코어
   * 프로필

   자세한 절차는 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension)를 참조하세요.

   ![](assets/inapp_config_5.png)

이제 인앱 채널이 구성되었습니다. 사용자에게 인앱 메시지를 보낼 수 있습니다.

## 콘텐츠 실험 사전 요구 사항 {#experiment-prerequisites}

인앱 채널에 대한 콘텐츠 실험을 활성화하려면 인앱 구현 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}에 사용된 [데이터 세트](../data/get-started-datasets.md)도 보고 구성에 포함되어 있는지 확인해야 합니다.

즉, 실험 보고를 구성할 때 웹 데이터 스트림에 없는 데이터 세트를 추가하면 웹 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다.

[이 섹션](../content-management/reporting-configuration.md#add-datasets)에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아보세요.

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템에서 읽기 전용으로 사용되며 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

데이터 세트 스키마 `AEP Web SDK ExperienceEvent` 및 `Consumer Experience Event`([이 페이지](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}에 정의됨)에 대해 미리 정의된 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}을(를) 사용하여 **not**&#x200B;하는 경우 `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` 및 `Web Details` 필드 그룹을 추가해야 합니다. 각 프로필이 참여하고 있는 실험과 처리를 추적하는 [!DNL Journey Optimizer] 콘텐츠 실험 보고에서 이러한 항목이 필요합니다.

>[!NOTE]
>
>이러한 필드 그룹을 추가해도 일반 데이터 수집에는 영향을 주지 않습니다. 실험이 실행 중인 페이지에만 추가되며 다른 모든 추적은 그대로 유지됩니다.

## 방법 비디오{#video}

아래 비디오에서는 앱 표면 메뉴에 액세스하기 위해 **앱 구성 관리** 권한을 할당하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**관련 항목:**

* [인앱 메시지 만들기 ](create-in-app.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)

