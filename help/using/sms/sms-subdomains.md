---
solution: Journey Optimizer
product: journey optimizer
title: 문자 메시지(SMS/MMS)에 대한 하위 도메인 구성
description: Journey Optimizer을 사용하여 SMS 하위 도메인을 구성하는 방법 알아보기
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: SMS, 하위 도메인, 구성
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: bcccc7b385f031fba2c2b57ec62cae127eda8466
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 24%

---

# SMS 하위 도메인 구성 {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="SMS/MMS 하위 도메인 위임"
>abstract="문자 메시지(SMS/MMS)용 하위 도메인을 설정합니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 새 하위 도메인을 구성할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="SMS/MMS 하위 도메인 위임"
>abstract="문자 메시지에 사용할 하위 도메인을 구성해야 하는데, 이는 SMS 구성을 만들기 위해 이 하위 도메인이 필요하기 때문입니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 새 하위 도메인을 구성할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="SMS 표면 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="SMS/MMS 하위 도메인 선택"
>abstract="SMS 구성을 만들려면 하위 도메인 이름 목록에서 선택할 SMS 하위 도메인을 이전에 하나 이상 구성했는지 확인합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="SMS 표면 만들기"

SMS/MMS 메시지에 추가되는 URL을 단축하려면 [SMS 구성을 만들 때](sms-configuration.md#message-preset-sms)선택할 하위 도메인을 설정해야 합니다.

이미 Adobe에 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다. [이 섹션](../configuration/delegate-subdomain.md)에서 하위 도메인을 Adobe으로 위임하는 방법에 대해 자세히 알아보세요.

>[!CAUTION]
>
>* SMS 하위 도메인 구성은 모든 환경에서 공유됩니다. 따라서 SMS 하위 도메인을 수정하면 다른 프로덕션 샌드박스에도 영향을 줍니다.
>
>* SMS 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대해 **[!UICONTROL SMS 하위 도메인 관리]** 권한이 있어야 합니다. [이 섹션](../administration/high-low-permissions.md)에서 권한에 대해 자세히 알아보십시오.
>

## 기존 하위 도메인 사용 {#sms-use-existing-subdomain}

이미 Adobe에게 위임된 하위 도메인을 사용하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴로 이동한 다음 **[!UICONTROL SMS 설정]** > **[!UICONTROL SMS 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

   ![](assets/sms_set-up-subdomain.png)

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 위임된 하위 도메인 사용]**&#x200B;을(를) 선택합니다.

   ![](assets/sms_use-delegated-subdomain.png)

1. SMS URL에 표시할 접두사를 입력합니다.

   >[!NOTE]
   >
   >영숫자와 하이픈만 사용할 수 있습니다.

1. 목록에서 위임된 하위 도메인을 선택합니다.

   >[!NOTE]
   >
   >이미 SMS 하위 도메인으로 사용되고 있는 하위 도메인은 선택할 수 없습니다.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >[CNAME 메서드](../configuration/delegate-subdomain.md#cname-subdomain-delegation)를 사용하여 Adobe으로 위임된 도메인을 선택하는 경우 호스팅 플랫폼에서 DNS 레코드를 만들어야 합니다. DNS 레코드를 생성하려면 새 SMS 하위 도메인을 구성할 때와 프로세스가 동일합니다. [이 섹션](#sms-configure-new-subdomain)에서 방법을 알아보세요.

1. **[!UICONTROL 제출을 클릭합니다]**.

1. 제출되면 하위 도메인이 목록에 **[!UICONTROL 처리 중]** 상태로 표시됩니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->을 참조하세요.

   >[!NOTE]
   >
   >해당 하위 도메인을 사용하여 메시지를 보내려면 Adobe에서 필요한 검사를 수행할 때까지 기다려야 하며 최대 4시간이 걸릴 수 있습니다.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. SMS 채널 구성을 만드는 데 사용할 준비가 되었습니다.

## 새 하위 도메인 구성 {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="일치하는 DNS 레코드 생성"
>abstract="새 SMS 하위 도메인을 구성하려면 Journey Optimizer 인터페이스에 표시된 Adobe 이름 서버 정보를 복사한 다음 도메인 호스팅 솔루션에 붙여넣어 일치하는 DNS 레코드를 생성해야 합니다. 확인이 완료되면 SMS 구성 만들기에 하위 도메인을 사용할 준비가 된 것입니다."

새 하위 도메인을 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴로 이동한 다음 **[!UICONTROL SMS 설정]** > **[!UICONTROL SMS 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

   ![](assets/sms_set-up-subdomain.png)

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 고유한 도메인 추가]**&#x200B;를 선택합니다.

   ![](assets/sms_add-your-own-subdomain.png)

1. 위임할 하위 도메인을 지정합니다.

   >[!CAUTION]
   >
   >* 기존 SMS 하위 도메인은 사용할 수 없습니다.
   >
   >* 하위 도메인에서는 대문자가 허용되지 않습니다.

   잘못된 하위 도메인을 Adobe으로 위임할 수 없습니다. marketing.yourcompany.com과 같이 조직에서 소유한 올바른 하위 도메인을 입력해야 합니다.

   >[!NOTE]
   >
   >(동일한 상위 도메인의) 다중 수준 하위 도메인이 지원됩니다. 예를 들어 &#39;sms.marketing.yourcompany.com&#39;을 사용할 수 있습니다.

1. DNS 서버에 배치할 레코드가 표시됩니다. 이 레코드를 복사하거나 CSV 파일을 다운로드한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. 도메인 호스팅 솔루션에 DNS 레코드가 생성되었는지 확인합니다. 모든 항목이 올바르게 구성된 경우 &quot;확인...&quot; 상자를 선택한 다음 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >새 SMS 하위 도메인을 구성할 때 항상 CNAME 레코드를 가리킵니다.

1. 하위 도메인 위임이 제출되면 하위 도메인이 목록에 **[!UICONTROL 처리]** 상태로 표시됩니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->을 참조하세요.

하위 도메인을 사용하여 SMS 메시지를 보내기 전에 Adobe에서 필요한 검사를 수행할 때까지 기다려야 하며 최대 4시간이 걸릴 수 있습니다.<!--Learn more in [this section](#subdomain-validation).--> 검사가 성공하면 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. SMS 채널 구성을 만드는 데 사용할 준비가 되었습니다.

호스팅 솔루션에서 유효성 검사 레코드를 만들지 못하면 하위 도메인이 **[!UICONTROL 실패]**(으)로 표시됩니다.
