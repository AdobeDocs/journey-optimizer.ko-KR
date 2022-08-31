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
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 43%

---

# 보고 구성 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="보고용 데이터 세트 설정"
>abstract="보고 구성을 사용하면 캠페인 보고서의 목표 탭에서 사용할 추가 지표를 검색할 수 있습니다. 기술 사용자가 수행해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="데이터 세트 선택"
>abstract="지원되는 필드 그룹 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다. 응용 프로그램 세부 정보, 상거래 세부 정보, 웹 세부 정보."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

보고 데이터 소스 구성에서는 **[!UICONTROL Objectives]** 캠페인 보고서의 탭. [자세히 보기](content-experiment.md#objectives-global)

>[!NOTE]
>
>보고 구성은 기술 사용자가 수행해야 합니다. <!--Rights?-->

이 구성의 경우 보고서에 사용할 추가 요소가 들어 있는 데이터 세트를 한 개 이상 추가해야 합니다. 이렇게 하려면 단계를 수행합니다 [아래](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 전제 조건


보고 구성에 데이터 세트를 추가하기 전에 해당 데이터 세트를 만들어야 합니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=ko#create){target=&quot;_blank&quot;}에서 자세한 내용을 알아보세요.

* 이벤트 유형 데이터 세트만 추가할 수 있습니다.

* 이러한 데이터 세트는 다음 중 하나 이상을 포함해야 합니다 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target=&quot;_blank&quot;}: **애플리케이션 세부 정보**, **상거래 세부 사항**, **웹 세부 사항**.

   >[!NOTE]
   >
   >현재 이러한 필드 그룹만 지원됩니다.

   예를 들어 이메일 캠페인이 구매 또는 주문과 같은 상거래 데이터에 미치는 영향을 알려면 을(를) 사용하여 경험 이벤트 데이터 세트를 만들어야 합니다 **상거래 세부 사항** 필드 그룹.

   마찬가지로, 모바일 상호 작용에 대해 보고하려면 를 사용하여 경험 이벤트 데이터 세트를 만들어야 합니다 **애플리케이션 세부 정보** 필드 그룹.

   각 필드 그룹에 해당하는 지표가 나열됩니다 [여기](#objective-list).

* 이러한 필드 그룹을 하나 또는 여러 데이터 세트에서 사용할 하나 또는 여러 스키마에 추가할 수 있습니다.

>[!NOTE]
>
>[XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}에서 XDM 스키마 및 필드 그룹에 대한 자세한 내용을 알아보세요.

## 각 필드 그룹에 해당하는 목표 {#objective-list}

아래 표는 페이지에 추가될 지표를 보여줍니다. **[!UICONTROL Objectives]** 각 필드 그룹에 대한 캠페인 보고서의 탭.

| 필드 그룹 | 목표 |
|--- |--- |
| 상거래 세부 사항 | 가격 합계<br>결제 금액<br>(고유) 체크아웃<br>(고유) 제품 목록 추가<br>(고유) 제품 목록 열기<br>(고유) 제품 목록 제거<br>(고유) 제품 목록 보기<br>(고유) 제품 보기<br>(고유) 구매<br>(고유) 래터용 저장<br>제품 가격 합계<br>제품 수량 |
| 애플리케이션 세부 정보 | (고유) 앱 실행<br>첫 번째 앱 실행<br>(고유) 앱 설치<br>(고유) 앱 업그레이드 |
| 웹 세부 사항 | (고유) 페이지 보기 수 |

## 데이터 세트 추가 {#add-datasets}

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
   >지원되는 이벤트 유형 데이터 세트 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **애플리케이션 세부 정보**, **상거래 세부 사항**, **웹 세부 사항**. 해당 기준과 일치하지 않는 데이터 세트를 선택하면 변경 사항을 저장할 수 없습니다.

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

이제 캠페인 보고서를 작성할 때 추가한 데이터 세트에 사용된 필드 그룹에 해당하는 지표를 볼 수 있습니다. 로 이동합니다. **[!UICONTROL Objectives]** 탭을 선택하고 선택한 지표를 선택하여 보고서를 더 잘 세밀하게 조정합니다. [자세히 보기](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>데이터 세트를 여러 개 추가하면 모든 데이터 세트의 모든 데이터를 보고에 사용할 수 있습니다.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
