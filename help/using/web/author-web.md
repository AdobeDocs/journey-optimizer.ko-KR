---
title: 웹 페이지 작성
description: Journey Optimizer에서 웹 페이지를 작성하고 해당 컨텐츠를 편집하는 방법을 알아봅니다
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 13%

---

# 웹 페이지 작성  {#author-web}

일단 [웹 작업을 추가했습니다.](create-web.md#create-web-campaign) 캠페인에 대한 웹 디자이너를 사용하여 사이트의 콘텐츠를 편집할 수 있습니다.

in [!DNL Journey Optimizer], 웹 작성 **Adobe Experience Cloud Visual Helper** chrome 브라우저 확장 프로그램. [자세히 알아보기](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>에서 웹 페이지에 액세스하여 작성할 수 있도록 하려면 [!DNL Journey Optimizer] 사용자 인터페이스에서는 [이 섹션](web-prerequisites.md).

[이 비디오에서 웹 캠페인을 작성하는 방법 알아보기](#video)

## 웹 페이지 컨텐츠 편집 {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="편집할 URL 확인"
>abstract="위에 정의된 웹 표면에 적용되는 콘텐츠 편집에 사용할 특정 웹 페이지의 URL을 확인합니다. Adobe Experience Platform Web SDK를 사용하여 웹 페이지를 구현해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR" text="추가 정보"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="편집할 URL 입력"
>abstract="규칙과 일치하는 모든 페이지에 적용되는 콘텐츠 편집에 사용할 특정 웹 페이지의 URL을 입력합니다. Adobe Experience Platform Web SDK를 사용하여 웹 페이지를 구현해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR" text="추가 정보"

웹 캠페인 작성을 시작하려면 아래 단계를 따르십시오.

1. 에서 **[!UICONTROL 작업]** 의 탭 [campaign](create-web.md#create-web-campaign), 선택 **[!UICONTROL 컨텐츠 편집]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 페이지 일치 규칙을 만든 경우 이 규칙과 일치하는 URL을 입력해야 합니다. 규칙과 일치하는 모든 페이지에 변경 사항이 적용됩니다. 페이지의 컨텐츠가 표시됩니다.

   >[!NOTE]
   >
   >웹 화면으로 단일 URL을 입력하면 개인화할 URL이 이미 채워집니다.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >웹 페이지에는 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}. [자세히 알아보기](web-prerequisites.md#implementation-prerequisites)

1. 클릭 **[!UICONTROL 웹 페이지 편집]** 작성을 시작하려면 다음을 수행하십시오. 웹 디자이너가 표시됩니다.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >로드하지 못하는 웹 사이트를 로드하려고 하면 설치를 제안하는 메시지가 표시됩니다 [시각적 편집 도우미 브라우저 확장](#install-visual-editing-helper). 에서 문제를 해결하기 위한 몇 가지 팁을 참조하십시오 [이 섹션](web-prerequisites.md#troubleshooting).

1. 이미지, 단추, 단락, 텍스트, 컨테이너, 제목, 링크 등의 요소를 캔버스에서 선택합니다. [자세히 알아보기](#content-components)

1. :

   * 컨텍스트 메뉴를 사용하여 콘텐츠, 레이아웃, 삽입 링크 또는 개인화 등을 편집할 수 있습니다.

      ![](assets/web-designer-contextual-bar.png)

   * 각 요소를 편집, 복제, 삭제 또는 숨길 오른쪽 패널 상단에 있는 아이콘입니다.

      ![](assets/web-designer-right-panel-icons.png)

   * 선택한 요소에 따라 동적으로 변경되는 오른쪽 패널입니다. 예를 들어 요소의 배경, 타이포그래피, 테두리, 크기, 위치, 간격, 효과 또는 인라인 스타일을 편집할 수 있습니다.

      ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>웹 콘텐츠 디자이너는 대부분 이메일 디자이너와 유사합니다. 추가 정보 [콘텐츠 디자인 [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## 구성 요소 사용 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="웹 페이지에 구성 요소 추가"
>abstract="여러 구성 요소를 웹 페이지에 추가하고 필요에 따라 편집할 수 있습니다."

1. 에서 **[!UICONTROL 구성 요소]** 왼쪽의 창에서 항목을 선택합니다. 다음 구성 요소를 웹 페이지에 추가하고 필요에 따라 편집할 수 있습니다.

   * [구분선](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [이미지](../email/content-components.md#image)
   * 제목 - 이 구성 요소를 사용하는 것은 **[!UICONTROL 텍스트]** 이메일 디자이너의 구성 요소입니다. [자세히 알아보기](../email/content-components.md#text)
   * 단락 - 이 구성 요소를 사용하는 것은 **[!UICONTROL 텍스트]** 이메일 디자이너의 구성 요소입니다. [자세히 알아보기](../email/content-components.md#text)
   * 링크
   * [오퍼 결정](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. 페이지를 마우스로 가리킨 다음 **[!UICONTROL 다음 항목 앞에 삽입]** 또는 **[!UICONTROL 다음 항목 뒤에 삽입]** 단추를 클릭하여 구성 요소를 페이지의 기존 요소에 추가합니다.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >구성 요소를 선택 취소하려면 **[!UICONTROL ESC]** 캔버스 맨 위에 표시되는 상황별 파란색 배너의 단추.

1. 필요에 따라 페이지의 컨텐츠에서 직접 구성 요소를 편집합니다.

   ![](assets/web-designer-edit-header.png)

1. 배경, 텍스트 색상, 테두리, 크기, 위치 등과 같이 오른쪽의 상황별 창에서 표시되는 스타일을 조정합니다. - 선택한 구성 요소에 따라 다릅니다.

   ![](assets/web-designer-header-style.png)

## 개인화 및 오퍼 추가

개인화를 추가하려면 컨테이너를 선택하고 표시되는 상황별 메뉴 표시줄에서 개인화 아이콘을 선택합니다. 표현식 편집기를 사용하여 변경 사항을 추가합니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

를 사용하십시오 **[!UICONTROL 오퍼 결정]** 삽입할 구성 요소 [오퍼](../offers/get-started/starting-offer-decisioning.md) 참조하십시오. 프로세스는 와 같습니다 [이메일에 오퍼 추가](../email/add-offers-email.md). 의사 결정 관리 를 활용하여 고객에게 제공할 최상의 오퍼를 선택할 수 있습니다.

![](assets/web-designer-offer.png)

## 수정 사항 관리 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="손쉽게 모든 변경 내용 관리"
>abstract="이 창을 사용하여 웹 페이지에 추가된 모든 조정 내용 및 스타일을 탐색하고 관리할 수 있습니다."

웹 페이지에 추가한 모든 구성 요소, 조정 및 스타일을 쉽게 관리할 수 있습니다.

1. 을(를) 선택합니다 **[!UICONTROL 수정 사항]** 아이콘을 클릭하여 왼쪽에 해당 창을 표시합니다.

   ![](assets/web-designer-modifications-pane.png)

1. 페이지에서 수행한 각 변경 사항을 검토할 수 있습니다.

1. 원치 않는 수정 사항을 선택하고 삭제 아이콘을 클릭하여 제거합니다.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >작업을 삭제하면 후속 작업에 영향을 줄 수 있으므로 삭제 시 주의해서 진행하십시오.

1. 를 사용하십시오 **[!UICONTROL 추가 작업]** 단추 **[!UICONTROL 수정 사항]** 모든 수정 사항을 한 번에 삭제할 수 있는 창입니다.

   ![](assets/web-designer-delete-modifications.png)

1. 에서 **[!UICONTROL 추가 작업]** 메뉴를 사용하면 잘못된 수정 사항만 삭제할 수 있습니다. 즉, 다른 변경 사항으로 인해 무시된 변경 사항입니다. 예를 들어, 텍스트 색상을 수정한 다음 해당 텍스트를 삭제하면, 텍스트가 더 이상 존재하지 않으므로 색상 수정은 비활성화됩니다.

1. 를 사용하여 작업을 취소하거나 재실행할 수도 있습니다 **[!UICONTROL 실행 취소/다시 실행]** 화면 오른쪽 상단의 단추.

   ![](assets/web-designer-undo-redo.png)

   버튼을 클릭하고 버튼을 눌러 **[!UICONTROL 실행 취소]** 및 **[!UICONTROL 다시 실행]** 옵션. 그런 다음 단추 자체를 클릭하여 원하는 작업을 적용합니다.

## 클릭 추적 사용 {#use-click-tracing}

웹 디자이너의 이 기능을 사용하면 웹 사이트의 요소를 선택하고 해당 요소의 클릭을 추적할 수 있습니다.

캠페인이 라이브되면 campaign 웹 보고서에서 각 요소에 대한 클릭 수를 확인할 수 있습니다. 이 정보는 웹 사이트 사용자의 경험을 개선하는 데 유용할 수 있습니다. 예를 들어 [웹 보고서](../reports/campaign-global-report.md#web-tab) 많은 사용자가 실제로 클릭할 수 없는 요소를 클릭한다는 것을 보여주면 해당 요소에 링크를 추가할 수 있습니다.

1. 페이지에서 요소를 선택하고 을(를) 선택합니다 **[!UICONTROL track 요소를 클릭합니다.]** 상황에 맞는 메뉴에서 사용할 수 있습니다.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >클릭 가능 여부에 관계없이 모든 항목을 선택할 수 있습니다.

1. 해당 추적 작업이 자동으로 **[!UICONTROL track 을 클릭합니다.]** 창의 왼쪽에 있습니다.

   ![](assets/web-designer-click-track-pane.png)

1. 추적된 모든 요소를 관리하고 보고서에서 쉽게 찾을 수 있도록 의미 있는 레이블을 추가합니다. 다음 **[!UICONTROL CSS 선택기]** 필드에는 선택한 요소를 찾기 위한 정보가 표시됩니다.

1. 위의 단계를 반복하여 클릭 추적에 필요한 여러 다른 요소를 선택합니다. 왼쪽 창에 해당 작업이 모두 나열됩니다.

   ![](assets/web-designer-click-tracking-actions.png)

1. 요소에서 클릭 추적을 제거하려면 해당 삭제 아이콘을 선택합니다.

캠페인이 활성화되면 캠페인 보고서를 확인할 수 있습니다 **[!UICONTROL 웹]** 탭하여 노출 횟수, 클릭률 및 요소별 클릭 수를 비교할 수 있습니다. [자세히 알아보기](../reports/campaign-global-report.md#web-tab)

## 웹 디자이너 탐색 {#navigate-web-designer}

### 탐색 표시 사용 {#breadcrumbs}

1. 캔버스에서 요소를 선택합니다.

1. 을(를) 클릭합니다. **[!UICONTROL 탐색 표시 확장/축소]** 화면의 왼쪽 하단에 있는 버튼을 클릭하여 선택한 요소에 대한 정보를 빠르게 표시합니다.

   ![](assets/web-designer-breadcrumbs.png)

1. 탐색 표시를 마우스로 가리키면 해당 요소가 편집기에서 강조 표시됩니다.

1. 이를 사용하면 시각적 편집기 내에서 상위 요소, 동일 수준의 요소 또는 하위 요소로 쉽게 이동할 수 있습니다.

### 찾아보기 모드로 교체 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="검색 모드 사용"
>abstract="이 모드의 선택한 표면에서 개인화하려는 정확한 페이지로 이동할 수 있습니다."

기본값에서 바꿀 수 있습니다 **[!UICONTROL 디자인]** 모드로 **[!UICONTROL 찾아보기]** 전용 단추를 사용하여 모드 지정

![](assets/web-designer-browse-mode.png)

에서 **[!UICONTROL 찾아보기]** 모드에서는 개인화할 선택한 서피스에서 정확한 페이지로 이동할 수 있습니다.

이 기능은 특히 특정 URL에서 시작 시점부터 사용할 수 없거나 인증이 뒤따르는 페이지를 처리할 때 유용합니다. 예를 들어 계정 페이지 또는 장바구니 페이지를 인증하고, 이동한 다음, **[!UICONTROL 디자인]** 모드 로 이동하여 원하는 페이지에서 변경할 수 있습니다.

### 장치 크기 변경 {#change-device-size}

웹 디자이너 디스플레이의 장치 크기를 미리 정의된 크기(예: **[!UICONTROL 태블릿]** 또는 **[!UICONTROL 모바일 가로]**&#x200B;또는 원하는 픽셀 수를 입력하여 사용자 지정 크기를 정의합니다.

확대/축소 포커스를 25%에서 400%로 변경할 수도 있습니다.

![](assets/web-designer-device.png)

장치 크기를 변경하는 기능은 다양한 장치, 창 및 화면 크기에 맞게 잘 렌더링되는 응답형 사이트용으로 설계되었습니다. 반응형 사이트는 데스크탑, 노트북, 태블릿 또는 휴대폰을 포함하여 모든 화면 크기를 자동으로 조정하고 적응합니다.

>[!CAUTION]
>
>특정 장치 크기로 웹 경험을 편집할 수 있습니다. 그러나 선택기가 동일한 한 이러한 변경 사항은 작업 중인 장치 크기뿐만 아니라 모든 크기와 장치에 적용됩니다. 마찬가지로 일반 데스크탑 보기에서 경험을 편집하면 데스크탑 보기뿐만 아니라 모든 화면 크기에 변경 사항이 적용됩니다.
>
>현재, [!DNL Journey Optimizer] 는 장치 크기별 페이지 변경을 지원하지 않습니다. 즉, 별도의 사이트 구조를 사용하는 별도의 모바일 웹 사이트가 있는 경우 다른 캠페인에서 모바일 사이트별로 변경 작업을 수행해야 합니다.

## 웹 캠페인 테스트 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="웹 경험 미리보기"
>abstract="웹 경험이 어떻게 시각화되는지 시뮬레이션을 수행합니다."

수정된 웹 경험의 미리 보기를 표시하려면 아래 단계를 따르십시오.

>[!CAUTION]
>
>사용자에게 전달될 오퍼를 시뮬레이션하려면 사용 가능한 테스트 프로필이 있어야 합니다. 방법 알아보기 [테스트 프로필 만들기](../segment/creating-test-profiles.md).

1. 웹 캠페인 편집 콘텐츠 화면에서 을 선택합니다 **[!UICONTROL 컨텐츠 시뮬레이션]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. 클릭 **[!UICONTROL 테스트 프로필 관리]** 테스트 프로필을 한 개 이상 선택하려면 다음을 수행하십시오.
1. 수정된 웹 페이지의 미리 보기가 표시됩니다.

   ![](assets/web-designer-preview.png)

1. 기본 브라우저에서 열거나 테스트 URL을 복사하여 브라우저에 붙여넣을 수도 있습니다. 이렇게 하면 캠페인이 라이브로 전환되기 전에 모든 브라우저에서 새 웹 경험을 미리 볼 수 있는 팀 및 이해 관계자와 링크를 공유할 수 있습니다.

   >[!NOTE]
   >
   >테스트 URL을 복사할 때에서 컨텐츠 시뮬레이션이 생성될 때 사용되는 테스트 프로필에 대해 개인화된 컨텐츠가 표시됩니다. [!DNL Journey Optimizer].

## 방법 비디오{#video}

아래 비디오에서는 의 웹 디자이너를 사용하여 웹 경험을 만드는 방법을 보여줍니다. [!DNL Journey Optimizer] 캠페인.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
