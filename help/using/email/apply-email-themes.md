---
solution: Journey Optimizer
product: journey optimizer
title: 향상된 이메일 작성 환경
description: 재사용 가능한 테마 및 모듈로 이메일 생성을 간소화하여 캠페인에서 디자인 일관성과 효율성을 보장하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 이메일 테마, 모듈, 재사용 가능성, 브랜드 일관성, 이메일 디자인, 사용자 지정 CSS, 모바일 최적화
exl-id: e81d9634-bbff-44d0-8cd7-e86f85075c06
source-git-commit: 23684c906d11c7f54eb28cac7c2697964e723a2e
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 7%

---

# 이메일 콘텐츠에 테마 적용 {#apply-email-themes}

>[!CONTEXTUALHELP]
>id="ajo_use_theme"
>title="이메일에 테마 적용"
>abstract="이메일 테마를 선택하여 브랜드와 디자인에 맞는 특정 스타일을 빠르게 적용할 수 있습니다."

<!--This documentation provides a comprehensive guide to using themes to streamline your email creation process. With the ability to define reusable themes and leverage pre-designed modules, marketers can create professional, brand-aligned emails faster and with less effort.-->

>[!AVAILABILITY]
>
>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.

테마를 사용하면 기술 전문가가 아닌 사용자도 표준 템플릿<!-- to achieve brand specific results--> 위에 사용자 지정 스타일을 추가하여 특정 브랜드 및 디자인 언어에 맞는 재사용 가능한 콘텐츠를 만들 수 있습니다.

이 기능을 통해 마케터는 시각적으로 호소력 있고 브랜드 일관성이 있는 이메일을 적은 노력으로 더 빠르고 활용할 수 있으며, 고유한 디자인 요구 사항에 대한 고급 사용자 지정 옵션을 제공할 수 있습니다.

<!--What is the Enhanced Email Authoring Experience?

This feature introduces two key components to simplify and enhance email creation:

* **Theme Management System**: A centralized system for creating, customizing, and applying reusable themes to emails. Themes ensure consistent styling across campaigns and eliminate the need for repetitive manual styling.

* **Modules**: Pre-designed, reusable content blocks that abstract common email elements (e.g., titles, descriptions, images, and links). Modules are built using customizable low-level components, offering flexibility while maintaining design standards.

Key Benefits:

- **Consistency**: Ensure all emails align with your brand's design guidelines.
- **Efficiency**: Save time by reusing themes and modules across campaigns.
- **Customization**: Add custom CSS and mobile-specific styles for advanced designs.
- **Scalability**: Eliminate repetitive styling tasks, enabling faster email creation.-->

## 가드레일 및 제한 사항 {#themes-guardrails}

* 처음부터 이메일을 만들 때는 테마를 사용하여 콘텐츠 작성을 시작하도록 선택하여 내 브랜드 및 디자인에 맞는 특정 스타일을 빠르게 적용할 수 있습니다.

  클래식 모드를 선택하면 이메일을 다시 설정하지 않는 한 테마를 적용할 수 없습니다.

* [조각](../content-management/fragments.md)은(는) 테마와 클래식 모드 간에 상호 호환되지 않습니다.

  테마가 적용되는 콘텐츠에서 조각을 사용할 수 있으려면 이 조각을 테마 모드에서 만들어야 합니다.

* HTML에서 만든 콘텐츠를 사용하는 경우 [호환성 모드](existing-content.md)가 되며 이 콘텐츠에 테마를 적용할 수 없습니다.

  테마를 포함하여 이메일 Designer의 모든 기능을 완전히 활용하려면 테마 모드에서 새 콘텐츠를 만들거나 가져온 HTML 콘텐츠를 변환해야 합니다. [자세히 알아보기](existing-content.md)

<!--If using a content created in Classic mode or HTML, you cannot apply themes to this content. You must create a new content in Theme mode.

If you apply a theme to a content using a [fragment](../content-management/fragments.md) created in Classic mode, the rendering may not be optimal.-->

## 테마 만들기 {#create-and-edit-themes}

향후 이메일 콘텐츠에서 활용할 수 있는 테마를 정의하려면 아래 단계를 따르십시오.

1. 시작하려면 새 [콘텐츠 템플릿](../content-management/create-content-templates.md)을 만드세요.

1. **[!UICONTROL 테마 만들기 또는 편집]** 옵션을 선택하십시오.

   ![](assets/theme-create.png)

1. 기본 테마를 선택하거나 Adobe 또는 사용자 지정 템플릿을 사용할 수 있습니다. 이 예제에서는 기본 테마를 선택하고 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   ![](assets/theme-select.png)

1. **[!UICONTROL 일반 설정]** 탭에서 브랜드의 특정 이름을 지정하여 테마 정의를 시작하십시오. 전자 메일의 기본 너비를 조정하고 현재 테마를 [샌드박스 간에 공유](../configuration/copy-objects-to-sandbox.md)하도록 내보낼 수 있습니다.

   <!--![](assets/theme-general-settings.png)-->

1. 오른쪽의 레일을 사용하여 다양한 탭을 탐색하고 디자인 설정을 업데이트합니다.

   ![](assets/theme-right-pane.png)

1. **[!UICONTROL 색상]** 탭에서:

   * **[!UICONTROL 편집]** 단추를 사용하여 브랜드의 기본 색상으로 **[!UICONTROL 색상 팔레트]**&#x200B;를 설정하십시오. **[!UICONTROL 사전 설정]**&#x200B;을 선택하여 색 구성표를 빠르게 만들거나 각 테마 색을 개별적으로 조정하세요. 두 가지를 조합하여 사용할 수도 있습니다.

     ![](assets/theme-colors.gif)

   * 각 변형마다 고유한 색상 팔레트 및 뉘앙스 컨트롤이 있는 밝은 모드와 어두운 모드와 같은 여러 색상 변형을 만들려면 **[!UICONTROL 변형 추가]**&#x200B;를 클릭하십시오.

     ![](assets/theme-colors-variant.png)

   * 각 변형에 대해 편집 아이콘을 클릭하여 개별 요소를 편집합니다. 만든 기본 팔레트 또는 사용자 지정 색상을 사용할 수 있습니다.

     ![](assets/theme-colors-edit-variant.gif)

1. **[!UICONTROL 텍스트 설정]**&#x200B;에서 전체 테마에 사용할 전역 글꼴을 설정할 수 있습니다. 더 세분화된 제어를 위해 각 제목과 단락 유형을 편집하여 글꼴, 크기, 스타일 등을 조정할 수도 있습니다.

   ![](assets/theme-text.png)

1. **[!UICONTROL 간격]** 탭의 목록에서 개별 요소를 선택하여 다른 구성 요소 사이에 적절하게 간격을 지정합니다.

   <!--![](assets/theme-spacing.png)-->

1. 오른쪽의 다른 탭을 사용하여 이 테마의 각 단추 요소, 구분선, 추가 이미지 서식 및 격자 레이아웃 간격을 별도로 관리할 수 있습니다.

   <!--![](assets/theme-buttons.png)-->

1. 나중에 사용할 수 있도록 이 테마를 저장하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

## 전자 메일에 테마 적용 {#apply-themes}

이메일에 기본 또는 사용자 지정 스타일 테마를 적용하려면 아래 단계를 따르십시오.

1. [!DNL Journey Optimizer]에서 여정 또는 캠페인에 [전자 메일을 추가](create-email.md) 및 [전자 메일 본문을 편집](get-started-email-design.md#key-steps)합니다.

1. 다음 작업 중 하나를 선택할 수 있습니다.

   * 기본 제공 [전자 메일 템플릿](use-email-templates.md)을(를) 선택하여 전자 메일 Designer을 엽니다. 각 템플릿에 해당하는 기본 테마는 자동으로 적용됩니다.

   * [새로운 콘텐츠를 처음부터 디자인하고](content-from-scratch.md) **[!UICONTROL 테마]**&#x200B;를 선택하여 미리 정의된 스타일 테마로 시작합니다.

     ![](assets/theme-from-scratch.png)

     >[!CAUTION]
     >
     >클래식 모드를 선택하면 이메일을 다시 설정하지 않는 한 테마를 적용할 수 없습니다.
     >
     >테마 모드에서 [조각](../content-management/fragments.md)을(를) 사용하려면 이 조각은 테마 모드를 사용하여 직접 만들었어야 합니다.

1. 이메일 Designer에서 오른쪽 레일의 **[!UICONTROL 테마]** 단추를 클릭합니다. 기본 테마 또는 템플릿의 테마가 표시됩니다. 이 테마의 두 색상 변형 간을 전환할 수 있습니다.

   ![](assets/theme-default-hero.png)

1. 현재 사용 중인 테마 옆의 화살표를 클릭합니다. 사용 가능한 사용자 지정 및 Adobe 테마 목록이 표시됩니다.

   ![](assets/theme-hero-change.png)

1. **[!UICONTROL 사용자 지정 테마]**&#x200B;를 클릭하고 만든 테마를 선택합니다.

   ![](assets/theme-select-custom.png)

1. 드롭다운 목록 외부를 클릭합니다. 새로 선택한 사용자 지정 테마는 모든 이메일 구성 요소에 스타일을 자동으로 적용합니다. 두 색상 변형 간을 전환할 수 있습니다.

1. 구성 요소를 선택한 경우에도 전용 아이콘을 사용하여 스타일 잠금을 해제할 수 있습니다.

   ![](assets/theme-unlock-style.png)

언제든지 테마를 전환할 수 있습니다. 이메일 콘텐츠는 변경되지 않지만 스타일은 새 테마를 반영하도록 업데이트됩니다.

<!--
>[!NOTE]
> - Themes apply styles globally. Ensure your theme is finalized before applying it to multiple emails.
> - Switching themes may override custom styles applied to individual components.

>[!CAUTION]
> - When using fragments, the email's theme will override the fragment's styles. A warning will be displayed in the editor if there is a conflict.

## Example Use Cases {#example-use-cases}

### 1. Creating a New Theme
- A marketer creates a theme with their brand's colors, fonts, and button styles.
- The theme is saved and reused across multiple email campaigns.

### 2. Switching Themes
- A marketer applies a holiday-themed design to an existing email by switching to a pre-designed holiday theme.-->
