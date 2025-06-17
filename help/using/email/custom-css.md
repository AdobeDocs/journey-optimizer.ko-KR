---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 콘텐츠에 사용자 정의 CSS 추가
description: Journey Optimizer의 이메일 Designer 내에서 직접 이메일 콘텐츠에 사용자 지정 CSS를 추가하는 방법을 알아봅니다
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, 편집기, 요약, 이메일
hide: true
hidefromtoc: true
source-git-commit: bf9f1dbacba54e8b2c499d888ba1f4d66c78b7ee
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 8%

---

# 이메일 콘텐츠에 사용자 정의 CSS 추가 {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="자체 CSS 입력"
>abstract="콘텐츠의 모양을 보다 유연하게 제어하려면 이메일 디자이너 내에서 사용자 정의 CSS를 직접 추가하여 고급 및 특정 스타일을 적용할 수 있습니다."

전자 메일을 디자인할 때 [!DNL Journey Optimizer] [전자 메일 Designer](get-started-email-design.md) 내에서 직접 사용자 지정 CSS를 추가할 수 있습니다. 이 기능을 사용하면 고급 및 특정 스타일을 적용하여 보다 유연하게 콘텐츠를 표시하고 제어할 수 있습니다.

## 사용자 지정 CSS 정의 {#define-custom-css}

이메일 콘텐츠에 사용자 지정 CSS를 추가하려면 아래 단계를 따르십시오.

1. 하나 이상의 [구성 요소](content-components.md)를 추가하여 전자 메일 Designer에 일부 콘텐츠가 정의되어 있는지 확인하십시오.

1. 왼쪽 **[!UICONTROL 탐색 트리]** 또는 오른쪽 창 상단에서 **[!UICONTROL 본문]**&#x200B;을(를) 선택하십시오. **[!UICONTROL CSS 스타일]** 섹션이 오른쪽에 표시됩니다.

   ![사용자 지정 CSS 추가 단추 선택](assets/email-body-css-styles.png){width="85%"}

   >[!NOTE]
   >
   >**[!UICONTROL CSS 스타일]** 섹션은 편집기에 콘텐츠가 이미 있는 경우에만 사용할 수 있습니다.

1. 표시되는 전용 텍스트 영역에 CSS 코드를 입력합니다. 사용자 지정 CSS가 올바르고 적절한 구문을 따르는지 확인하십시오. [자세히 알아보기](#use-valid-css)

   ![전용 텍스트 영역에 사용자 지정 CSS 입력](assets/email-body-custom-css.png){width="65%"}

   >[!NOTE]
   >
   >**[!UICONTROL 사용자 지정 CSS 추가]** 단추는 **[!UICONTROL 본문]**&#x200B;을 선택한 경우에만 사용할 수 있습니다. 하지만 사용자 지정 CSS 스타일을 콘텐츠 내의 모든 구성 요소에 적용할 수 있습니다.

1. 사용자 지정 CSS를 저장하고 사용자 지정 CSS가 콘텐츠에 올바르게 적용되었는지 확인합니다. 그렇지 않은 경우 [문제 해결](#troubleshooting) 섹션을 확인하십시오.

   ![사용자 지정 CSS 추가 단추 선택](assets/email-body-custom-css-applied.png){width="85%"}

1. 모든 콘텐츠를 제거하면 섹션이 사라지고 이전에 정의한 사용자 지정 CSS가 더 이상 적용되지 않습니다.

1. **[!UICONTROL CSS 스타일]** 섹션이 다시 표시되도록 편집기에 콘텐츠를 다시 추가하십시오. 사용자 지정 CSS가 다시 적용됩니다.

## 유효한 CSS를 사용하는지 확인 {#use-valid-css}

**[!UICONTROL 사용자 지정 CSS 추가]** 텍스트 영역에 올바른 CSS 문자열을 입력할 수 있습니다. 적절한 포맷의 CSS가 즉시 콘텐츠에 적용됩니다.

>[!CAUTION]
>
>사용자는 사용자 지정 CSS의 보안을 책임집니다. CSS에 취약점이 도입되거나 기존 콘텐츠와 충돌하지 않는지 확인하십시오.
>
>의도하지 않게 컨텐츠의 레이아웃 또는 기능을 손상시킬 수 있는 CSS를 사용하지 마십시오.

### 유효한 CSS

다음은 유효한 CSS의 예입니다.

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

### 잘못된 CSS

잘못된 CSS를 입력하면 CSS를 저장할 수 없음을 나타내는 오류 메시지가 표시됩니다. 다음은 잘못된 CSS의 예입니다.

`<style>` 태그를 사용할 수 없습니다.

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

중괄호 누락과 같은 잘못된 구문은 허용되지 않습니다.

```css
body {
  background: red;
```

## 기술 구현 {#implementation}

사용자 지정 CSS는 아래 예와 같이 `data-name="global-custom"` 특성이 있는 `<style>` 태그의 일부로 `<head>` 섹션의 끝에 추가됩니다. 이렇게 하면 사용자 지정 스타일이 콘텐츠에 전체적으로 적용됩니다.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

사용자 지정 CSS는 이메일 Designer의 **[!UICONTROL 설정]** 창에서 해석되거나 확인되지 않습니다. 완전히 독립적이며 **[!UICONTROL 사용자 지정 CSS 추가]** 옵션을 통해서만 수정할 수 있습니다.

`global-custom` 스타일 태그에 `data-disabled` 특성이 `true`(으)로 설정된 경우 사용자 지정 CSS가 적용되지 않습니다. 예:

```html
<style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>
```

### 가져온 콘텐츠

이메일 Designer으로 가져온 콘텐츠와 함께 사용자 지정 CSS를 사용하려면 다음을 고려하십시오.

* CSS를 포함한 외부 HTML 콘텐츠를 가져오는 경우 해당 콘텐츠를 변환하지 않으면 **[!UICONTROL CSS 스타일]** 섹션을 사용할 수 없는 **[!UICONTROL 호환성 모드]**&#x200B;에 있게 됩니다. [기존 콘텐츠 가져오기에 대한 자세한 정보](existing-content.md)

* **[!UICONTROL 사용자 지정 CSS 추가]** 옵션을 통해 적용된 CSS를 포함하는 이메일 Designer으로 만든 콘텐츠를 가져오는 경우 이전에 적용된 CSS가 동일한 옵션에서 표시되고 편집할 수 있습니다.

<!--
* If importing content created with the Email Designer with CSS applied externally, the CSS code previously applied cannot be accessed within the **[!UICONTROL Add custom CSS]** pop-up window, but you can still override it with new custom CSS.-->

## 문제 해결 {#troubleshooting}

사용자 지정 CSS가 적용되지 않은 경우 아래 옵션을 고려하십시오.

* CSS가 올바르고 구문 오류(예: 중괄호 누락, 잘못된 속성 이름)가 없는지 확인합니다. [방법 알아보기](#use-valid-css)

* CSS가 `data-name="global-custom"` 특성이 있는 `<style>` 태그에 추가되고 있으며 `data-disabled`이(가) `global-custom`에 적용되지 않았는지 확인하십시오. [자세히 알아보기](#implementation)

* 콘텐츠에 적용된 [테마](apply-email-themes.md)를 포함한 다른 CSS 규칙으로 CSS가 재정의되지 않았는지 확인하십시오.

   * 브라우저 개발자 도구를 사용하여 콘텐츠를 검사하고 CSS가 올바른 선택기를 타깃팅하는지 확인하십시오.

   * 선언이 우선하도록 선언에 `!important`을(를) 추가해 보십시오. 예:

     ```css
     .acr-Form {
       background: red !important;
     }
     ```
