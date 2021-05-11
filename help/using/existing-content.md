---
title: 이메일 가져오기 또는 코딩
description: 이메일 컨텐츠를 가져오거나 이메일을 코딩하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 5%

---

# 이메일 컨텐츠 {#existing-content} 가져오기 또는 코드 작성

![](assets/do-not-localize/badge.png)

Journey Optimizer을 사용하면 이메일을 디자인할 수 있도록 기존 HTML 컨텐츠를 가져올 수 있습니다. 이 컨텐츠는 기존 HTML 파일이나 zip 폴더의 원시 HTML 코드나 컨텐츠일 수 있습니다.

HTML 콘텐츠를 코딩하거나 기존 콘텐츠를 가져오려면 아래 단계를 수행하십시오.

1. [메시지 만들기](create-message.md)

1. **[!UICONTROL Edit Content]** 섹션에서 **[!UICONTROL Email Designer]**&#x200B;을 엽니다.

   ![](assets/import-html_1.png)

1. **[!UICONTROL Code your own]** 또는&#x200B;**[!UICONTROL Import HTML]**&#x200B;를 선택합니다. 다음 단계는 아래 섹션을 참조하십시오.

## 자신의 {#import-raw-html-code} 코드를

**[!UICONTROL Code your own]** 모드를 사용하여 원시 HTML을 가져오거나 이메일 컨텐츠를 코딩할 수 있습니다. 이 방법을 사용하려면 HTML 기술이 필요합니다.

>[!CAUTION]
>
> 이 메서드를 사용할 때는 [Adobe Experience Manager Assets Essentials](assets-essentials.md)의 이미지를 참조할 수 없습니다. HTML 코드에서 참조된 이미지는 공개 위치에 저장해야 합니다.

1. 이메일 디자이너 홈 페이지에서 **[!UICONTROL Code your own]**&#x200B;을 선택합니다.

   ![](assets/code-your-own.png)

1. 원시 HTML 코드를 입력하거나 붙여 넣습니다.

1. 왼쪽 창에서 [!DNL Journey Optimizer] 개인화 기능을 활용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](personalization/personalize.md)을 참조하십시오.

   ![](assets/code-editor.png)

1. 새 디자인에서 전자 메일을 시작할 이메일 디자이너를 열려면 옵션 메뉴에서 **[!UICONTROL Change your design]**&#x200B;을 선택합니다.

   ![](assets/code-editor-change-design.png)

1. 테스트 프로필을 사용하여 메시지 디자인 및 개인화를 확인하려면 **[!UICONTROL Preview]** 단추를 클릭합니다. 이 작업에 대한 자세한 정보는 [이 섹션](preview.md)을 참조하십시오.

   ![](assets/code-editor-preview.png)

1. 코드가 준비되면 **[!UICONTROL Save]**&#x200B;을 클릭한 다음 메시지 작성 화면으로 돌아가 메시지를 완료합니다.

   ![](assets/code-editor-save.png)


## HTML {#import-html-content-from-file} 가져오기

이메일 디자이너에서 HTML 컨텐츠를 가져올 수 있습니다. 이 컨텐츠는 다음과 같습니다.

* 스타일 시트가 포함된 **HTML 파일**,
* HTML 파일, 스타일 시트(.css) 및 이미지가 포함된 **.zip 폴더**.

   >[!NOTE]
   >
   >.zip 파일 구조에 제한 사항이 없습니다. 그러나 참조는 상대 경로여야 하며 .zip 폴더의 트리 구조에 맞아야 합니다.

HTML 내용이 포함된 파일을 가져오려면 아래 단계를 수행하십시오.

1. 이메일 디자이너 홈 페이지에서 **[!UICONTROL Import HTML]**&#x200B;을 선택합니다.

   ![](assets/import-html_2.png)

1. HTML 내용이 포함된 HTML 또는 .zip 파일을 드래그 앤 드롭합니다.

1. HTML 콘텐츠가 업로드되면 이메일 디자이너 기능을 활용하여 이메일을 편집하고 미리 볼 수 있습니다. [이 섹션에서 자세한 내용을 살펴보십시오](create-email-content.md).

   ![](assets/html-imported.png)
