---
title: 랜딩 페이지 사전 설정 정의
description: Journey Optimizer에서 랜딩 페이지를 만들고 사용하도록 환경을 구성하는 방법을 알아봅니다
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# 랜딩 페이지 사전 설정 정의 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="랜딩 페이지 사전 설정 만들기"
>abstract="랜딩 페이지를 작성하고 Journey Optimizer을 통해 이를 활용하려면 사용할 하위 도메인을 포함하는 랜딩 페이지 사전 설정을 만들어야 합니다."

When [랜딩 페이지 만들기](../landing-pages/create-lp.md#create-a-lp)을(를) 통해 랜딩 페이지를 작성하고 활용할 수 있으려면 랜딩 페이지 사전 설정을 선택해야 합니다 **[!DNL Journey Optimizer]**.

## 랜딩 페이지 사전 설정에 액세스 {#access-lp-presets}

랜딩 페이지 사전 설정에 액세스하려면 아래 단계를 따르십시오.

1. 액세스 권한 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 랜딩 페이지 사전 설정]**.

   ![](assets/lp_presets-access.png)

1. 사전 설정 레이블을 클릭하여 랜딩 페이지 사전 설정 세부 정보에 액세스합니다.

   ![](assets/lp_preset-details.png)

## 랜딩 페이지 사전 설정 만들기 {#lp-create-preset}

랜딩 페이지 사전 설정을 만들려면 아래 단계를 수행하십시오.

>[!NOTE]
>
>사전 설정을 만들려면 이전에 하나 이상의 랜딩 페이지 하위 도메인을 구성했는지 확인하십시오. [방법 알아보기](lp-subdomains.md)

1. 액세스 권한 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴를 선택한 다음 **[!UICONTROL 브랜딩]** > **[!UICONTROL 랜딩 페이지 사전 설정]**.

1. 선택 **[!UICONTROL 랜딩 페이지 사전 설정 만들기]**.

   ![](assets/lp_create-preset-temp.png)

1. 사전 설정의 이름과 설명을 입력합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 드롭다운 목록에서 랜딩 페이지 하위 도메인을 선택합니다.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >하위 도메인을 선택하려면 이전에 하나 이상의 랜딩 페이지 하위 도메인을 구성했는지 확인합니다. [방법 알아보기](#lp-subdomains)

   선택한 하위 도메인에 해당하는 설정이 표시됩니다.

1. 랜딩 페이지 하위 도메인을 추적 URL로 선택하려면 을(를) 선택합니다 **[!UICONTROL 랜딩 페이지 하위 도메인과 동일]** 선택 사항입니다. [추적에 대해 자세히 알아보기](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   예를 들어 랜딩 페이지 URL이 &#39;pages.mail.luma.com&#39;이고 추적 URL이 &#39;data.mail.luma.com&#39;인 경우 추적 하위 도메인으로 사용할 &#39;pages.mail.luma.com&#39;을 선택할 수 있습니다.

1. 클릭 **[!UICONTROL 제출]** 랜딩 페이지 사전 설정 생성을 확인하려면. 사전 설정을 초안으로 저장하고 나중에 해당 구성을 다시 시작할 수도 있습니다.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. 랜딩 페이지 사전 설정이 만들어지면 와 함께 목록에 표시됩니다 **[!UICONTROL 활성]** 상태. 랜딩 페이지에 사용할 준비가 되었습니다.

   ![](assets/lp-preset-active-temp.png)

이제 준비가 되었습니다. [랜딩 페이지 만들기](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**관련 항목**:

* [랜딩 페이지 시작](../landing-pages/get-started-lp.md)
* [랜딩 페이지 만들기](../landing-pages/create-lp.md#create-a-lp)
