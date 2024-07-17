---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠를 조각으로 저장
description: 콘텐츠를 조각으로 저장하여 Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하는 방법에 대해 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 11%

---

# 콘텐츠를 조각으로 저장 {#save-as-fragment}

[!DNL Journey Optimizer]에서 콘텐츠를 편집할 때 나중에 다시 사용할 수 있도록 콘텐츠의 전부 또는 일부를 조각으로 저장할 수 있습니다. 콘텐츠를 [이메일 Designer에서](#save-as-visual-fragment) 또는 [식 편집기에서](#save-as-expression-fragment) 조각으로 저장할 수 있습니다.

## 시각적 조각으로 저장 {#save-as-visual-fragment}

이메일 Designer의 콘텐츠를 조각으로 저장하려면 다음 단계를 수행합니다.

1. [전자 메일 Designer](../email/get-started-email-design.md)에서 화면 오른쪽 상단의 생략 부호를 클릭합니다.

1. 드롭다운 메뉴에서 **[!UICONTROL 조각으로 저장]**&#x200B;을(를) 선택합니다.

   ![](assets/fragment-save-as.png)

1. **[!UICONTROL 조각으로 저장]** 화면이 표시됩니다. 여기에서 개인화 필드 및 다이내믹 콘텐츠를 포함하여 조각에 포함할 요소를 선택합니다. 컨텍스트 속성은 조각에서 지원되지 않습니다.

   ![](assets/fragment-save-as-screen.png)

   >[!CAUTION]
   >
   >서로 인접한 섹션만 선택할 수 있습니다. 빈 구조나 다른 조각은 선택할 수 없습니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하고 필요한 경우 조각 이름과 설명을 입력합니다.

1. 조각에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 화면 상단의 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. **태그** 필드에서 Adobe Experience Platform 태그를 선택하거나 만들어 검색 개선을 위해 템플릿을 분류합니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. Click **[!UICONTROL Create]**. 조각이 **초안** 상태의 [조각 목록](#access-manage-fragments)에 추가됩니다. 해당 목록에서 다른 시각적 조각으로 사용할 수 있는 독립 실행형 조각이 됩니다.

   >[!NOTE]
   >
   >해당 새 조각에 대한 모든 변경 사항은 원래 이메일이나 템플릿에 전파되지 않습니다. 마찬가지로 원래 콘텐츠가 해당 이메일 또는 템플릿 내에서 편집되는 경우 새 조각은 수정되지 않습니다.

1. 여정 및 캠페인에서 조각을 사용하려면 해당 조각을 라이브로 만들어야 합니다. [조각을 미리 보고 게시하는 방법을 알아봅니다](../content-management/create-fragments.md#publish)

## 표현식 조각으로 저장 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="표현식 조각으로 저장"
>abstract="[!DNL Journey Optimizer] 개인화 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 빌드할 수 있습니다."

[!DNL Journey Optimizer] 개인화 편집기를 사용하면 콘텐츠를 표현식 조각으로 저장할 수 있습니다. 그런 다음 이러한 표현식을 사용하여 개인화된 콘텐츠를 빌드할 수 있습니다.

콘텐츠를 표현식 조각으로 저장하려면 아래 단계를 수행합니다.

1. [개인화 편집기](../personalization/personalization-build-expressions.md) 인터페이스에서 식을 만든 다음 **[!UICONTROL 조각으로 저장]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >표현식은 200KB를 초과할 수 없습니다.

1. 오른쪽 창에서 사용자가 쉽게 찾을 수 있도록 표현식의 이름과 설명을 입력합니다.

   ![](assets/expression-fragment-save-as.png)

1. **[!UICONTROL 조각 저장]**&#x200B;을 클릭합니다.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 조각이 **초안** 상태의 [조각 목록](#access-manage-fragments)에 추가됩니다. 해당 목록에서 다른 표현식 조각으로 사용할 수 있는 독립형 조각이 됩니다.

1. 여정 및 캠페인에서 조각을 사용하려면 해당 조각을 라이브로 만들어야 합니다. [조각을 미리 보고 게시하는 방법을 알아봅니다](../content-management/create-fragments.md#publish)
