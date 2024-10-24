---
solution: Journey Optimizer
product: journey optimizer
title: 조각 만들기
description: Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하기 위해 조각을 만드는 방법을 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: f715fb9135c446d569a4384ce73e9e92c72cb9ff
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 14%

---

# 조각 만들기 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="비주얼 유형 선택"
>abstract="여정 또는 캠페인 내의 이메일이나 콘텐츠 템플릿에서 콘텐츠를 재사용할 수 있도록 독립 실행형 시각적 조각을 만듭니다."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/communication/channels/email/design-email/add-content/use-visual-fragments" text="이메일에 비주얼 조각 추가"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="표현식 유형 선택"
>abstract="여러 여정과 캠페인 전반에서 콘텐츠를 재사용할 수 있도록 독립 실행형 표현식 조각을 만듭니다. 개인화 편집기를 사용하면 현재 샌드박스에서 생성된 모든 표현식 조각을 활용할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments" text="표현식 조각 활용"

**[!UICONTROL 조각]** 왼쪽 메뉴에서 조각을 처음부터 만들 수 있습니다. 또한 콘텐츠를 디자인할 때 기존 콘텐츠의 일부를 조각으로 저장할 수도 있습니다. [방법 알아보기](#save-as-fragment)

저장되면 여정, 캠페인 또는 템플릿에서 조각을 사용할 수 있습니다. 여정 및 캠페인 내에서 콘텐츠를 작성할 때 이 조각을 사용할 수 있습니다. [시각적 조각 추가](../email/use-visual-fragments.md) 및 [식 조각 활용](../personalization/use-expression-fragments.md)을 참조하십시오.

조각을 만들려면 아래 단계를 수행합니다.

## 조각의 속성 정의 {#properties}

1. **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴를 통해 조각 목록에 액세스합니다.

1. **[!UICONTROL 조각 만들기]**&#x200B;를 선택하고 조각 이름과 설명을 채우십시오(필요한 경우).

   ![](assets/fragment-details.png)

1. 개선된 검색을 위해 조각을 분류하려면 **[!UICONTROL 태그]** 필드에서 Adobe Experience Platform 태그를 선택하거나 만드십시오. [통합 태그를 사용하여 작업하는 방법을 알아봅니다](../start/search-filter-categorize.md#tags)

1. 조각 유형을 선택하십시오. **시각적 조각** 또는 **표현식 조각**. [시각적 및 식 조각에 대해 자세히 알아보기](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >현재 시각적 조각은 **전자 메일** 채널에서만 사용할 수 있습니다.

1. 표현식 조각을 만드는 경우 사용할 코드 형식(**[!UICONTROL HTML]**, **[!UICONTROL JSON]** 또는 **[!UICONTROL 텍스트]**)을 선택하십시오.

   ![](assets/fragment-expression-type.png)

1. 조각에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 화면 상단의 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. 조각의 콘텐츠를 디자인하려면 **[!UICONTROL 만들기]**&#x200B;를 클릭하세요.

## 조각 콘텐츠 디자인 {#content}

조각의 속성을 구성하면 생성 중인 조각 유형에 따라 이메일 Designer 또는 개인화 편집기가 열립니다.

* 시각적 조각의 경우 여정 또는 캠페인 내의 이메일에 대해 수행하는 것과 동일한 방식으로 콘텐츠를 필요에 따라 편집합니다. [자세히 알아보기](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* 표현식 조각의 경우 [!DNL Journey Optimizer] 개인화 편집기와 모든 개인화 및 작성 기능을 활용하여 조각 콘텐츠를 작성합니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

콘텐츠가 준비되면 **저장** 단추를 클릭합니다. 조각이 만들어지고 **초안** 상태의 조각 목록에 추가됩니다. 이를 미리 보고 게시하여 여정 및 캠페인에서 사용할 수 있도록 할 수 있습니다.

## 조각 미리보기 및 게시 {#publish}

>[!NOTE]
>
>조각을 게시하려면 [Publish 조각](../administration/ootb-product-profiles.md#content-library-manager) 사용자 권한이 있어야 합니다.

조각의 실행이 준비되면 미리 보고 게시하여 여정 및 캠페인에서 사용할 수 있도록 할 수 있습니다. 이렇게 하려면 다음 단계를 수행합니다.

1. 콘텐츠를 디자인한 후 조각 만들기 화면으로 돌아가거나 조각 목록에서 엽니다.

1. **태그** 필드에서 조각 미리 보기를 사용하여 렌더링을 확인할 수 있습니다. 변경해야 하는 경우 화면 상단의 **편집** 단추를 클릭하여 조각 유형에 따라 전자 메일 Designer 또는 개인화 편집기를 엽니다.

   ![](assets/fragment-preview.png)

1. 조각을 게시하려면 오른쪽 상단의 **Publish** 단추를 클릭하십시오.

   조각이 라이브 여정 또는 캠페인에서 사용 중인 경우 알려주는 메시지가 열립니다. 참조되는 여정 및/또는 캠페인 목록에 액세스하려면 **자세히 보기** 링크를 클릭하십시오. [조각의 참조를 탐색하는 방법 알아보기](../content-management/manage-fragments.md#explore-references)

   조각을 게시하고 이를 사용하는 실시간 여정/캠페인에서 업데이트하려면 **확인**&#x200B;을 클릭합니다.

   ![](assets/fragment-publish.png){width="70%" align="center"}

이제 조각은 **Live**&#x200B;이며 [!DNL Journey Optimizer] 전자 메일 Designer 또는 개인화 편집기 내에서 콘텐츠를 빌드할 때 사용할 수 있습니다.

* [시각적 조각 사용 방법 알아보기](../email/use-visual-fragments.md)
* [표현식 조각 사용 방법 알아보기](../personalization/use-expression-fragments.md)
