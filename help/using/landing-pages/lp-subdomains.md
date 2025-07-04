---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지 하위 도메인 구성
description: Journey Optimizer을 사용하여 랜딩 페이지 하위 도메인을 구성하는 방법 알아보기
feature: Landing Pages, Subdomains
role: Admin
level: Experienced
keywords: 랜딩, 랜딩 페이지, 하위 도메인, 구성
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 19%

---

# 랜딩 페이지 하위 도메인 구성 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="랜딩 페이지 하위 도메인 위임"
>abstract="랜딩 페이지를 사용하려면 하위 도메인을 설정합니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="랜딩 페이지 하위 도메인 위임"
>abstract="랜딩 페이지 사전 설정을 만드는 데 이 하위 도메인이 필요하므로 랜딩 페이지에 사용할 하위 도메인을 구성해야 합니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 새 하위 도메인을 구성할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets.html?lang=ko#lp-create-preset" text="랜딩 페이지 사전 설정 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="랜딩 페이지 사전 설정 만들기"
>abstract="랜딩 페이지 사전 설정을 만들려면 하위 도메인 이름 목록에서 선택할 랜딩 페이지 하위 도메인을 이전에 하나 이상 구성했는지 확인합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets.html?lang=ko#lp-create-preset" text="랜딩 페이지 사전 설정 만들기"

## 랜딩 페이지 하위 도메인 시작 {#gs-lp-subdomains}

[랜딩 페이지 사전 설정을 만들기](lp-presets.md)하려면 랜딩 페이지에 사용할 하위 도메인을 설정해야 합니다.

이미 Adobe에 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다. [이 섹션](../configuration/delegate-subdomain.md)에서 하위 도메인을 Adobe으로 위임하는 방법에 대해 자세히 알아보세요.

랜딩 페이지 하위 도메인 구성은 **모든 환경에 공통됩니다**. 그 결과는 다음과 같습니다.

* 랜딩 페이지 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대한 **[!UICONTROL 랜딩 페이지 하위 도메인 관리]** 권한이 있어야 합니다.

* 랜딩 페이지 하위 도메인을 수정하면 프로덕션 샌드박스에도 영향을 줍니다.

## 기존 하위 도메인 사용 {#lp-use-existing-subdomain}

이미 Adobe에 위임된 하위 도메인을 사용하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴에 액세스한 다음 **[!UICONTROL 랜딩 페이지 설정]** > **[!UICONTROL 랜딩 페이지 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

   ![](assets/lp_set-up-subdomain.png)

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 위임된 도메인 사용]**&#x200B;을(를) 선택합니다.

   ![](assets/lp_use-delegated-subdomain.png)

1. 랜딩 페이지 URL에 표시할 접두사를 입력합니다.

   영숫자와 하이픈만 사용할 수 있습니다.

   >[!CAUTION]
   >
   >`cdn` 또는 `data` 접두사는 내부용으로 예약되었으므로 사용하지 마십시오. `dmarc` 또는 `spf`과(와) 같은 기타 제한되거나 예약된 접두사도 사용하지 않아야 합니다.

1. 목록에서 위임된 하위 도메인을 선택합니다.

   이미 랜딩 페이지 하위 도메인으로 사용된 하위 도메인은 선택할 수 없습니다.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   동일한 상위 도메인의 위임된 하위 도메인은 여러 개 사용할 수 없습니다. 예를 들어 &#39;marketing1.yourcompany.com&#39;이 이미 랜딩 페이지의 Adobe에 위임된 경우 &#39;marketing2.yourcompany.com&#39;을 사용할 수 없습니다. 그러나 랜딩 페이지에 대해 지원되는 다중 수준 하위 도메인은 &#39;marketing1.yourcompany.com&#39;의 하위 도메인(&#39;email.marketing1.yourcompany.com&#39; 등) 또는 다른 상위 도메인을 사용하여 진행할 수 있습니다.

   >[!CAUTION]
   >
   >[CNAME 메서드](../configuration/delegate-subdomain.md#cname-subdomain-delegation)를 사용하여 Adobe에 위임된 도메인을 선택하는 경우 호스팅 플랫폼에서 DNS 레코드를 만들어야 합니다. DNS 레코드를 생성하기 위한 프로세스는 새 랜딩 페이지 하위 도메인을 구성할 때와 동일합니다. [이 섹션](#lp-configure-new-subdomain)에서 방법을 알아보세요.

1. **[!UICONTROL 제출을 클릭합니다]**.

1. 제출되면 하위 도메인이 목록에 **[!UICONTROL 처리 중]** 상태로 표시됩니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->을 참조하세요.

   ![](assets/lp_subdomain-processing.png)

   해당 하위 도메인을 사용하여 메시지를 보내려면 먼저 Adobe에서 필요한 검사를 수행할 때까지 기다려야 합니다(최대 **시간**.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->).

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. 랜딩 페이지 사전 설정을 만드는 데 사용할 준비가 되었습니다.

## 새 하위 도메인 구성 {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="일치하는 DNS 레코드 생성"
>abstract="새 랜딩 페이지 하위 도메인을 구성하려면 Journey Optimizer 인터페이스에 표시된 Adobe 이름 서버 정보를 복사한 다음 도메인 호스팅 솔루션에 붙여넣어 일치하는 DNS 레코드를 생성해야 합니다. 확인이 완료되면 랜딩 페이지 사전 설정 만들기에 하위 도메인을 사용할 준비가 되었습니다."

새 하위 도메인을 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴에 액세스한 다음 **[!UICONTROL 랜딩 페이지 설정]** > **[!UICONTROL 랜딩 페이지 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 고유한 도메인 추가]**&#x200B;를 선택합니다.

   ![](assets/lp_add-your-own-subdomain.png)

1. 위임할 하위 도메인을 지정합니다.

   >[!CAUTION]
   >
   >* 기존 랜딩 페이지 하위 도메인은 사용할 수 없습니다.
   >
   >* 하위 도메인에서는 대문자가 허용되지 않습니다.

   잘못된 하위 도메인을 Adobe에 위임할 수 없습니다. marketing.yourcompany.com과 같이 조직에서 소유한 올바른 하위 도메인을 입력해야 합니다.

   랜딩 페이지의 경우 다중 수준 하위 도메인이 지원됩니다. 예를 들어 &#39;email.marketing.yourcompany.com&#39;을 사용할 수 있습니다.

1. DNS 서버에 배치할 레코드가 표시됩니다. 이 레코드를 복사하거나 CSV 파일을 다운로드한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. 도메인 호스팅 솔루션에 DNS 레코드가 생성되었는지 확인합니다. 모든 항목이 올바르게 구성된 경우 &quot;확인...&quot; 상자를 선택한 다음 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   새 랜딩 페이지 하위 도메인을 구성할 때 항상 CNAME 레코드를 가리킵니다.

1. 하위 도메인 위임이 제출되면 하위 도메인이 목록에 **[!UICONTROL 처리]** 상태로 표시됩니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->을 참조하세요.

   랜딩 페이지에 해당 하위 도메인을 사용하려면 Adobe에서 필요한 검사를 수행할 때까지 기다려야 합니다. 필요한 검사는 **최대 4시간**.<!--Learn more in [this section](#subdomain-validation).--> 정도 소요될 수 있습니다.

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. 랜딩 페이지 사전 설정을 만드는 데 사용할 준비가 되었습니다.

   호스팅 솔루션에서 유효성 검사 레코드를 만들지 못하면 하위 도메인이 **[!UICONTROL 실패]**(으)로 표시됩니다.

## 하위 도메인 위임 취소 {#undelegate-subdomain}

랜딩 페이지 하위 도메인의 위임을 취소하려면 아래 단계를 따르십시오.

1. [!DNL Journey Optimizer]에서 하위 도메인과 연결된 모든 랜딩 페이지의 게시를 취소합니다. [방법 알아보기](create-lp.md#access-landing-pages)

1. 랜딩 페이지 하위 도메인이 CNAME 레코드를 가리키면 호스팅 솔루션에서 랜딩 페이지 하위 도메인용으로 만든 CNAME DNS 레코드를 삭제할 수 있습니다(원본 이메일 하위 도메인이 있는 경우 삭제하지 마십시오).

   >[!NOTE]
   >
   >랜딩 페이지 하위 도메인은 CNAME 레코드를 지정할 수 있습니다. 이는 [CNAME 메서드](../configuration/delegate-subdomain.md#cname-subdomain-delegation)을(를) 사용하여 Adobe에 위임된 [기존 하위 도메인](#lp-use-existing-subdomain) 또는 구성한 [새 랜딩 페이지 하위 도메인](#lp-configure-new-subdomain)이기 때문입니다.

1. 위임을 해제할 하위 도메인을 사용하여 Adobe 담당자에게 문의하십시오.

요청이 Adobe에 의해 처리되면 위임되지 않은 도메인이 더 이상 하위 도메인 인벤토리 페이지에 표시되지 않습니다.
