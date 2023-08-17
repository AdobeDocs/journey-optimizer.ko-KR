---
title: 인앱 구성
description: Journey Optimizer을 사용하여 인앱 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
role: Admin
level: Intermediate
keywords: 인앱, 메시지, 구성, 플랫폼
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 13020825a0cf06bd67f48ccbe6f46b6eaea210d3
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 10%

---

# 인앱 채널 구성 {#inapp-configuration}

인앱 메시지를 보내기 전에에서 인앱 채널을 구성해야 합니다 [!DNL Adobe Experience Platform Data Collection].

1. 출처: [!DNL Adobe Experience Platform Data Collection] 계정, 액세스 **[!UICONTROL 데이터스트림]** 메뉴 및 클릭 **[!UICONTROL 새 데이터스트림]**. 데이터 스트림 만들기에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR).

1. 다음 항목 선택 [!DNL Adobe Experience Platform] 서비스.

   [!DNL Edge Segmentation] 및 [!DNL Adobe Journey Optimizer] 을(를) 선택해야 합니다.

   ![](assets/inapp_config_6.png)

   >[!NOTE]
   >
   >인앱 채널에 대해 콘텐츠 실험을 활성화하려면 다음을 확인해야 합니다. [데이터 세트](../data/get-started-datasets.md) 인앱에서 사용됨 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=ko-KR){target="_blank"} 는 보고 구성에도 있습니다. 그렇지 않으면 인앱 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다. [데이터 세트를 추가하는 방법 알아보기](../campaigns/reporting-configuration.md#add-datasets)
   >
   >데이터 집합은 [!DNL Journey Optimizer] 보고 시스템이며, 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

1. 그런 다음 **[!UICONTROL 앱 표면]** 메뉴 및 클릭 **[!UICONTROL 앱 표면 만들기]**.

   >[!NOTE]
   >
   > 다음이 필요합니다. **앱 구성 관리** 다음에 대한 액세스 권한을 가집니다. **[!UICONTROL 앱 표면]** 메뉴 아래의 제품에서 사용할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [이 비디오](#video).

   ![](assets/inapp_config_1.png)

1. 에 이름 추가 **[!UICONTROL 앱 표면]**.


1. Apple iOS 드롭다운에서 **iOS 번들 ID**. 을(를) 참조하십시오 [Apple 설명서](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 에 대한 추가 정보를 위해 **번들 ID**.

   ![](assets/inapp_config_2.png)

1. Android 드롭다운에서 **Android 패키지 이름**. 을(를) 참조하십시오 [Android 설명서](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 에 대한 추가 정보를 위해 **패키지 이름**.

1. 클릭 **[!UICONTROL 저장]** 의 구성을 완료했을 때 **[!UICONTROL 앱 표면]**.

   ![](assets/inapp_config_3.png)

   사용자 **[!UICONTROL 앱 표면]** 이제 인앱 메시지로 새 캠페인을 만들 때 사용할 수 있습니다. [자세히 알아보기](create-in-app.md)

1. 앱 표면을 만든 후 이제 모바일 속성을 만들어야 합니다.

   을(를) 참조하십시오 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 자세한 절차.

   ![](assets/inapp_config_4.png)

1. 새로 만든 속성의 확장 메뉴에서 다음 확장을 설치합니다.

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP 보증
   * 동의
   * 신원
   * 모바일 코어
   * 프로필

   을(를) 참조하십시오 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) 자세한 절차.

   ![](assets/inapp_config_5.png)

이제 인앱 채널이 구성되었습니다. 사용자에게 인앱 메시지를 보낼 수 있습니다.

**관련 항목:**

* [인앱 메시지 만들기 ](create-in-app.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)


## 방법 비디오{#video}

* 아래 비디오에서는 를 할당하는 방법을 보여 줍니다. **앱 구성 관리** 앱 표면 메뉴에 대한 액세스 권한.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)

