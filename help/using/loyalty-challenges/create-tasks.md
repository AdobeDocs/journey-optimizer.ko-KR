---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제를 위한 작업 만들기
description: Adobe Journey Optimizer에서 충성도 문제를 해결하기 위한 작업을 만들고 구성하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
source-git-commit: 342df0950622de1c4c246bf624d05843671e199f
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---


# 작업 만들기 {#create-tasks}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md)
* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* **작업 만들기** ◀︎**현재 상태**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

작업은 고객이 충성도 도전에서 보상을 얻기 위해 완료해야 하는 특정 작업 또는 이정표를 정의합니다. 매력적인 개인화된 충성도 경험을 만들기 위해 작업 유형, 수량 및 제품 요구 사항을 구성할 수 있습니다.

각 작업은 측정 가능한 작업을 나타내며 과제 완성에 기여합니다. 작업은 재사용 가능한 구성 요소로서 독립적으로 만든 다음 하나 이상의 문제에 추가하거나 과제 내에서 직접 만들 수 있습니다.

## 작업 만들기 {#create-task}

두 진입점에서 작업을 생성할 수 있습니다. 구성 프로세스는 시작하는 위치에 관계없이 동일합니다.

>[!BEGINTABS]

>[!TAB 작업 인벤토리에서]

**[!UICONTROL 작업]** 탭을 선택하고 **[!UICONTROL 작업 만들기]**&#x200B;를 선택합니다. 인벤토리에서 생성된 작업은 저장되며 여러 문제에 걸쳐 재사용할 수 있습니다.

![](assets/task-create-inventory.png)

>[!TAB 문제 내에서]

기존 과제를 열거나 새 과제를 만듭니다. **[!UICONTROL 작업 추가]**&#x200B;를 선택하고 **[!UICONTROL 새로 만들기]** 단추를 클릭합니다. 이러한 방식으로 생성된 작업은 자동으로 과제에 추가되고 다른 과제에서 재사용할 수 있도록 작업 인벤토리에 저장됩니다.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## 고객 활동 선택 {#choose-activity}

고객이 이 작업을 완료하기 위해 수행해야 하는 활동 유형을 선택합니다.

* **[!UICONTROL 구매]**: 이 작업을 완료하려면 고객이 하나 이상의 항목을 구입해야 합니다.
* **[!UICONTROL 지출]**: 이 작업을 완료하려면 고객이 지정된 금액을 사용해야 합니다.

활동을 선택하려면 **+** 아이콘을 클릭하고 결과 목표에 가장 적합한 고객 활동을 선택하십시오. 각 활동 유형에는 작업 요구 사항을 추가로 정의하고 형성하기 위해 구성 가능한 특정 속성이 있습니다.
![](assets/task-create-activity.png)

## 작업 특성 정의 {#define-attributes}

선택한 활동 유형에 따라 작업 속성을 구성합니다. 각 활동 유형에 사용할 수 있는 속성을 보려면 아래 탭을 검색하십시오.

>[!BEGINTABS]

>[!TAB 구매 활동]

**구매** 활동에 사용 가능한 특성:

* **[!UICONTROL 수량]**: 이 작업을 완료하려면 구매해야 하는 항목의 수를 입력하십시오.
* **[!UICONTROL 적격 항목 및 제외]**: 작업 완료 시 계산되는 항목 또는 항목 그룹과 그렇지 않은 항목 그룹을 정의합니다. [적격 항목 및 제외에 대한 자세한 정보](#eligible-items-exclusions)
* **[!UICONTROL 최소 지출 금액]**: 최소 구매 금액 요구 사항을 설정합니다.
* **[!UICONTROL 최대 트랜잭션 수]**: 작업을 완료하는 데 사용할 수 있는 트랜잭션 수를 제한합니다.

![](assets/task-create-purchase.png)

>[!TAB 활동 사용]

**지출** 활동에 사용 가능한 특성:

* **[!UICONTROL 금액]**: 작업을 완료하는 데 필요한 총 지출 금액을 입력합니다.
* **[!UICONTROL 적격 항목 및 제외]**: 작업 완료 시 계산되는 항목 또는 항목 그룹과 그렇지 않은 항목 그룹을 정의합니다. [적격 항목 및 제외에 대한 자세한 정보](#eligible-items-exclusions)
* **[!UICONTROL 최대 트랜잭션 수]**: 지출 요구 사항을 충족하는 데 허용되는 트랜잭션 수를 지정합니다. 매개변수 아이콘에서 이 속성을 활성화할 수 있습니다.

![](assets/task-create-spend.png)

>[!ENDTABS]

## 적격 품목 및 제외 정의 {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

**구매**&#x200B;와(과) **지출** 활동 모두에 대해 **[!UICONTROL 적격 항목 및 제외]** 특성을 사용하여 적격 항목 및 그룹과 제외되는 그룹을 정의할 수 있습니다. 이를 통해 과제 목표에 맞게 특정 제품, 카테고리 또는 위치를 타깃팅할 수 있습니다.

예를 들어 지출 작업을 특정 제품 범주로 제한하거나 작업 완료 시 기프트 카드나 프로모션 항목을 카운트하지 않도록 할 수 있습니다.

![](assets/tasks-create-eligible.png)

* 적격 항목을 정의하려면 **[!UICONTROL 적격 작업 구매는 다음]** 필드로 제한됩니다. 필드에 특정 항목 ID, 범주 또는 대상 ID를 쉼표로 구분하여 입력하십시오. 이 필드를 비워 두면 기본적으로 모든 구매를 이용할 수 있습니다. 또한 `*`을(를) 입력하여 모든 구매를 명시적으로 적용할 수 있습니다.

  예: `SKU001, SKU002, CategoryA`

* 작업에서 항목을 제외하려면 **[!UICONTROL 다음 항목이 이 작업에서 제외됩니다]** 필드에 특정 항목 ID, 범주 또는 대상 ID를 입력하십시오.

  예: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## 작업 속성 정의 {#define-task-properties}

작업 **[!UICONTROL 속성]** 창에서 기본 작업 정보를 구성합니다.

* **[!UICONTROL 작업 이름]**: 작업에 대한 수사적 이름을 입력하십시오.
* **[!UICONTROL 작업 설명]**: 구성된 활동 및 특성을 기반으로 설명이 자동으로 생성됩니다. 사용자 정의 설명을 입력하려면 자동 생성 옵션을 끄고 텍스트 필드에 설명을 입력합니다.

![](assets/tasks-create-properties.png)

모든 특성과 속성을 구성한 후 **[!UICONTROL 만들기]**&#x200B;를 선택하여 작업을 저장합니다. 작업은 작업 인벤토리에 저장되며 문제 내에서 생성된 경우 해당 문제에 자동으로 추가됩니다.
