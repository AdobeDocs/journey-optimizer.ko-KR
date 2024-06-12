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
source-git-commit: e35f6b8ddc1e7bb8a737b33be200115a3022c99c
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 2%

---

# 조각 관리 {#manage-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="새 조각 상태"
>abstract="다음 이후 **초안** 및 **라이브** Journey Optimizer 6월 릴리스와 함께 상태가 도입되었습니다. 이 릴리스 전에 생성된 모든 조각은 여정 또는 캠페인에서 사용되더라도 &quot;초안&quot; 상태를 갖습니다. 이러한 조각을 변경하는 경우 해당 조각을 &quot;라이브&quot;로 만들고 관련 캠페인 및 여정에 변경 사항을 전파하도록 게시해야 합니다."

조각을 관리하려면 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴.

![](assets/fragment-list.png)

현재 샌드박스에서 생성된 모든 조각 - 다음 중 하나 [다음에서 **[!UICONTROL 조각]** 메뉴](#create-fragments), 다음 중 하나를 사용하여 [조각으로 저장](#save-as-fragment) option - 이 표시됩니다.

조각에서 조각을 필터링할 수 있습니다.

* 유형: **[!UICONTROL 비주얼]** 또는 **[!UICONTROL 표현식]**
* 태그
* 생성 또는 수정 날짜

모든 조각을 표시하도록 선택하거나 현재 사용자가 만들거나 수정한 항목만 표시하도록 선택할 수 있습니다.

다음을 표시할 수도 있습니다 **[!UICONTROL 보관됨]** 조각. [자세히 알아보기](#archive-fragments)

![](assets/fragment-list-filters.png)

다음에서 **[!UICONTROL 추가 작업]** 각 조각 옆에 있는 버튼을 사용하여 다음을 수행할 수 있습니다.

* 조각을 복제합니다.

* 사용 **[!UICONTROL 참조 탐색]** 옵션을 사용하여 여정, 캠페인 또는 템플릿이 사용되는 위치를 확인합니다. [자세히 알아보기](#explore-references)

* 조각 보관 [자세히 알아보기](#archive-fragments)

* 조각 편집 [태그](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 조각 편집 {#edit-fragments}

조각을 편집하려면 아래 단계를 따르십시오.

1. 에서 원하는 항목을 클릭합니다. **[!UICONTROL 조각]** 목록을 표시합니다.
1. 조각 속성에서 다음을 수행할 수 있습니다. [참조 살펴보기](#explore-references), [액세스 관리](../administration/object-based-access.md)및 다음을 포함한 조각 세부 사항 업데이트 [태그](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. 조각을 처음부터 만들 때와 마찬가지로 해당 버튼을 선택하여 콘텐츠를 편집합니다. [자세히 알아보기](#create-from-scratch)

>[!NOTE]
>
>조각을 편집할 때 해당 조각을 사용하는 모든 콘텐츠에 변경 사항이 자동으로 전파됩니다. 단, 에서 사용하는 콘텐츠는 제외됩니다. **[!UICONTROL 라이브]** 여정 또는 캠페인. 원본 조각에서 상속을 중단할 수도 있습니다. 다음에서 자세히 알아보기 [이메일에 시각적 조각 추가](../email/use-visual-fragments.md#break-inheritance) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md#break-inheritance) 섹션.

## 참조 탐색 {#explore-references}

현재 조각을 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 표시할 수 있습니다.

이렇게 하려면 을(를) 선택합니다 **[!UICONTROL 참조 탐색]** 다음 중 하나에서 **[!UICONTROL 추가 작업]** 조각 목록 또는 조각 속성 화면의 메뉴

![](assets/fragment-explore-references.png)

여정, 캠페인, 템플릿 및 조각 간에 전환하려면 탭을 선택합니다. 해당 상태를 보고 조각을 참조하는 해당 항목으로 리디렉션할 이름을 클릭할 수 있습니다.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>조각에 액세스할 수 없는 레이블이 있는 여정, 캠페인 또는 템플릿에서 조각을 사용하는 경우 선택한 탭 위에 경고 메시지가 표시됩니다. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md)

## 조각 보관 {#archive-fragments}

더 이상 브랜드와 관련이 없는 항목에서 조각 목록을 정리할 수 있습니다.

이렇게 하려면 **[!UICONTROL 추가 작업]** 원하는 조각 옆에 있는 버튼을 선택하고 **[!UICONTROL 보관]**. 조각 목록에서 사라지므로 사용자가 향후 이메일 또는 템플릿에서 사용할 수 없습니다.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>콘텐츠에 사용되는 조각을 보관하는 경우 <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->해당 콘텐츠는 영향을 받지 않습니다.

조각을 보관 해제하려면 **[!UICONTROL 보관됨]** 항목 및 선택 **[!UICONTROL 보관 해제]** 다음에서 **[!UICONTROL 추가 작업]** 메뉴 아래의 제품에서 사용할 수 있습니다. 이제 조각 목록에서 다시 액세스할 수 있으며 모든 이메일 또는 템플릿에서 사용할 수 있습니다.

![](assets/fragment-list-unarchive.png)
