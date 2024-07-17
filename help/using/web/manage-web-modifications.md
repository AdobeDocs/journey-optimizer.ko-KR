---
title: 웹 수정 사항 관리
description: Journey Optimizer 웹 페이지 콘텐츠의 수정 사항을 관리하는 방법 알아보기
feature: Web Channel
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 8%

---

# 웹 수정 사항 관리 {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="손쉽게 모든 변경 내용 관리"
>abstract="이 창을 사용하여 웹 페이지에 추가된 모든 조정 내용 및 스타일을 탐색하고 관리할 수 있습니다."

웹 페이지에 추가한 모든 구성 요소, 조정 및 스타일을 쉽게 관리할 수 있습니다. 전용 창에서 직접 수정 사항을 추가할 수도 있습니다.

## 수정 사항 창 작업 {#use-modifications-pane}

1. **[!UICONTROL 수정 사항]** 아이콘을 선택하여 왼쪽에 해당 창을 표시합니다.

   ![](assets/web-designer-modifications-pane.png)

1. 페이지에 수행한 각 변경 사항을 검토할 수 있습니다.

1. 원치 않는 수정 내용을 선택하고 **[!UICONTROL 추가 작업]** 단추에서 **[!UICONTROL 수정 내용 삭제]** 옵션을 클릭하여 제거하십시오.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >후속 작업에 영향을 미칠 수 있으므로 작업을 삭제할 때 주의하여 진행하십시오.

1. 동시에 여러 수정 사항을 삭제하려면 **[!UICONTROL 수정 사항]** 창 상단의 **[!UICONTROL 선택]** 단추를 클릭하고 선택한 수정 사항을 확인한 다음 **[!UICONTROL 삭제]** 아이콘을 클릭합니다.

   ![](assets/web-designer-modifications-select-delete.png)

1. **[!UICONTROL 수정 사항]** 창 위에 있는 **[!UICONTROL 추가 작업]** 단추를 사용하여 모든 수정 사항을 한 번에 삭제합니다.

   ![](assets/web-designer-delete-modifications.png)

1. 잘못된 수정 사항만 삭제할 수도 있습니다. 즉, 다른 변경 사항으로 인해 재정의된 변경 사항만 삭제할 수 있습니다. 예를 들어, 텍스트 색상을 수정한 다음 해당 텍스트를 삭제하면 텍스트가 더 이상 존재하지 않으므로 색상 수정이 유효하지 않게 됩니다.

1. 화면 오른쪽 상단의 **[!UICONTROL 실행 취소/다시 실행]** 단추를 사용하여 작업을 취소하거나 다시 실행할 수 있습니다.

   ![](assets/web-designer-undo-redo.png)

   버튼을 길게 클릭하여 **[!UICONTROL 실행 취소]**&#x200B;와(과) **[!UICONTROL 다시 실행]** 옵션 간을 전환합니다. 그런 다음 버튼 자체를 클릭하여 원하는 작업을 적용합니다.

## 전용 창에서 수정 사항 추가 {#add-modifications}

웹 디자이너를 사용하여 페이지를 편집할 때 구성 요소를 선택하고 웹 디자이너 인터페이스에서 편집할 필요 없이 **[!UICONTROL 수정 사항]** 창에서 직접 콘텐츠에 새로운 변경 사항을 추가할 수 있습니다. 아래 단계를 수행합니다.

1. **[!UICONTROL 수정 사항]** 창에서 **[!UICONTROL 추가 작업]** 단추를 클릭합니다.

1. **[!UICONTROL 수정 추가]**&#x200B;를 선택합니다.

   ![](assets/web-designer-add-modification.png)

1. 수정 유형을 선택합니다.

   * **[!UICONTROL CSS 선택기]** - [자세히 알아보기](#css-selector)
   * **[!UICONTROL 페이지`<Head>`]** - [자세히 알아보기](#page-head)

1. 콘텐츠를 입력하고 변경 내용을 **[!UICONTROL 저장]**&#x200B;합니다.

1. 수정 내용 옆에 있는 **[!UICONTROL 추가 작업]** 단추를 클릭하고 **[!UICONTROL 정보]**&#x200B;를 선택하여 세부 정보를 표시합니다.

   ![](assets/web-designer-add-modification-info.png)

### CSS 선택기 {#css-selector}

**CSS 선택기** 유형 수정을 추가하려면 아래 단계를 따르십시오.

1. 수정 유형으로 **[!UICONTROL CSS 선택기]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL CSS 요소 선택기]** 필드는 변경 사항을 적용할 HTML 요소(또는 DOM 트리의 노드)를 찾아 선택하는 데 도움이 됩니다. <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. 작업 유형(**[!UICONTROL 콘텐츠 설정]** 또는 **[!UICONTROL 특성 설정]**)을 선택하고 필요한 정보/콘텐츠를 입력하십시오.

   * **[!UICONTROL 콘텐츠 설정]**: **[!UICONTROL CSS 요소 선택기]** 필드에 의해 식별된 요소에 들어가는 콘텐츠를 지정합니다.

   * **[!UICONTROL 특성 설정]**: 이 선택기를 이 특성으로도 식별할 수 있도록 현재 CSS 선택기와 연결할 특성을 지정합니다. 이렇게 하려면 **[!UICONTROL 특성 이름]** 필드에 이름을 입력하고 **[!UICONTROL 콘텐츠]** 필드에 값을 입력하십시오. 속성이 이미 있으면 값이 업데이트되고, 그렇지 않으면 지정된 이름과 값으로 새 속성이 추가됩니다.

     ![](assets/web-designer-add-modification-css-attribute.png)

### 페이지 `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="사용자 정의 코드 추가"
>abstract="HEAD 요소는 메타데이터 컨테이너이며 HTML 태그와 BODY 태그 사이에 배치됩니다. SCRIPT 및 STYLE 요소만 추가하십시오. DIV 태그 및 기타 요소를 추가하면 나머지 HEAD 요소가 BODY에 들어갈 수 있습니다."

**[!UICONTROL 페이지`<head>`]** 수정 형식을 사용하여 사용자 지정 코드를 추가할 수 있습니다.

`<head>` 요소는 메타데이터(데이터에 대한 데이터)의 컨테이너이며 `<html>` 태그와 `<body>` 태그 사이에 있습니다. 이 경우 코드는 본문 또는 페이지 로드 이벤트를 기다리지 않고 페이지 로드 시작 시 실행됩니다.

`<head>` 요소는 일반적으로 JavaScript 또는 CSS 코드를 페이지의 맨 위에 추가하는 데 사용됩니다. 이후 시각적 작업을 위한 선택기는 이 탭에 추가된 HTML 요소에 따라 다릅니다.

**페이지`<head>`** 형식 수정을 추가하려면 아래 단계를 수행합니다.

1. 수정 유형으로 **[!UICONTROL 페이지`<head>`]**&#x200B;을(를) 선택하십시오.

   ![](assets/web-designer-add-modification-head-type.png)

1. **[!UICONTROL 콘텐츠]** 상자에 사용자 지정 코드를 추가합니다.

   >[!CAUTION]
   >
   >`<head>` 섹션에는 `<script>` 및 `<style>` 요소만 추가할 수 있습니다. `<div>`개 태그 및 기타 요소를 추가하면 나머지 `<head>`개 요소가 `<body>`에 들어갈 수 있습니다.

1. **[!UICONTROL 고급 편집 옵션]** 단추를 클릭합니다. 개인화 편집기가 열립니다.

   ![](assets/web-designer-add-modification-head-advanced.png)

   [!DNL Journey Optimizer] 개인화 편집기를 모든 개인화 및 작성 기능과 함께 활용할 수 있습니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

#### 사용자 지정 코드 예 {#custom-code-examples}

**[!UICONTROL 페이지`<head>`]** 수정 형식을 사용하여 다음을 수행할 수 있습니다.

* JavaScript 인라인 또는 외부 JavaScript 파일에 대한 링크를 사용합니다.

  예를 들어 요소의 색상을 변경하려면 다음과 같이 하십시오.

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* 외부 스타일시트에 대한 스타일 인라인 또는 링크를 구성합니다.

  예를 들어 오버레이 요소의 클래스를 정의하려면

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### 사용자 지정 코드 우수 사례 {#custom-code-best-practices}

+++ **항상 하나의 요소에 사용자 지정 코드를 래핑합니다.**

예:

```
<script>
// Code goes here
</script>
```

수정이 필요한 경우 이 컨테이너 내에서 변경합니다.

사용자 지정 코드가 더 이상 필요하지 않은 경우 이 컨테이너를 비워 두되 제거하지 마십시오. 이렇게 하면 다른 경험 수정 사항에는 영향을 주지 않습니다.

+++

+++ **사용자 지정 코드 스크립트에서 document.write 작업을 수행하지 마십시오.**

스크립트는 비동기적으로 실행됩니다. 이로 인해 document.write 작업이 종종 페이지의 잘못된 위치에 나타납니다. 사용자 지정 코드에서 생성된 스크립트에는 document.write를 사용하지 않는 것이 좋습니다.

+++

+++ **요소를 만든 다음 수정하는 경우 원래 요소를 삭제하지 마십시오.**

각 변경 사항은 **[!UICONTROL 수정 사항]** 패널에 새 요소를 만듭니다. 두 번째 작업은 요소 1을 수정하므로, 요소 1을 삭제하면 해당 작업에는 더 이상 수정할 사항이 없게 되며, 따라서 변경이 더 이상 작동하지 않습니다.

+++

+++ **동일한 URL에 영향을 주는 두 캠페인에 대해**[!UICONTROL &#x200B;페이지 `<head>`]**수정 형식을 사용할 때는 주의하십시오.**

동일한 URL에 영향을 주는 두 개의 캠페인에 **[!UICONTROL 페이지`<head>`]** 수정 형식을 사용하는 경우 두 캠페인의 페이지에 JavaScript이 삽입됩니다. [!DNL Journey Optimizer]은(는) 배달된 콘텐츠의 순서를 자동으로 결정합니다. 코드가 배치에 따라 달라지지 않는지 확인하십시오. 코드에 충돌이 없는지 확인하는 것은 귀하의 책임입니다.

+++
