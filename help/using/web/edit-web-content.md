---
title: 웹 콘텐츠 편집
description: Journey Optimizer에서 웹 페이지를 작성하고 콘텐츠를 편집하는 방법에 대해 알아봅니다
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 503bedc30c35305537c62f9452f4a2dc07424523
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 16%

---

# 웹 콘텐츠 편집 {#edit-web-content}

[웹 경험을 여정 또는 캠페인에 추가](create-web.md#create-web-experience)하면 웹 디자이너를 사용하여 사이트의 콘텐츠를 편집할 수 있습니다.

[이 비디오에서는 웹 캠페인을 만드는 방법을 알아봅니다.](#video)

[!DNL Journey Optimizer]에서 웹 작성은 **Adobe Experience Cloud Visual Helper** chrome 브라우저 확장 기능을 기반으로 합니다. [자세히 알아보기](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>[!DNL Journey Optimizer] 사용자 인터페이스에서 웹 페이지에 액세스하고 작성하려면 [이 섹션](web-prerequisites.md)에 나열된 필수 구성 요소를 따라야 합니다.

다음 섹션에 액세스하여 각 주제에 대해 자세히 알아보십시오.

* [수정 사항 관리](manage-web-modifications.md)

* [웹 캠페인 모니터링](monitor-web-experiences.md)

## 웹 디자이너를 사용하여 작업 {#work-with-web-designer}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="편집할 URL 확인"
>abstract="위에 정의된 웹 구성에 적용되는 콘텐츠 편집에 사용할 특정 웹 페이지의 URL을 확인합니다. Adobe Experience Platform Web SDK를 사용하여 웹 페이지를 구현해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR" text="자세히 알아보기"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="편집할 URL 입력"
>abstract="규칙과 일치하는 모든 페이지에 적용되는 콘텐츠 편집에 사용할 특정 웹 페이지의 URL을 입력합니다. Adobe Experience Platform Web SDK를 사용하여 웹 페이지를 구현해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR" text="자세히 알아보기"

웹 경험 작성을 시작하려면 아래 단계를 따르십시오.

1. 여정 또는 캠페인의 웹 경험 활동의 **[!UICONTROL 작업]** 탭에서 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 선택합니다.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 페이지 일치 규칙을 만든 경우 이 규칙과 일치하는 URL을 입력해야 합니다. 변경 사항은 규칙과 일치하는 모든 페이지에 적용됩니다. 페이지의 콘텐츠가 표시됩니다.

   >[!NOTE]
   >
   >단일 URL을 웹 구성으로 입력한 경우 개인화할 URL이 이미 채워져 있습니다.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >웹 페이지에는 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}가 포함되어야 합니다. [자세히 알아보기](web-prerequisites.md#implementation-prerequisites)

1. 작성을 시작하려면 **[!UICONTROL 웹 페이지 편집]**&#x200B;을 클릭하세요. 웹 디자이너가 표시됩니다.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >로드하지 못하는 웹 사이트를 로드하려고 하면 [Visual Editing Helper 브라우저 확장 기능](#install-visual-editing-helper)을 설치하라는 메시지가 표시됩니다. [이 섹션](web-prerequisites.md#troubleshooting)에서 문제 해결을 위한 팁을 확인하십시오.

1. 캔버스에서 이미지, 단추, 단락, 텍스트, 컨테이너, 머리글, 링크 등과 같은 요소를 선택합니다. [자세히 알아보기](#content-components)

1. 사용:

   * 컨텍스트 메뉴 를 사용하여 콘텐츠, 레이아웃, 링크 또는 개인화 등을 편집할 수 있습니다.

     ![](assets/web-designer-contextual-bar.png)

   * 오른쪽 패널 상단에 있는 아이콘으로 각 요소를 편집, 복제, 삭제 또는 숨길 수 있습니다.

     ![](assets/web-designer-right-panel-icons.png)

   * 선택한 요소에 따라 동적으로 변경되는 오른쪽 패널. 예를 들어 요소의 배경, 타이포그래피, 테두리, 크기, 위치, 간격, 효과 또는 인라인 스타일을 편집할 수 있습니다.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>웹 콘텐츠 디자이너는 대부분 이메일 디자이너와 유사합니다. [콘텐츠를 디자인 [!DNL Journey Optimizer]](../email/get-started-email-design.md)에 대해 자세히 알아보세요.

## 구성 요소 사용 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="웹 페이지에 구성 요소 추가"
>abstract="여러 구성 요소를 웹 페이지에 추가하고 필요에 따라 편집할 수 있습니다."

1. 왼쪽의 **[!UICONTROL 구성 요소]** 창에서 항목을 선택합니다. 웹 페이지에 다음 구성 요소를 추가하고 필요에 따라 편집할 수 있습니다.

   * [구분선](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [이미지](../email/content-components.md#image)
   * 제목 - 이 구성 요소를 사용하는 것은 이메일 디자이너에서 **[!UICONTROL 텍스트]** 구성 요소를 사용하는 것과 비슷합니다. [자세히 알아보기](../email/content-components.md#text)
   * 단락 - 이 구성 요소를 사용하는 것은 이메일 디자이너에서 **[!UICONTROL 텍스트]** 구성 요소를 사용하는 것과 비슷합니다. [자세히 알아보기](../email/content-components.md#text)
   * 링크

   ![](assets/web-designer-components.png)

1. 페이지에서 마우스를 가져간 후 **[!UICONTROL 다음 항목 앞에 삽입]** 또는 **[!UICONTROL 다음 항목 뒤에 삽입]** 단추를 클릭하여 구성 요소를 페이지의 기존 요소에 추가하십시오.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >구성 요소의 선택을 취소하려면 캔버스 위에 표시된 파란색 상황에 맞는 배너에서 **[!UICONTROL ESC]** 단추를 클릭합니다.

1. 페이지 콘텐츠에서 필요에 따라 구성 요소를 바로 편집합니다.

   ![](assets/web-designer-edit-header.png)

1. 배경, 텍스트 색상, 테두리, 크기, 위치 등과 같이 오른쪽에 있는 상황별 창에서 표시되는 스타일을 조정합니다. - 선택한 구성 요소에 따라 다릅니다.

   ![](assets/web-designer-header-style.png)

## 개인화 추가

개인화를 추가하려면 컨테이너를 선택하고 표시되는 상황별 메뉴 모음에서 개인화 아이콘을 선택합니다. 개인화 편집기를 사용하여 변경 사항을 추가합니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## 웹 디자이너 탐색 {#navigate-web-designer}

이 섹션에서는 웹 디자이너를 탐색할 수 있는 다양한 방법에 대해 자세히 설명합니다. 웹 경험에 추가된 수정 사항을 보고 관리하려면 [이 섹션](manage-web-modifications.md)을 참조하세요.

### 탐색 표시 사용 {#breadcrumbs}

1. 캔버스에서 요소를 선택합니다.

1. 선택한 요소에 대한 정보를 빠르게 표시하려면 화면 왼쪽 하단의 **[!UICONTROL 이동 경로 확장/축소]** 단추를 클릭합니다.

   ![](assets/web-designer-breadcrumbs.png)

1. 이동 경로를 마우스로 가리키면 편집기에서 해당 요소가 강조 표시됩니다.

1. 이를 사용하여 시각적 편집기 내에서 상위 요소, 동위 요소 또는 하위 요소로 쉽게 이동할 수 있습니다.

### 찾아보기 모드로 전환 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="찾아보기 모드 사용"
>abstract="이 모드의 선택한 구성에서 개인화하려는 정확한 페이지로 이동할 수 있습니다."

전용 단추를 사용하여 기본 **[!UICONTROL 디자인]** 모드에서 **[!UICONTROL 찾아보기]** 모드로 전환할 수 있습니다.

![](assets/web-designer-browse-mode.png)

**[!UICONTROL 찾아보기]** 모드에서 개인화할 선택한 구성에서 정확한 페이지로 이동할 수 있습니다.

이 메서드는 인증이 지연되거나 특정 URL에서 처음부터 사용할 수 없는 페이지를 처리할 때 특히 유용합니다. 예를 들어, 원하는 페이지에서 변경을 수행하기 위해 인증하고, 계정 페이지 또는 장바구니 페이지로 이동한 다음, **[!UICONTROL 디자인]** 모드로 다시 전환할 수 있습니다.

**[!UICONTROL 찾아보기]** 모드를 사용하면 단일 페이지 응용 프로그램을 작성할 때 웹 사이트의 모든 보기를 탐색할 수도 있습니다. [자세히 알아보기](web-spa.md)

### 장치 크기 변경 {#change-device-size}

웹 디자이너 디스플레이의 장치 크기를 **[!UICONTROL 태블릿]** 또는 **[!UICONTROL 모바일 가로]**&#x200B;와 같이 미리 정의된 크기로 변경하거나 원하는 픽셀 수를 입력하여 사용자 지정 크기를 정의할 수 있습니다.

확대/축소 포커스를 25%에서 400%로 변경할 수도 있습니다.

![](assets/web-designer-device.png)

장치 크기를 변경하는 기능은 다양한 장치, 창 및 화면 크기에서 잘 렌더링되는 반응형 사이트를 위해 설계되었습니다. 반응형 사이트는 데스크탑, 노트북, 태블릿 또는 휴대폰을 포함하여 모든 화면 크기를 자동으로 조정하고 적응합니다.

>[!CAUTION]
>
>특정 장치 크기로 웹 경험을 편집할 수 있습니다. 그러나 선택기가 동일한 한 이러한 변경 사항은 작업 중인 장치 크기뿐만 아니라 모든 크기와 장치에 적용됩니다. 마찬가지로, 일반 데스크탑 보기에서 경험을 편집하면 데스크탑 보기뿐만 아니라 모든 화면 크기에 변경 사항이 적용됩니다.
>
>현재 [!DNL Journey Optimizer]은(는) 장치 크기별 페이지 변경을 지원하지 않습니다. 즉, 별도의 사이트 구조를 사용하는 별도의 모바일 웹 사이트가 있는 경우 다른 캠페인에서 모바일 사이트별로 변경해야 합니다.

## 방법 비디오{#video}

아래 비디오에서는 [!DNL Journey Optimizer] 캠페인에서 웹 디자이너를 사용하여 웹 경험을 만드는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)