---
title: 하위 도메인 위임
description: Learn how to delegate your subdomains.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 9%

---

# 하위 도메인 위임 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Subdomain delegation"
>abstract="Journey Optimizer allows you to delegate your subdomains to Adobe. You can fully delegate a subdomain to Adobe, which is the recommended method. You can also create a subdomain using CNAMEs to point to Adobe-specific records, but this approach requires you to maintain and manage DNS records on your own."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="Subdomain configuration methods"

Domain name delegation is a method that allows the owner of a domain name (technically: a DNS zone) to delegate a subdivision of it (technically: a DNS zone under it, which can be called a sub-zone) to another entity. Basically, as a customer, if you are handling the “example.com” zone, you can delegate the sub-zone “marketing.example.com” to Adobe. [](about-subdomain-delegation.md)

>[!NOTE]
>
>[!DNL Journey Optimizer] Reach out to your Adobe contact if you want to increase this limitation.

You can fully delegate a subdomain, or create a subdomain using CNAMEs to point to Adobe-specific records.

>[!CAUTION]
>
>The full subdomain delegation is the recommended method. [](about-subdomain-delegation.md#subdomain-delegation-methods)

## 전체 하위 도메인 위임 {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Generate the matching DNS records"
>abstract="To fully delegate a new subdomain to Adobe, you need to copy the Adobe nameserver information displayed in the Journey Optimizer interface and paste it into your domain-hosting solution to generate the matching DNS records. Once the checks are successful, the subdomain is ready to be used to deliver messages."

[!DNL Journey Optimizer] By doing so, Adobe will be able to deliver messages as a managed service by controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking of email campaigns.

You can rely on Adobe to maintain the DNS infrastructure required to meet industry-standard deliverability requirements for your email marketing sending domains, while continuing to maintain and control DNS for your internal email domains.

To fully delegate a new subdomain to Adobe, follow the steps below:

1. **[!UICONTROL Administration]****[!UICONTROL Channels]****[!UICONTROL Subdomains]****[!UICONTROL Set up subdomain]**

   ![](assets/subdomain-delegate.png)

1. **[!UICONTROL Fully delegated]****[!UICONTROL Set up method]**

   ![](assets/subdomain-method-full.png)

1. Specify the name of the subdomain to delegate.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.
   >
   >Note that multi-level subdomains such as email.marketing.yourcompany.com are currently not supported.

1. DNS 서버에 배치할 레코드 목록이 표시됩니다. 이러한 레코드를 하나씩 복사하거나 CSV 파일을 다운로드하여 복사한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. Make sure that all the DNS records have been generated into your domain hosting solution. **[!UICONTROL Submit]**

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >**[!UICONTROL Save as draft]** You will then be able to resume the subdomain delegation by opening it from the subdomains list.

1. **[!UICONTROL Processing]** [](access-subdomains.md)

   ![](assets/subdomain-processing.png)

   Before being able to use that subdomain to send messages, you must wait until Adobe performs the required checks, which can take up to 3 hours. 자세한 내용은 [이 섹션](#subdomain-validation)을 참조하십시오.

   >[!NOTE]
   >
   >Any missing records, meaning the records not yet created on your hosting solution, will be listed out.

1. **[!UICONTROL Success]** It is ready to be used to deliver messages.

   >[!NOTE]
   >
   >**[!UICONTROL Failed]**

   <!-- later on, users will be notified in Pulse -->

[!DNL Journey Optimizer] [자세히 보기](ptr-records.md)

>[!CAUTION]
>
>[!DNL Journey Optimizer] **[!UICONTROL Processing]**

## CNAME 하위 도메인 위임 {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Generate the matching DNS and validation records"
>abstract="To delegate a subdomain using CNAMEs, you need to copy-paste the Adobe nameserver information and the SSL CDN URL validation record displayed in the Journey Optimizer interface into your hosting platform. Once the checks are successful, the subdomain is ready to be used to deliver messages."

If you have domain-specific restriction policies and you want Adobe to have only partial control over DNS, you can choose to carry out all DNS-related activities on your side.

CNAME 하위 도메인을 위임하면 하위 도메인을 만들고 CNAME을 사용하여 Adobe 특정 레코드를 가리키도록 설정할 수 있습니다. 이 구성을 사용하면 사용자와 Adobe가 이메일을 보내고 렌더링 및 추적하기 위한 환경을 설정하기 위한 DNS 유지 관리를 공동으로 수행합니다.

>[!CAUTION]
>
>The CNAME method is recommended if your organization&#39;s policies restrict the full subdomain delegation method. This approach requires you to maintain and manage DNS records on your own. Adobe will not be able to assist in changing, maintaining or managing DNS for a subdomain configured through the CNAME method.

[](#video)

To delegate a subdomain using CNAMEs, follow the steps below:

1. **[!UICONTROL Administration]****[!UICONTROL Channels]****[!UICONTROL Subdomains]****[!UICONTROL Set up subdomain]**

1. **[!UICONTROL CNAME set up]**

   ![](assets/subdomain-method-cname.png)

1. Specify the name of the subdomain to delegate.

   >[!CAUTION]
   >
   >Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.
   >
   >Note that multi-level subdomains such as email.marketing.yourcompany.com are currently not supported.

1. DNS 서버에 배치할 레코드 목록이 표시됩니다. 이러한 레코드를 하나씩 복사하거나 CSV 파일을 다운로드하여 복사한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. Make sure that all the DNS records have been generated into your domain hosting solution. If everything is configured properly, check the box &quot;I confirm...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >**[!UICONTROL Save as draft]** You will then be able to resume the subdomain delegation at this stage by opening it from the subdomains list.

1. Wait until Adobe verifies that these records are generated without errors on your hosting solution. This process can take up to 2 minutes.

   >[!NOTE]
   >
   >Any missing records, meaning the records not yet created on your hosting solution, will be listed out.

1. Adobe generates an SSL CDN URL validation record. Copy this validation record into your hosting platform. **[!UICONTROL Submit]**

   ![](assets/subdomain-cdn-url-validation.png)

   >[!NOTE]
   >
   >**[!UICONTROL Save as draft]** You will then be able to resume the subdomain delegation by opening it from the subdomains list.

1. **[!UICONTROL Processing]** [](access-subdomains.md)

   Before being able to use that subdomain to send messages, you must wait until Adobe performs the required checks, which usually takes 2 to 3 hours. 자세한 내용은 [이 섹션](#subdomain-validation)을 참조하십시오.

1. <!--i.e Adobe validates the record you created and installs it-->**[!UICONTROL Success]** It is ready to be used to deliver messages.

   >[!NOTE]
   >
   >**[!UICONTROL Failed]**

Upon validating the record and installing the certificate, Adobe automatically creates the PTR record for the CNAME subdomain. [자세히 보기](ptr-records.md)

>[!CAUTION]
>
>[!DNL Journey Optimizer] **[!UICONTROL Processing]**

## Subdomain validation {#subdomain-validation}

The checks and actions below will be performed until the subdomain is verified and can be used to send messages.

>[!NOTE]
>
>These steps are performed by Adobe and can take up to 3 hours.

1. **** If the pre-validation step fails, an error is returned along with the corresponding reason, otherwise Adobe proceeds to the next step.

1. ****

   * ****
   * ****
   * ****
   * ****
   * ****

1. **** It is secured by installing the SSL certificate.

1. ****

1. ****

1. ****

1. ****

1. **** Gmail also recommends having PTR records for each IP. Adobe creates PTR records only when you delegate a subdomain for the first time, one for each IP, all IPs pointing that subdomain. ****** You can update the PTR record afterwards to point to the new delegated domain. [](ptr-records.md)

## How-to video{#video}

CNAME을 사용하여 Adobe 관련 레코드를 가리키도록 하위 도메인을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
