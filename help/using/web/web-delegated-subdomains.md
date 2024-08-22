---
solution: Journey Optimizer
product: journey optimizer
title: 웹 하위 도메인 구성
description: Journey Optimizer을 사용하여 웹 하위 도메인을 설정하는 방법 알아보기
role: Admin
feature: Web Channel, Subdomains
level: Experienced
keywords: 웹, 하위 도메인, 구성
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 24%

---

# 웹 하위 도메인 구성 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="웹 하위 도메인 위임"
>abstract="웹 채널을 사용하려면 하위 도메인을 설정합니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="웹 하위 도메인 위임"
>abstract="Adobe Experience Manager Assets의 콘텐츠를 웹 경험에 추가하는 경우 이 콘텐츠를 게시하는 데 사용할 하위 도메인을 설정해야 합니다. Adobe에 이미 위임된 하위 도메인을 중에서 선택하거나 새 하위 도메인을 구성할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="웹 하위 도메인 설정"
>abstract="Adobe에 위임된 하위 도메인 목록에서 하위 도메인을 선택합니다. 이 웹 하위 도메인을 기본 하위 도메인으로 설정할 수 있지만 기본 하위 도메인은 한 번에 하나만 사용할 수 있습니다."

웹 경험을 작성할 때 [Adobe Experience Manager Assets](../content-management/assets.md) 라이브러리에서 얻은 콘텐츠를 추가하는 경우 이 콘텐츠를 게시하는 데 사용할 하위 도메인을 설정해야 합니다.

이미 Adobe에 위임된 하위 도메인을 사용하거나 다른 하위 도메인을 구성할 수 있습니다. [이 섹션](../configuration/delegate-subdomain.md)에서 하위 도메인을 Adobe으로 위임하는 방법에 대해 자세히 알아보세요.

>[!CAUTION]
>
>웹 하위 도메인 구성은 모든 환경에 공통됩니다. 그 결과는 다음과 같습니다.
>
>* 웹 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대한 **[!UICONTROL 웹 하위 도메인 관리]** 권한이 있어야 합니다.
>
> * 웹 하위 도메인을 수정하면 프로덕션 샌드박스에도 영향을 줍니다.

여러 웹 하위 도메인을 만들 수 있지만 **기본** 하위 도메인만 사용됩니다. 기본 웹 하위 도메인을 변경할 수 있지만 한 번에 하나만 사용할 수 있습니다.

## 웹 하위 도메인 액세스 및 관리 {#access-web-subdomains}

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴로 이동한 다음 **[!UICONTROL 웹 설정]** > **[!UICONTROL 웹 하위 도메인]**&#x200B;을 선택합니다. 현재 샌드박스로 설정된 모든 하위 도메인이 표시됩니다.

   ![](assets/web-access-subdomains.png)

1. 각 하위 도메인을 위임한 사용자 또는 위임 상태(**[!UICONTROL 초안]**, **[!UICONTROL 처리]**, **[!UICONTROL 성공]** 또는 **[!UICONTROL 실패]**)를 필터링할 수 있습니다.

   ![](assets/web-filter-subdomains.png)

1. 현재 기본값으로 사용되는 하위 도메인 옆에 **[!UICONTROL 기본]** 배지가 표시됩니다. 기본 하위 도메인을 변경하려면 원하는 하위 도메인 옆에 있는 **[!UICONTROL 추가 작업]** 단추에서 **[!UICONTROL 기본값으로 설정]**&#x200B;을 선택합니다.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >기본 웹 하위 도메인을 변경할 수 있지만 한 번에 하나만 사용할 수 있습니다.

## 기존 하위 도메인 사용 {#web-use-existing-subdomain}

이미 Adobe에게 위임된 하위 도메인을 사용하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴에 액세스한 다음 **[!UICONTROL 웹 설정]** > **[!UICONTROL 웹 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 위임된 하위 도메인 사용]** 옵션을 선택하고 목록에서 위임된 하위 도메인을 선택합니다.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >이미 웹 하위 도메인으로 사용되고 있는 하위 도메인은 선택할 수 없습니다.

1. 웹 URL에 표시될 접두사가 자동으로 추가됩니다. 변경할 수 없습니다.

1. 이 하위 도메인을 기본값으로 설정하려면 해당 옵션을 선택합니다.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >**기본** 하위 도메인만 사용됩니다.

1. **[!UICONTROL 제출]**&#x200B;을 클릭합니다. 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. 웹 경험에 사용할 준비가 되었습니다.

   >[!NOTE]
   >
   >매우 드문 경우이지만 하위 도메인 설정이 실패할 수 있습니다. 이 경우 **[!UICONTROL 추가 작업]** 아이콘에서 **[!UICONTROL 삭제]** 단추를 사용하여 **[!UICONTROL 실패]** 하위 도메인을 삭제하여 목록을 정리할 수 있습니다.

## 새 하위 도메인 구성 {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="일치하는 DNS 레코드 생성"
>abstract="새 웹 하위 도메인을 구성하려면 Journey Optimizer 인터페이스에 표시된 Adobe 이름 서버 정보를 복사한 다음 도메인 호스팅 솔루션에 붙여넣어 일치하는 DNS 레코드를 생성해야 합니다. 확인이 성공적으로 완료되면 하위 도메인을 사용하여 Adobe Experience Manager Assets 라이브러리의 콘텐츠를 게시할 수 있습니다."

새 하위 도메인을 구성하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>기본적으로 [!DNL Journey Optimizer]에서는 전자 메일과 웹 채널을 모두 포함하는 총 10개의 하위 도메인을 위임할 수 있습니다. 그러나 라이선스 계약에 따라 최대 100개의 하위 도메인을 위임할 수 있습니다. 부여된 하위 도메인 수에 대해 자세히 알아보려면 Adobe 담당자에게 문의하십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 메뉴에 액세스한 다음 **[!UICONTROL 웹 설정]** > **[!UICONTROL 웹 하위 도메인]**&#x200B;을 선택합니다.

1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 구성 유형]** 섹션에서 **[!UICONTROL 고유한 도메인 추가]**&#x200B;를 선택합니다.

1. 위임할 하위 도메인을 지정합니다.

   >[!CAUTION]
   >
   >기존 웹 하위 도메인은 사용할 수 없습니다.
   >
   >하위 도메인에서는 대문자가 허용되지 않습니다.

   ![](assets/web-add-your-own-domain.png)

   잘못된 하위 도메인을 Adobe으로 위임할 수 없습니다. marketing.yourcompany.com과 같이 조직에서 소유한 올바른 하위 도메인을 입력해야 합니다.

   >[!NOTE]
   >
   >(동일한 상위 도메인의) 다중 수준 하위 도메인이 지원됩니다. 예를 들어 &#39;web.marketing.yourcompany.com&#39;을 사용할 수 있습니다.

1. 이 하위 도메인을 기본값으로 설정하려면 해당 옵션을 선택합니다.

   >[!NOTE]
   >
   >**기본** 하위 도메인만 사용됩니다.

1. DNS 서버에 배치할 레코드가 표시됩니다. 이 레코드를 복사하거나 CSV 파일을 다운로드한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 DNS 레코드를 생성합니다.

1. 도메인 호스팅 솔루션에 DNS 레코드가 생성되었는지 확인합니다. 모든 항목이 올바르게 구성된 경우 &quot;확인...&quot; 상자를 선택한 다음 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

   ![](assets/web-add-your-own-domain-confirm.png)

   >[!NOTE]
   >
   >새 웹 하위 도메인을 구성할 때 항상 CNAME 레코드를 가리킵니다.

1. 하위 도메인 위임이 제출되면 하위 도메인이 목록에 **[!UICONTROL 처리]** 상태로 표시됩니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->을 참조하세요.

   >[!NOTE]
   >
   >해당 하위 도메인을 사용하여 웹 메시지를 보내려면 먼저 Adobe이 필요한 검사를 수행할 때까지 기다려야 하며 최대 4시간이 걸릴 수 있습니다.

1. 확인이 성공하면 하위 도메인이 **[!UICONTROL 성공]** 상태를 가져옵니다. 웹 채널 구성을 만드는 데 사용할 준비가 되었습니다.

   호스팅 솔루션에서 유효성 검사 레코드를 만들지 못하면 하위 도메인이 **[!UICONTROL 실패]**(으)로 표시됩니다.

<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->
