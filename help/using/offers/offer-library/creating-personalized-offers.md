---
title: 개인화된 오퍼 만들기
description: 오퍼를 만들고, 구성하고, 관리하는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 55d9befff9b9bf1bc81c6553cd76f015fdd3116e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 3%

---

# 개인화된 오퍼 만들기 {#create-personalized-offers}

오퍼를 만들기 전에 다음을 만들었는지 확인하십시오.

* A **배치** 오퍼가 표시되는 위치입니다. 자세한 내용은 [배치 만들기](../offer-library/creating-placements.md)
* 자격 조건을 추가하려면 a **의사 결정 규칙** 이 경우 오퍼가 표시될 조건을 정의합니다. 자세한 내용은 [의사 결정 규칙 만들기](../offer-library/creating-decision-rules.md).
* 하나 또는 여러 개 **태그** 오퍼와 연결할 수 있습니다. 자세한 내용은 [태그 만들기](../offer-library/creating-tags.md).

➡️ [비디오에서 이 기능 살펴보기](#video)

개인화된 오퍼 목록은 **[!UICONTROL Offers]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](../assets/offers_list.png)

## 오퍼 만들기 {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="오퍼 속성 기본 정보"
>abstract="오퍼 속성을 사용하여 보고 및 분석을 위해 키 값 쌍을 오퍼와 연결할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="오퍼 속성"
>abstract="오퍼 속성을 사용하여 보고 및 분석을 위해 키 값 쌍을 오퍼와 연결할 수 있습니다."

을(를) 만들려면 **오퍼**&#x200B;다음 단계를 수행합니다.

1. 클릭 **[!UICONTROL Create offer]**&#x200B;를 선택하고 을 선택합니다. **[!UICONTROL Personalized offer]**.

   ![](../assets/create_offer.png)

1. 오퍼의 이름과 시작 및 종료 날짜 및 시간을 지정합니다. 이 날짜 외에도 Decisioning 엔진에서 오퍼를 선택하지 않습니다.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >시작/종료 날짜를 업데이트하면 최대 가용성에 영향을 줄 수 있습니다. [자세히 보기](add-constraints.md#capping-change-date)

1. 하나 또는 여러 개의 기존 항목을 연결할 수도 있습니다 **[!UICONTROL tags]** 오퍼 라이브러리를 보다 쉽게 검색하고 구성할 수 있도록 오퍼에 매핑합니다. [자세히 알아보기](creating-tags.md).

1. 다음 **[!UICONTROL Offer attributes]** 섹션에서 보고 및 분석 목적으로 키-값 쌍을 오퍼와 연결할 수 있습니다.

1. 표현을 추가하여 오퍼가 메시지에 표시되는 위치를 정의합니다. [자세히 보기](add-representations.md)

   ![](../assets/channel-placement.png)

1. 표시할 오퍼에 대한 조건을 설정하려면 제약조건을 추가하십시오. [자세히 보기](add-constraints.md)

   >[!NOTE]
   >
   >세그먼트나 결정 규칙을 선택하면 예상 자격을 갖춘 프로필에 대한 정보를 볼 수 있습니다. 클릭 **[!UICONTROL Refresh]** 를 눌러 데이터를 업데이트합니다.
   >
   >규칙 매개 변수에 컨텍스트 데이터 등의 프로필에 없는 데이터가 포함된 경우 프로필 예측을 사용할 수 없습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 자격 규칙입니다.

   ![](../assets/offer-constraints-example.png)

1. 오퍼를 검토하고 저장합니다. [자세히 보기](#review)

## 오퍼 검토 {#review}

자격 규칙 및 제한이 정의되면 오퍼 속성 요약이 표시됩니다.

1. 모든 것이 제대로 구성되어 있는지 확인하십시오.

1. 예상 자격을 갖춘 프로필에 대한 정보를 표시할 수 있습니다. 클릭 **[!UICONTROL Refresh]** 를 눌러 데이터를 업데이트합니다.

   ![](../assets/offer-summary-estimate.png)

1. 사용자에게 오퍼를 제공할 준비가 되면 **[!UICONTROL Finish]**.

1. **[!UICONTROL Save and approve]**&#x200B;를 선택합니다.

   ![](../assets/offer_review.png)

   나중에 편집하고 승인하기 위해 오퍼를 초안으로 저장할 수도 있습니다.

오퍼가 목록에 **[!UICONTROL Approved]** 또는 **[!UICONTROL Draft]** 상태(이전 단계에서 승인했는지 여부에 따라 다름).

이제 사용자에게 전달할 준비가 되었습니다.

![](../assets/offer_created.png)

## 오퍼 관리 {#offer-list}

오퍼 목록에서 해당 속성을 표시할 오퍼를 선택할 수 있습니다. 편집, 상태 변경(**초안**, **승인됨**, **보관됨**), 오퍼를 복제하거나, 삭제합니다.

![](../assets/offer_created.png)

을(를) 선택합니다 **[!UICONTROL Edit]** 버튼을 클릭하여 오퍼를 수정할 수 있는 오퍼 편집 모드로 돌아갑니다. [세부 정보](#create-offer), [표현](#representations)를 편집할 수 있습니다 [자격 규칙 및 제한](#eligibility).

승인된 오퍼를 선택하고 을(를) 클릭합니다 **[!UICONTROL Undo approve]** 오퍼 상태를 다시 로 설정하려면 **[!UICONTROL Draft]**.

상태를 다시 설정하려면 **[!UICONTROL Approved]**&#x200B;에서 이제 표시되는 해당 버튼을 선택합니다.

![](../assets/offer_approve.png)

다음 **[!UICONTROL More actions]** 버튼을 사용하면 아래 설명된 작업을 사용할 수 있습니다.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: 등록 정보, 표현, 자격 규칙 및 제약 조건이 동일한 오퍼를 생성합니다. 기본적으로 새 오퍼에는 **[!UICONTROL Draft]** 상태.
* **[!UICONTROL Delete]**: 목록에서 오퍼를 제거합니다.

   >[!CAUTION]
   >
   >오퍼와 해당 콘텐츠는 더 이상 액세스할 수 없습니다. 이 작업은 취소할 수 없습니다.
   >
   >오퍼가 컬렉션이나 결정에 사용되는 경우 삭제할 수 없습니다. 먼저 모든 개체에서 오퍼를 제거해야 합니다.

* **[!UICONTROL Archive]**: 오퍼 상태를 로 설정합니다. **[!UICONTROL Archived]**. 오퍼는 여전히 목록에서 사용할 수 있지만 상태를 다시 로 설정할 수 없습니다 **[!UICONTROL Draft]** 또는 **[!UICONTROL Approved]**. 복제하거나 삭제할 수만 있습니다.

해당 확인란을 선택하여 여러 오퍼의 상태를 동시에 삭제하거나 변경할 수도 있습니다.

![](../assets/offer_multiple-selection.png)

상태가 다른 여러 오퍼의 상태를 변경하려면 관련 상태만 변경됩니다.

![](../assets/offer_change-status.png)

오퍼가 만들어지면 목록에서 해당 이름을 클릭할 수 있습니다.

![](../assets/offer_click-name.png)

이렇게 하면 해당 오퍼에 대한 세부 정보에 액세스할 수 있습니다. 을(를) 선택합니다 **[!UICONTROL Change log]** 탭 대상 [모든 변경 사항 모니터링](../get-started/user-interface.md#monitoring-changes) 그것은 그 제의에 대한 것입니다.

![](../assets/offer_information.png)

## 튜토리얼 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
