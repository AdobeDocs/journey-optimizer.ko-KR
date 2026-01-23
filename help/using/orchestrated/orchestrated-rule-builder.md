---
solution: Journey Optimizer
product: journey optimizer
title: 규칙 빌더를 사용하여 작업
description: 오케스트레이션된 캠페인에 대한 규칙을 만드는 방법을 알아봅니다
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
version: Campaign Orchestration
source-git-commit: 78fe305975ec97b45e73d60b1dcd66800f67d26e
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 78%

---


# 규칙 빌더를 사용하여 작업 {#orchestrated-rule-builder}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_predefinedfilter"
>title="미리 정의된 필터"
>abstract="**미리 정의된 필터** 옵션을 사용하여 사용자 정의 필터 목록이나 즐겨찾기에서 미리 정의된 필터를 선택할 수 있습니다."

오케스트레이션된 캠페인에는 다양한 기준을 기반으로 데이터베이스를 필터링하는 프로세스를 간소화하는 규칙 빌더가 함께 제공됩니다. 규칙 빌더는 매우 복잡하고 긴 쿼리를 효율적으로 관리하여 향상된 유연성과 정밀성을 제공합니다.

또한 조건 내 미리 정의된 필터를 지원하므로 포괄적인 대상자 타겟팅 및 세분화 전략에 고급 표현식과 연산자를 활용하면서 쿼리를 쉽게 세분화할 수 있습니다.

## 규칙 빌더 액세스

규칙을 정의하여 데이터를 필터링해야 하는 모든 컨텍스트에서 규칙 빌더를 사용할 수 있습니다.

| 사용 | 예 |
|  ---  |  ---  |
| **대상자 빌드**: **[!UICONTROL 대상자 빌드]** 활동을 사용하여 오케스트레이션된 캠페인에서 타깃팅할 모집단을 지정하고 필요에 맞게 새 대상자를 쉽게 만들 수 있습니다. [대상자를 작성하는 방법 알아보기](../orchestrated/activities/build-audience.md) | ![대상자 작성 인터페이스에 액세스하는 방법을 보여 주는 이미지](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **캠페인 캔버스에 조건 만들기**: **[!UICONTROL 분할]** 활동을 사용하여 캠페인 캔버스 내에 규칙을 적용하여 특정 요구 사항에 맞춥니다. [분할 활동을 사용하는 방법을 알아봅니다.](../orchestrated/activities/split.md) | ![워크플로 사용자 정의 옵션에 액세스하는 방법을 보여 주는 이미지](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **고급 필터 만들기**: 캠페인 로그 또는 타겟팅 차원과 같은 목록에 표시된 데이터를 필터링하는 규칙을 빌드합니다. | ![목록 필터를 사용자 정의하는 방법을 보여 주는 이미지](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## 규칙 빌더 인터페이스 {#interface}

규칙 빌더는 쿼리를 작성하는 중앙 캔버스와 규칙에 대한 정보를 제공하는 속성 창을 제공합니다.

![규칙 빌더 인터페이스를 표시하는 이미지](assets/rule-builder-interface.png)

* **중앙 캔버스**&#x200B;에서 다른 구성 요소를 추가하고 결합하여 규칙을 만듭니다. [규칙 작성 방법 알아보기](../orchestrated/build-query.md)

* **[!UICONTROL 규칙 속성]** 창은 규칙에 대한 정보를 제공합니다. 다양한 작업을 수행하여 규칙을 확인하고 해당 규칙이 필요에 맞도록 할 수 있습니다.

  이 창은 대상자를 만들기 위한 쿼리를 작성할 때 표시됩니다. [쿼리를 확인하는 방법 알아보기](build-query.md#check-and-validate-your-query)
