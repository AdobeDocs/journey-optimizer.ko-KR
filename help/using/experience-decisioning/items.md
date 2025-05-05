---
title: 결정 항목
description: 의사 결정 항목으로 작업하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: ab70ce5b686a54dc1be7336411c5b0959fc3c584
workflow-type: tm+mt
source-wordcount: '1752'
ht-degree: 15%

---

# 첫 결정 항목 만들기 {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="결정 항목 관리"
>abstract="Journey Optimizer를 사용하면 결정 항목이라고 하는 마케팅 오퍼를 생성하여 중앙 집중식 카탈로그 및 컬렉션으로 구성할 수 있습니다. 현재 생성된 모든 결정 항목은 단일 “오퍼” 카탈로그 내에 통합되어 있습니다. 이 화면에서 **스키마 편집** 버튼을 사용하여 카탈로그의 스키마에 액세스하고 결정 항목에 대한 사용자 정의 속성을 생성할 수도 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/decision-items/catalogs.html?lang=ko" text="항목 카탈로그 구성"

Journey Optimizer를 사용하면 결정 항목이라고 하는 마케팅 오퍼를 생성하여 중앙 집중식 카탈로그 및 컬렉션으로 구성할 수 있습니다. 요구 사항에 맞게 정확하게 조정할 수 있도록 설계된 표준 및 사용자 지정 속성으로 구성됩니다. 또한 의사 결정 항목을 표시할 대상을 정의할 수 있는 프로필 제약 조건을 통합합니다.

결정 항목을 만들기 전에 결정 항목을 표시할 수 있는 대상을 결정하는 조건을 설정하려면 **결정 규칙**&#x200B;을 만들었는지 확인하십시오. [의사 결정 규칙을 만드는 방법을 알아봅니다](rules.md).

의사 결정 항목을 만들려면 **[!UICONTROL 의사 결정]** > **[!UICONTROL 카탈로그]**(으)로 이동한 다음 **[!UICONTROL 항목 만들기]**&#x200B;를 클릭하고 아래 섹션에 설명된 단계를 따릅니다.

## 결정 항목의 속성 정의 {#attributes}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="결정 항목의 우선순위 정의"
>abstract="프로필이 여러 항목에 적합한 경우 우선순위를 통해 이 결정 항목을 다른 항목과 비교할 수 있습니다. 우선순위가 높을수록 해당 항목이 다른 항목보다 우선적으로 적용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="사용자 정의 속성 정의"
>abstract="사용자 정의 속성은 결정 항목에 할당할 수 있으며 필요에 맞게 조정된 특정 속성입니다. 이는 결정 항목의 카탈로그 스키마에 생성됩니다. 이 섹션은 카탈로그 스키마에 하나 이상의 사용자 정의 속성을 추가한 경우에만 표시됩니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/decision-items/catalogs.html?lang=ko" text="항목 카탈로그 구성"

먼저 의사 결정 항목의 표준 및 사용자 지정 속성 을 정의합니다.

![](assets/item-attributes.png)

1. 이름과 설명을 입력합니다.
1. 시작 및 종료 날짜를 지정합니다. 이 항목은 이 날짜 내에 의사 결정 엔진에서만 고려됩니다.
1. 프로필이 여러 항목에 적합한 경우 결정 항목의 **[!UICONTROL 우선 순위]**&#x200B;를 다른 항목과 비교하여 설정하십시오. 우선순위가 높을수록 해당 항목이 다른 항목보다 우선적으로 적용됩니다.

   >[!NOTE]
   >
   >우선 순위는 정수 데이터 형식입니다. 정수 데이터 유형인 모든 속성에는 정수 값(소수점 없음)이 포함되어야 합니다.

1. **태그** 필드를 사용하면 Adobe Experience Platform 통합 태그를 의사 결정 항목에 할당할 수 있습니다. 이를 통해 손쉽게 분류하고 검색을 개선할 수 있습니다. [태그 작업 방법 알아보기](../start/search-filter-categorize.md#tags)

1. 사용자 지정 특성을 지정합니다(선택 사항). 사용자 정의 속성은 결정 항목에 할당할 수 있으며 필요에 맞게 조정된 특정 속성입니다. 의사 결정 항목의 카탈로그 스키마에 정의됩니다. [카탈로그 작업 방법 알아보기](catalogs.md)

1. 결정 항목의 특성이 정의되면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

## 결정 항목의 적격성 구성 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="대상자 또는 의사 결정 규칙 추가"
>abstract="기본적으로 모든 프로필은 결정 항목을 수신할 수 있지만 대상자 또는 규칙을 사용하여 항목을 특정 프로필로만 제한할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=ko" text="대상자 사용"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/selection/rules.html?lang=ko" text="의사 결정 규칙 사용"

기본적으로 모든 프로필은 의사 결정 항목을 받을 수 있지만, 대상자 또는 규칙을 사용하여 항목을 특정 프로필로만 제한할 수 있습니다. 두 솔루션은 서로 다른 사용법에 해당합니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

+++대상과 의사 결정 규칙 사용

기본적으로 대상자의 출력은 프로필 목록이지만 의사 결정 규칙은 의사 결정 프로세스 동안 단일 프로필에 대해 온디맨드로 실행되는 함수입니다.

* **대상**: 한편으로 대상은 프로필 특성 및 경험 이벤트를 기반으로 특정 논리와 일치하는 Adobe Experience Platform 프로필 그룹입니다. 그러나 오퍼 관리에서는 대상을 다시 계산하지 않습니다. 오퍼를 표시할 때 최신이 아닐 수 있습니다.

* **의사 결정 규칙**: 한편 의사 결정 규칙은 Adobe Experience Platform에서 사용 가능한 데이터를 기반으로 하며 오퍼를 표시할 대상을 결정합니다. 오퍼 또는 주어진 배치에 대한 의사 결정에서 선택되면 의사 결정이 내려질 때마다 규칙이 실행되어 각 프로필이 최신 오퍼와 최상의 오퍼를 얻도록 합니다.

+++

* 하나 이상의 Adobe Experience Platform 대상의 구성원으로 결정 항목을 표시하려면 **[!UICONTROL 하나 이상의 대상에 속하는 방문자]** 옵션을 선택한 다음 왼쪽 창에서 하나 이상의 대상을 추가하고 **[!UICONTROL And]** / **[!UICONTROL Or]** 논리 연산자를 사용하여 대상을 결합하십시오. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md).

* 특정 결정 규칙을 결정 항목에 연결하려면 **[!UICONTROL 규칙별]**&#x200B;을 선택한 다음 왼쪽 창에서 원하는 규칙을 중앙 영역으로 끕니다. [의사 결정 규칙에 대해 자세히 알아보세요](rules.md).

![](assets/item-constraints.png)

대상자 또는 의사 결정 규칙을 선택하면 예상 적격 프로필에 대한 정보를 볼 수 있습니다. 데이터를 업데이트하려면 **[!UICONTROL 새로 고침]**&#x200B;을 클릭하세요.

>[!NOTE]
>
>규칙 매개 변수에 컨텍스트 데이터와 같이 프로필에 없는 데이터가 포함되어 있으면 프로필 추정치를 사용할 수 없습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 자격 규칙이 있습니다.

## 최대 가용량 규칙 설정 {#capping}

한도는 오퍼를 표시할 수 있는 최대 횟수를 정의하는 제약 조건으로 사용됩니다. 사용자가 특정 오퍼를 받는 횟수를 제한하면 고객에게 과다 청탁을 하지 않고 최상의 오퍼로 각 접점을 최적화할 수 있습니다. 특정 결정 항목에 대해 최대 10개의 캡션을 만들 수 있습니다.

![](assets/item-capping.png)

>[!NOTE]
>
>
>최대 가용량 카운터 값은 업데이트하는 데 최대 3초가 걸릴 수 있습니다. 예를 들어 웹 사이트에 오퍼를 표시하는 웹 배너를 표시한다고 가정해 보겠습니다. 주어진 사용자가 3초 이내에 웹 사이트의 다음 페이지로 이동하면 해당 사용자에 대해 카운터 값이 증가하지 않습니다.

결정 항목에 대한 최대 가용량 규칙을 설정하려면 **[!UICONTROL 최대 가용량 만들기]** 단추를 클릭한 다음 다음 단계를 수행합니다.

1. 카운터를 늘리기 위해 고려할 **[!UICONTROL Capping 이벤트]**&#x200B;를 정의합니다.

   * **[!UICONTROL 결정 이벤트]**(기본값): 오퍼를 표시할 수 있는 최대 횟수입니다.
   * **[!UICONTROL 노출]**(인바운드 채널만): 사용자에게 오퍼를 표시할 수 있는 최대 횟수입니다.
   * **[!UICONTROL 클릭 수]**: 사용자가 결정 항목을 클릭할 수 있는 최대 횟수입니다.
   * **[!UICONTROL 사용자 지정 이벤트]**: 항목 전송 횟수를 제한하는 데 사용할 사용자 지정 이벤트를 정의할 수 있습니다. 예를 들어 환매가 10000 때까지 또는 주어진 프로필이 1회 환매될 때까지 환매 수를 제한할 수 있습니다. 이렇게 하려면 [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"} 스키마를 사용하여 사용자 지정 이벤트 규칙을 만듭니다.

   >[!NOTE]
   >
   >의사 결정 이벤트를 제외한 모든 최대 가용량 이벤트에 대해 의사 결정 관리 피드백이 자동으로 수집되지 않을 수 있으므로 최대 가용량 카운터가 올바르게 증가하지 않을 수 있습니다. 각 최대 가용량 이벤트가 최대 가용량 카운터에서 추적 및 처리되도록 하려면 경험 이벤트를 수집하는 데 사용되는 스키마에 해당 이벤트에 대한 올바른 필드 그룹이 포함되어 있는지 확인하십시오. 데이터 수집에 대한 자세한 내용은 Journey Optimizer 의사 결정 관리 설명서에서 확인할 수 있습니다.
   >* [의사 결정 관리 데이터 수집](../offers/data-collection/data-collection.md)
   >* [데이터 수집 구성](../offers/data-collection/schema-requirement.md)

1. 한도 유형을 선택합니다.

   * **[!UICONTROL 총]**&#x200B;을(를) 선택하여 모든 사용자를 의미하는 결합된 대상 대상에서 항목을 제안할 수 있는 횟수를 정의합니다. 예를 들어, 전자 제품 retailer에 &#39;TV 초보자용 거래&#39;가 있는 경우 모든 프로필에서 오퍼가 200배만 반환되기를 원합니다.

   * 동일한 사용자에게 오퍼를 제안할 수 있는 횟수를 정의하려면 **[!UICONTROL 프로필당]**&#x200B;을(를) 선택하십시오. 예를 들어 &#39;플래티넘 신용카드&#39; 오퍼가 있는 은행인 경우 이 오퍼가 프로필당 5회 이상 표시되지 않도록 할 수 있습니다. 실제로, 사용자가 오퍼를 5번 보고 실행하지 않은 경우 다음 최상의 오퍼에 대해 조치를 취할 수 있는 기회가 더 높다고 판단합니다.

1. **[!UICONTROL 최대 가용량 제한]** 필드에서 선택한 최대 가용량 유형에 따라 모든 사용자에게 또는 프로필별로 오퍼를 표시할 수 있는 횟수를 지정합니다. 숫자는 0보다 큰 정수여야 합니다.

   예를 들어, 체크아웃 수를 고려하는 사용자 정의 캡핑 이벤트를 정의했습니다. **[!UICONTROL 최대 개수 제한]** 필드에 10을 입력하면 10회 체크아웃 후에는 더 이상 오퍼가 전송되지 않습니다.

1. **[!UICONTROL 최대 가용량 다시 설정]** 드롭다운 목록에서 최대 가용량 카운터가 다시 설정되는 빈도를 설정하십시오. 이렇게 하려면 계산 기간(일별, 주별 또는 월별)을 정의하고 선택한 일/주/개월을 입력합니다. 예를 들어 2주마다 최대 가용량 수를 재설정하려면 해당 드롭다운 목록에서 **[!UICONTROL 주별]**&#x200B;을 선택하고 다른 필드에 **2**&#x200B;을(를) 입력하십시오.

   >[!NOTE]
   >
   >빈도 제한 카운터 재설정은 **오전 12시(UTC**)에, 정의한 날이나 해당되는 경우 주/월의 첫 날에 수행됩니다. 주 시작일은 **일요일**&#x200B;입니다. 선택한 기간은 **2년**(즉, 해당 개월, 주 또는 일 수)을 초과할 수 없습니다.
   >
   >결정 항목을 게시한 후에는 빈도에 대해 선택한 기간(월별, 주별 또는 일별)을 변경할 수 없습니다. 항목이 **[!UICONTROL 초안]** 상태이고 이전에 게시되지 않았으며 빈도 설정이 활성화된 경우에도 빈도 설정을 편집할 수 있습니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하여 최대 가용량 규칙 만들기를 확인합니다. 단일 결정 항목에 대해 최대 10개의 규칙을 만들 수 있습니다. 이렇게 하려면 **[!UICONTROL 최대 가용량 만들기]** 단추를 클릭하고 위의 단계를 반복합니다.

   ![](assets/item-capping-rules.png)

1. 결정 항목의 자격 및 최대 가용량 규칙이 정의되면 **[!UICONTROL 다음]**&#x200B;을 클릭하여 항목을 검토하고 저장합니다.

1. 이제 결정 항목이 **[!UICONTROL 초안]** 상태로 목록에 나타납니다. 프로필을 표시할 준비가 되면 줄임표 버튼을 클릭하고 **[!UICONTROL 승인]**&#x200B;을 선택합니다.

   ![](assets/item-approve.png)

<!--* Identifying how many times a given customer has been shown a decision item. 
If a marketer wants to determine how many times a specific customer has been shown an offer, they can do that. Go to Profiles menu, Attributes tab. You'll see all counter values. The alphanumeric string is associated to the offer. To make the map, go to an item, in the URL check the last alphanumeric strings. D stands for day, w stands for week, m for month. "Ce" custom event-->

## 결정 항목 관리 {#manage}

결정 항목 목록에서 결정 항목을 편집하거나, 상태(**초안**, **승인됨**, **보관됨**)를 변경하거나, 복제하거나 삭제할 수 있습니다.

결정 항목을 수정하려면 해당 결정 항목을 열고 수정한 후 저장합니다.

결정 항목을 선택하거나 줄임표 버튼을 클릭하면 아래에 설명된 작업이 활성화됩니다.

* **[!UICONTROL 승인]**: 결정 항목의 상태를 승인됨으로 설정합니다.
* **[!UICONTROL 승인 실행 취소]**: 결정 항목의 상태를 **[!UICONTROL 초안]**(으)로 다시 설정합니다.
* **[!UICONTROL 중복]**: 특성과 제약 조건이 동일한 결정 항목을 만듭니다. 기본적으로 새 항목은 **[!UICONTROL 초안]** 상태입니다.
* **[!UICONTROL 삭제]**: 목록에서 결정 항목을 제거합니다.

  >[!IMPORTANT]
  >
  >삭제하면 결정 항목과 해당 콘텐츠에 더 이상 액세스할 수 없습니다. 이 작업은 취소할 수 없습니다.

  승인된 오퍼 항목은 컬렉션이나 의사 결정에 사용되는 경우 삭제할 수 없습니다. 삭제하려면 상태를 &quot;초안&quot;으로 변경하십시오. 이렇게 하려면 줄임표 버튼을 클릭하고 **[!UICONTROL 승인 취소]**&#x200B;를 선택하십시오.

  ![](assets/item-undo.png)

* **[!UICONTROL 보관]**: 결정 항목 상태를 **[!UICONTROL 보관]**(으)로 설정합니다. 결정 항목은 여전히 목록에서 사용할 수 있지만 상태를 **[!UICONTROL 초안]** 또는 **[!UICONTROL 승인됨]**(으)로 다시 설정할 수 없습니다. 복제하거나 삭제할 수만 있습니다.
