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
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 26%

---

# 조각 관리 {#manage-fragments}

조각을 관리하려면 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴.

현재 샌드박스에서 생성된 모든 조각 - 다음 중 하나 [다음에서 **[!UICONTROL 조각]** 메뉴](#create-fragments), 다음 중 하나를 사용하여 [조각으로 저장](#save-as-fragment) option - 이 표시됩니다.

![](assets/fragment-list-filters.png)

조각에서 조각을 필터링할 수 있습니다.

* 상태(초안 또는 라이브)
* 유형(시각적 또는 표현식)
* 생성 또는 수정 날짜
* 상태(보관 여부)
* 태그

모든 조각을 표시하도록 선택하거나 현재 사용자가 만들거나 수정한 항목만 표시하도록 선택할 수도 있습니다.

다음에서 **[!UICONTROL 추가 작업]** 각 조각 옆에 있는 버튼을 사용하여 다음을 수행할 수 있습니다.

* 조각을 복제합니다.
* 사용 **[!UICONTROL 참조 탐색]** 옵션을 사용하여 여정, 캠페인 또는 템플릿이 사용되는 위치를 확인합니다. [자세히 알아보기](#explore-references)
* 조각 보관 [자세히 알아보기](#archive-fragments)
* 조각의 태그 편집 [통합 태그를 사용한 작업 방법 알아보기](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 조각 상태

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="새로운 조각 상태"
>abstract="**초안** 및 **라이브** 상태가 Journey Optimizer 6월 릴리스에 도입되었으므로 이 릴리스 이전에 생성된 모든 조각은 여정이나 캠페인에서 사용되더라도 “초안” 상태입니다. 이러한 조각을 변경할 경우 해당 조각을 게시하여 “라이브”로 만들고 관련 캠페인 및 여정에 변경 사항을 전파해야 합니다. 또한 여정/캠페인 버전을 새로 만들어 게시해야 합니다. <br/>게시하려면 <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Publish 조각</a> 사용자 권한."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="콘텐츠 조각 권한에 대해 자세히 알아보기"

조각에는 여러 상태가 있을 수 있습니다.

* **[!UICONTROL 초안]**: 조각이 편집 중이며 승인되지 않았습니다.

* **[!UICONTROL 라이브]**: 조각이 승인되었으며 라이브 상태입니다. [조각 게시 방법 알아보기](../content-management/create-fragments.md#publish)

  라이브 조각을 편집하는 동안 상태 옆에 특정 아이콘이 표시됩니다. 조각의 초안 버전을 열려면 이 아이콘을 클릭하십시오.

* **[!UICONTROL 게시]**: 조각이 승인되어 게시 중입니다.
* **[!UICONTROL 보관됨]**: 조각이 보관되었습니다. [조각을 보관하는 방법 알아보기](#archive-fragments)

>[!CAUTION]
>
>**초안** 및 **라이브** 상태가 Journey Optimizer 6월 릴리스에 도입되었으므로 이 릴리스 이전에 생성된 모든 조각은 여정이나 캠페인에서 사용되더라도 “초안” 상태입니다. 이러한 조각을 변경할 경우 해당 조각을 게시하여 “라이브”로 만들고 관련 캠페인 및 여정에 변경 사항을 전파해야 합니다. 또한 여정/캠페인 버전을 새로 만들어 게시해야 합니다. 게시하려면 [Publish 조각](../administration/ootb-product-profiles.md#content-library-manager) 사용자 권한.

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

1. 에서 원하는 조각을 클릭합니다. **[!UICONTROL 조각]** 목록을 표시합니다.

1. 조각 속성이 콘텐츠 미리보기와 함께 열립니다.

1. 편집 중인 조각에 **라이브** 상태를 보려면 **수정** 버튼을 클릭하여 조각의 초안 버전을 만듭니다. 조각의 현재 버전은 초안 버전을 게시하기 전까지 계속 활성 상태가 됩니다.

1. 원하는 대로 조각을 변경합니다. 콘텐츠를 편집하려면 **편집** 버튼을 클릭한 다음 조각을 처음부터 만들 때와 마찬가지로 콘텐츠를 편집합니다. [조각을 만드는 방법 알아보기](#create-from-scratch)

   >[!NOTE]
   >
   >표현식 조각을 편집할 때 개인화 필드를 제거할 수 있지만 조각 콘텐츠에 새 개인화 필드를 추가할 수 없습니다. 개인화 필드를 추가하려면 조각을 복제하여 새 조각을 만드십시오.

   을(를) 선택하여 조각이 현재 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 확인할 수도 있습니다. **탐색기 참조** 옵션을 선택합니다. [자세히 알아보기](#explore-references)

   ![](assets/fragment-edit.png)

1. 변경 사항이 준비되면 **Publish** 버튼을 클릭하여 수정 사항을 실시간으로 적용합니다.

조각을 편집하면 원본 조각의 상속을 중단한 콘텐츠를 제외하고 라이브 여정 및 캠페인을 포함하여 해당 조각을 사용하는 모든 콘텐츠에 변경 사항이 자동으로 전파됩니다. 에서 상속을 중단하는 방법을 알아봅니다. [이메일에 시각적 조각 추가](../email/use-visual-fragments.md#break-inheritance) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md#break-inheritance) 섹션.

## 참조 탐색 {#explore-references}

현재 조각을 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 표시할 수 있습니다. 이렇게 하려면 을(를) 선택합니다 **[!UICONTROL 참조 탐색]** 다음 중 하나에서 **[!UICONTROL 추가 작업]** 조각 목록 또는 조각 속성 화면의 메뉴

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
