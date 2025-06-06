---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 콘텐츠에 사용자 지정 CSS 추가
description: Journey Optimizer의 이메일 Designer 내에서 직접 이메일 콘텐츠에 사용자 지정 CSS를 추가하는 방법을 알아봅니다
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, 편집기, 요약, 이메일
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# 이메일 콘텐츠에 메타데이터 추가 {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="사용자 지정 CSS 추가"
>abstract="xxx."

전자 메일을 디자인할 때 [!DNL Journey Optimizer] [전자 메일 Designer](get-started-email-design.md) 내에서 직접 사용자 지정 CSS를 추가할 수 있습니다.

사용자 지정 CSS 추가 텍스트 영역에 필요한 것은 유효한 CSS 문자열입니다.

![](assets/email-body-css.png)

이용 가능 조건

사용자 지정 CSS 추가 기능은 편집기에 정의된 콘텐츠가 있는 경우에만 사용할 수 있습니다. 사용자 지정 CSS 추가 섹션을 보려면 사용자가 편집기에 콘텐츠를 추가해야 합니다. 사용자가 모든 콘텐츠를 제거하면 섹션이 사라지고 사용자 지정 css가 적용되지 않습니다. 사용자가 콘텐츠를 다시 추가하면 섹션을 사용할 수 있고 사용자 지정 css가 적용됩니다.

**잘못된 CSS 입력의 예**

잘못된 CSS를 저장할 수 없으며, CSS가 잘못된 경우 CSS를 저장할 수 없음을 나타내는 빨간색 토스트가 나타납니다.

`<style>`이(가) 허용되지 않습니다.


```
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


중괄호 누락이 잘못되었습니다.

```
body {
 background: red; 
```
