---
title: 랜딩 페이지 하위 도메인 구성
description: Journey Optimizer을 사용하여 랜딩 페이지 하위 도메인을 구성하는 방법 알아보기
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 911df5b5b81c0e803c41e4e12817c4773d498b73
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 1%

---

# 랜딩 페이지 하위 도메인 구성 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="랜딩 페이지 사전 설정 만들기"
>abstract="랜딩 페이지 사전 설정을 만들려면 하위 도메인 이름 목록에서 선택할 하나 이상의 랜딩 페이지 하위 도메인을 이전에 구성했는지 확인하십시오."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="랜딩 페이지 사전 설정 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="랜딩 페이지 하위 도메인 위임"
>abstract="랜딩 페이지 사전 설정을 만들려면 이 하위 도메인이 필요하므로 랜딩 페이지에 사용할 하위 도메인을 구성해야 합니다. 이미 새 하위 도메인을 Adobe 또는 구성하는 데 위임된 하위 도메인을 사용할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="랜딩 페이지 사전 설정 만들기"

다음을 수행할 수 있습니다. [랜딩 페이지 사전 설정 만들기](lp-presets.md): 랜딩 페이지에 사용할 하위 도메인을 설정해야 합니다.

이미 Adobe에 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다. 하위 도메인을 에서 도메인으로 위임하는 방법에 대해 자세히 알아보십시오 [이 섹션](delegate-subdomain.md).

## 기존 하위 도메인 사용 {#lp-use-existing-subdomain}

이미 Adobe에 위임된 하위 도메인을 사용하려면 아래 단계를 따르십시오.

1. 액세스 권한 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** 메뉴를 선택한 다음 **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

   ![](assets/lp_access-subdomains.png)

1. **[!UICONTROL Set up subdomain]**&#x200B;을(를) 클릭합니다.

   ![](assets/lp_set-up-subdomain.png)

1. 선택 **[!UICONTROL Use delegated domain]** 에서 **[!UICONTROL Configuration type]** 섹션을 참조하십시오.

   ![](assets/lp_use-delegated-subdomain.png)

1. 랜딩 페이지 URL에 표시할 접두사를 입력합니다.

   >[!NOTE]
   >
   >영숫자 문자와 하이픈만 사용할 수 있습니다.

1. 목록에서 위임된 하위 도메인을 선택합니다.

   >[!NOTE]
   >
   >이미 랜딩 페이지 하위 도메인으로 사용되는 하위 도메인은 선택할 수 없습니다.

   ![](assets/lp_prefix-and-subdomain.png)

   동일한 상위 도메인의 여러 위임된 하위 도메인은 사용할 수 없습니다. 예를 들어 &#39;marketing1.yourcompany.com&#39;이 랜딩 페이지의 Adobe에 이미 위임된 경우에는 &#39;marketing2.yourcompany.com&#39;을 사용할 수 없습니다. 그러나 다중 수준 하위 도메인은 랜딩 페이지에 대해 지원되므로 &#39;email.marketing1.yourcompany.com&#39;을 사용할 수 있습니다.

   <!--For landing pages, multi-level subdomains are supported. For example, you can use 'email.marketing.yourcompany.com'.-->

   >[!CAUTION]
   >
   >을 사용하여 Adobe에 위임된 도메인을 선택하는 경우 [CNAME 메서드](delegate-subdomain.md#cname-subdomain-delegation)를 채울 때는 호스팅 플랫폼에 DNS 레코드를 만들어야 합니다. DNS 레코드를 생성하기 위해 프로세스는 새 랜딩 페이지 하위 도메인을 구성할 때와 동일합니다. 방법 알아보기 [이 섹션](#lp-configure-new-subdomain).

1. **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

1. 제출되면 하위 도메인이 와 함께 목록에 표시됩니다 **[!UICONTROL Processing]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >해당 하위 도메인을 사용하여 메시지를 보내려면 Adobe이 필요한 검사를 수행할 때까지 기다려야 하며, 이 작업은 최대 4시간이 걸릴 수 있습니다.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL Success]** 상태. 랜딩 페이지 사전 설정을 만드는 데 사용할 준비가 되었습니다.

## 새 하위 도메인 구성 {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="일치하는 DNS 레코드 생성"
>abstract="새 랜딩 페이지 하위 도메인을 구성하려면 Journey Optimizer 인터페이스에 표시된 Adobe 이름 서버 정보를 복사하여 도메인 호스팅 솔루션에 붙여넣어 일치하는 DNS 레코드를 생성해야 합니다. 이 확인이 성공하면 하위 도메인을 사용하여 랜딩 페이지 사전 설정을 만들 준비가 되었습니다."

새 하위 도메인을 구성하려면 아래 단계를 따르십시오.

1. 액세스 권한 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** 메뉴를 선택한 다음 **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

1. **[!UICONTROL Set up subdomain]**&#x200B;을(를) 클릭합니다.

1. 선택 **[!UICONTROL Add your own domain]** 에서 **[!UICONTROL Configuration type]** 섹션을 참조하십시오.

   ![](assets/lp_add-your-own-subdomain.png)

1. 위임할 하위 도메인을 지정합니다.

   >[!CAUTION]
   >
   >기존 랜딩 페이지 하위 도메인은 사용할 수 없습니다.

   잘못된 하위 도메인을 Adobe으로 위임하는 것은 허용되지 않습니다. marketing.yourcompany.com과 같이 조직이 소유한 유효한 하위 도메인을 입력해야 합니다.

   >[!NOTE]
   >
   >랜딩 페이지의 경우 다중 수준 하위 도메인이 지원됩니다. 예를 들어 &#39;email.marketing.yourcompany.com&#39;을 사용할 수 있습니다.

   <!--Journey Optimizer currently does not support multiple subdomains of the same parent domain for landing page configuration-->

1. DNS 서버에 배치할 레코드가 표시됩니다. 이 레코드를 복사하거나 CSV 파일을 다운로드한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. DNS 레코드가 도메인 호스팅 솔루션에 생성되었는지 확인합니다. 모든 것이 제대로 구성된 경우 &quot;확인...&quot; 상자를 선택한 다음 를 클릭합니다. **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >새 랜딩 페이지 하위 도메인을 구성할 때 항상 CNAME 레코드를 가리킵니다.

1. 하위 도메인 위임이 제출되면 하위 도메인이 와 함께 목록에 표시됩니다. **[!UICONTROL Processing]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >해당 하위 도메인을 사용하여 메시지를 보내려면 Adobe이 필요한 검사를 수행할 때까지 기다려야 하며, 이 작업은 최대 4시간이 걸릴 수 있습니다.<!--Learn more in [this section](#subdomain-validation).-->

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL Success]** 상태. 랜딩 페이지 사전 설정을 만드는 데 사용할 준비가 되었습니다.

   하위 도메인은 로 표시됩니다 **[!UICONTROL Failed]** 호스팅 솔루션에 대한 유효성 검사 레코드를 만들지 못한 경우.
