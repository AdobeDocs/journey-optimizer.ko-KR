---
title: 의사 결정 만들기
description: 의사 결정을 내리는 방법 학습
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 3%

---

# 결정 만들기 {#create-offer-activities}

의사 결정(이전의 오퍼 활동이라고 함)은 전달 대상에 따라 가장 잘 전달할 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용하는 오퍼용 컨테이너입니다.

![](../../assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

결정 목록은 **[!UICONTROL Offers]** 메뉴 / **[!UICONTROL Decisions]** 탭에서 액세스할 수 있습니다. 필터는 상태 또는 시작 날짜와 종료 날짜에 따라 결정을 가져오는 데 도움이 됩니다.

![](../../assets/activities-list.png)

결정을 만들기 전에 아래 구성 요소가 오퍼 라이브러리에 만들어졌는지 확인하십시오.

* [배치](../offer-library/creating-placements.md),
* [컬렉션](../offer-library/creating-collections.md),
* [개인화된 오퍼](../offer-library/creating-personalized-offers.md),
* [대체 오퍼](../offer-library/creating-fallback-offers.md).

## 결정 만들기 {#create-activity}

1. 결정 목록에 액세스한 다음 **[!UICONTROL Create activity]**&#x200B;을 클릭합니다.

1. 결정 이름, 시작 날짜 및 종료 날짜 및 시간을 지정하고 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   ![](../../assets/activities-name.png)

## 결정 추가 {#add-decisions}

1. 목록에서 배치를 드래그하여 놓아 의사 결정에 추가한 다음 **[!UICONTROL Add collection]**&#x200B;을 클릭합니다.

   ![](../../assets/activities-placement.png)

1. 고려할 오퍼가 포함된 컬렉션을 선택한 다음 **[!UICONTROL Add]**&#x200B;을 클릭합니다.

   ![](../../assets/activities-collection.png)

1. 선택한 오퍼가 배치에 추가됩니다. 이 예에서는 오퍼를 콜 센터 솔루션에 제시하기 위해 JSON 유형 배치에 표시되는 2개의 오퍼를 선택했습니다.

   ![](../../assets/offers-added.png)

1. 기본적으로 여러 오퍼가 이 배치에 적합하면 우선 순위가 가장 높은 오퍼가 고객에게 전달됩니다.

   특정 공식을 사용하여 전달할 적합한 오퍼를 선택하려면 **[!UICONTROL Rank offers by]** 드롭다운 목록에서 등급 공식을 선택합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../offer-activities/configure-offer-selection.md)을 참조하십시오.

1. **[!UICONTROL Constraint]** 필드는 이 배치에 대한 오퍼 선택을 제한합니다. 이 제약 조건은 결정 규칙 또는 하나 또는 여러 Adobe Experience Platform 세그먼트를 사용하여 적용할 수 있습니다.

   Adobe Experience Platform 세그먼트 멤버에 대한 오퍼 선택을 제한하려면 **[!UICONTROL Segments]**&#x200B;을 선택하고 **[!UICONTROL Add segments]**&#x200B;을 클릭합니다.

   ![](../../assets/activity_constraint_segment.png)

   왼쪽 창에서 하나 이상의 세그먼트를 추가하고 **[!UICONTROL And]** / **[!UICONTROL Or]** 논리 연산자를 사용하여 조합한 다음 **[!UICONTROL Select]**&#x200B;를 클릭하여 확인합니다.

   세그먼트 작업 방법에 대한 자세한 내용은 [세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)를 참조하십시오.

   ![](../../assets/activity_constraint_segment2.png)

   결정 규칙을 사용하여 이 배치에 대한 선택 제한을 추가하려면 **[!UICONTROL Decision rule]** 옵션을 선택한 다음 왼쪽 창에서 원하는 규칙을 **[!UICONTROL Decision rule]** 영역으로 드래그합니다. 결정 규칙을 만드는 방법에 대한 자세한 내용은 [이 섹션](../offer-library/creating-decision-rules.md)을 참조하십시오.

   ![](../../assets/activity_constraint_rule.png)

## 대체 오퍼 {#add-fallback} 추가

오퍼 자격 규칙 및 제약 조건과 일치하지 않는 고객을 위한 마지막 수단으로 사용할 대체 오퍼를 선택한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

![](../../assets/add-fallback-offer.png)

## 결정 사항 {#review} 검토 및 저장

모든 것이 올바르게 구성되고 고객에게 오퍼를 제공하는 데 사용자의 결정이 사용될 준비가 되었으면 **[!UICONTROL Finish]**&#x200B;을 클릭한 다음 **[!UICONTROL Save and activate]**&#x200B;을 선택합니다.

나중에 의사 결정을 편집하고 활성화하기 위해 초안을 저장할 수도 있습니다.

![](../../assets/save-activities.png)

이전 단계에서 활성화했는지 여부에 따라 목록에 **[!UICONTROL Live]** 또는 **[!UICONTROL Draft]** 상태가 표시됩니다.

이제 고객에게 제안을 전달하는 데 사용할 준비가 되었습니다. 속성을 표시하고 속성을 편집하거나 제외하도록 선택할 수 있습니다.

오퍼에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [메시지에 개인화된 오퍼 추가](../../deliver-personalized-offers.md)
* [API를 사용하여 오퍼 제공](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>결정이 생성되면 목록에서 해당 이름을 클릭하여 자세한 정보에 액세스할 수 있으며 **[!UICONTROL Change log]** 탭을 사용하여 모든 변경 사항을 확인할 수 있습니다([오퍼 및 결정 변경 로그](../get-started/user-interface.md#changes-log) 참조).

## 자습서 비디오 {#video}

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform 기반으로 구축된 Offer decisioning 응용 프로그램 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하기 위한 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
