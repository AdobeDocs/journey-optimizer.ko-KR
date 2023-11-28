---
solution: Journey Optimizer
product: journey optimizer
title: 조각을 사용한 작업
description: Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하기 위해 조각을 만드는 방법을 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 08f3fc1837a4daa1ecaa7afcd53c80381177efb0
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 14%

---

# 조각을 사용한 작업 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="나만의 조각 정의"
>abstract="여러 여정과 캠페인 전반에서 콘텐츠를 재사용할 수 있도록 독립 실행형 조각을 만들고 관리합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/reusable-content/fragments.html#create-fragments" text="조각 만들기"

조각은 의 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다 [!DNL Journey Optimizer] 캠페인 및 여정.

이 기능을 사용하면 마케팅 사용자가 향상된 디자인 프로세스에서 이메일 콘텐츠를 빠르게 조합하는 데 사용할 수 있는 여러 사용자 지정 콘텐츠 블록을 미리 빌드할 수 있습니다.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다](#video-fragments)

조각을 최대한 활용하려면 다음을 수행하십시오.

* 나만의 조각을 만들어 보세요. 시각적 조각 또는 표현식 조각을 만들 수 있습니다. [자세히 알아보기](#create-fragments)

* 콘텐츠에서 필요한 횟수만큼 사용하십시오. 다음을 참조하십시오 [시각적 조각 추가](../email/use-visual-fragments.md) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md)

>[!NOTE]
>
>**시각적 조각** 에서 사용할 수 있습니다. [이메일 디자이너](../email/get-started-email-design.md), 반면 **표현식 조각** 을 통해 액세스할 수 있습니다. [표현식 편집기](../personalization/personalization-build-expressions.md).

또한 Journey Optimizer을 활용할 수 있습니다 **콘텐츠 REST API** 콘텐츠 조각을 관리합니다. 자세한 내용은 [Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

## 시작하기 전 {#fragment-prerequisites}

>[!CAUTION]
>
>조각을 만들고, 편집하고, 보관하려면 **[!DNL Manage library items]** 에 포함된 권한 **[!DNL Content Library Manager]** 제품 프로필. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

이 버전에서는 다음 제한 사항이 적용됩니다.

* 시각적 조각은 이메일 채널에만 사용할 수 있습니다.

* 웹 및 인앱 채널에는 표현식 조각을 사용할 수 없습니다.

## 조각 액세스 및 관리 {#access-manage-fragments}

조각 목록에 액세스하려면 다음을 선택합니다. **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴에서

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

* 다른 샌드박스에 조각을 복사합니다. <!--Learn more?-->

* 조각 보관 [자세히 알아보기](#archive-fragments)

* 조각 편집 [태그](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

### 조각 편집 {#edit-fragments}

조각을 편집하려면 아래 단계를 따르십시오.

1. 에서 원하는 항목을 클릭합니다. **[!UICONTROL 조각]** 목록을 표시합니다.
1. 조각 속성에서 다음을 수행할 수 있습니다. [참조 살펴보기](#explore-references), [액세스 관리](../administration/object-based-access.md)및 다음을 포함한 조각 세부 사항 업데이트 [태그](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. 조각을 처음부터 만들 때와 마찬가지로 해당 버튼을 선택하여 콘텐츠를 편집합니다. [자세히 알아보기](#create-from-scratch)

>[!NOTE]
>
>조각을 편집할 때 해당 조각을 사용하는 모든 콘텐츠에 변경 사항이 자동으로 전파됩니다. 단, 에서 사용하는 콘텐츠는 제외됩니다. **[!UICONTROL 라이브]** 여정 또는 캠페인. 원본 조각에서 상속을 중단할 수도 있습니다. 다음에서 자세히 알아보기 [이메일에 시각적 조각 추가](../email/use-visual-fragments.md#break-inheritance) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md#break-inheritance) 섹션.

### 참조 탐색 {#explore-references}

현재 조각을 사용 중인 여정, 캠페인 및 콘텐츠 템플릿 목록을 표시할 수 있습니다.

이렇게 하려면 을(를) 선택합니다 **[!UICONTROL 참조 탐색]** 다음 중 하나에서 **[!UICONTROL 추가 작업]** 조각 목록 또는 조각 속성 화면의 메뉴

![](assets/fragment-explore-references.png)

여정, 캠페인, 템플릿 및 조각 간에 전환하려면 탭을 선택합니다. 해당 상태를 보고 조각을 참조하는 해당 항목으로 리디렉션할 이름을 클릭할 수 있습니다.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>조각에 액세스할 수 없는 레이블이 있는 여정, 캠페인 또는 템플릿에서 조각을 사용하는 경우 선택한 탭 위에 경고 메시지가 표시됩니다. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md)

### 조각 보관 {#archive-fragments}

더 이상 브랜드와 관련이 없는 항목에서 조각 목록을 정리할 수 있습니다.

이렇게 하려면 **[!UICONTROL 추가 작업]** 원하는 조각 옆에 있는 버튼을 선택하고 **[!UICONTROL 보관]**. 조각 목록에서 사라지므로 사용자가 향후 이메일 또는 템플릿에서 사용할 수 없습니다.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>콘텐츠에 사용되는 조각을 보관하는 경우 <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->해당 콘텐츠는 영향을 받지 않습니다.

조각을 보관 해제하려면 **[!UICONTROL 보관됨]** 항목 및 선택 **[!UICONTROL 보관 해제]** 다음에서 **[!UICONTROL 추가 작업]** 메뉴 아래의 제품에서 사용할 수 있습니다. 이제 조각 목록에서 다시 액세스할 수 있으며 모든 이메일 또는 템플릿에서 사용할 수 있습니다.

![](assets/fragment-list-unarchive.png)

## 조각 만들기 {#create-fragments}

조각을 만드는 방법에는 두 가지가 있습니다.

* 조각을 사용하여 처음부터 새로 만들기 **[!UICONTROL 조각]** 전용 메뉴. [방법 알아보기](#create-from-scratch)

* 콘텐츠를 디자인할 때 콘텐츠의 일부를 조각으로 저장합니다. [방법 알아보기](#save-as-fragment)

저장되면 여정, 캠페인 또는 템플릿에서 조각을 사용할 수 있습니다. 처음부터 작성하든 기존 콘텐츠에서 작성하든 이제 내에서 콘텐츠를 작성할 때 이 조각을 사용할 수 있습니다 [!DNL Journey Optimizer]. 다음을 참조하십시오 [시각적 조각 추가](../email/use-visual-fragments.md) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md)

### 처음부터 만들기 {#create-from-scratch}

조각을 처음부터 만들려면 아래 단계를 수행합니다.

1. [조각 목록 액세스](#access-manage-fragments) 다음을 통해 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴.

1. 선택 **[!UICONTROL 조각 만들기]**.

1. 조각 세부 사항, 즉 이름 및 설명(필요한 경우)을 입력합니다.

   ![](assets/fragment-details.png)

1. 조각 유형을 선택합니다. [시각적 조각](#create-visual-fragment) 또는 [표현식 조각](#create-expression-fragment).

1. 조각에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다. **[!UICONTROL 액세스 관리]**. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md).

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **[!UICONTROL 태그]** 개선된 검색을 위해 조각을 분류할 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

### 시각적 조각 만들기 {#create-visual-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="비주얼 유형 선택"
>abstract="여정 또는 캠페인 내의 이메일이나 콘텐츠 템플릿에서 콘텐츠를 재사용할 수 있도록 독립 실행형 시각적 조각을 만듭니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="이메일에 비주얼 조각 추가"

1. [조각 만들기](#create-from-scratch) 다음에서 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴에서 **[!UICONTROL 시각적 조각]** 유형.

   >[!NOTE]
   >
   >현재 시각적 조각에만 해당 **이메일** 채널이 지원됩니다.

1. 다음 [이메일 디자이너](../email/get-started-email-design.md) 표시됩니다. 여정 또는 캠페인 내의 이메일에 대해 수행하는 것과 동일한 방식으로 필요에 따라 콘텐츠를 편집합니다.

   >[!NOTE]
   >
   >개인화 필드 및 다이내믹 콘텐츠를 추가할 수 있지만 컨텍스트 속성은 조각에서 지원되지 않습니다.

   ![](assets/fragment-designer.png)

1. 조각이 준비되면 **[!UICONTROL 저장]**. 에 추가됩니다. [조각 목록](#access-manage-fragments).

1. 필요한 경우 조각 이름 옆에 있는 화살표를 클릭하여 로 돌아갑니다. **[!UICONTROL 세부 사항]** 화면을 표시하고 편집합니다.

   ![](assets/fragment-designer-back.png)

이제 이 조각을 작성할 때 사용할 준비가 되었습니다. [이메일](../email/get-started-email-design.md) 또는 [콘텐츠 템플릿](content-templates.md) 다음 범위 내 [!DNL Journey Optimizer]. [방법 알아보기](../email/use-visual-fragments.md)

### 표현식 조각 만들기 {#create-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="표현식 유형 선택"
>abstract="여러 여정과 캠페인 전반에서 콘텐츠를 재사용할 수 있도록 독립 실행형 표현식 조각을 만듭니다. 표현식 편집기를 사용하면 현재 샌드박스에서 생성된 모든 표현식 조각을 활용할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="표현식 조각 활용"

1. [조각 만들기](#create-from-scratch) 다음에서 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴에서 **[!UICONTROL 표현식 조각]** 유형.

1. 사용할 코드 유형을 선택합니다. **[!UICONTROL HTML]**, **[!UICONTROL JSON]** 또는 **[!UICONTROL 텍스트]**.

   ![](assets/fragment-expression-type.png)

   <!--Expression fragments can be used in any channel.-->

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 표현식 편집기가 열립니다.

1. 다음을 활용할 수 있습니다. [!DNL Journey Optimizer] 모든 개인화 및 작성 기능이 있는 표현식 편집기. [자세히 알아보기](../personalization/personalization-build-expressions.md)

   ![](assets/fragment-expression-editor.png)

1. 조각이 준비되면 **[!UICONTROL 저장]**. 에 추가됩니다. [조각 목록](#access-manage-fragments).

1. 필요한 경우 조각 이름 옆에 있는 화살표를 클릭하여 로 돌아갑니다. **[!UICONTROL 세부 사항]** 화면을 표시하고 편집합니다.

이제 이 조각을 사용하여 내에서 콘텐츠를 작성할 수 있습니다. [!DNL Journey Optimizer] 표현식 편집기. [방법 알아보기](../personalization/use-expression-fragments.md)

## 조각으로 저장 {#save-as-fragment}

에서 콘텐츠를 편집할 때 [!DNL Journey Optimizer], 콘텐츠의 전부 또는 일부를 조각으로 저장하여 나중에 다시 사용할 수 있습니다.

### 시각적 조각으로 저장 {#save-as-visual-fragment}

디자인 시 [콘텐츠 템플릿](content-templates.md) 또는 [이메일](../email/get-started-email-design.md) 캠페인 또는 여정에서 콘텐츠의 일부를 시각적 조각으로 저장할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 다음에서 [이메일 디자이너](../email/get-started-email-design.md)을 클릭하고 화면 오른쪽 위의 생략 부호를 클릭합니다.

1. 선택 **[!UICONTROL 조각으로 저장]** 드롭다운 메뉴에서 을(를) 선택합니다.

   ![](assets/fragment-save-as.png)

1. 다음 **[!UICONTROL 조각으로 저장]** 화면이 표시됩니다. 여기에서 개인화 필드 및 다이내믹 콘텐츠를 포함하여 조각에 포함할 요소를 선택합니다. 컨텍스트 속성은 조각에서 지원되지 않습니다.

   >[!CAUTION]
   >
   >서로 인접한 섹션만 선택할 수 있습니다. 빈 구조나 다른 조각은 선택할 수 없습니다.

   ![](assets/fragment-save-as-screen.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 조각 세부 사항, 즉 이름 및 설명(필요한 경우)을 입력합니다.

1. 조각에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다. **[!UICONTROL 액세스 관리]**. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md).

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **태그** 검색을 개선하기 위해 템플릿을 분류하는 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. 클릭 **[!UICONTROL 만들기]** 다시. 조각이에 저장되며에 추가됩니다. [조각 목록](#access-manage-fragments)에서 액세스 가능 [!DNL Journey Optimizer] 전용 메뉴.

   다음과 같을 수 있는 독립형 조각이 됩니다. [액세스됨](#access-manage-fragments), [편집됨](#edit-fragments) 및 [보관됨](#archive-fragments) 을(를) 해당 목록의 다른 항목으로 사용하십시오.

이제 작성할 때 이 조각을 사용할 수 있습니다. [이메일](../email/get-started-email-design.md) 또는 [콘텐츠 템플릿](content-templates.md) 다음 범위 내 [!DNL Journey Optimizer]. [방법 알아보기](../email/use-visual-fragments.md)

>[!NOTE]
>
>해당 새 조각에 대한 모든 변경 사항은 원래 이메일이나 템플릿에 전파되지 않습니다. 마찬가지로 원래 콘텐츠가 해당 이메일 또는 템플릿 내에서 편집되는 경우 새 조각은 수정되지 않습니다.

### 표현식 조각으로 저장 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="표현식 조각으로 저장"
>abstract="[!DNL Journey Optimizer] 표현식 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 빌드할 수 있습니다."

[!DNL Journey Optimizer] 표현식 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 빌드할 수 있습니다.

콘텐츠를 표현식 조각으로 저장하려면 아래 단계를 수행합니다.

1. 다음에서 [표현식 편집기](../personalization/personalization-build-expressions.md) 인터페이스를 만들고 표현식을 작성한 다음 **[!UICONTROL 조각으로 저장]**.

1. 오른쪽 창에서 사용자가 쉽게 찾을 수 있도록 표현식의 이름과 설명을 입력합니다.

   ![](assets/expression-fragment-save-as.png)

1. 클릭 **[!UICONTROL 조각 저장]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 표현식 조각이에 추가됩니다 [조각 목록](#access-manage-fragments). 이제 이를 사용하여 개인화된 콘텐츠를 작성할 수 있습니다.

>[!NOTE]
>
>표현식은 200KB를 초과할 수 없습니다.

## 방법 비디오 {#video-fragments}

에서 시각적 조각을 관리, 작성 및 사용하는 방법에 대해 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

에서 표현식 조각을 관리, 작성 및 사용하는 방법에 대해 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
