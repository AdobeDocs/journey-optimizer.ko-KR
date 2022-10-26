---
title: 인앱 구성
description: Journey Optimizer을 사용하여 인앱 메시지를 전송하도록 환경을 구성하는 방법을 알아봅니다
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# 인앱 채널 구성 {#inapp-configuration}

인앱 메시지를 보내기 전에 인앱 채널을에서 구성해야 합니다 [!DNL Adobe Experience Platform Data Collection].

1. 사용 [!DNL Adobe Experience Platform Data Collection] 계정, 액세스 권한 **[!UICONTROL 데이터 스트림]** 메뉴를 클릭하고 **[!UICONTROL 새 데이터 스트림]**. 데이터 스트림 만들기에 대한 자세한 내용은 [이 페이지](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. 을(를) 선택합니다 [!DNL Adobe Experience Platform] 서비스.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] 및 [!DNL Adobe Journey Optimizer] 을 선택해야 합니다.

   ![](assets/inapp_config_6.png)

1. 그런 다음 **[!UICONTROL 앱 서피스]** 메뉴를 클릭한 다음 **[!UICONTROL 앱 서피스 만들기]**.

   ![](assets/inapp_config_1.png)

1. 에 이름 추가 **[!UICONTROL 앱 표면]**.

1. Apple iOS 드롭다운에서 **iOS 번들 ID**. 을(를) 참조하십시오. [Apple 설명서](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 추가 정보 **번들 ID**.

   ![](assets/inapp_config_2.png)

1. Android 드롭다운에서 을(를) 입력합니다. **Android 패키지 이름**. 을(를) 참조하십시오. [Android 설명서](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 추가 정보 **패키지 이름**.

1. 클릭 **[!UICONTROL 저장]** 구성을 마치면 **[!UICONTROL 앱 표면]**.

   ![](assets/inapp_config_3.png)

   사용자 **[!UICONTROL 앱 표면]** 이제 인앱 메시지로 새 캠페인을 만들 때 사용할 수 있습니다. [자세히 보기](create-in-app.md)

1. 앱 서피스를 만든 후 이제 모바일 속성을 만들어야 합니다.

   을(를) 참조하십시오. [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 자세한 절차.

   ![](assets/inapp_config_4.png)

1. 새로 만든 속성의 확장 메뉴에서 다음 확장을 설치합니다.

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP Assurance
   * 동의
   * 식별
   * Mobile Core
   * 프로필

   을(를) 참조하십시오. [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) 자세한 절차.

   ![](assets/inapp_config_5.png)

이제 인앱 채널이 구성되었습니다. 사용자에게 인앱 메시지 보내기를 시작할 수 있습니다.

**관련 항목:**

* [인앱 메시지 만들기](create-in-app.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서](inapp-report.md)
