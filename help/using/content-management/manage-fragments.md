---
solution: Journey Optimizer
product: journey optimizer
title: 조각 관리
description: 콘텐츠 조각을 관리하는 방법 알아보기
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: 69aa2eb79ac5a86c8cc5e27951d3b4edd2a5d8bf
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 11%

---

# 조각 관리 {#manage-fragments}

조각을 관리하려면 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴에서 조각 목록에 액세스하십시오.

[조각으로 저장](#save-as-fragment) 옵션을 사용하여 **[!UICONTROL 조각]** 메뉴](#create-fragments)의 [현재 샌드박스에서 만든 모든 조각이 표시됩니다.

조각에서 조각을 필터링할 수 있습니다.

* 상태(초안 또는 라이브)
* 유형(시각적 또는 표현식)
* 생성 또는 수정 날짜
* 상태(보관 여부)
* 태그

![](assets/fragment-list-filters.png){width="90%" align="left"}

모든 조각을 표시하도록 선택하거나 현재 사용자가 만들거나 수정한 항목만 표시하도록 선택할 수도 있습니다.

각 조각 옆에 있는 **[!UICONTROL 추가 작업]** 단추에서 다음을 수행할 수 있습니다.

* 내보낼 패키지에 추가합니다. [자세히 알아보기](#export)
* 조각이 라이브인 경우 초안 버전을 열어 편집합니다. [자세히 알아보기](#edit-fragments)
* 조각을 복제합니다.
* **[!UICONTROL 참조 탐색]** 옵션을 사용하여 여정, 캠페인 또는 템플릿이 사용되는 위치를 확인하십시오. [자세히 알아보기](#explore-references)
* 조각을 보관합니다. [자세히 알아보기](#archive-fragments)
* 조각의 태그를 편집합니다. [통합 태그를 사용하여 작업하는 방법을 알아봅니다](../start/search-filter-categorize.md#tags)

![](assets/fragment-list-more-actions.png){width="70%" align="left"}

## 조각 상태

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="새로운 조각 상태"
>abstract="**초안** 및 **라이브** 상태가 Journey Optimizer 6월 릴리스와 함께 도입되었으므로 이 릴리스 전에 만들어진 모든 조각은 여정 또는 캠페인에서 사용되더라도 **초안** 상태입니다. 이러한 조각을 변경하는 경우 해당 조각을 게시하여 **Live**&#x200B;로 설정하고 변경 내용을 관련 캠페인 및 여정에 전파해야 합니다. 또한 여정/캠페인 버전을 새로 만들어 게시해야 합니다. <br/>게시하려면 <a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">조각 게시</a> 사용자 권한이 필요합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="콘텐츠 조각 권한에 대해 자세히 알아보기"

조각에는 여러 상태가 있을 수 있습니다.

* **[!UICONTROL 초안]**: 조각을 편집 중이며 승인되지 않았습니다.

* **[!UICONTROL Live]**: 조각이 승인되었으며 활성 상태입니다. [조각을 게시하는 방법 알아보기](../content-management/create-fragments.md#publish)

  라이브 조각을 편집하는 동안 상태 옆에 특정 아이콘이 표시됩니다. 조각의 초안 버전을 열려면 이 아이콘을 클릭하십시오.

* **[!UICONTROL 게시]**: 조각이 승인되어 게시되고 있습니다.
* **[!UICONTROL 보관됨]**: 조각이 보관되었습니다. [조각을 보관하는 방법 알아보기](#archive-fragments)

>[!CAUTION]
>
>**초안** 및 **라이브** 상태가 Journey Optimizer 6월 릴리스와 함께 도입되었으므로 이 릴리스 전에 만들어진 모든 조각은 여정 또는 캠페인에서 사용되더라도 **초안** 상태입니다. 이러한 조각을 변경하는 경우 해당 조각을 게시하여 **Live**&#x200B;로 설정하고 변경 내용을 관련 캠페인 및 여정에 전파해야 합니다. 또한 여정/캠페인 버전을 새로 만들어 게시해야 합니다. 게시하려면 [Publish 조각](../administration/ootb-product-profiles.md#content-library-manager) 사용자 권한이 필요합니다.

## 조각 편집 {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="캠페인에서의 조각 업데이트"
>abstract="조각에 대한 변경 사항을 게시하면 이 캠페인은 업데이트되지 않습니다. 조각 업데이트 기능을 지원하려면 새 버전을 게시해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="여정에서의 조각 업데이트"
>abstract="조각에 대한 변경 사항을 게시하면 이 여정은 업데이트되지 않습니다. 조각 업데이트 기능을 지원하려면 새 버전을 게시해야 합니다."

조각을 편집하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 조각]** 목록에서 원하는 조각을 클릭합니다. 조각 속성 화면이 열리고 콘텐츠 미리보기가 표시됩니다.

1. 조각이 현재 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 확인할 수 있습니다. 이렇게 하려면 [기타] 작업 단추에서 **[!UICONTROL 참조 탐색]** 옵션을 선택합니다. [자세히 알아보기](#explore-references)

1. 편집 중인 조각의 상태가 **[!UICONTROL Live]**&#x200B;인 경우 **[!UICONTROL 수정]** 단추를 클릭하여 조각의 초안 버전을 만드십시오. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

   >[!NOTE]
   >
   >조각의 현재 버전은 새로 업데이트된 버전을 게시하기 전까지 계속 활성 상태가 됩니다.

1. 필요한 경우 조각 세부 사항을 원하는 대로 변경합니다.

1. 조각의 콘텐츠를 수정하려면 **[!UICONTROL 편집]** 단추를 클릭하고 조각을 처음부터 만들 때와 마찬가지로 콘텐츠를 업데이트하십시오. [조각을 만드는 방법을 알아봅니다](create-fragments.md#content)

   ![](assets/fragment-edit.png){width="70%" align="left"}

   >[!NOTE]
   >
   >게시된 조각을 편집할 때 개인화 필드를 제거할 수 있지만 조각 콘텐츠에 새 개인화 필드를 추가할 수는 없습니다. 개인화된 속성을 추가하려면 조각을 복제해야 합니다. [자세히 알아보기](#adding-new-attributes)

1. 변경 사항이 준비되면 변경 사항을 저장하고 **[!UICONTROL Publish]** 단추를 클릭하여 수정 사항을 실시간으로 적용합니다. [자세히 알아보기](create-fragments.md#publish)

조각을 편집하면 원래 조각의 상속을 중단한 콘텐츠를 제외하고, 라이브 여정 및 캠페인을 포함하여 해당 조각을 사용하는 모든 콘텐츠에 변경 사항이 자동으로 전파됩니다.

>[!NOTE]
>
>[전자 메일에 시각적 조각 추가](../email/use-visual-fragments.md#break-inheritance) 및 [식 조각 활용](../personalization/use-expression-fragments.md#break-inheritance) 섹션에서 상속을 중단하는 방법을 알아봅니다.

## 라이브 조각에 새 속성 추가 {#adding-new-attributes}

>[!WARNING]
>
>라이브 조각에 새 [개인화된 특성](../personalization/personalization-build-expressions.md)을(를) 추가할 수 없습니다.

조각이 게시되면 해당 조각을 참조하는 모든 캠페인 및 여정에 대해 개인화된 또는 상황별 속성 세트가 잠깁니다.

라이브 조각에 추가 속성을 통합하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 추가 작업]** 단추를 사용하여 기존 조각을 복제합니다.

   ![](assets/fragment-list-more-actions.png){width="70%" align="left"}

1. 복제된 조각을 선택하여 열고 **[!UICONTROL 편집]** 단추를 클릭합니다.

1. [새 원하는 특성을 ](../personalization/personalization-build-expressions.md#add) 개인화 필드와 같이 복제된 조각에 추가합니다.

   ![](assets/fragment-add-new-attribute.png){width="70%" align="left"}

1. 변경 사항을 저장하고 새 조각을 게시합니다. [방법 알아보기](create-fragments.md#publish)

1. 캠페인 또는 여정을 업데이트하여 새 속성이 추가된 업데이트된 조각을 참조합니다.

   * [시각적 조각 사용 방법 알아보기](../email/use-visual-fragments.md)
   * [표현식 조각 사용 방법 알아보기](../personalization/use-expression-fragments.md)

## 참조 탐색 {#explore-references}

현재 조각을 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 표시할 수 있습니다. 이렇게 하려면 조각 목록 또는 조각 속성 화면의 **[!UICONTROL 추가 작업]** 메뉴에서 **[!UICONTROL 참조 탐색]**&#x200B;을(를) 선택하십시오.

![](assets/fragment-explore-references.png){width="70%" align="left"}

여정, 캠페인, 템플릿 및 조각 간에 전환하려면 탭을 선택합니다. 해당 상태를 보고 조각을 참조하는 해당 항목으로 리디렉션할 이름을 클릭할 수 있습니다.

![](assets/fragment-usage-screen.png){width="70%" align="left"}

>[!NOTE]
>
>조각에 액세스할 수 없는 레이블이 있는 여정, 캠페인 또는 템플릿에서 조각을 사용하는 경우 선택한 탭 위에 경고 메시지가 표시됩니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보기](../administration/object-based-access.md)

## 조각 보관 {#archive-fragments}

더 이상 브랜드와 관련이 없는 항목에서 조각 목록을 정리할 수 있습니다.

이렇게 하려면 원하는 조각 옆에 있는 **[!UICONTROL 추가 작업]** 단추를 클릭하고 **[!UICONTROL 보관]**&#x200B;을 선택합니다. 조각 목록에서 사라지므로 사용자가 향후 이메일 또는 템플릿에서 사용할 수 없습니다.

![](assets/fragment-list-archive.png){width="70%" align="left"}

>[!NOTE]
>
>콘텐츠에 사용된 조각을 보관하는 경우 해당 콘텐츠는 영향을 받지 않습니다. <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->

조각을 보관 해제하려면 **[!UICONTROL 보관됨]** 항목을 필터링하고 **[!UICONTROL 추가 작업]** 메뉴에서 **[!UICONTROL 보관 해제]**&#x200B;을(를) 선택하십시오. 이제 조각 목록에서 다시 액세스할 수 있으며 모든 이메일 또는 템플릿에서 사용할 수 있습니다.

![](assets/fragment-list-unarchive.png){width="70%" align="left"}

## 다른 샌드박스로 조각 내보내기 {#export}

Journey Optimizer을 사용하면 한 샌드박스에서 다른 샌드박스로 조각을 복사할 수 있습니다. 예를 들어 Stage 샌드박스 환경에서 프로덕션 샌드박스로 조각을 복사할 수 있습니다.

복사 프로세스는 원본 샌드박스와 대상 샌드박스 간에 **패키지 내보내기 및 가져오기**&#x200B;를 통해 수행됩니다. 개체를 내보내고 대상 샌드박스로 가져오는 방법에 대한 자세한 내용은 [다른 샌드박스로 개체 복사](../configuration/copy-objects-to-sandbox.md) 섹션에서 확인할 수 있습니다.
