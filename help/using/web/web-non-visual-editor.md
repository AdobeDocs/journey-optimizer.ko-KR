---
title: 비시각적 편집기를 사용하여 콘텐츠 편집
description: Journey Optimizer 비시각적 편집기를 사용하여 웹 페이지를 작성하고 콘텐츠를 편집하는 방법에 대해 알아봅니다
feature: Web Channel
topic: Content Management
role: User
level: Experienced
source-git-commit: d51e28261908018824bcf65180534ced836b3765
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 시각적이지 않은 웹 편집기 사용 {#web-non-visual-editor}

[!DNL Journey Optimizer] 비주얼 [웹 디자이너](web-visual-editor.md) 외에도 **비비주얼 편집기**&#x200B;를 사용하여 웹 페이지에 수정 사항을 추가할 수도 있습니다.

이 기능은 웹 디자이너에서 페이지를 로드하는 데 필요한 [Adobe Experience Cloud Visual Helper](web-prerequisites.md#visual-authoring-prerequisites)와 같은 브라우저 확장 기능을 설치할 수 없거나 설치할 수 없는 경우에 유용합니다.

경우에 따라, 웹 페이지의 다른 요소를 수정하거나 페이지 구조를 변경하지 않고도 시각적이지 않은 편집기를 사용하여 특정 CSS 선택기에 수정 사항을 적용하는 것이 더 쉬울 수 있습니다.

시각적이지 않은 편집기로 웹 경험을 작성하려면 아래 단계를 따르십시오.

1. 여정 또는 캠페인의 **[!UICONTROL 콘텐츠 편집]** 화면에서 **[!UICONTROL 시각적 편집기]** 옵션을 선택 취소합니다.

1. 웹 콘텐츠 편집을 시작하려면 **[!UICONTROL 수정 사항 추가]**&#x200B;를 클릭하세요.

   ![](assets/web-campaign-add-modification-button.png)

1. 비시각적 편집기가 표시됩니다. 왼쪽 창을 사용하여 첫 번째 수정 사항을 추가할 수 있습니다.

   ![](assets/web-non-visual-editor.png)

1. 드롭다운 목록에서 수정 유형을 선택합니다.

   두 가지 유형을 사용할 수 있습니다. 다양한 옵션이 제공됩니다. 자세한 내용은 아래 링크를 참조하십시오.

   * **[!UICONTROL CSS 선택기]** - [자세히 알아보기](manage-web-modifications.md#css-selector)
   * **[!UICONTROL 페이지`<head>`]** - [자세히 알아보기](manage-web-modifications.md#page-head)

1. **[!UICONTROL 개인화 추가]** 단추를 클릭합니다. 개인화 편집기가 열립니다.

   [!DNL Journey Optimizer] 개인화 편집기를 모든 개인화 및 작성 기능과 함께 활용할 수 있습니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

1. 콘텐츠를 입력하고 변경 내용을 **[!UICONTROL 저장]**&#x200B;합니다.

   ![](assets/web-non-visual-editor-ex-save.png)

1. 첫 번째 수정 사항이 **[!UICONTROL 수정 사항]** 창 위에 표시됩니다.

   수정 내용 옆에 있는 **[!UICONTROL 추가 작업]** 단추를 클릭하고 **[!UICONTROL 정보]**&#x200B;를 선택하여 세부 정보를 표시합니다. 필요한 경우 **[!UICONTROL 수정 내용을 삭제]**&#x200B;할 수도 있습니다.

   ![](assets/web-non-visual-editor-ex-more.png){width="50%" align="left"}

   >[!NOTE]
   >
   >**[!UICONTROL 수정 사항]** 창은 [웹 디자이너](web-visual-editor.md)을 사용할 때와 동일합니다. 수행할 수 있는 모든 작업은 [이 섹션](manage-web-modifications.md#use-modifications-pane)에 자세히 설명되어 있습니다.

1. **[!UICONTROL 수정 사항]** 창 상단의 **[!UICONTROL 추가]** 단추를 클릭하여 다른 수정 사항을 추가하고 위의 단계를 반복합니다.


1. 또한 웹 사이트의 요소를 선택하고 해당 요소에 대한 클릭 수를 추적할 수 있습니다. 클릭 추적을 활성화하고 추적할 작업을 정의하려면 아래와 같이 왼쪽 레일에서 두 번째 아이콘을 클릭합니다.

   ![](assets/web-campaign-click.png){width="50%" align="left"}

   **구성 요소 추가** 단추를 사용하여 추적할 새 작업을 선택하십시오. [이 섹션](monitor-web-experiences.md#use-click-tracking)에서 클릭 추적 사용에 대해 자세히 알아보세요.


1. 화면 왼쪽 위의 화살표를 클릭하여 여정 또는 캠페인 버전 화면으로 다시 이동합니다. 현재 변경 사항 수를 보고 더 많은 수정 사항을 추가할 수 있습니다.

   ![](assets/web-campaign-modifications.png)

   원하는 경우 웹 디자이너로 전환할 수도 있습니다. 수정 사항이 모두 유지됩니다.
