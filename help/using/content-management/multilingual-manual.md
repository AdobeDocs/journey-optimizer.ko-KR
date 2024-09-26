---
solution: Journey Optimizer
product: journey optimizer
title: 수동 번역을 사용하여 다국어 콘텐츠 만들기
description: Journey Optimizer에서 수동 번역을 사용하여 다국어 콘텐츠를 만드는 방법을 알아봅니다
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: 시작하기, 시작, 콘텐츠, 실험
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="제한된 가용성" type="Informative"
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 6%

---

# 수동 번역을 사용하여 다국어 콘텐츠 만들기 {#multilingual-manual}

>[!AVAILABILITY]
>
>다국어 콘텐츠는 현재 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 자세한 내용은 Adobe 담당자에게 문의하십시오.

수동 흐름을 사용하면 이메일, 푸시 알림 또는 SMS 캠페인 및 여정에서 콘텐츠를 손쉽게 직접 번역할 수 있으므로 다국어 메시지에 대한 정확한 제어 및 사용자 지정 옵션을 제공합니다. 또한 HTML 가져오기 옵션을 사용하여 기존 다국어 콘텐츠를 쉽게 가져올 수 있습니다.

수동 번역을 사용하여 다국어 콘텐츠를 만들려면 다음 단계를 따르십시오.

1. [로케일을 만듭니다](#create-locale).

1. [언어 설정을 만듭니다](#create-language-settings).

1. [다국어 콘텐츠를 만듭니다](#create-a-multilingual-campaign).

## 로케일 만들기 {#create-locale}

[언어 설정 만들기](#language-settings) 섹션에 설명된 대로 언어 설정을 구성할 때 특정 로케일을 다국어 콘텐츠에 사용할 수 없는 경우 **[!UICONTROL 번역]** 메뉴를 사용하여 필요한 수만큼 새 로케일을 만들 수 있습니다.

1. **[!UICONTROL 콘텐츠 관리]** 메뉴에서 **[!UICONTROL 번역]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 로케일 사전]** 탭에서 **[!UICONTROL 로케일 추가]**&#x200B;를 클릭합니다.

   ![](assets/locale_1.png)

1. **[!UICONTROL 언어]** 목록 및 관련 **[!UICONTROL 지역]**&#x200B;에서 로케일 코드를 선택합니다.

1. 로케일을 만들려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

   ![](assets/locale_2.png)

## 언어 설정 만들기 {#language-settings}

이 섹션에서는 다국어 콘텐츠 관리를 위한 기본 언어 및 관련 로케일을 설정할 수 있습니다. 프로필 언어와 관련된 정보를 조회하는 데 사용할 속성을 선택할 수도 있습니다

1. **[!UICONTROL 관리]** 메뉴에서 **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 언어 설정]** 메뉴에서 **[!UICONTROL 언어 설정 만들기]**&#x200B;를 클릭합니다.

   ![](assets/language_settings_1.png)

1. **[!UICONTROL 언어 설정]**&#x200B;의 이름을 입력하세요.

1. 이 설정에 연결된 **[!UICONTROL 로케일]**&#x200B;을(를) 선택하십시오. 최대 50개의 로케일을 추가할 수 있습니다.

   **[!UICONTROL 로케일]**&#x200B;이(가) 누락된 경우 **[!UICONTROL 번역]** 메뉴에서 또는 API별로 미리 수동으로 만들 수 있습니다. [새 로케일 만들기](#create-locale)를 참조하세요.

   ![](assets/multilingual-settings-2.png)

1. **[!UICONTROL 기본 설정 보내기]** 메뉴에서 프로필 언어에 대한 정보를 찾기 위해 조회할 특성을 선택합니다.

   ![](assets/multilingual-settings-3.png)

1. **[!UICONTROL 로케일]** 옆에 있는 **[!UICONTROL 편집]**&#x200B;을 클릭하여 추가로 개인화하고 **[!UICONTROL 프로필 환경 설정]**&#x200B;을(를) 추가하십시오.

   ![](assets/multilingual-settings-4.png)

1. 프로필 환경 설정 드롭다운에서 다른 **[!UICONTROL 로케일]**&#x200B;을 선택하고 **[!UICONTROL 프로필 추가]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 로케일]**&#x200B;의 고급 메뉴에 액세스하여 **[!UICONTROL 기본 로케일]**, 즉 프로필 특성이 지정되지 않은 경우 기본 언어를 정의합니다.

   이 고급 메뉴에서 로케일을 삭제할 수도 있습니다.

   ![](assets/multilingual-settings-5.png)

1. **[!UICONTROL 제출]**&#x200B;을 클릭하여 **[!UICONTROL 언어 설정]**&#x200B;을 만듭니다.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## 다국어 콘텐츠 만들기 {#create-multilingual-campaign}

다국어 콘텐츠를 설정한 후에는 캠페인이나 여정을 제작하고 선택한 각 로케일에 대한 콘텐츠를 사용자 지정할 수 있습니다.

1. 요구 사항에 따라 이메일, SMS 또는 푸시 알림 [campaign](../campaigns/create-campaign.md) 또는 [여정](../building-journeys/journeys-message.md)을(를) 만들고 구성하는 것부터 시작합니다.

   >[!AVAILABILITY]
   >
   >여정 당 하나의 번역 프로젝트만 포함하는 것이 좋습니다.

1. 원래 콘텐츠를 만들거나 가져온 후 필요에 따라 개인화합니다.

1. 기본 콘텐츠가 만들어지면 **[!UICONTROL 저장]**&#x200B;을 클릭하고 캠페인 구성 화면으로 돌아갑니다.

   ![](assets/multilingual-campaign-2.png)

1. **[!UICONTROL 언어 추가]**&#x200B;를 클릭하고 이전에 만든 **[!UICONTROL 언어 설정]**&#x200B;을 선택합니다. [자세히 알아보기](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. **[!UICONTROL 로케일]** 메뉴의 고급 설정에 액세스하여 **[!UICONTROL 모든 로케일에 기본 복사]**&#x200B;를 선택합니다.

   ![](assets/multilingual-campaign-4.png)

1. 이제 기본 콘텐츠가 선택한 **[!UICONTROL 로케일]** 전체에서 복제되었으므로 각 로케일에 액세스하고 **[!UICONTROL 전자 메일 본문 편집]**&#x200B;을 클릭하여 콘텐츠를 번역하십시오.

   ![](assets/multilingual-campaign-5.png)

1. 선택한 로케일의 **[!UICONTROL 추가 작업]** 메뉴를 사용하여 로케일을 비활성화하거나 활성화할 수 있습니다.

   ![](assets/multilingual-campaign-6.png)

1. 다국어 구성을 비활성화하려면 **[!UICONTROL 언어 추가]**&#x200B;를 클릭하고 로컬 언어로 유지할 언어를 선택하십시오.

   ![](assets/multilingual-campaign-7.png)

1. **[!UICONTROL 활성화하려면 검토]**&#x200B;를 클릭하여 캠페인 요약을 표시합니다.

   요약을 사용하면 필요한 경우 캠페인을 수정하고 매개 변수가 틀리거나 누락되었는지 확인할 수 있습니다.

1. 다국어 콘텐츠를 탐색하여 각 언어로 렌더링을 확인합니다.

   ![](assets/multilingual-campaign-8.png)

이제 캠페인이나 여정을 활성화할 수 있습니다. 전송되면 보고서 내에서 다국어 여정 또는 캠페인의 영향을 측정할 수 있습니다.

>[!IMPORTANT]
>
>9월 릴리스부터 새로운 캠페인 및 여정 활성화 환경을 사용하면 전체 승인 프로세스를 관리할 수 있으므로 캠페인 및 여정이 시작하기 전에 해당 관련자로부터 철저하게 검토 및 승인되도록 합니다. 이 기능은 제한된 가용성으로 사용할 수 있습니다. [자세히 알아보기](../test-approve/gs-approval.md)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
