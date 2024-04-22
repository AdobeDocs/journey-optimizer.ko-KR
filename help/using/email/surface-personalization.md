---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 표면 설정 개인화
description: 이메일 채널 표면 수준에서 설정에 대한 개인화된 값을 정의하는 방법을 알아봅니다
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 설정, 이메일, 구성, 하위 도메인
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 513fddf21eaf7958df45d97f028103519c77ec44
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 13%

---

# 이메일 표면 설정 개인화 {#surface-personalization}

이메일 설정을 보다 유연하게 제어하고, [!DNL Journey Optimizer] 하위 도메인 및 헤더에 대해 개인화된 값을 정의할 수 있습니다.<!--and URL tracking parameters--> 이메일 표면을 만들 때.

>[!AVAILABILITY]
>
>이 기능은 현재 사용자를 선택하는 베타 버전으로만 사용할 수 있습니다. <!--To join the beta program, contact Adobe Customer Care.-->

## 동적 하위 도메인 추가 {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="개인화를 사용할 수 없음"
>abstract="이 표면은 개인화 속성 없이 생성되었습니다. 개인화가 필요한 경우 해결 단계는 설명서를 참조하십시오."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="동적 하위 도메인 활성화"
>abstract="이메일 표면을 생성할 때 표현식 편집기를 사용하여 정의한 조건을 기반으로 동적 하위 도메인을 설정할 수 있습니다. 최대 50개의 동적 하위 도메인을 추가할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="일부 하위 도메인은 사용하지 못할 수 있습니다."
>abstract="현재 피드백 루프 등록이 보류되어 특정 하위 도메인을 선택할 수 없습니다. 이 과정은 영업일 기준 최대 10일 정도 소요될 수 있습니다. 완료되면 사용 가능한 모든 하위 도메인 중에서 선택할 수 있습니다."

이메일 표면을 만들 때 특정 조건을 기반으로 동적 하위 도메인을 설정할 수 있습니다.

예를 들어 국가별 전용 이메일 주소에서 메시지를 보낼 수 있는 법적 제한이 있는 경우 동적 하위 도메인을 사용할 수 있습니다. 이렇게 하면 국가별로 여러 표면을 만드는 대신, 여러 전송 하위 도메인이 다른 국가에 해당하는 단일 표면을 만들 수 있습니다. 그런 다음 하나의 캠페인으로 통합된 다양한 국가의 고객을 타겟팅할 수 있습니다.

이메일 채널 표면에 동적 하위 도메인을 정의하려면 아래 단계를 따르십시오.

1. 표면을 만들기 전에 사용 사례에 따라 이메일 전송에 사용할 하위 도메인을 설정합니다. [방법 알아보기](../configuration/about-subdomain-delegation.md)

   예를 들어 국가마다 다른 하위 도메인을 사용한다고 가정해 보겠습니다. 예를 들어 미국에 고유한 하위 도메인 하나, 영국에 고유한 하위 도메인 하나를 설정합니다.

1. 채널 표면을 만듭니다. [방법 알아보기](../configuration/channel-surfaces.md)

1. 다음 항목 선택 **[!UICONTROL 이메일]** 채널.

1. 다음에서 **하위 도메인** 섹션, 활성화 **[!UICONTROL 동적 하위 도메인]** 옵션을 선택합니다.

   ![](assets/surface-email-dynamic-subdomain.png)

1. 첫 번째 옆에 있는 편집 아이콘을 선택합니다 **[!UICONTROL 조건]** 필드.

1. 다음 [표현식 편집기](../personalization/personalization-build-expressions.md) 열림. 이 예에서는 다음과 같은 조건을 설정합니다. `Country` 다음과 같음 `US`.

   ![](assets/surface-email-edit-condition.png)

1. 이 조건과 연결할 하위 도메인을 선택하십시오. [하위 도메인에 대해 자세히 알아보기](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >일부 하위 도메인은 보류 중으로 인해 현재 선택할 수 없습니다. [되먹임 루프](../reports/deliverability.md#feedback-loops) 등록. 이 과정은 영업일 기준 최대 10일 정도 소요될 수 있습니다. 완료되면 사용 가능한 모든 하위 도메인 중에서 선택할 수 있습니다. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   미국에 기반을 둔 모든 수신자는 해당 국가에 대해 선택한 하위 도메인을 사용하여 메시지를 수신하게 됩니다. 즉, 관련된 모든 URL(예: 미러 페이지, 추적 URL 또는 구독 취소 링크)이 해당 하위 도메인을 기반으로 채워집니다.

1. 다른 동적 하위 도메인을 원하는 대로 설정합니다. 최대 50개의 항목을 추가할 수 있습니다.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. 다른 모든 항목 정의 [이메일 설정](email-settings.md) 및 [제출](../configuration/channel-surfaces.md#create-channel-surface) 당신 표면

서피스에 동적 하위 도메인을 하나 이상 추가하면 다음 항목이 이 서피스에 대해 해결된 동적 하위 도메인을 기반으로 채워집니다.

* 모든 URL(리소스 URL, 미러 페이지 URL 및 추적 URL)

* 다음 [구독 취소 URL](email-settings.md#list-unsubscribe)

* 다음 **보낸 사람 이메일** 및 **오류 이메일** 접미사

>[!NOTE]
>
>동적 하위 도메인을 설정한 다음 **[!UICONTROL 동적 하위 도메인]** 옵션을 선택하면 모든 동적 값이 제거됩니다. 하위 도메인을 선택하고 변경 사항을 적용할 서피스를 제출합니다.

## 헤더 개인화 {#personalize-header}

표면에 정의된 모든 헤더 매개 변수에 개인화를 사용할 수도 있습니다.

예를 들어 여러 브랜드가 있는 경우 단일 표면을 만들고 이메일 헤더에 개인화된 값을 사용할 수 있습니다. 이를 통해 서로 다른 브랜드에서 보낸 모든 이메일이 올바른 주소로 각 고객에게 발송되도록 할 수 있습니다 **출처:** 이름 및 이메일. 마찬가지로 수신자가 **답변** 이메일 클라이언트 소프트웨어에서 단추를 클릭하면 **회신 대상** 이름과 이메일은 올바른 사용자에게 올바른 브랜드에 해당합니다.

서피스 헤더 매개변수에 개인화된 변수를 사용하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>다음을 모두 개인화할 수 있습니다. **[!UICONTROL 헤더 매개 변수]** 필드, 제외 **[!UICONTROL 오류 이메일 접두사]** 필드.


1. 일반적인 방법으로 헤더 매개 변수를 정의합니다. [방법 알아보기](email-settings.md#email-header)

1. 각 필드에 대해 편집 아이콘을 선택합니다.

   ![](assets/surface-email-personalize-header.png)

1. 다음 [표현식 편집기](../personalization/personalization-build-expressions.md) 열림. 조건을 원하는 대로 정의하고 변경 사항을 저장합니다.

   예를 들어, 각 수신자가 자신의 브랜드 담당자로부터 이메일을 받는 것과 같은 조건을 설정합니다.

   >[!NOTE]
   >
   >선택할 수만 있습니다. **[!UICONTROL 프로필 속성]** 및 **[!UICONTROL 도우미 함수]**.

1. 개인화를 추가할 각 매개 변수에 대해 위의 단계를 반복합니다.

>[!NOTE]
>
>화면에 동적 하위 도메인을 한 개 이상 추가한 경우 **보낸 사람 이메일** 및 **오류 이메일** 해결된 내용에 따라 접미사가 채워집니다. [동적 하위 도메인](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## 표면 세부 사항 보기 {#view-surface-details}

캠페인이나 서피스에서 개인화된 설정이 있는 서피스를 사용할 경우 캠페인이나 서피스 내에서 직접 서피스 세부 정보를 표시할 수 있습니다. 아래 단계를 수행합니다.

1. 이메일 만들기 [campaign](../campaigns/create-campaign.md) 또는 [여정](../building-journeys/journey-gs.md).

1. 다음 항목 선택 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다.

1. 다음을 클릭합니다. **[!UICONTROL 표면 세부 사항 보기]** 단추를 클릭합니다.

   ![](assets/campaign-view-surface-details.png)

1. 다음 **[!UICONTROL 게재 설정]** 창이 표시됩니다. 동적 하위 도메인 및 개인화된 헤더 매개 변수를 포함하여 모든 표면 설정을 볼 수 있습니다.

   >[!NOTE]
   >
   >이 화면의 모든 정보는 읽기 전용입니다.

1. 선택 **[!UICONTROL 확장]** 동적 하위 도메인의 세부 사항을 표시합니다.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
