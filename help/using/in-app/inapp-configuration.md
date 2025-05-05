---
title: 인앱 채널 사전 요구 사항 및 구성
description: Journey Optimizer을 사용하여 인앱 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
role: Admin
feature: In App
level: Intermediate
keywords: 인앱, 메시지, 구성, 플랫폼
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 9%

---

# 전제 조건 및 구성 {#inapp-configuration}

## 구성 단계 {#inapp-steps}

[!DNL Journey Optimizer]을(를) 사용하여 여정 및 캠페인에서 인앱 메시지를 보내려면 다음 구성 단계를 수행해야 합니다.

1. 시작하기 전에 적절한 Journey Optimizer 캠페인 권한이 있는지 확인해야 합니다. 인앱 메시지를 여정에서만 사용하려는 경우에도 마찬가지입니다. 이 경우에도 Campaign 권한이 필요합니다. [자세히 알아보기](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
1. Adobe Experience Platform 데이터 수집 데이터스트림에서 Adobe Journey Optimizer을 사용하도록 설정하고, 아래 [게재 필수 구성 요소](#delivery-prerequisites)에 설명된 대로 Adobe Experience Platform에서 기본 병합 정책을 확인하십시오.
1. [이 섹션](#channel-prerequisites)에 자세히 설명된 대로 관리 > 채널 > 채널 구성에서 인앱 메시지 채널 구성을 만듭니다.
1. 콘텐츠 실험을 사용하는 경우 [이 섹션](#experiment-prerequisite)에 나열된 요구 사항을 따라야 합니다.

권한 부여가 완료되면 첫 인앱 메시지를 만들고 구성하고 전송할 수 있습니다. 방법은 [이 섹션](create-in-app.md)을 참조하십시오.

## 게재 사전 요구 사항 {#delivery-prerequisites}

인앱 메시지를 올바르게 배달하려면 다음 설정을 정의해야 합니다.

* [Adobe Experience Platform 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}에서 **[!UICONTROL Adobe Experience Platform]** 서비스 아래에 Adobe Experience Platform Edge 및 **[!UICONTROL Adobe Journey Optimizer]** 옵션이 활성화되어 있는지와 같이 데이터 스트림이 정의되어 있는지 확인합니다.

  이렇게 하면 Journey Optimizer 인바운드 이벤트가 Adobe Experience Platform Edge에서 올바르게 처리됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko){target="_blank"}

  ![](assets/inapp_config_6.png)

* [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}에서 **[!UICONTROL Active-On-Edge 병합 정책]** 옵션이 활성화된 기본 병합 정책이 있는지 확인하십시오. 이렇게 하려면 **[!UICONTROL 고객]** > **[!UICONTROL 프로필]** > **[!UICONTROL 정책 병합]** Experience Platform 메뉴에서 정책을 선택합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko#configure){target="_blank"}

  [!DNL Journey Optimizer] 인바운드 채널이 이 병합 정책을 사용하여 에지에서 인바운드 캠페인을 올바르게 활성화하고 게시합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=ko){target="_blank"}

  >[!NOTE]
  >
  >사용자 지정 **[!UICONTROL 데이터 집합 환경 설정]** 병합 정책을 사용하는 경우 지정된 병합 정책 내에 **[!UICONTROL 여정 인바운드]** 데이터 집합을 추가해야 합니다.

  ![](assets/inapp_config_8.png)

* Journey Optimizer 모바일 경험의 배달 문제를 해결하려면 **Adobe Experience Platform Assurance**&#x200B;에서 **Edge Delivery** 보기를 사용할 수 있습니다. 이 플러그인을 사용하면 요청 호출을 자세히 검사하고, 예상 Edge 호출이 예상대로 발생하는지 확인하고, ID 맵, 세그먼트 멤버십 및 동의 설정을 포함한 프로필 데이터를 검사할 수 있습니다. 또한 요청이 자격을 부여한 활동을 검토하고 자격이 없는 활동을 식별할 수 있습니다.

  **Edge Delivery** 플러그인을 사용하면 인바운드 구현을 효과적으로 이해하고 문제를 해결하는 데 필요한 인사이트를 얻을 수 있습니다.

  [Edge Delivery 보기에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery)

## 인앱 구성 만들기 {#channel-prerequisites}


1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/inapp_config_1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력한 다음 구성할 채널을 선택합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.`, 하이픈 `-`도 사용할 수 있습니다.

1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

1. **인앱 메시지** 채널을 선택하십시오.

   ![](assets/inapp_config_9.png)

1. 설정을 정의할 플랫폼을 선택합니다. 이를 통해 각 플랫폼에 대한 대상 앱을 지정할 수 있으며, 여러 플랫폼에서 일관적으로 콘텐츠를 게재할 수 있습니다.

   >[!NOTE]
   >
   >iOS 및 Android 플랫폼의 경우 게재는 앱 ID만을 기반으로 합니다. 두 앱이 동일한 앱 ID를 공유하는 경우 **[!UICONTROL 채널 구성]**&#x200B;에서 선택한 플랫폼에 관계없이 콘텐츠가 두 앱 ID 모두에 전달됩니다.

   ![](assets/inapp_config_10.png)

1. 웹:

   * **[!UICONTROL 페이지 URL]**&#x200B;을 입력하여 특정 페이지에 변경 내용을 적용할 수 있습니다.

   * 동일한 패턴을 따르는 여러 URL을 타겟팅하는 규칙을 만들 수 있습니다.

+++ 페이지 일치 규칙을 작성하는 방법입니다.

      1. **[!UICONTROL 규칙과 일치하는 페이지]**&#x200B;을(를) 앱 구성으로 선택하고 **[!UICONTROL 페이지 URL]**&#x200B;을(를) 입력하십시오.

      1. **[!UICONTROL 구성 규칙 편집]** 창에서 **[!UICONTROL 도메인]** 및 **[!UICONTROL 페이지]** 필드에 대한 조건을 정의합니다.
      1. 조건 드롭다운에서 기준을 추가로 개인화합니다.

         예를 들어, 여기에서 Luma 웹 사이트의 모든 판매 제품 페이지에 표시되는 요소를 편집하려면 도메인 > 다음으로 시작 > luma 및 페이지 > 포함 > 판매 를 선택합니다.

         ![](assets/in_app_web_surface_4.png)

      1. 필요한 경우 다른 규칙을 만들려면 **[!UICONTROL 다른 페이지 규칙 추가]**&#x200B;를 클릭합니다.

      1. **[!UICONTROL 기본 작성 및 미리 보기 URL]**&#x200B;을(를) 선택하십시오.

      1. 변경 내용을 저장합니다. 규칙이 **[!UICONTROL 캠페인 만들기]** 화면에 표시됩니다.

+++

1. iOS 및 Android의 경우

   * **[!UICONTROL 앱 ID]**&#x200B;를 입력하세요.

1. 변경 사항을 제출합니다.

이제 인앱 메시지를 만들 때 구성을 선택할 수 있습니다.

## 보고 사전 요구 사항 {#experiment-prerequisites}

>[!NOTE]
>
>데이터 집합은 [!DNL Journey Optimizer] 보고 시스템에서 읽기 전용으로 사용되며 데이터 수집이나 데이터 수집에는 영향을 주지 않습니다.

인앱 채널에 대한 보고를 활성화하려면 인앱 구현 [데이터스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=ko){target="_blank"}에 사용된 [데이터 세트](../data/get-started-datasets.md)도 보고 구성에 포함되어 있는지 확인해야 합니다.

즉, 보고를 구성할 때 앱 데이터 스트림에 없는 데이터 세트를 추가하면 앱 데이터가 보고서에 표시되지 않습니다.

[이 섹션](../reports/reporting-configuration.md#add-datasets)에서 보고할 데이터 세트를 추가하는 방법을 알아보세요.

데이터 세트 스키마 `AEP Web SDK ExperienceEvent` 및 `Consumer Experience Event`([이 페이지](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html?lang=ko#add-field-groups){target="_blank"}에 정의됨)에 대해 미리 정의된 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}을(를) 사용하여 **not**&#x200B;하는 경우 `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` 및 `Web Details` 필드 그룹을 추가해야 합니다. [!DNL Journey Optimizer] 보고에서는 각 프로필이 참여하고 있는 캠페인과 여정을 추적하므로 이러한 항목이 필요합니다.

[보고 구성에 대해 자세히 알아보기](../reports/reporting-configuration.md)

>[!NOTE]
>
>이러한 필드 그룹을 추가해도 일반 데이터 수집에는 영향을 주지 않습니다. 다른 모든 추적은 그대로 두고 캠페인이나 여정이 실행 중인 페이지에만 추가됩니다

**관련 항목:**

* [인앱 메시지 만들기 ](create-in-app.md)
* [캠페인 만들기](../campaigns/create-campaign.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report-cja-inapp.md)

