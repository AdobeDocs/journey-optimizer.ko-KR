---
title: 인앱 채널 사전 요구 사항
description: Journey Optimizer을 사용하여 인앱 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
role: Admin
feature: In App
level: Intermediate
keywords: 인앱, 메시지, 구성, 플랫폼
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 7e850261f1a82492c5df93c4437b4e3c6859a2d7
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 6%

---

# 인앱 채널 사전 요구 사항 {#inapp-configuration}

## 게재 사전 요구 사항 {#delivery-prerequisites}

인앱 메시지를 올바르게 배달하려면 다음 설정을 정의해야 합니다.

* 다음에서 [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}와 같은 데이터 스트림이 아래에 정의되어 있는지 확인합니다. **[!UICONTROL Adobe Experience Platform]** Adobe Experience Platform Edge 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되었습니다.

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR){target="_blank"}

  ![](assets/inapp_config_6.png)

* 위치 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}, make sure you have the default merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  이 병합 정책은 다음 사용자가 사용합니다. [!DNL Journey Optimizer] 인바운드 채널을 통해 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  >[!NOTE]
  >
  >사용자 지정 사용 시 **[!UICONTROL 데이터 세트 환경 설정]** 병합 정책입니다. 다음을 추가하십시오. **[!UICONTROL 여정 인바운드]** 지정된 병합 정책 내의 데이터 세트입니다.

  ![](assets/inapp_config_8.png)

## 채널 구성 사전 요구 사항 {#channel-prerequisites}

1. 액세스 **[!UICONTROL 앱 표면]** 메뉴 및 클릭 **[!UICONTROL 앱 표면 만들기]**.

1. 에 이름 추가 **[!UICONTROL 앱 표면]**.

   ![](assets/inapp_config_2b.png)

1. 다음에서 **[!UICONTROL Apple iOS]** 드롭다운에서 Apple iOS에 대한 모바일 애플리케이션을 구성합니다.

+++ 추가 정보

   1. 을(를) 입력합니다. **[!UICONTROL iOS 번들 ID]**. 을(를) 참조하십시오 [Apple 설명서](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 에 대한 추가 정보를 위해 **번들 ID**.

   1. (선택 사항) **[!UICONTROL 샌드박스]** 푸시 알림을 보낼 위치. 특정 샌드박스를 선택하려면 필요한 액세스 권한이 필요합니다.

      샌드박스 관리에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../administration/sandboxes.md#assign-sandboxes).

   1. 활성화 **[!UICONTROL 푸시 자격 증명]** 필요한 경우 .p8 인증 키 파일을 끌어서 놓는 옵션입니다.

      또한 을 활성화할 수 있습니다. **[!UICONTROL 푸시 자격 증명 수동 입력]** APNs 인증 키를 직접 복사하여 붙여넣는 옵션.

   1. 다음을 입력하십시오. **[!UICONTROL 키 ID]** 및 **[!UICONTROL 팀 ID]**.

      ![](assets/inapp_config_2.png)

+++

1. 다음에서 **[!UICONTROL Android]** 드롭다운에서 Android용 모바일 애플리케이션을 구성합니다.

+++ 추가 정보

   1. 을(를) 입력합니다. **[!UICONTROL Android 패키지 이름]**. 을(를) 참조하십시오 [Android 설명서](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 에 대한 추가 정보를 위해 **패키지 이름**.

   1. (선택 사항) **[!UICONTROL 샌드박스]** 푸시 알림을 보낼 위치. 특정 샌드박스를 선택하려면 필요한 액세스 권한이 필요합니다.

      샌드박스 관리에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../administration/sandboxes.md#assign-sandboxes).

   1. 활성화 **[!UICONTROL 푸시 자격 증명]** 필요한 경우 .json 개인 키 파일을 드래그 앤 드롭하는 옵션입니다.

      또한 을 활성화할 수 있습니다. **[!UICONTROL 푸시 자격 증명 수동 입력]** 옵션을 사용하여 FCM 개인 키를 직접 복사하여 붙여넣을 수 있습니다.

      ![](assets/inapp_config_7.png)

1. 클릭 **[!UICONTROL 저장]** 의 구성을 완료했을 때 **[!UICONTROL 앱 표면]**.

   ![](assets/inapp_config_3.png)

   사용자 **[!UICONTROL 앱 표면]** 이제 인앱 메시지로 새 캠페인을 만들 때 사용할 수 있습니다. [자세히 알아보기](create-in-app.md)

1. 앱 표면을 만든 후 이제 모바일 속성을 만들어야 합니다.

   을(를) 참조하십시오 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 자세한 절차.

   ![](assets/inapp_config_4.png)

1. 새로 만든 속성의 확장 메뉴에서 다음 확장을 설치합니다.

   * Adobe Experience Platform 에지 네트워크
   * Adobe Journey Optimizer
   * AEP 보증
   * 동의
   * 신원
   * 모바일 코어
   * 프로필

   을(를) 참조하십시오 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) 자세한 절차.

   ![](assets/inapp_config_5.png)

이제 인앱 채널이 구성되었습니다. 사용자에게 인앱 메시지를 보낼 수 있습니다.

## 콘텐츠 실험 사전 요구 사항 {#experiment-prerequisites}

인앱 채널에 대해 콘텐츠 실험을 활성화하려면 다음을 확인해야 합니다. [데이터 세트](../data/get-started-datasets.md) 인앱 구현에 사용됨 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 는 보고 구성에도 포함됩니다.

즉, 실험 보고를 구성할 때 웹 데이터 스트림에 없는 데이터 세트를 추가하면 웹 데이터가 콘텐츠 실험 보고서에 표시되지 않습니다.

에서 콘텐츠 실험 보고를 위한 데이터 세트를 추가하는 방법을 알아봅니다. [이 섹션](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템이며, 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

다음과 같은 경우 **아님** 다음 사전 정의 사용 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}) 다음 필드 그룹을 추가해야 합니다. `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, 및 `Web Details`. 이러한 요구 사항은 [!DNL Journey Optimizer] 콘텐츠 실험 보고는 각 프로필이 참여하고 있는 실험 및 처리를 추적합니다.

>[!NOTE]
>
>이러한 필드 그룹을 추가해도 일반 데이터 수집에는 영향을 주지 않습니다. 실험이 실행 중인 페이지에만 추가되며 다른 모든 추적은 그대로 유지됩니다.

## 방법 비디오{#video}

* 아래 비디오에서는 를 할당하는 방법을 보여 줍니다. **앱 구성 관리** 앱 표면 메뉴에 대한 액세스 권한.

  +++비디오 참조

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++

**관련 항목:**

* [인앱 메시지 만들기 ](create-in-app.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)

