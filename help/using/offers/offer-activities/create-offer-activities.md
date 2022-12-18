---
title: 의사 결정 만들기
description: 결정을 만드는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 1%

---

# 의사 결정 만들기 {#create-offer-activities}

결정 사항은 게재 대상에 따라 게재할 최상의 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용할 오퍼의 컨테이너입니다.

➡️ [이 비디오에서 오퍼 활동을 만드는 방법을 알아봅니다](#video)

결정 목록은 **[!UICONTROL 오퍼]** 메뉴 > **[!UICONTROL 결정]** 탭. 필터를 사용하여 상태 또는 시작 날짜와 종료 날짜에 따라 결정을 검색할 수 있습니다.

![](../assets/activities-list.png)

결정을 내리기 전에 아래 구성 요소가 오퍼 라이브러리에서 만들어졌는지 확인하십시오.

* [배치](../offer-library/creating-placements.md)
* [컬렉션](../offer-library/creating-collections.md)
* [개인화된 오퍼](../offer-library/creating-personalized-offers.md)
* [대체 오퍼](../offer-library/creating-fallback-offers.md)

## 결정 만들기 {#create-activity}

1. 결정 목록에 액세스한 다음 **[!UICONTROL 결정 만들기]**.

1. 결정 이름을 지정합니다.

1. 필요한 경우 시작 및 종료 날짜 및 시간을 정의한 다음 를 클릭합니다. **[!UICONTROL 다음]**.

   ![](../assets/activities-name.png)

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 결정에 지정하려면 을(를) 선택합니다 **[!UICONTROL 액세스 관리]**. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보기](../../administration/object-based-access.md)

## 결정 범위 정의 {#add-decision-scopes}

1. 드롭다운 목록에서 배치를 선택합니다. 결정에서 첫 번째 결정 범위에 추가됩니다.

   ![](../assets/activities-placement.png)

1. 클릭 **[!UICONTROL 추가]** 를 눌러 이 배치에 대한 평가 기준을 선택합니다.

   ![](../assets/activities-evaluation-criteria.png)

   각 기준은 자격 제한과 연관된 오퍼 컬렉션과 배치에 표시할 오퍼를 결정하는 순위 메서드에 구성됩니다.

   >[!NOTE]
   >
   >적어도 하나의 평가 기준이 필요합니다.

1. 고려할 오퍼가 포함된 오퍼 컬렉션을 선택한 다음 **[!UICONTROL 추가]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >을(를) 클릭합니다. **[!UICONTROL 오퍼 컬렉션 열기]** 링크를 클릭하여 새 탭에 컬렉션 목록을 표시하면 컬렉션과 해당 컬렉션이 포함된 오퍼를 찾을 수 있습니다.

   선택한 컬렉션이 기준에 추가됩니다.

   ![](../assets/activities-collection-added.png)

1. 를 사용하십시오 **[!UICONTROL 자격]** 이 배치에 대한 오퍼 선택을 제한하는 필드입니다.

   이 제약 조건은 **의사 결정 규칙**&#x200B;또는 하나 또는 여러 개 **Adobe Experience Platform 세그먼트**. 둘 다 에 자세히 설명되어 있습니다. [이 섹션](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * 오퍼의 선택을 Experience Platform 세그먼트의 멤버로 제한하려면 **[!UICONTROL 세그먼트]**&#x200B;를 클릭한 다음 **[!UICONTROL 세그먼트 추가]**.

      ![](../assets/activity_constraint_segment.png)

      왼쪽 창에서 하나 또는 여러 개의 세그먼트를 추가하고 을(를) 사용하여 결합합니다 **[!UICONTROL 및]** / **[!UICONTROL 또는]** 논리 연산자입니다.

      ![](../assets/activity_constraint_segment2.png)

      에서 세그먼트 작업 방법 알아보기 [이 섹션](../../segment/about-segments.md).

   * 결정 규칙에 선택 제약 조건을 추가하려면 **[!UICONTROL 의사 결정 규칙]** 옵션을 선택하고 선택한 규칙을 선택합니다.

      ![](../assets/activity_constraint_rule.png)

      에서 의사 결정 규칙을 만드는 방법을 알아봅니다. [이 섹션](../offer-library/creating-decision-rules.md).

1. 세그먼트나 결정 규칙을 선택하면 예상 자격을 갖춘 프로필에 대한 정보를 볼 수 있습니다. 클릭 **[!UICONTROL 새로 고침]** 를 눌러 데이터를 업데이트합니다.

   >[!NOTE]
   >
   >규칙 매개 변수에 컨텍스트 데이터 등의 프로필에 없는 데이터가 포함된 경우 프로필 예측을 사용할 수 없습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 자격 규칙입니다.

   ![](../assets/activity_constraint-estimate.png)

1. 각 프로필에 대해 가장 적합한 오퍼를 선택하는 데 사용할 등급 방법을 정의합니다.

   ![](../assets/activity_ranking-method.png)

   * 기본적으로 이 배치에 여러 오퍼가 적합한 경우 우선 순위가 가장 높은 오퍼가 고객에게 전달됩니다.

   * 특정 공식을 사용하여 게재할 적합한 오퍼를 선택하려면 을 선택합니다 **[!UICONTROL 등급 공식]**. 에서 오퍼의 등급을 매기는 방법을 알아봅니다 [이 섹션](../offer-activities/configure-offer-selection.md).

1. 클릭 **[!UICONTROL 추가]** 를 클릭하여 동일한 배치에 대한 더 많은 기준을 정의합니다.

   ![](../assets/activity_add-collection.png)

1. 여러 기준을 추가하면 해당 기준이 특정 순서로 평가됩니다. 시퀀스에 추가된 첫 번째 컬렉션은 먼저 평가됩니다.

   기본 시퀀스를 변경하려면 컬렉션을 끌어다 놓아 원하는 대로 순서를 변경할 수 있습니다.

   ![](../assets/activity_reorder-collections.png)

1. 여러 기준을 동시에 평가할 수도 있습니다. 이렇게 하려면 컬렉션을 다른 컬렉션 위에 끌어다 놓습니다.

   ![](../assets/activity_move-collection.png)

   모두 평행선이어서 평가를 동시에 받게 된다.

   ![](../assets/activity_same-rank-collections.png)

1. 이 결정의 일부로 오퍼에 대한 다른 배치를 추가하려면 **[!UICONTROL 새 범위]** 버튼을 클릭합니다. 각 결정 범위에 대해 위의 단계를 반복합니다.

   ![](../assets/activity_new-scope.png)

## 대체 오퍼 추가 {#add-fallback}

결정 범위를 정의했으면 오퍼 자격 규칙 및 제약 조건과 일치하지 않는 고객을 위한 마지막 수단으로 표시되는 대체 오퍼를 정의합니다.

이렇게 하려면 결정에서 정의된 배치에 대해 사용 가능한 대체 오퍼 목록에서 선택한 다음 을 클릭합니다 **[!UICONTROL 다음]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>을(를) 클릭합니다. **[!UICONTROL 오퍼 라이브러리 열기]** 새 탭에 오퍼 목록을 표시하는 링크입니다.

## 결정 검토 및 저장 {#review}

모든 것이 제대로 구성되면 결정 속성의 요약이 표시됩니다.

1. 오퍼를 고객에게 제공하는 데 이 결정을 사용할 준비가 되었는지 확인합니다. 모든 결정 범위 및 여기에 포함된 대체 오퍼가 표시됩니다.

   ![](../assets/review-decision.png)

1. 각 배치를 확장하거나 축소할 수 있습니다. 각 배치에 대해 사용 가능한 오퍼, 자격 및 등급 세부 사항을 미리 볼 수 있습니다. 예상 자격을 갖춘 프로필에 대한 정보를 표시할 수도 있습니다. 클릭 **[!UICONTROL 새로 고침]** 를 눌러 데이터를 업데이트합니다.

   ![](../assets/review-decision-details.png)

1. **[!UICONTROL 마침을 클릭합니다]**.
1. 선택 **[!UICONTROL 저장 및 활성화]**.

   ![](../assets/save-activities.png)

   나중에 편집하고 활성화하기 위해 결정을 초안으로 저장할 수도 있습니다.

결정은 목록에 **[!UICONTROL 라이브]** 또는 **[!UICONTROL 초안]** 상태, 이전 단계에서 활성화했는지 여부에 따라 다릅니다.

이제 고객에게 오퍼를 전달하는 데 사용할 준비가 되었습니다.

## 의사 결정 목록 {#decision-list}

결정 목록에서 해당 속성을 표시하는 결정을 선택할 수 있습니다. 여기에서 편집할 수도 있습니다.**초안**, **라이브**, **완료**, **보관됨**), 결정을 복제하거나, 삭제합니다.

![](../assets/decision_created.png)

을(를) 선택합니다 **[!UICONTROL 편집]** 버튼을 클릭하여 결정 편집 모드로 돌아갑니다. 여기서 결정 모드를 수정할 수 있습니다 [세부 정보](#create-activity), [결정 범위](#add-decision-scopes) 및 [대체 오퍼](#add-fallback).

라이브 결정을 선택하고 을(를) 클릭합니다. **[!UICONTROL 비활성화]** 결정 상태를 **[!UICONTROL 초안]**.

상태를 다시 설정하려면 **[!UICONTROL 라이브]**&#x200B;에서 을(를) 선택합니다. **[!UICONTROL 활성화]** 이제 표시되는 단추입니다.

![](../assets/decision_activate.png)

다음 **[!UICONTROL 추가 작업]** 버튼을 사용하면 아래 설명된 작업을 사용할 수 있습니다.

![](../assets/decision_more-actions.png)

* **[!UICONTROL 완료]**: 결정 상태를 로 설정합니다. **[!UICONTROL 완료]**&#x200B;즉, 이 결정을 더 이상 호출할 수 없게 되었습니다. 이 작업은 활성화된 결정에만 사용할 수 있습니다. 결정은 목록에서 계속 사용할 수 있지만 상태를 다시 로 설정할 수는 없습니다 **[!UICONTROL 초안]** 또는 **[!UICONTROL 승인됨]**. 복제, 삭제 또는 보관만 가능합니다.

* **[!UICONTROL 복제]**: 동일한 속성, 결정 범위 및 대체 오퍼로 결정을 만듭니다. 기본적으로 새 결정에는 **[!UICONTROL 초안]** 상태.

* **[!UICONTROL 삭제]**: 목록에서 결정을 제거합니다.

   >[!CAUTION]
   >
   >결정 및 내용은 더 이상 액세스할 수 없습니다. 이 작업은 취소할 수 없습니다.
   >
   >다른 개체에 의사 결정을 사용하면 삭제할 수 없습니다.

* **[!UICONTROL 아카이브]**: 결정 상태를 로 설정합니다. **[!UICONTROL 보관됨]**. 결정은 목록에서 계속 사용할 수 있지만 상태를 다시 로 설정할 수는 없습니다 **[!UICONTROL 초안]** 또는 **[!UICONTROL 승인됨]**. 복제하거나 삭제할 수만 있습니다.

해당 확인란을 선택하여 여러 의사 결정의 상태를 동시에 삭제하거나 변경할 수도 있습니다.

![](../assets/decision_multiple-selection.png)

상태가 다른 여러 결정의 상태를 변경하려면 관련 상태만 변경됩니다.

![](../assets/decision_change-status.png)

결정이 생성되면 목록에서 해당 이름을 클릭할 수 있습니다.

![](../assets/decision_click-name.png)

이를 통해 해당 결정에 대한 자세한 정보에 액세스할 수 있습니다. 을(를) 선택합니다 **[!UICONTROL 변경 로그]** 탭 대상 [모든 변경 사항 모니터링](../get-started/user-interface.md#changes-log) 그것은 그 결정에 의해 이루어졌습니다.

![](../assets/decision_information.png)

## 방법 비디오{#video}

의사 결정 관리에서 오퍼 활동을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


