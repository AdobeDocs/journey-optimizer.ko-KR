---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지 사전 설정 정의
description: Journey Optimizer을 사용하여 랜딩 페이지를 만들고 사용하도록 환경을 구성하는 방법에 대해 알아봅니다
role: Admin
level: Intermediate
keywords: 랜딩, 랜딩 페이지, 구성, 환경, 하위 도메인, 사전 설정
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 18%

---

# 랜딩 페이지 사전 설정 정의 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="랜딩 페이지 사전 설정 만들기"
>abstract="랜딩 페이지를 빌드하고 Journey Optimizer를 통해 활용하려면 사용할 하위 도메인이 포함된 랜딩 페이지 사전 설정을 만들어야 합니다."

날짜 [랜딩 페이지 만들기](../landing-pages/create-lp.md#create-a-lp), 랜딩 페이지를 빌드하고 를 통해 활용하려면 랜딩 페이지 사전 설정을 선택해야 합니다. **[!DNL Journey Optimizer]**.

## 랜딩 페이지 사전 설정 액세스 {#access-lp-presets}

랜딩 페이지 사전 설정에 액세스하려면 아래 단계를 따르십시오.

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 랜딩 페이지 사전 설정]**.

   ![](assets/lp_presets-access.png)

1. 사전 설정 레이블을 클릭하여 랜딩 페이지 사전 설정 세부 정보에 액세스합니다.

   ![](assets/lp_preset-details.png)

## 랜딩 페이지 사전 설정 만들기 {#lp-create-preset}

랜딩 페이지 사전 설정을 만들려면 아래 단계를 수행합니다.

>[!NOTE]
>
>사전 설정을 만들려면 적어도 하나 이상의 랜딩 페이지 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](lp-subdomains.md)

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴, 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 랜딩 페이지 사전 설정]**.

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
   >하위 도메인을 선택하려면 적어도 한 개의 랜딩 페이지 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](#lp-subdomains)

   선택한 하위 도메인에 해당하는 설정이 표시됩니다.

1. 추적 URL에 대한 랜딩 페이지 하위 도메인을 선택하려면 다음을 확인하십시오. **[!UICONTROL 랜딩 페이지 하위 도메인과 동일]** 옵션을 선택합니다. [추적에 대해 자세히 알아보십시오](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   예를 들어 랜딩 페이지 URL이 &#39;pages.mail.luma.com&#39;이고 추적 URL이 &#39;data.mail.luma.com&#39;인 경우 추적 하위 도메인으로 사용할 &#39;pages.mail.luma.com&#39;을 선택할 수 있습니다.

1. 클릭 **[!UICONTROL 제출]** 랜딩 페이지 사전 설정 만들기를 확인합니다. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. 랜딩 페이지 사전 설정이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 활성]** 상태. 랜딩 페이지에 사용할 준비가 되었습니다.

   ![](assets/lp-preset-active-temp.png)

이제 다음을 수행할 준비가 되었습니다. [랜딩 페이지 만들기](../landing-pages/create-lp.md) 위치: [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**관련 항목**:

* [랜딩 페이지 시작](../landing-pages/get-started-lp.md)
* [랜딩 페이지 만들기](../landing-pages/create-lp.md#create-a-lp)
