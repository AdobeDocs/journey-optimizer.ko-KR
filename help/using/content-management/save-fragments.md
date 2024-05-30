---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠를 조각으로 저장
description: 콘텐츠를 조각으로 저장하여 Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하는 방법에 대해 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# 콘텐츠를 조각으로 저장 {#save-as-fragment}

에서 콘텐츠를 편집할 때 [!DNL Journey Optimizer], 콘텐츠의 전부 또는 일부를 조각으로 저장하여 나중에 다시 사용할 수 있습니다.

## 시각적 조각으로 콘텐츠 저장 {#save-as-visual-fragment}

디자인 시 [콘텐츠 템플릿](content-templates.md) 또는 [이메일](../email/get-started-email-design.md) 캠페인 또는 여정에서 콘텐츠의 일부를 시각적 조각으로 저장할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 다음에서 [이메일 디자이너](../email/get-started-email-design.md)을 클릭하고 화면 오른쪽 위의 생략 부호를 클릭합니다.

1. 선택 **[!UICONTROL 조각으로 저장]** 드롭다운 메뉴에서 을(를) 선택합니다.

   ![](assets/fragment-save-as.png)

1. 다음 **[!UICONTROL 조각으로 저장]** 화면이 표시됩니다. 여기에서 개인화 필드 및 다이내믹 콘텐츠를 포함하여 조각에 포함할 요소를 선택합니다. 컨텍스트 속성은 조각에서 지원되지 않습니다.

   >[!CAUTION]
   >
   >서로 인접한 섹션만 선택할 수 있습니다. 빈 구조나 다른 조각은 선택할 수 없습니다.

   ![](assets/fragment-save-as-screen.png)

1. 클릭 **[!UICONTROL 만들기]**. 조각 세부 사항, 즉 이름 및 설명(필요한 경우)을 입력합니다.

1. 조각에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다. **[!UICONTROL 액세스 관리]**. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md).

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **태그** 검색을 개선하기 위해 템플릿을 분류하는 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. 클릭 **[!UICONTROL 만들기]** 다시. 조각이에 저장되며에 추가됩니다. [조각 목록](#access-manage-fragments)에서 액세스 가능 [!DNL Journey Optimizer] 전용 메뉴.

   다음과 같을 수 있는 독립형 조각이 됩니다. [액세스됨](#access-manage-fragments), [편집됨](#edit-fragments) 및 [보관됨](#archive-fragments) 을(를) 해당 목록의 다른 항목으로 사용하십시오.

이제 작성할 때 이 조각을 사용할 수 있습니다. [이메일](../email/get-started-email-design.md) 또는 [콘텐츠 템플릿](content-templates.md) 다음 범위 내 [!DNL Journey Optimizer]. [방법 알아보기](../email/use-visual-fragments.md)

>[!NOTE]
>
>해당 새 조각에 대한 모든 변경 사항은 원래 이메일이나 템플릿에 전파되지 않습니다. 마찬가지로 원래 콘텐츠가 해당 이메일 또는 템플릿 내에서 편집되는 경우 새 조각은 수정되지 않습니다.

## 콘텐츠 표현식 조각 저장 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="표현식 조각으로 저장"
>abstract="다음 [!DNL Journey Optimizer] 개인화 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 작성할 수 있습니다."

다음 [!DNL Journey Optimizer] 개인화 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 작성할 수 있습니다.

콘텐츠를 표현식 조각으로 저장하려면 아래 단계를 수행합니다.

1. 다음에서 [개인화 편집기](../personalization/personalization-build-expressions.md) 인터페이스를 만들고 표현식을 작성한 다음 **[!UICONTROL 조각으로 저장]**.

1. 오른쪽 창에서 사용자가 쉽게 찾을 수 있도록 표현식의 이름과 설명을 입력합니다.

   ![](assets/expression-fragment-save-as.png)

1. 클릭 **[!UICONTROL 조각 저장]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 표현식 조각이에 추가됩니다 [조각 목록](#access-manage-fragments). 이제 이를 사용하여 개인화된 콘텐츠를 작성할 수 있습니다.

>[!NOTE]
>
>표현식은 200KB를 초과할 수 없습니다.
