---
solution: Journey Optimizer
product: journey optimizer
title: 실험을 위한 Journey Optimizer 보고 구성
description: 보고 데이터 소스를 설정하는 방법 알아보기
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 구성, 실험, 보고, 최적화 도구
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 9910c748cf66828ccbd314757c252b9093d2af75
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 28%

---

# 실험에 대한 보고 구성 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="보고용 데이터 세트 설정"
>abstract="보고 구성을 사용하여 캠페인 보고서의 목표 탭에서 사용되는 추가 지표를 검색할 수 있습니다. 기술 사용자가 수행해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="데이터 세트 선택"
>abstract="지원되는 필드 그룹(애플리케이션 세부 사항, 상거래 세부 사항, 웹 세부 사항) 중 하나 이상이 포함되어야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

보고 데이터 소스 구성을 사용하면 다음에서 사용할 추가 지표를 검색할 수 있습니다. **[!UICONTROL 목표]** 캠페인 보고서 탭. [자세히 알아보기](content-experiment.md#objectives-global)

>[!NOTE]
>
>기술 사용자가 보고 구성을 수행해야 합니다. <!--Rights?-->

이 구성의 경우 보고서에 사용할 추가 요소가 포함된 데이터 세트를 한 개 이상 추가해야 합니다. 이렇게 하려면 단계를 수행합니다 [아래](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 사전 요구 사항


보고 구성에 데이터 세트를 추가하려면 먼저 해당 데이터 세트를 만들어야 합니다. 에서 방법 알아보기 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* 이벤트 유형 데이터 세트만 추가할 수 있습니다.

* 이러한 데이터 세트에는 다음 중 하나 이상이 포함되어야 합니다 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}: **애플리케이션 세부 정보**, **상거래 세부 정보**, **웹 세부 정보**.

   >[!NOTE]
   >
   >현재 이러한 필드 그룹만 지원됩니다.

   예를 들어 이메일 캠페인이 구매 또는 주문과 같은 상거래 데이터에 미치는 영향을 알려면 다음으로 경험 이벤트 데이터 세트를 만들어야 합니다. **상거래 세부 정보** 필드 그룹입니다.

   마찬가지로, 모바일 상호 작용에 대해 보고하려면 를 사용하여 경험 이벤트 데이터 세트를 만들어야 합니다. **애플리케이션 세부 정보** 필드 그룹입니다.

   각 필드 그룹에 해당하는 지표가 나열됩니다 [여기](#objective-list).

* 이러한 필드 그룹을 하나 또는 여러 데이터 세트에서 사용할 하나 또는 여러 스키마에 추가할 수 있습니다.

>[!NOTE]
>
>에서 XDM 스키마 및 필드 그룹에 대한 자세한 내용을 알아봅니다. [XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}.

## 각 필드 그룹에 해당하는 목표 {#objective-list}

아래 표는 에 추가될 지표를 보여 줍니다. **[!UICONTROL 목표]** 각 필드 그룹에 대한 캠페인 보고서 탭.

| 필드 그룹 | 목표 |
|--- |--- |
| 상거래 세부 정보 | 가격 합계<br>결제 금액<br>(고유) 체크아웃<br>(고유) 제품 목록 추가 횟수<br>(고유) 제품 목록 열람수<br>(고유) 제품 목록 제거<br>(고유) 제품 목록 보기<br>(고유) 제품 조회수<br>(고유) 구매<br>(고유) 나중에 저장<br>제품 가격 합계<br>제품 수량 |
| 애플리케이션 세부 정보 | (고유) 앱 실행<br>첫 번째 앱 실행<br>(고유) 앱 설치<br>(고유) 앱 업그레이드 |
| 웹 세부 정보 | (고유) 페이지 조회수 |

## 데이터 세트 추가 {#add-datasets}

1. 다음에서 **[!UICONTROL 관리]** 메뉴, 선택 **[!UICONTROL 구성]**. 다음에서  **[!UICONTROL 보고]** 섹션, 클릭 **[!UICONTROL 관리]**.

   ![](assets/reporting-config-menu.png)

   이미 추가된 데이터 세트 목록이 표시됩니다.

1. 다음에서 **[!UICONTROL 데이터 세트]** 탭을 클릭하고 **[!UICONTROL 데이터 세트 추가]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >을(를) 선택하는 경우 **[!UICONTROL 시스템 데이터 세트]** 탭에는 시스템에서 만든 데이터 세트만 표시됩니다. 다른 데이터 세트를 추가할 수 없습니다.

1. 다음에서 **[!UICONTROL 데이터 세트]** 드롭다운 목록에서 보고서에 사용할 데이터 세트를 선택합니다.

   >[!CAUTION]
   >
   >지원되는 데이터 세트 중 하나 이상을 포함해야 하는 이벤트 유형 데이터 세트만 선택할 수 있습니다. [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}: **애플리케이션 세부 정보**, **상거래 세부 정보**, **웹 세부 정보**. 해당 기준과 일치하지 않는 데이터 세트를 선택하면 변경 사항을 저장할 수 없습니다.

   ![](assets/reporting-config-datasets.png)

   의 데이터 세트에 대한 자세한 내용 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=ko){target="_blank"}.

1. 다음에서 **[!UICONTROL 프로필 ID]** 드롭다운 목록에서 보고서에서 각 프로필을 식별하는 데 사용할 데이터 세트 필드 속성을 선택합니다.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >보고에 사용할 수 있는 ID만 표시됩니다.

1. 다음 **[!UICONTROL 기본 ID 네임스페이스 사용]** 옵션은 기본적으로 활성화되어 있습니다. 선택한 경우 **[!UICONTROL 프로필 ID]** 은(는) **[!UICONTROL ID 맵]**, 이 옵션을 비활성화하고 표시되는 드롭다운 목록에서 다른 네임스페이스를 선택할 수 있습니다.

   ![](assets/reporting-config-namespace.png)

   에서 네임스페이스에 대해 자세히 알아보기 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=ko){target="_blank"}.

1. 변경 사항을 저장하여 선택한 데이터 세트를 보고 구성 목록에 추가합니다.

   >[!CAUTION]
   >
   >이벤트 유형이 아닌 데이터 세트를 선택한 경우 진행할 수 없습니다.

이제 캠페인 보고서를 작성할 때 추가한 데이터 세트에 사용된 필드 그룹에 해당하는 지표를 볼 수 있습니다. 로 이동 **[!UICONTROL 목표]** 을 탭하고 선택한 지표를 선택하여 보고서를 보다 세밀하게 조정합니다. [자세히 보기](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>데이터 세트를 여러 개 추가하면 모든 데이터 세트의 모든 데이터를 보고에 사용할 수 있습니다.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
