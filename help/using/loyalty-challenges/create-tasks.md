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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---


# 작업 만들기 {#create-tasks}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md) - 개요, 워크플로, 사전 요구 사항
* [충성도 문제 액세스](access-loyalty-challenges.md) - 인벤토리 및 필터링
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* **작업 만들기** ◀︎**현재 상태** - 과제 작업 정의
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 개요 {#overview}

작업은 고객이 충성도 도전에서 보상을 얻기 위해 완료해야 하는 특정 작업 또는 이정표를 정의합니다. 작업 유형, 수량, 제품 요구 사항 및 보상 값을 구성하여 매력적인 개인화된 충성도 경험을 만들 수 있습니다.

각 작업은 측정 가능한 작업을 나타내며 과제 완성에 기여합니다. 작업은 재사용 가능한 구성 요소로서 독립적으로 만든 다음 하나 이상의 문제에 추가하거나 과제 내에서 직접 만들 수 있습니다.

### 다양한 과제 유형에서 작업이 작동하는 방식 {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

과제 유형(표준, 연속 또는 순차적)에 따라 고객은 다음과 같이 작업을 다르게 완료합니다.

* **표준 과제**: 고객은 순서에 관계없이 지정된 수의 작업을 완료합니다
* **연속 문제**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다
* **순차적 문제**: 고객은 정의된 순서로 작업을 완료합니다

## 작업 만들기 {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

두 진입점에서 작업을 생성할 수 있습니다. 구성 프로세스는 시작하는 위치에 관계없이 동일합니다.

+++작업 인벤토리에서

1. Journey Optimizer의 **[!UICONTROL 충성도 과제(Beta)]**(으)로 이동합니다.

1. **[!UICONTROL 작업]** 탭을 선택합니다.

1. **[!UICONTROL 작업 만들기]**&#x200B;를 선택합니다.

인벤토리에서 생성된 작업은 저장되며 여러 문제에 걸쳐 재사용할 수 있습니다.

+++

+++과제 내에서

1. 기존 과제를 열거나 새 과제를 만듭니다.

1. **[!UICONTROL 작업]** 섹션으로 이동합니다.

1. **[!UICONTROL 작업 추가]**&#x200B;를 선택한 다음 **[!UICONTROL 새 작업 만들기]**&#x200B;를 선택합니다.

이러한 방식으로 생성된 작업은 자동으로 과제에 추가되고 다른 과제에서 재사용할 수 있도록 작업 인벤토리에 저장됩니다.

+++

### 작업 속성 정의 {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

기본 작업 정보를 구성합니다.

* **작업 이름**: 작업에 대한 수사적 이름을 입력하십시오. 이 이름은 사용자와 팀이 볼 수 있지만 콘텐츠 카드 디자인에 따라 고객에게 표시되지 않을 수 있습니다.
* **작업 설명**: (선택 사항) 작업 목적 또는 요구 사항에 대한 세부 정보를 추가합니다.

### 고객 활동 선택 {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

이 작업을 완료하기 위해 고객이 수행해야 하는 고객 활동의 유형을 선택합니다.

* **[!UICONTROL 구매]**: 이 작업을 완료하려면 고객이 하나 이상의 항목을 구입해야 합니다.
* **[!UICONTROL 지출]**: 이 작업을 완료하려면 고객이 지정된 금액을 사용해야 합니다.

결과 목표에 가장 적합한 고객 활동을 선택합니다. 각 활동 유형에는 작업 요구 사항을 추가로 정의하고 형성하기 위해 구성 가능한 특정 속성이 있습니다.

### 속성 정의 {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

선택한 활동 유형에 따라 작업 속성을 구성합니다.

+++구매 활동용

다음 속성을 구성합니다.

* **수량**: 이 작업을 완료하려면 구매해야 하는 항목의 수를 입력하십시오.
* **적격 항목 및 제외**: 작업 완료 시 계산되는 항목 또는 항목 그룹과 그렇지 않은 항목 그룹을 정의합니다. [적격 항목 및 제외 정의](#eligible-items-exclusions)에 대해 자세히 알아보기

**선택적 특성**(매개 변수 아이콘을 통해 구성):

* **최소 지출 금액**: 최소 구매 금액 요구 사항을 설정합니다.
* **최대 트랜잭션 수**: 작업을 완료하는 데 사용할 수 있는 트랜잭션 수를 제한합니다

+++

+++지출 활동용

다음 속성을 구성합니다.

* **금액**: 작업을 완료하는 데 필요한 총 지출 금액을 입력하십시오.
* **최대 트랜잭션 수**: 지출 요구 사항을 충족하는 데 허용되는 트랜잭션 수를 지정합니다. 트랜잭션 수를 제한하지 않으려면 매개변수 아이콘에서 이 속성을 비활성화할 수 있습니다
* **적격 항목 및 제외**: (선택 사항) 작업 완료 시 계산되는 항목 또는 항목 그룹과 그렇지 않은 항목 또는 항목 그룹을 정의합니다. [적격 항목 및 제외 정의](#eligible-items-exclusions)에 대해 자세히 알아보기

+++

모든 특성을 구성한 후 **[!UICONTROL 만들기]**&#x200B;를 선택하여 작업을 저장합니다. 작업은 작업 인벤토리에 저장되며 문제 내에서 생성된 경우 해당 문제에 자동으로 추가됩니다.

## 적격 품목 및 제외 정의 {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

구매 및 지출 활동 모두에 대해 적격 품목 및 그룹을 정의하고 품목 및 그룹을 제외할 수 있습니다. 이를 통해 과제 목표에 맞게 특정 제품, 카테고리 또는 위치를 타깃팅할 수 있습니다.

**사용 사례:**

* 고객에게 커피 품목을 구매하면 보상을 제공하지만 통관 제품은 제외하는 작업을 생성합니다.
* 특정 제품 범주로 지출 작업 제한
* 작업 완료 시 기프트 카드 또는 판촉 상품 계산 제외

### 적격 항목 구성 {#configure-eligible-items}

적격 항목을 정의하려면 **[!UICONTROL 적격 작업 구매를 다음]** 섹션으로 제한합니다.

* 특정 항목 ID, 범주 또는 대상 ID를 쉼표로 구분하여 입력합니다.
* 예: `SKU001, SKU002, CategoryA, StoreLocation123`
* **팁**: 모든 구매를 허용하려면 `*`을(를) 입력하십시오(비워 두면 기본 동작).

### 제외 구성 {#configure-exclusions}

작업에서 항목을 제외하려면 **[!UICONTROL 다음 항목이 이 작업에서 제외됩니다]** 섹션:

* 작업 완료에 계산되지 않아야 하는 특정 항목 ID, 범주 또는 대상 ID를 입력합니다.
* 예: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* 일반적인 제외: 판매 또는 통관 품목, 기프트 카드, 프로모션 품목

>[!NOTE]
>
>제외가 적격 품목보다 우선합니다. 항목이 적격 항목 및 제외와 모두 일치하는 경우 작업에서 제외됩니다.

## 다음 단계 {#next-steps}

이제 작업을 만들고 구성하는 방법을 알았습니다.

* [과제 만들기](create-challenges.md) - 완전한 과제를 만들고 보상을 구성하는 방법에 대해 알아봅니다.
* [문제 관리](manage-challenges.md) - 문제를 편집, 모니터링 및 최적화하는 방법을 알아봅니다.
