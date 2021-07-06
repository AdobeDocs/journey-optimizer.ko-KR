---
title: 이메일 디자이너 콘텐츠 구성 요소 사용
description: 이메일에서 콘텐츠 구성 요소를 사용하는 방법을 알아봅니다
feature: 개요
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 2%

---

# 이메일 디자이너 콘텐츠 구성 요소 사용 {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="컨텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 전자 메일 레이아웃을 만드는 데 사용할 수 있는 빈 콘텐츠 자리 표시자입니다."


이메일 콘텐츠를 처음부터 만들 때 **[!UICONTROL Content components]**을(를) 사용하면 이메일에 배치되면 사용할 수 있는 비어 있는 원시 구성 요소로 이메일을 더 개인화할 수 있습니다.
전자 메일의 레이아웃을 정의하는 **[!UICONTROL Structure component]** 내부에 필요한 만큼 **[!UICONTROL Content components]**&#x200B;을 추가할 수 있습니다.

## 단추 {#buttons}

**[!UICONTROL Button]** 구성 요소를 사용하여 이메일에 여러 버튼을 삽입하고 이메일 대상을 다른 페이지로 리디렉션합니다.

1. **[!UICONTROL Content components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL Button]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_13.png)

1. 새로 추가한 단추를 클릭하여 텍스트를 개인화하고 이메일 디자이너의 오른쪽 창에서 **[!UICONTROL Components Settings]**&#x200B;에 액세스할 수 있습니다.

   ![](assets/email_designer_14.png)

1. **[!UICONTROL Components Settings]** 의 **[!UICONTROL Link]** 필드에서 버튼을 클릭할 때 대상을 리디렉션할 URL을 추가합니다.

1. **[!UICONTROL Target]** 드롭다운을 사용하여 대상을 리디렉션하는 방법을 선택합니다.

   * **[!UICONTROL None]**:클릭한 것과 동일한 프레임에서 링크를 엽니다(기본값).
   * **[!UICONTROL Blank]**:새 창이나 탭에서 링크를 엽니다.
   * **[!UICONTROL Self]**:클릭한 것과 동일한 프레임에서 링크를 엽니다.
   * **[!UICONTROL Parent]**:상위 프레임에서 링크를 엽니다.
   * **[!UICONTROL Top]**:창의 전체 본문에 링크를 엽니다.

   ![](assets/email_designer_15.png)

1. 예를 들어 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 및 **[!UICONTROL Border]**&#x200B;를 변경하여 버튼을 추가로 개인화할 수 있습니다.

## 텍스트 {#text}

**[!UICONTROL Text]** 구성 요소를 사용하여 전자 메일에 텍스트를 삽입합니다. **[!UICONTROL Component Settings]**&#x200B;에서 텍스트의 색상, 스타일 및 크기를 조정할 수 있습니다.

1. **[!UICONTROL Content Components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL Text]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_11.png)

1. 새로 추가된 구성 요소를 클릭하여 텍스트를 개인화하고 이메일 디자이너의 오른쪽 창에서 **[!UICONTROL Components Settings]**&#x200B;에 액세스할 수 있습니다.

1. 도구 모음에서 사용할 수 있는 다음 옵션을 사용하여 텍스트를 변경합니다.

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**:텍스트에 굵게, 기울임체, 밑줄 또는 취소선을 적용합니다.
   * **정렬 변경**:텍스트의 왼쪽, 오른쪽, 가운데 또는 좌우 정렬 중에서 선택합니다.
   * **[!UICONTROL Create list]**:텍스트에 글머리 기호 또는 번호 목록을 추가합니다.
   * **[!UICONTROL Set heading]**:텍스트에 최대 6개의 제목 수준을 추가합니다.
   * **글꼴 크기**:텍스트의 글꼴 크기를 픽셀 단위로 선택합니다.
   * **[!UICONTROL Edit image]**:텍스트 구성 요소에 이미지나 자산을 추가합니다. [자산 관리에 대해 자세히 알아보십시오](assets-essentials.md).
   * **[!UICONTROL Show the source code]**:텍스트의 소스 코드를 표시합니다. 수정할 수 없습니다.
   * **[!UICONTROL Duplicate]**:텍스트 구성 요소의 사본을 추가합니다.
   * **[!UICONTROL Delete]**:이메일에서 선택한 텍스트 구성 요소를 삭제합니다.
   * **[!UICONTROL Add personalization]**:프로필 데이터의 콘텐츠를 사용자 지정하려면 개인화 필드를 추가합니다. [콘텐츠 개인화에 대해 자세히 알아보십시오](personalization/personalize.md).

1. 더 나은 사용자 경험을 위해 개인화 필드를 추가하여 대상자를 타깃팅할 수 있습니다. 자세한 정보는 이 [섹션](personalization/personalize.md)을 참조하십시오.

1. **[!UICONTROL Components Settings]**&#x200B;에서 **[!UICONTROL Text color]**, **[!UICONTROL Font family]** 및 **[!UICONTROL Size]**&#x200B;를 조정합니다.

   ![](assets/email_designer_12.png)

## 구분선 {#divider}

**[!UICONTROL Divider]** 구성 요소를 사용하여 전자 메일의 레이아웃과 콘텐츠를 구성하는 분할선을 삽입합니다.
**[!UICONTROL Component Settings]**&#x200B;에서 줄바꿈 선의 색상, 스타일 및 크기를 선택할 수 있습니다.

![](assets/email_designer_16.png)

## HTML {#HTML}

**[!UICONTROL HTML]** 을 사용하여 기존 HTML의 다른 부분을 복사하여 붙여넣습니다. 이렇게 하면 무료 모듈식 HTML 구성 요소를 만들 수 있습니다.

이메일 디자이너와 호환되는 외부 콘텐츠를 만들고자 하는 경우, Adobe은 메시지를 처음부터 만들고 기존 이메일의 콘텐츠를 구성 요소로 복사하는 것을 권장합니다.

1. **[!UICONTROL Content Components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL HTML]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_22.png)

1. 새로 추가한 구성 요소를 클릭한 다음 **[!UICONTROL Show the source code]** 을 클릭하여 HTML을 추가합니다.

   ![](assets/email_designer_23.png)

1. 전자 메일에 추가할 HTML 코드를 복사하여 붙여 넣고 **[!UICONTROL Save]** 을 클릭합니다.

1. 예를 들어 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 및 **[!UICONTROL Border]**&#x200B;를 변경하거나 링크를 추가하여 대상자를 다른 콘텐츠로 리디렉션하여 HTML을 추가로 개인화할 수 있습니다.

## 이미지 {#image}

**[!UICONTROL Image]** 구성 요소를 사용하여 컴퓨터의 이미지 파일을 전자 메일에 삽입합니다.

1. **[!UICONTROL Content Components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL Image]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_9.png)

1. **[!UICONTROL Browse]** 을 클릭하여 자산에서 이미지 파일을 선택합니다.

   [!DNL Assets Essentials]에 대한 자세한 내용은 [Adobe Experience Manager Assets Essentials 설명서](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}를 참조하십시오.

1. 새로 추가된 구성 요소를 클릭하여 **[!UICONTROL Content Components]** 구성을 시작하고 이메일 디자이너의 오른쪽 창에서 **[!UICONTROL Components Settings]**&#x200B;에 액세스할 수 있습니다.

1. 이미지 속성을 설정합니다.

   * **[!UICONTROL Image Title]** 이미지에 제목을 정의할 수 있습니다.
   * **[!UICONTROL Alt text]** 이미지에 연결된 캡션을 정의할 수 있습니다. 이것은 대체 HTML 속성에 해당합니다.

   ![](assets/email_designer_10.png)

1. 예를 들어 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 및 **[!UICONTROL Border]**&#x200B;를 변경하거나 링크를 추가하여 대상자를 다른 콘텐츠로 리디렉션하여 이미지를 추가로 개인화할 수 있습니다.

## 비디오 {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="비디오 설정"
>abstract="이 구성 요소를 사용하여 이메일에 비디오를 삽입합니다. 모든 이메일 클라이언트는 비디오가 작동하지 않습니다. 대체 이미지를 설정하는 것이 좋습니다."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="추가 정보"

**[!UICONTROL Video]** 구성 요소를 사용하여 URL 링크를 통해 이메일에 비디오를 삽입합니다.

1. **[!UICONTROL Content Components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL Video]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_17.png)

1. 새로 추가된 구성 요소를 클릭하여 **[!UICONTROL Content Components]** 구성을 시작하고 이메일 디자이너의 오른쪽 창에서 **[!UICONTROL Components Settings]**&#x200B;에 액세스할 수 있습니다.

1. **[!UICONTROL Components Settings]** 의 **[!UICONTROL Video link]** 필드에서 비디오 URL을 추가합니다.

   ![](assets/email_designer_18.png)

1. 비디오에 **[!UICONTROL Poster image]** 을 추가하여 대상자가 재생 버튼을 클릭할 때까지 표시할 이미지를 지정할 수 있습니다.

1. 예를 들어 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 및 **[!UICONTROL Border]**&#x200B;를 변경하여 이미지를 추가로 개인화할 수 있습니다.

## Social {#social}

**[!UICONTROL Social]** 구성 요소를 사용하여 이메일에 있는 소셜 미디어 페이지에 대한 링크를 삽입합니다.

1. **[!UICONTROL Content Components]**&#x200B;에서 **[!UICONTROL Structure component]**&#x200B;에 **[!UICONTROL Social]**&#x200B;을(를) 끌어다 놓습니다.

   ![](assets/email_designer_19.png)

1. 새로 추가된 구성 요소를 클릭하여 **[!UICONTROL Content Components]** 구성을 시작하고 이메일 디자이너의 오른쪽 창에서 **[!UICONTROL Components Settings]**&#x200B;에 액세스할 수 있습니다.

1. **[!UICONTROL Components Settings]** 의 **[!UICONTROL Social]** 필드에서 추가하거나 제거할 소셜 미디어를 선택합니다.

   ![](assets/email_designer_20.png)

1. **[!UICONTROL Size of images]** 필드에서 아이콘 크기를 선택합니다.

1. 각 소셜 미디어 아이콘을 클릭하여 대상이 리디렉션될 **[!UICONTROL URL]** 을 구성합니다.

   ![](assets/email_designer_21.png)

1. 필요한 경우 **[!UICONTROL Image]** 필드에서 각 소셜 미디어의 아이콘을 변경할 수도 있습니다.

1. 이제 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 및 **[!UICONTROL Border]**&#x200B;를 변경하여 소셜 미디어 아이콘을 추가로 개인화할 수 있습니다.

## 오퍼 결정 {#offer-decision}

**[!UICONTROL Offer decision]** 구성 요소를 사용하여 의사 결정(이전에 오퍼 활동이라고 함)을 메시지에 삽입합니다. 의사 결정 관리 를 활용하여 고객에게 제공할 최상의 오퍼를 선택할 수 있습니다.

관련 항목:

* [의사 결정 관리를 시작합니다](offers/get-started/starting-offer-decisioning.md).
* [메시지에 개인화된 오퍼를 추가합니다](deliver-personalized-offers.md).

