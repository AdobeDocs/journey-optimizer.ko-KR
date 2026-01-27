---
solution: Journey Optimizer
product: journey optimizer
title: 미리 정의된 필터 작업
description: 오케스트레이션된 캠페인에서 사전 정의된 필터를 저장, 적용 및 관리하는 방법을 알아봅니다
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# 미리 정의된 필터 작업 {#predefined-filters}

사전 정의된 필터는 규칙 빌더에서 재사용할 수 있는 저장된 규칙입니다. 이를 사용하여 일반적인 쿼리를 다시 작성하지 않도록 하고 오케스트레이션된 캠페인 간에 타깃팅 논리를 표준화합니다.

사전 정의된 필터를 즐겨찾기로 표시하고, 다른 사용자와 공유하고, 필터가 적용될 때 선택한 필드를 편집할 수 있도록 매개 변수를 추가할 수 있습니다.

## 사전 정의된 필터 만들기 {#create}

나중에 사용할 수 있도록 규칙 빌더에서 사용자 지정 필터를 저장합니다. 다음 단계를 수행하십시오.

1. 규칙 빌더를 열고 필터링 조건을 정의합니다. [규칙 작성 방법 알아보기](../orchestrated/build-query.md)

1. 선택 사항: 필터를 사용할 때 특정 필드를 편집할 수 있도록 하려면 필드를 선택하고 **[!UICONTROL 매개 변수로 설정]**&#x200B;을 켭니다. 필터를 적용하면 이러한 필드만 편집할 수 있습니다.

   ![](assets/predefined-filter-parameter-enable.png)

1. 필터를 저장하려면 **[!UICONTROL 필터 선택 또는 저장]**&#x200B;을 클릭하고 **[!UICONTROL 필터로 저장]**&#x200B;을 선택합니다.

   ![](assets/predefined-filter-save.png)

1. 필터에 대한 레이블과 설명을 입력한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   * 필터를 즐겨찾기로 저장하려면 **[!UICONTROL 자주 사용하는 필터]** 옵션을 켜십시오. 자세한 내용은 [이 섹션](#fav-filter)을 참조하십시오.
   * 다른 사용자가 필터에 액세스할 수 있도록 하려면 **[!UICONTROL 공유 필터]** 옵션을 사용하도록 설정하십시오. 자세한 내용은 [이 섹션](#share-filter)을 참조하십시오.

   ![](assets/predefined-filter-save-name.png)

이제 사용자 지정 필터를 **미리 정의된 필터** 목록에서 사용할 수 있습니다.

## 규칙에서 사전 정의된 필터 사용 {#apply}

규칙 빌더에서 쿼리를 정의할 때 사전 정의된 필터를 사용할 수 있습니다.

1. **[!UICONTROL 규칙 속성]** 창에서 **[!UICONTROL 필터 선택 또는 저장]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 미리 정의된 필터 선택]**&#x200B;을 선택하고 필터를 선택합니다. 즐겨찾기에 추가된 경우 목록에서 미리 정의된 필터를 직접 선택할 수도 있습니다.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >사전 정의된 필터를 선택하면 캔버스에 내장된 규칙이 선택한 필터로 바뀝니다.

1. 필터가 캔버스에서 열립니다. 필요에 따라 조건을 계속 편집합니다.

   ![](assets/predefined-filter-added.png)

   선택한 필터에 매개 변수가 포함되어 있으면 매개 변수로 표시된 필드만 편집할 수 있습니다. **[!UICONTROL 규칙 속성]** 창 옆의 창에 표시됩니다.

   ![](assets/predefined-filter-parameter-apply.png)

   미리 정의된 필터 자체를 편집하려면 ![줄임표 단추](assets/do-not-localize/rule-builder-icon-more.svg) 단추를 클릭하고 **[!UICONTROL 규칙 편집으로 전환]**&#x200B;을 선택합니다. 모든 변경 사항은 작성 중인 현재 규칙에만 적용됩니다. 사전 정의된 필터는 수정되지 않습니다.

   ![](assets/predefined-filter-parameter-edit.png)

## 즐겨찾기로 필터 저장 {#fav-filter}

미리 정의된 필터를 만드는 경우 즐겨찾기에서 이 미리 정의된 필터를 보려면 **[!UICONTROL 즐겨찾는 필터]** 옵션을 사용하도록 설정하십시오.

필터를 즐겨찾기로 저장하면 아래와 같이 필터 목록의 **[!UICONTROL 즐겨찾는 필터]** 섹션에 표시됩니다.

![즐겨찾기 필터 섹션](assets/predefined-filter-favorites.png)

## 사전 정의된 필터 공유 {#share-filter}

기본적으로 사전 정의된 필터는 비공개이며 사용자에게만 표시됩니다. 조직의 다른 연산자가 필터에 액세스할 수 있도록 하려면 **[!UICONTROL 공유 필터]** 옵션을 사용하도록 설정하십시오.

![공유 필터 옵션](assets/predefined-filter-shared.png)

공유 필터는 모든 사용자에 대해 사전 정의된 필터 목록에 나타나며 사용자가 자신의 규칙에서 이러한 필터를 사용할 수 있도록 합니다.

## 사전 정의된 필터 관리 {#manage-predefined-filter}

사전 정의된 필터를 편집하거나 삭제하려면 다음 단계를 수행합니다.

1. 규칙 빌드에서 **[!UICONTROL 필터 선택 또는 저장]** 단추를 사용하여 미리 정의된 필터 목록을 엽니다.

1. 필터 옆에 있는 ![줄임표 단추](assets/do-not-localize/rule-builder-icon-more.svg) 단추를 선택하고 원하는 작업을 선택합니다.

![](assets/predefined-filters-edit.png)
