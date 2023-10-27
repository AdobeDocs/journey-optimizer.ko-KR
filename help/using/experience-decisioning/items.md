---
title: 결정 항목
description: 의사 결정 항목으로 작업하는 방법을 알아봅니다.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 33%

---

# 결정 항목 {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="결정 항목 관리"
>abstract="Journey Optimizer를 사용하면 결정 항목이라고 하는 마케팅 오퍼를 생성하여 중앙 집중식 카탈로그 및 컬렉션으로 구성할 수 있습니다. 현재 생성된 모든 결정 항목은 단일 “오퍼” 카탈로그 내에 통합되어 있습니다. 이 화면에서 **스키마 편집** 버튼을 사용하여 카탈로그의 스키마에 액세스하고 결정 항목에 대한 사용자 정의 속성을 생성할 수도 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="항목 카탈로그 구성"

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 결정 항목 관리
   * [항목 카탈로그 구성](catalogs.md)
   * **[결정 항목 만들기](items.md)**
   * [항목 컬렉션 관리](collections.md)
* 항목 선택 구성
   * [의사 결정 규칙 만들기](rules.md)
   * [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

Journey Optimizer를 사용하면 결정 항목이라고 하는 마케팅 오퍼를 생성하여 중앙 집중식 카탈로그 및 컬렉션으로 구성할 수 있습니다. 요구 사항에 맞게 정확하게 조정할 수 있도록 설계된 표준 및 맞춤형 특성으로 구성됩니다. 또한 의사 결정 항목을 표시할 대상을 정의할 수 있는 프로필 제약 조건을 통합합니다.

의사 결정 항목을 만들기 전에 **결정 규칙** 결정 항목을 표시할 대상을 결정하는 조건을 설정하려면 를 선택합니다. [의사 결정 규칙을 만드는 방법을 알아봅니다](rules.md).

## 첫 번째 결정 항목 만들기

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="결정 항목의 우선 순위 정의"
>abstract="프로필이 여러 항목에 적합한 경우 우선 순위를 통해 이 결정 항목을 다른 항목과 비교할 수 있습니다. 우선 순위가 높을수록 해당 항목이 다른 항목보다 우선적으로 적용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="사용자 정의 속성 정의"
>abstract="사용자 정의 속성은 결정 항목에 할당할 수 있으며 필요에 맞게 조정된 특정 속성입니다. 이는 결정 항목의 카탈로그 스키마에 생성됩니다. 이 섹션은 카탈로그 스키마에 하나 이상의 사용자 정의 속성을 추가한 경우에만 표시됩니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="항목 카탈로그 구성"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="대상자 또는 의사 결정 규칙 추가"
>abstract="기본적으로 모든 프로필은 결정 항목을 수신할 수 있지만, 대상자 또는 규칙을 사용하여 항목을 특정 프로필로만 제한할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="대상자 사용"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="의사 결정 규칙 사용"

의사 결정 항목을 만들려면 다음 단계를 수행합니다.

1. 다음으로 이동 **[!UICONTROL 경험 의사 결정]** > **[!UICONTROL 항목]**.

1. 결정 항목의 표준 속성을 정의합니다.

   1. 이름과 설명을 입력합니다.
   1. 시작 및 종료 날짜를 지정합니다. 이 항목은 이 날짜 내에 의사 결정 엔진에서만 고려됩니다.
   1. 설정 **[!UICONTROL 우선 순위]** 프로필이 여러 항목에 적합한 경우 다른 항목과 비교하여 결정 항목. 우선 순위가 높을수록 해당 항목이 다른 항목보다 우선적으로 적용됩니다.

   ![](assets/item-attributes.png)

1. 사용자 정의 속성은 결정 항목에 할당할 수 있으며 필요에 맞게 조정된 특정 속성입니다. 의사 결정 항목의 카탈로그 스키마에 정의됩니다. [카탈로그 작업 방법 알아보기](catalogs.md)

1. 결정 항목의 속성이 정의되면 다음을 클릭합니다. **[!UICONTROL 다음]** 항목에 대한 프로파일 제약조건을 설정합니다.

   기본적으로 모든 프로필은 의사 결정 항목을 받을 수 있지만, 대상자 또는 규칙을 사용하여 항목을 특정 프로필로만 제한할 수 있습니다. 두 솔루션은 서로 다른 사용법에 해당합니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

   +++대상과 의사 결정 규칙 사용

   기본적으로 대상자의 출력은 프로필 목록이지만 의사 결정 규칙은 의사 결정 프로세스 동안 단일 프로필에 대해 온디맨드로 실행되는 함수입니다.

   * **대상**: 한 편으로는 대상자가 프로필 속성 및 경험 이벤트를 기반으로 특정 논리와 일치하는 Adobe Experience Platform 프로필 그룹입니다. 그러나 오퍼 관리에서는 대상을 다시 계산하지 않습니다. 오퍼를 표시할 때 최신이 아닐 수 있습니다.

   * **의사 결정 규칙**: 반면 의사 결정 규칙은 Adobe Experience Platform에서 사용할 수 있는 데이터를 기반으로 하며 오퍼를 표시할 수 있는 사용자를 결정합니다. 오퍼 또는 주어진 배치에 대한 의사 결정에서 선택되면 의사 결정이 내려질 때마다 규칙이 실행되어 각 프로필이 최신 오퍼와 최상의 오퍼를 얻도록 합니다.

+++

   ![](assets/item-constraints.png)

   * 결정 항목을 하나 또는 여러 Adobe Experience Platform 대상의 구성원으로 제한하려면 다음을 선택합니다. **[!UICONTROL 하나 또는 여러 대상에 속하는 방문자]** 옵션을 선택한 다음 왼쪽 창에서 하나 또는 여러 대상자를 추가하고 **[!UICONTROL 및]** / **[!UICONTROL 또는]** 논리 연산자. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md).

   * 특정 결정 규칙을 결정 항목에 연결하려면 다음을 선택합니다. **[!UICONTROL 규칙별]**&#x200B;을 클릭한 다음 왼쪽 창에서 중앙 영역으로 원하는 규칙을 드래그합니다. [의사 결정 규칙에 대해 자세히 알아보기](rules.md).

   대상자 또는 결정 규칙을 선택하면 예상 적격 프로필에 대한 정보를 볼 수 있습니다. 클릭 **[!UICONTROL 새로 고침]** 을 클릭하여 데이터를 업데이트합니다.

   >[!NOTE]
   >
   >규칙 매개 변수에 컨텍스트 데이터와 같이 프로필에 없는 데이터가 포함되어 있으면 프로필 추정치를 사용할 수 없습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 자격 규칙이 있습니다.

1. 결정 항목의 제약 조건이 정의되면 **[!UICONTROL 다음]** 를 클릭하여 항목을 검토하고 저장합니다.

1. 이제 결정 항목이 목록에 나타나고 **[!UICONTROL 초안]** 상태. 프로필에 제공할 준비가 되면 줄임표 버튼을 클릭하고 다음을 선택합니다. **[!UICONTROL 승인]**.

   ![](assets/item-approve.png)

## 결정 항목 관리

결정 항목 목록에서 결정 항목을 편집하고 상태를 변경할 수 있습니다(**초안**, **승인됨**, **보관됨**), 복제하거나 삭제합니다.

결정 항목을 수정하려면 해당 결정 항목을 열고 수정한 후 저장합니다.

결정 항목을 선택하거나 줄임표 버튼을 클릭하면 아래에 설명된 작업이 활성화됩니다.

* **[!UICONTROL 승인]**: 결정 항목의 상태를 승인됨으로 설정합니다.
* **[!UICONTROL 승인 실행 취소]**: 결정 항목의 상태를 다음으로 다시 설정합니다. **[!UICONTROL 초안]**.
* **[!UICONTROL 복제]**: 속성 및 제약 조건이 동일한 결정 항목을 만듭니다. 기본적으로 새 항목에는 **[!UICONTROL 초안]** 상태.
* **[!UICONTROL 삭제]**: 목록에서 결정 항목을 제거합니다.

  >[!IMPORTANT]
  >
  >삭제하면 결정 항목과 해당 콘텐츠에 더 이상 액세스할 수 없습니다. 이 작업은 실행 취소할 수 없습니다. 결정 항목이 컬렉션이나 결정에 사용되는 경우 삭제할 수 없습니다. 먼저 오브젝트에서 결정 항목을 제거해야 합니다.

* **[!UICONTROL 보관]**: 결정 항목 상태를 다음으로 설정합니다. **[!UICONTROL 보관됨]**. 결정 항목은 여전히 목록에서 사용할 수 있지만 상태를 다시 로 설정할 수 없습니다. **[!UICONTROL 초안]** 또는 **[!UICONTROL 승인됨]**. 복제하거나 삭제할 수만 있습니다.
