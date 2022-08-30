---
title: 보고 구성
description: 보고 데이터 소스를 설정하는 방법 알아보기
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# 보고 구성 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="보고용 데이터 세트 설정"
>abstract="보고 구성을 사용하면 보고서에서 사용할 추가 사용자 정의 정보를 검색할 수 있도록 시스템에 대한 연결을 정의할 수 있습니다. 기술 사용자가 수행해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="데이터 세트 선택"
>abstract="지원되는 필드 그룹 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다(experienceevent-web, experienceevent-application, experienceevent-commerce)."

데이터 소스 구성을 보고하면 보고서에서 사용할 추가 정보 검색을 위해 시스템에 대한 연결을 정의할 수 있습니다.

>[!NOTE]
>
>데이터 소스는 항상 기술 사용자가 구성해야 합니다. <!--Rights?-->

이 구성의 경우 보고서에 사용할 속성이 포함된 데이터 세트를 한 개 이상 추가해야 합니다. 이렇게 하려면 아래 단계를 수행합니다.

>[!CAUTION]
>
>보고 구성에 데이터 세트를 추가하려면 먼저 데이터 세트를 만들어야 합니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=ko#create){target=&quot;_blank&quot;}에서 자세한 내용을 알아보세요.
>
>지원되는 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target=&quot;_blank&quot;} 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다(**experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**).

<!--
➡️ [Discover this feature in video](#video)
-->

예를 들어 이메일 캠페인이 구매 또는 주문과 같은 상거래 데이터에 미치는 영향을 알려면 **experience-event-commerce** 필드 그룹으로 경험 이벤트 데이터 세트를 만들어야 합니다. 마찬가지로, 모바일 상호 작용에 대해 보고하려면 **experienceevent-application** 필드 그룹으로 경험 이벤트 데이터 세트를 만들어야 합니다. <!--If you want to report on web interactions then you need to include the web field group.--> 이러한 필드 그룹을 하나의 데이터 세트 또는 다른 데이터 세트에서 사용할 하나 또는 여러 스키마에 추가할 수 있습니다.

>[!NOTE]
>
>[XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}에서 XDM 스키마 및 필드 그룹에 대한 자세한 내용을 알아보세요.

1. **[!UICONTROL ADMINISTRATION]** 메뉴에서 **[!UICONTROL Configurations]**&#x200B;을(를) 선택합니다. **[!UICONTROL Reporting]** 섹션에서 **[!UICONTROL Manage]**&#x200B;을(를) 클릭합니다.

   ![](assets/reporting-config-menu.png)

   이미 추가된 데이터 세트 목록이 표시됩니다.

1. **[!UICONTROL Dataset]** 탭에서 **[!UICONTROL Add dataset]**&#x200B;을(를) 클릭합니다.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >**[!UICONTROL System dataset]** 탭을 선택하는 경우 시스템에서 만든 데이터 세트만 표시됩니다. 다른 데이터 세트를 추가할 수 없습니다.

1. **[!UICONTROL Dataset]** 드롭다운 목록에서 보고서에 사용할 데이터 세트를 선택합니다.

   >[!CAUTION]
   >
   >지원되는 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다(**experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**). 해당 기준과 일치하지 않는 데이터 세트를 선택하면 변경 사항을 저장할 수 없습니다.

   ![](assets/reporting-config-datasets.png)

   [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=ko){target=&quot;_blank&quot;}에서 데이터 세트에 대한 자세한 내용을 알아보세요.

1. **[!UICONTROL Profile ID]** 드롭다운 목록에서 보고서에서 각 프로필을 식별하는 데 사용할 데이터 세트 필드 속성을 선택합니다.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >보고에 사용할 수 있는 ID만 표시됩니다.

1. **[!UICONTROL Use Primary ID namespace]** 옵션은 기본적으로 활성화되어 있습니다. 선택된 **[!UICONTROL Profile ID]**&#x200B;이(가) **[!UICONTROL Identity Map]**&#x200B;인 경우 이 옵션을 비활성화하고 표시되는 드롭다운 목록에서 다른 네임스페이스를 선택할 수 있습니다.

   ![](assets/reporting-config-namespace.png)

   [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=ko){target=&quot;_blank&quot;}에서 네임스페이스에 대한 자세한 내용을 알아보세요.

1. 변경 사항을 저장하여 선택한 데이터 세트를 보고 구성 목록에 추가합니다.

   >[!CAUTION]
   >
   >이벤트 유형이 아닌 데이터 세트를 선택한 경우 진행할 수 없습니다.

이제 게재 보고서를 작성할 때 이 데이터 세트의 데이터를 사용하여 추가 사용자 정의 정보를 검색하고 보고서를 보다 세밀하게 조정할 수 있습니다. [자세히 보기](content-experiment.md#objectives-global)

>[!NOTE]
>
>데이터 세트를 여러 개 추가하면 모든 데이터 세트의 모든 데이터를 보고에 사용할 수 있습니다.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
