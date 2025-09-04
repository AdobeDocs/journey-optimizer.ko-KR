---
solution: Journey Optimizer
product: journey optimizer
title: 여정 게시
description: 여정 지표에 대해 보고하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 게시, 여정, 라이브, 유효성, 확인
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 6%

---

# 여정 지표 구성 및 추적 {#success-metrics}

여정 지표를 통해 고객 여정의 효과를 명확하게 파악할 수 있습니다. 이 기능을 사용하면 정의된 KPI에 대해 성과를 추적하고 작동 중인 항목에 대한 통찰력을 확보하고 최적화할 영역을 식별할 수 있습니다. 실시간으로 영향을 측정함으로써 지속적인 개선을 유도하고 데이터 정보에 기반한 의사 결정을 내려 고객 참여를 높일 수 있습니다.

## 전제 조건 {#prerequisites}

여정 지표를 사용하기 전에 Adobe Experience Platform의 구성 > 보고에서 `Commerce Details`, `Web` 및 `Mobile` [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}을(를) 포함하는 데이터 세트를 추가해야 합니다.

이러한 필드 그룹은 사용자 지정 그룹이 아닌 기본 제공 옵션에서 선택해야 합니다. [데이터 세트 추가](../reports/reporting-configuration.md#add-datasets) 섹션을 참조하십시오.

## 사용 가능한 지표 {#metrics}

지표 목록은 데이터 집합에 포함된 [필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=ko#field-group){target="_blank"}에 따라 다릅니다.

데이터 세트가 구성되지 않은 경우 다음 지표만 사용할 수 있습니다. **[!UICONTROL 클릭]**, **[!UICONTROL 고유 클릭]**, **[!UICONTROL 클릭스루 비율]** 및 **[!UICONTROL 열기 비율]**.

Customer Journey Analytics 라이선스를 사용하면 사용자 지정 성공 지표를 만들 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| 지표 | 관련 필드 그룹 |
|-|-|
| 클릭수 | 필드 그룹 필요 없음 |
| 고유 클릭수 | 필드 그룹 필요 없음 |
| 클릭스루 비율(CTR) | 필드 그룹 필요 없음 |
| 클릭스루 열람율(CTOR) | 필드 그룹 필요 없음 |
| 페이지 보기 횟수 | 웹 필드 그룹 |
| 앱 실행 | 모바일 필드 그룹 |
| 첫 번째 앱 실행 | 모바일 필드 그룹 |
| 앱 설치 | 모바일 필드 그룹 |
| 앱 업그레이드 | 모바일 필드 그룹 |
| 구매 | Commerce 세부 정보 필드 그룹 |
| 체크아웃 | Commerce 세부 정보 필드 그룹 |
| 장바구니 추가 | Commerce 세부 정보 필드 그룹 |
| 장바구니 열기 | Commerce 세부 정보 필드 그룹 |
| 장바구니 보기 | Commerce 세부 정보 필드 그룹 |
| 장바구니 제거 | Commerce 세부 정보 필드 그룹 |
| 제품 보기 | Commerce 세부 정보 필드 그룹 |
| 나중에 저장 | Commerce 세부 정보 필드 그룹 |

## 기여도 {#attribution}

각 지표는 특정 결과에 기여하는 터치포인트 또는 상호 작용을 결정하는 속성 세트를 제공합니다.

* **Journey Optimizer 라이선스가 있는 지표 속성**:

  Journey Optimizer 라이센스만 있는 경우, 선택한 지표에 대해 사용 가능한 최대 전환 확인 기간은 7일로 설정됩니다. 이러한 지표의 경우 속성 모델은 기본적으로 **마지막 터치**, 즉 전환 전 가장 최근 상호 작용으로 설정됩니다.

  예를 들어 고객이 지난 7일 이내에 여정과 상호 작용한 후 구매가 이루어졌는지 여부를 추적할 수 있습니다.

* **Customer Journey Analytics 라이선스가 있는 지표 속성**:

  Journey Optimizer 및 Customer Journey Analytics 라이선스를 모두 사용하여 특정 속성 설정으로 사용자 지정 지표를 만들거나 기본 제공 지표의 속성을 변경할 수 있습니다.

  [속성 모델](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)에 대해 자세히 알아보기

## 여정 지표 할당 {#assign}

>[!IMPORTANT]
>
>여정 당 하나의 여정 지표만 허용됩니다.

여정 지표 추적을 시작하려면 아래에 설명된 단계를 수행합니다.

1. **[!UICONTROL 여정]** 메뉴에서 **[!UICONTROL 여정 만들기]**&#x200B;를 클릭합니다.

1. 여정의 구성 창을 편집하여 여정 이름을 정의하고 속성을 설정합니다. [이 여정](../building-journeys/journey-properties.md)에서 페이지의 속성을 설정하는 방법을 알아보세요.

1. 여정 효과를 측정하는 데 사용할 **[!UICONTROL 여정 지표]**&#x200B;를 선택하십시오.

   지표는 여정 자체에 적용되며 여정의 모든 요소에 적용할 수 있습니다.

   ![](assets/success_metric.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 필요한 **[!UICONTROL 활동]**(으)로 여정을 디자인합니다.

1. 여정 테스트 및 게시

1. 여정 보고서를 열어 지정된 성공 지표의 성과를 추적합니다.

   선택한 지표는 보고서의 KPI 및 여정 상태 테이블에 표시됩니다.

   ![](assets/success_metric_2.png)

