---
title: 의사 결정 만들기
description: 결정을 만드는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 89e0223ebbf5015b61b55da693e0c6401307ce9f
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 2%

---

# 의사 결정 만들기 {#create-offer-activities}

결정(이전에 오퍼 활동이라고 함)은 게재 대상에 따라 게재할 최상의 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용하는 오퍼용 컨테이너입니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

결정 목록은 **[!UICONTROL Offers]** 메뉴 > **[!UICONTROL Decisions]** 탭에서 액세스할 수 있습니다. 필터를 사용하여 상태 또는 시작 날짜와 종료 날짜에 따라 결정을 검색할 수 있습니다.

![](../../assets/activities-list.png)

결정을 내리기 전에 아래 구성 요소가 오퍼 라이브러리에서 만들어졌는지 확인하십시오.

* [배치](../offer-library/creating-placements.md)
* [컬렉션](../offer-library/creating-collections.md)
* [개인화된 오퍼](../offer-library/creating-personalized-offers.md)
* [대체 오퍼](../offer-library/creating-fallback-offers.md)

## 결정 만들기 {#create-activity}

1. 결정 목록에 액세스한 다음 **[!UICONTROL Create decision]** 을 클릭합니다.

1. 결정 이름을 지정합니다.

1. 시작 및 종료 날짜 및 시간을 정의한 다음 **[!UICONTROL Next]** 을 클릭합니다.

   ![](../../assets/activities-name.png)

## 결정 범위 추가 {#add-decision-scopes}

1. 목록에서 배치를 끌어다 놓아 결정에 추가한 다음 **[!UICONTROL Add collection]** 을 클릭합니다.

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >결정에서 동일한 배치를 여러 번 선택할 수 있습니다.

1. 고려할 오퍼가 포함된 컬렉션을 선택한 다음 **[!UICONTROL Add]** 을 클릭합니다.

   ![](../../assets/activities-collection.png)

1. 선택한 오퍼가 배치에 추가됩니다.

   이 예에서는 오퍼를 콜 센터 솔루션에 제시하기 위해 JSON 유형 배치에 표시되는 두 개의 오퍼를 선택했습니다.

   ![](../../assets/offers-added.png)

1. 기본적으로 이 배치에 여러 오퍼가 적합한 경우 우선 순위가 가장 높은 오퍼가 고객에게 전달됩니다.

   특정 공식 또는 등급 전략을 사용하여 게재할 적합한 오퍼를 선택하려면 **[!UICONTROL Rank offers by]** 드롭다운 목록에서 등급 공식을 선택합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../offer-activities/configure-offer-selection.md)을 참조하십시오.

1. **[!UICONTROL Constraint]** 필드는 이 배치에 대한 오퍼 선택을 제한합니다. 이 제한은 **의사 결정 규칙** 또는 하나 또는 여러 개의 **Adobe Experience Platform 세그먼트**&#x200B;를 사용하여 적용할 수 있습니다. 두 섹션 모두 [이 섹션에 자세히 설명되어 있습니다.](#segments-vs-decision-rules)

   * 오퍼의 선택을 Adobe Experience Platform 세그먼트의 구성원으로만 제한하려면 **[!UICONTROL Segments]** 을 선택하고 **[!UICONTROL Add segments]** 을 클릭합니다.

      ![](../../assets/activity_constraint_segment.png)

      왼쪽 창에서 하나 또는 여러 개의 세그먼트를 추가하고 **[!UICONTROL And]** / **[!UICONTROL Or]** 논리 연산자를 사용하여 조합한 다음 **[!UICONTROL Select]** 를 클릭하여 확인합니다.

      ![](../../assets/activity_constraint_segment2.png)

      [이 섹션](../../segment/about-segments.md)에서 세그먼트를 사용하는 방법에 대해 자세히 알아보십시오.

   * 결정 규칙을 사용하여 이 배치에 대한 선택 제약 조건을 추가하려면 **[!UICONTROL Decision rule]** 옵션을 선택한 다음 왼쪽 창에서 원하는 규칙을 **[!UICONTROL Decision rule]** 영역으로 드래그합니다.

      ![](../../assets/activity_constraint_rule.png)

      [이 섹션](../offer-library/creating-decision-rules.md)에서 의사 결정 규칙을 만드는 방법에 대해 자세히 알아보십시오.

### 세그먼트와 의사 결정 규칙 사용 {#segments-vs-decision-rules}

<!--to move to create-offers?-->

제한을 적용하려면 하나 또는 여러 **Adobe Experience Platform 세그먼트**&#x200B;의 구성원으로 오퍼 선택을 제한하거나, 서로 다른 용도에 해당하는 두 솔루션을 모두 사용하는 **의사 결정 규칙**&#x200B;을 사용할 수 있습니다.

기본적으로 세그먼트의 출력은 프로필 목록이지만, 의사 결정 규칙은 의사 결정 프로세스 동안 단일 프로필에 대해 주문형 실행되는 함수입니다. 그 두 사용법의 차이는 아래에 자세히 나와 있다.

* **세그먼트**

   반면 세그먼트는 프로필 속성 및 경험 이벤트를 기반으로 특정 논리를 일치하는 Adobe Experience Platform 프로필 그룹입니다. 그러나 오퍼 관리 는 세그먼트를 다시 계산하지 않으므로 오퍼를 표시할 때 최신 상태가 아닐 수 있습니다.

   [이 섹션](../../segment/about-segments.md)의 세그먼트에 대해 자세히 알아보십시오.

* **의사 결정 규칙**

   반면, 의사 결정 규칙은 Adobe Experience Platform에서 사용할 수 있는 데이터를 기반으로 하며 오퍼를 표시할 수 있는 사용자를 결정합니다. 오퍼나 지정된 배치에 대한 결정에서 선택하면, 규칙이 결정될 때마다 실행되어 각 프로필은 최신 오퍼와 최상의 오퍼를 얻을 수 있습니다.

   [이 섹션](../offer-library/creating-decision-rules.md)의 의사 결정 규칙에 대해 자세히 알아보십시오.

## 대체 오퍼 추가 {#add-fallback}

오퍼 자격 규칙 및 제약 조건과 일치하지 않는 고객을 위한 마지막 수단으로 표시되는 대체 오퍼를 선택한 다음 **[!UICONTROL Next]** 를 클릭합니다.

![](../../assets/add-fallback-offer.png)

## 결정 검토 및 저장 {#review}

모든 것이 제대로 구성되면 결정 속성의 요약이 표시됩니다.

1. 오퍼를 고객에게 제공하는 데 사용할 준비가 되었는지 확인합니다.
1. **[!UICONTROL Finish]**&#x200B;을(를) 클릭합니다.
1. 그런 다음 **[!UICONTROL Save and activate]** 을 선택합니다.

   ![](../../assets/save-activities.png)

   나중에 편집하고 활성화하기 위해 결정을 초안으로 저장할 수도 있습니다.

이 결정은 이전 단계에서 활성화했는지 여부에 따라 **[!UICONTROL Live]** 또는 **[!UICONTROL Draft]** 상태로 목록에 표시됩니다.

이제 고객에게 오퍼를 전달하는 데 사용할 준비가 되었습니다.

## 의사 결정 목록 {#decision-list}

결정 목록에서 해당 속성을 표시하는 결정을 선택할 수 있습니다. 여기에서 해당 상태를 편집하거나, 해당 상태(**초안**, **라이브**, **완료**, **보관**)를 변경하거나, 결정을 복제하거나, 삭제할 수도 있습니다.

![](../../assets/decision_created.png)

**[!UICONTROL Edit]** 단추를 선택하여 결정 편집 모드로 돌아갑니다. 결정 모드에서 결정의 [세부 정보](#create-activity), [결정 범위](#add-decision-scopes) 및 [대체 오퍼](#add-fallback)를 수정할 수 있습니다.

라이브 결정을 선택하고 **[!UICONTROL Deactivate]** 을 클릭하여 결정 상태를 다시 **[!UICONTROL Draft]** 로 설정합니다.

상태를 **[!UICONTROL Live]**(으)로 다시 설정하려면 이제 표시되는 **[!UICONTROL Activate]** 단추를 선택하십시오.

![](../../assets/decision_activate.png)

**[!UICONTROL More actions]** 단추를 사용하면 아래 설명된 작업이 활성화됩니다.

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: 결정 상태를 로 설정합니다.  **[!UICONTROL Complete]**&#x200B;즉, 더 이상 결정을 호출할 수 없습니다. 이 작업은 활성화된 결정에만 사용할 수 있습니다. 이 결정은 목록에서 계속 사용할 수 있지만 상태를 다시 **[!UICONTROL Draft]** 또는 **[!UICONTROL Approved]** 로 설정할 수 없습니다. 복제, 삭제 또는 보관만 가능합니다.

* **[!UICONTROL Duplicate]**: 동일한 속성, 결정 범위 및 대체 오퍼로 결정을 만듭니다. 기본적으로 새 결정은 **[!UICONTROL Draft]** 상태입니다.

* **[!UICONTROL Delete]**: 목록에서 결정을 제거합니다.

   >[!CAUTION]
   >
   >결정 및 내용은 더 이상 액세스할 수 없습니다. 이 작업은 취소할 수 없습니다.
   >
   >다른 개체에 의사 결정을 사용하면 삭제할 수 없습니다.

* **[!UICONTROL Archive]**: 결정 상태를 로 설정합니다  **[!UICONTROL Archived]**. 이 결정은 목록에서 계속 사용할 수 있지만 상태를 다시 **[!UICONTROL Draft]** 또는 **[!UICONTROL Approved]** 로 설정할 수 없습니다. 복제하거나 삭제할 수만 있습니다.

해당 확인란을 선택하여 여러 의사 결정의 상태를 동시에 삭제하거나 변경할 수도 있습니다.

![](../../assets/decision_multiple-selection.png)

상태가 다른 여러 결정의 상태를 변경하려면 관련 상태만 변경됩니다.

![](../../assets/decision_change-status.png)

결정이 생성되면 목록에서 해당 이름을 클릭할 수 있습니다.

![](../../assets/decision_click-name.png)

이를 통해 해당 결정에 대한 자세한 정보에 액세스할 수 있습니다. **[!UICONTROL Change log]** 탭을 선택하여 결정에 수행된 모든 변경 사항](../get-started/user-interface.md#changes-log)을 모니터링합니다.[

![](../../assets/decision_information.png)

## 튜토리얼 비디오 {#video}

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform을 기반으로 하는 Offer decisioning 애플리케이션 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하는 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
