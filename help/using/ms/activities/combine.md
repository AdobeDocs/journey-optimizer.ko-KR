---
solution: Journey Optimizer
product: journey optimizer
title: 결합 활동 사용
description: Combine 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 86%

---

# 결합 {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="활동 결합"
>abstract="**결합** 활동을 통해 인바운드 모집단에 대한 세분화를 수행할 수 있습니다. 따라서 여러 모집단을 결합하거나, 일부를 제외하거나, 데이터를 여러 대상에 공통으로 유지할 수 있습니다."

**결합** 활동은 **타깃팅** 활동입니다. 이 활동을 통해 인바운드 모집단에 대한 세분화를 수행할 수 있습니다. 따라서 여러 모집단을 결합하거나, 일부를 제외하거나, 데이터를 여러 대상에 공통으로 유지할 수 있습니다. 사용 가능한 세분화 유형은 다음과 같습니다.

<!--
The **Combine** activity can be placed after any other activity, but not at the beginning of the workflow. Any activity can be placed after the **Combine**.
-->

* **합집합** 기능을 사용하면 여러 활동의 결과를 하나의 타깃으로 다시 그룹화할 수 있습니다.
* **교집합** 기능을 사용하면 활동에서 다른 인바운드 집단에 공통되는 요소만 유지할 수 있습니다.
* **제외** 기능을 사용하면 특정 기준에 따라 하나의 모집단에서 요소를 제외할 수 있습니다.

## 결합 활동 구성 {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="교차 병합 옵션"
>abstract="교집합 기능을 사용하면 활동에서 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다. 참여 설정 섹션에서 참여하려는 모든 이전 활동을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="제외 병합 옵션"
>abstract="제외 기능을 사용하면 특정 기준에 따라 하나의 모집단에서 요소를 제외할 수 있습니다. 참여 설정 섹션에서 참여하려는 모든 이전 활동을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="세분화 유형 선택"
>abstract="대상자 결합 방법을 선택합니다. **합집합** 기능을 사용하면 여러 활동의 결과를 하나의 타깃으로 다시 그룹화할 수 있습니다. **교집합** 기능을 사용하면 활동에서 다른 인바운드 모집단에 공통되는 요소만 유지할 수 있습니다. **제외** 기능을 사용하면 특정 기준에 따라 하나의 모집단에서 요소를 제외할 수 있습니다. "

**결합** 활동 구성을 시작하려면 다음과 같은 일반적인 단계를 따르십시오.

![](../assets/workflow-combine.png)

1. **대상자 빌드** 활동과 같은 여러 활동을 추가하여 두 개 이상의 서로 다른 실행 분기를 구성합니다.
1. 이전 분기에 **결합** 활동을 추가합니다.
1. [합집합](#union), [교차](#intersection) 또는 [제외](#exclusion) 중에서 세분화 유형을 선택합니다.
1. **계속을 클릭합니다**.
1. **참여 설정** 섹션에서 참여하려는 모든 이전 활동을 선택하십시오.

## 합집합 {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="조정 옵션"
>abstract="중복 처리 방법을 정의하려면 **조정 유형**&#x200B;을 선택합니다. 기본적으로 **키** 옵션이 활성화되어 있는데, 이는 서로 다른 인바운드 전환의 요소가 동일한 키를 가질 때 활동이 하나의 요소만 유지한다는 것을 의미합니다. 데이터 조정을 적용할 열 목록을 정의하려면 **열 선택** 옵션을 사용합니다."

**결합** 활동에서 **결합**&#x200B;을 구성할 수 있습니다. 이를 위해 **조정 유형**&#x200B;을(를) 선택하여 중복 처리 방법을 정의해야 합니다.

* **키 전용**: 기본 모드입니다. 다른 인바운드 전환의 요소가 동일한 키를 가지면 활동은 하나의 요소만 유지합니다. 이 옵션은 인바운드 모집단이 동질적일 경우에만 사용할 수 있습니다.
* **열 선택**: 데이터 조정을 적용할 열 목록을 정의하려면 이 옵션을 선택하십시오. 기본 세트(소스 데이터가 있는 세트)를 먼저 선택한 다음 결합에 사용할 열을 선택해야 합니다.

## 교집합 {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="교집합 조정 옵션"
>abstract="중복 처리 방법을 정의하려면 **조정 유형**&#x200B;을 선택합니다. 기본적으로 **키** 옵션이 활성화되어 있는데, 이는 서로 다른 인바운드 전환의 요소가 동일한 키를 가질 때 활동이 하나의 요소만 유지한다는 것을 의미합니다. 데이터 조정을 적용할 열 목록을 정의하려면 **열 선택** 옵션을 사용합니다."

**결합** 활동에서 **교차**&#x200B;를 구성할 수 있습니다. 이를 위해 아래의 추가 단계를 수행해야 합니다.

1. 중복 처리 방법을 정의하려면 **조정 유형**&#x200B;을 선택합니다. [합집합](#union) 섹션을 참조하십시오.
1. 나머지 모집단을 처리하려면 **완료 생성** 옵션을 선택할 수 있습니다. 여집합에는 교차를 제외한 모든 인바운드 활동 결과의 합집합이 포함됩니다. 그런 다음 추가 아웃바운드 전환이 활동에 추가됩니다.

## 제외 {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="제외 규칙"
>abstract="필요한 경우 인바운드 테이블을 조작할 수 있습니다. 다른 차원에서 대상을 제외하려면 이 대상을 기본 대상과 동일한 타기팅 차원으로 반환해야 합니다. 이 작업을 수행하려면 제외 규칙 섹션에서 규칙 추가를 클릭하고 차원 변경 조건을 지정합니다. 데이터 조정은 속성 또는 참여를 통해 수행됩니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="결합할 세트 선택"
>abstract="**참여 설정** 섹션에서 인바운드 전환의 **기본 세트**&#x200B;를 선택합니다. 요소가 제외되는 집합입니다. 다른 집합은 기본 집합에서 제외되기 전에 요소와 일치합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="제외 규칙"
>abstract="필요한 경우 인바운드 테이블을 조작할 수 있습니다. 다른 차원에서 대상을 제외하려면 이 대상을 기본 대상과 동일한 타기팅 차원으로 반환해야 합니다. 이 작업을 수행하려면 제외 규칙 섹션에서 규칙 추가를 클릭하고 차원 변경 조건을 지정합니다. 데이터 조정은 속성 또는 참여를 통해 수행됩니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="결합 생성 여집합"
>abstract="추가 전환에서 나머지 집단을 처리하려면 ‘여집합 생성’ 옵션을 토글합니다."

**결합** 활동에서 **제외**&#x200B;를 구성할 수 있습니다. 이를 위해 아래의 추가 단계를 수행해야 합니다.

1. **참여 설정** 섹션에서 인바운드 전환의 **기본 세트**&#x200B;를 선택합니다. 요소가 제외되는 집합입니다. 다른 집합은 기본 집합에서 제외되기 전에 요소와 일치합니다.
1. 필요한 경우 인바운드 테이블을 조작할 수 있습니다. 다른 차원에서 대상을 제외하려면 이 대상을 기본 대상과 동일한 타기팅 차원으로 반환해야 합니다. 이 작업을 수행하려면 **제외 규칙** 섹션에서 **규칙 추가**&#x200B;를 클릭하고 차원 변경 조건을 지정합니다. 데이터 조정은 속성 또는 참여를 통해 수행됩니다.
1. 나머지 모집단을 처리하려면 **완료 생성** 옵션을 선택할 수 있습니다. [교차](#intersection) 섹션을 참조하십시오.

## 예시{#combine-examples}

다음 예제에서는 **Combine** 활동을 사용하고 **union**&#x200B;을(를) 추가하여 두 쿼리의 모든 프로필을 검색합니다. 18~27세 사용자 및 34~40세 사용자.

![](../assets/workflow-union-example.png)

다음 예는 두 쿼리 활동 간의 **교차**&#x200B;를 보여 줍니다. 여기에서 18세에서 27세 사이의 프로필과 이메일 주소가 제공된 프로필을 검색하는 데 사용됩니다.

![](../assets/workflow-intersection-example.png)

다음 **제외** 예에서는 18세에서 27세 사이의 Adobe 이메일 도메인이 있는 프로필을 필터링하도록 구성된 두 개의 쿼리를 보여 줍니다. Adobe 이메일 도메인이 있는 프로필은 첫 번째 집합에서 제외됩니다.

![](../assets/workflow-exclusion-example.png)
