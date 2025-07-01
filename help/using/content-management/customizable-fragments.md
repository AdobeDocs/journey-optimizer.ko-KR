---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 정의 가능한 조각
description: 일부 필드를 편집할 수 있도록 만들어 조각을 사용자 지정하는 방법을 알아봅니다.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: cd47ca1d-f707-4425-b865-14f3fbbe5fd1
source-git-commit: 7a8a0c133318b0bfc33b0fdb294e5b9ef53de9a5
workflow-type: tm+mt
source-wordcount: '1478'
ht-degree: 1%

---

# 사용자 정의 가능한 조각 {#customizable-fragments}

조각이 캠페인이나 여정 작업에 사용되면 상속으로 인해 기본적으로 잠깁니다. 즉, 조각에 수행된 모든 변경 사항은 조각이 사용되는 모든 캠페인 및 여정에 자동으로 전파됩니다. 사용자 지정 가능한 조각을 사용하면 캠페인 또는 여정 작업에 조각을 추가할 때 조각 내의 특정 필드를 편집 가능한 것으로 정의할 수 있습니다. 예를 들어 배너, 일부 텍스트 및 버튼이 있는 조각이 있다고 가정해 보겠습니다. 이미지 또는 단추 대상 URL과 같은 특정 필드를 편집 가능한 것으로 지정할 수 있습니다. 이렇게 하면 사용자가 조각을 캠페인이나 여정에 통합할 때 이러한 요소를 수정할 수 있으므로 원본 조각에 영향을 주지 않고 맞춤 경험을 제공할 수 있습니다.

사용자 지정 가능한 조각은 이전에 조각 수준에서 중앙 집중식 변경 내용이 캠페인 및 여정에 전파되지 않도록 중단했던 조각 상속을 중단하지 않아도 됩니다. 이 접근 방식을 사용하면 콘텐츠 부분을 사용할 때 조정할 수 있으므로 컨텍스트별 세부 사항으로 기본값을 유연하게 대체할 수 있습니다.

사용자 지정 가능한 조각을 활용함으로써 완전히 새로운 콘텐츠 블록을 만들거나 원본 조각의 상속을 중단하지 않고도 콘텐츠를 효율적으로 관리하고 개인화할 수 있습니다. 이렇게 하면 조각 수준에서 수행된 변경 사항이 계속 전파되는 동시에 캠페인 또는 여정 수준에서 필요한 사용자 지정을 허용할 수 있습니다.

시각적 조각과 표현식 조각을 모두 사용자 지정으로 표시할 수 있습니다. 각 조각 유형을 계속 진행하는 방법에 대한 자세한 지침은 아래 섹션을 참조하십시오.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## 시각적 조각에 편집 가능한 필드 추가 {#visual}

시각적 조각의 일부를 편집할 수 있도록 하려면 다음 단계를 수행합니다.

>[!NOTE]
>
>편집 가능한 필드는 **이미지**, **텍스트** 및 **단추** 구성 요소에 추가할 수 있습니다. **HTML** 구성 요소의 경우 표현식 조각과 유사하게 개인화 편집기를 사용하여 편집 가능한 필드가 추가됩니다. [HTML 구성 요소 및 식 조각에서 편집 가능한 필드를 추가하는 방법을 알아봅니다](#expression)

1. 조각 콘텐츠 편집 화면을 엽니다.

1. 조각에서 편집 가능한 필드를 구성할 구성 요소를 선택합니다.

1. 오른쪽에 구성 요소 속성 창이 열립니다. **편집 가능한 필드** 탭을 선택한 다음 **편집 사용** 옵션을 전환합니다.

1. 선택한 구성 요소에 대해 편집할 수 있는 모든 필드가 창에 나열됩니다. 편집할 수 있는 필드는 선택한 구성 요소 유형에 따라 다릅니다.

   아래 예에서는 &quot;여기를 클릭&quot; 버튼 URL의 편집을 허용합니다.

   ![](assets/fragment-param-enable.png)

1. 편집 가능한 모든 필드와 해당 기본값을 확인하려면 **개요**&#x200B;를 클릭하십시오.

   이 예에서 버튼 URL 필드는 구성 요소에 정의된 기본값으로 표시됩니다. 사용자는 콘텐츠에 조각을 추가한 후 이 값을 사용자 지정할 수 있습니다.

   ![](assets/fragment-param-preview.png)

1. 준비가 되면 변경 사항을 저장하여 조각을 업데이트합니다.

1. 조각을 이메일에 추가하면 사용자는 조각에 구성된 편집 가능한 모든 필드를 사용자 지정할 수 있습니다. [시각적 조각에서 편집 가능한 필드를 사용자 지정하는 방법에 대해 알아봅니다.](../email/use-visual-fragments.md#customize-fields)

## HTML 구성 요소 및 표현식 조각에 편집 가능한 필드 추가 {#expression}

HTML 구성 요소 또는 표현식 조각의 일부를 편집할 수 있도록 하려면 표현식 편집기에서 특정 구문을 사용해야 합니다. 여기에는 콘텐츠에 조각을 추가한 후 사용자가 재정의할 수 있는 기본값으로 **변수**&#x200B;을(를) 선언하는 작업이 포함됩니다.

예를 들어, 이메일에 추가할 조각을 만들고 사용자가 프레임 또는 버튼의 배경색과 같이 다른 위치에서 사용되는 특정 색상을 사용자 지정할 수 있도록 허용하려고 한다고 가정합니다. 조각을 만들 때는 &quot;color&quot;와 같은 **고유 ID**&#x200B;를 가진 변수를 선언하고 이 색상을 적용할 조각 콘텐츠의 원하는 위치에서 호출해야 합니다. 조각을 콘텐츠에 추가하면 사용자는 변수가 참조되는 곳마다 사용되는 색상을 사용자 지정할 수 있습니다.

HTML 구성 요소의 경우 특정 요소만 편집 가능한 필드가 될 수 있습니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

+++HTML 구성 요소에서 편집 가능한 요소:

아래 요소는 HTML 구성 요소에서 편집 가능한 필드가 될 수 있습니다.

* 텍스트 일부
* 링크 또는 이미지에 대한 전체 URL(URL의 일부와 작동하지 않음)
* 전체 CSS 속성(partial 속성과 함께 작동하지 않음)

예를 들어 아래 코드에서 빨간색으로 강조 표시된 각 요소는 속성이 될 수 있습니다.

![](assets/fragment-html.png){width="70%"}

+++

변수를 선언하고 조각에서 사용하려면 다음 단계를 따르십시오.

1. 표현식 조각을 연 다음 개인화 편집기에서 콘텐츠를 편집합니다.

   ![](assets/fragment-html-edit.png)

   HTML 구성 요소의 경우 조각에서 구성 요소를 선택하고 **소스 코드 표시** 단추를 클릭합니다.

1. 사용자가 편집할 변수를 선언합니다. 왼쪽 탐색 창에서 **도우미 함수** 메뉴로 이동한 다음 **인라인** 도우미 함수를 추가합니다. 변수를 선언하고 호출하는 구문은 콘텐츠에 자동으로 추가됩니다.

   ![](assets/fragment-add-helper.png)

1. 편집 가능한 필드를 식별하려면 `"name"`을(를) 고유 ID로 바꾸십시오.

   >[!NOTE]
   >
   >필드 ID는 고유해야 하며 공백이 없어야 합니다. 이 ID는 변수의 값을 표시하려는 콘텐츠의 모든 곳에서 사용해야 합니다.

1. 아래 표에 설명된 매개 변수를 추가하여 필요에 맞게 구문을 조정합니다.

   | 작업 | 매개변수 | 예 |
   | ------- | ------- | ------- |
   | 편집 가능한 필드를 **기본값**(으)로 선언합니다. 조각을 콘텐츠에 추가할 때 사용자 지정하지 않으면 이 기본값이 사용됩니다. | 인라인 태그 사이에 기본값을 추가합니다. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | 편집 가능한 필드에 대해 **레이블**&#x200B;을(를) 정의합니다. 이 레이블은 조각의 필드를 편집할 때 이메일 Designer에 표시됩니다. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | 게시해야 하는 **이미지 소스**&#x200B;가 포함된 편집 가능한 필드를 선언하십시오. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | 추적해야 하는 **URL**&#x200B;이(가) 포함된 편집 가능한 필드를 선언합니다.<br/>기본 제공되는 &quot;미러 페이지 URL&quot; 및 &quot;구독 취소 링크&quot; 미리 정의된 블록은 편집 가능한 필드가 될 수 없습니다. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. 편집 가능한 필드 값을 표시할 모든 위치에서 코드에 `{{{name}}}` 구문을 사용합니다. `name`을(를) 이전에 정의된 필드의 고유 ID로 바꾸십시오.

   ![](assets/fragment-call-variable.png)

1. 조각을 저장합니다.

이제 이메일 콘텐츠에 조각을 추가할 때 변수의 기본값을 선택한 값으로 재정의할 수 있습니다.

* 표현식 조각의 경우 특정 구문을 사용하여 변수 값을 재정의합니다. [식 조각에서 편집 가능한 필드를 사용자 지정하는 방법에 대해 알아봅니다.](../personalization/use-expression-fragments.md#customize-fields)

* HTML 구성 요소의 경우 변수는 이메일 Designer의 편집 가능한 필드 목록에 표시됩니다. [시각적 조각에서 편집 가능한 필드를 사용자 지정하는 방법에 대해 알아봅니다.](../email/use-visual-fragments.md#customize-fields)

## 편집 가능한 표현식 조각 예 {#example}

아래 예제에서는 새로운 스포츠 컬렉션을 나타내는 표현식 조각을 만들고 있습니다. 기본적으로 조각은 다음 콘텐츠를 표시합니다. *더 많은 콘텐츠를 찾고 계십니까? 최신 스포츠 컬렉션을 놓치지 마세요!*

사용자가 이 콘텐츠의 &quot;스포츠&quot;를 선택한 스포츠로 대체할 수 있도록 허용하려고 합니다. 예를 들어 *더 많은 항목을 찾고 계십니까? 최신 요가 컬렉션을 놓치지 마세요!*

방법은 다음과 같습니다.

1. ID가 &quot;sport&quot;인 &quot;sport&quot; 변수를 선언합니다.

   기본적으로 사용자가 컨텐츠에 조각을 추가한 후 변수 값을 변경하지 않으면 `{{#inline}}`과(와) `{{/inline}}` 태그 사이에 정의된 값(예: &quot;sports&quot;)이 표시됩니다.

1. 변수 값(예: 기본적으로 &quot;sports&quot;) 또는 사용자가 선택한 값을 표시할 조각 콘텐츠에 ``{{{sport}}}`` 구문을 추가합니다.

   ![](assets/fragment-expression-custom.png)

1. 콘텐츠에 표현식 조각을 추가할 때 사용자는 표현식 편집기에서 직접 선택하여 변수 값을 변경할 수 있습니다. [식 조각에서 편집 가능한 필드를 사용자 지정하는 방법에 대해 알아봅니다.](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)

## 사용자 지정 가능한 조각에 서식 있는 텍스트 추가 {#rich-text}

HTML 구성 요소를 사용하여 편집 가능한 조각에 줄 바꿈, 굵게, 기울임체 등과 같은 리치 텍스트를 추가할 수 있습니다. 그 방법은 다음과 같습니다.

➡️ [이 비디오에서 편집 가능한 조각 내에서 HTML 구성 요소에 서식 있는 텍스트를 추가하고 사용하는 방법을 알아봅니다.](#video)

### 리치 텍스트를 포함하는 조각 만들기 {#add-rich-text}

1. 시각적 조각을 만들고 구성 요소 추가를 시작합니다.

1. [HTML 구성 요소](../email/content-components.md#HTML)를 추가하고 HTML 편집기를 엽니다.

1. 왼쪽 탐색 창에서 **[!UICONTROL 도우미 함수]** 메뉴로 이동한 다음 **인라인** 도우미 함수를 추가합니다.

1. `"name"`을(를) 편집 가능한 콘텐츠에 사용할 ID로 바꾸십시오(예: &quot;EditableContent&quot;).

1. `render_content`을(를) 원하는 기본 콘텐츠에 해당하는 HTML 코드로 바꾸십시오.

   ![](assets/fragment-rich-editable-content.png)
<!--
    +++For example:

    ```html

    <h1>Main title</h1>

    <h2>Subtitle One</h2>
    <p>This is a paragraph with a line break.<br>Here is the new line.</p>

    <p class="bold">This text is bold.</p>
    <p class="italic">This text is italic.</p>
    <p class="bold-italic">This text is bold and italic.</p>

    <ul>
        <li>First bullet point</li>
        <li>Second bullet point with more text</li>
        <li>Third bullet point</li>
    </ul>

    <hr>

    <h2>Subtitle Two</h2>
    <blockquote>This is a blockquote or note with styled background and border.</blockquote>

    ```

    +++
-->

1. 동일한 HTML 구성 요소 내에서 스타일 요소에 대한 다른 **inline** 도우미 함수를 추가하십시오.

1. `"name"` 및 `render_content`을(를) 원하는 기본 스타일에 해당하는 ID 및 HTML 코드로 바꾸십시오.

   ![](assets/fragment-rich-editable-styling.png)

1. 콘텐츠를 저장합니다. 선택한 편집 가능한 필드가 오른쪽에 표시됩니다.

   ![](assets/fragment-rich-editable-fields.png)

1. 조각을 게시합니다.

### 리치 텍스트 편집 가능한 조각 사용 {#use-rich-text}

이제 이메일 콘텐츠에 조각을 추가할 때 사용자가 만든 서식 있는 텍스트 콘텐츠와 스타일을 편집할 수 있습니다. 마케터가 리치 텍스트 편집 가능한 조각을 사용하려면 아래 단계를 따르십시오.

1. 캠페인 또는 여정에서 이메일을 만든 다음 만든 조각을 추가합니다.

   오른쪽 창에 만든 편집 가능한 필드 2개를 볼 수 있습니다.

   ![](assets/fragment-use-rich-editable-fields.png)

1. **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하여 편집 가능한 콘텐츠와 스타일이 렌더링되는 방식을 확인할 수 있습니다.

1. 편집 가능한 필드 중 하나 옆에 있는 **[!UICONTROL 개인화 추가]** 아이콘을 선택하고 원하는 대로 CSS 스타일 및/또는 콘텐츠를 편집하십시오.

## 사용 방법 비디오 {#video}

이 비디오는 조각 내에서 HTML 구성 요소를 편집 가능하게 만들어 콘텐츠와 스타일 모두에 대한 동적 업데이트를 허용하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3464363/?learn=on&#x26;enablevpops)
