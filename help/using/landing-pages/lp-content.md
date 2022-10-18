---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지별 콘텐츠 정의
description: Journey Optimizer에서 랜딩 페이지별 콘텐츠를 디자인하는 방법 알아보기
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 3%

---

# 랜딩 페이지별 콘텐츠 정의 {#lp-content}

사용자가 랜딩 페이지에서 선택 및 제출 할 수 있는 특정 콘텐츠를 정의하려면 **[!UICONTROL 양식]** 구성 요소. 이렇게 하려면 아래 절차를 따르십시오.

>[!NOTE]
>
>또한 클릭 스루 랜딩 페이지를 **[!UICONTROL 양식]** 구성 요소. 이 경우 랜딩 페이지는 사용자에게 표시되지만, 양식을 제출할 필요는 없습니다. 이 기능은 옵트인 또는 옵트아웃과 같은 수신자의 작업을 수행하지 않고 랜딩 페이지를 쇼케이션하거나 사용자 입력이 필요하지 않은 정보를 제공하려는 경우에만 유용할 수 있습니다.

## 양식 구성 요소 사용 {#use-form-component}

1. 랜딩 페이지별로 끌어서 놓습니다 **[!UICONTROL 양식]** 구성 요소를 생성할 수 있습니다.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >다음 **[!UICONTROL 양식]** 구성 요소는 동일한 페이지에서 한 번만 사용할 수 있습니다.

1. 패턴을 선택합니다. 다음 **[!UICONTROL 양식 콘텐츠]** 오른쪽 팔레트에 탭이 표시되어 양식의 다른 필드를 편집할 수 있습니다.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >로 전환 **[!UICONTROL 양식 스타일]** 언제든지 탭하여 양식 구성 요소 컨텐츠의 스타일을 편집할 수 있습니다. [자세히 보기](#define-lp-styles)

1. 에서 **[!UICONTROL 확인란 1]** 섹션에서 이 확인란에 해당하는 레이블을 편집할 수 있습니다.

1. 이 확인란을 사용하여 사용자를 옵트아웃할지 여부를 정의합니다. 그들은 통신을 받는 것에 동의합니까, 아니면 더 이상 연락하지 않도록 요청합니까?

   ![](assets/lp_designer-form-update.png)

   아래 세 가지 옵션 중에서 선택합니다.

   * **[!UICONTROL 선택 시 옵트인]**: 동의(옵트인)를 하려면 상자를 선택해야 합니다.
   * **[!UICONTROL 체크 아웃한 경우 옵트아웃]**: 사용자는 동의(옵트아웃)를 제거하려면 상자를 선택해야 합니다.
   * **[!UICONTROL 선택 시 옵트인하고, 선택 취소하면 옵트아웃]**: 이 옵션을 사용하면 옵트인/옵트아웃에 대한 단일 확인란을 삽입할 수 있습니다. 사용자는 동의(옵트인)하려면 이 확인란을 선택하고 동의를 제거(옵트아웃)하려면 선택을 해제해야 합니다. 

1. 다음 세 옵션 중에서 업데이트할 항목을 선택합니다.

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL 구독 목록]**: 프로필에서 이 확인란을 선택하면 업데이트되는 구독 목록을 선택해야 합니다. 추가 정보 [구독 목록](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL 채널(이메일)]**: 옵트인 또는 옵트아웃은 전체 채널에 적용됩니다. 예를 들어 옵트아웃하는 프로필에 두 개의 이메일 주소가 있는 경우 두 주소가 모두 모든 통신에서 제외됩니다.

   * **[!UICONTROL 이메일 ID]**: 옵트인 또는 옵트아웃은 랜딩 페이지에 액세스하는 데 사용한 이메일 주소에만 적용됩니다. 예를 들어 프로필에 두 개의 이메일 주소가 있는 경우 옵트인에 사용된 이메일 주소만 브랜드로부터 커뮤니케이션을 받습니다.

1. 클릭 **[!UICONTROL 필드 추가]** > **[!UICONTROL 확인란]** 다른 확인란을 추가합니다. 위의 단계를 반복하여 해당 속성을 정의합니다.

   ![](assets/lp_designer-form-checkbox-2.png)

1. 원하는 확인란을 모두 추가했으면 을 클릭합니다 **[!UICONTROL 클릭유도문안]** 를 클릭하여 해당 섹션을 확장합니다. 여기에서 **[!UICONTROL 양식]** 구성 요소.

   ![](assets/lp_designer-form-call-to-action.png)

1. 버튼을 클릭하면 발생할 작업을 정의합니다.

   * **[!UICONTROL 리디렉션 URL]**: 사용자가 리디렉션될 페이지의 URL을 입력합니다.
   * **[!UICONTROL 확인 텍스트]**: 표시할 확인 텍스트를 입력합니다.
   * **[!UICONTROL 하위 페이지에 링크]**: 구성 [하위 페이지](create-lp.md#configure-subpages) 표시되는 드롭다운 목록에서 선택합니다.

   ![](assets/lp_designer-form-confirmation-action.png)

1. 오류가 발생할 경우 버튼을 클릭하면 발생하는 내용을 정의합니다.

   * **[!UICONTROL 리디렉션 URL]**: 사용자가 리디렉션될 페이지의 URL을 입력합니다.
   * **[!UICONTROL 오류 텍스트]**: 표시할 오류 텍스트를 입력합니다. 를 정의할 때 오류 텍스트를 미리 볼 수 있습니다 [양식 스타일](#define-lp-styles).

   * **[!UICONTROL 하위 페이지에 링크]**: 구성 [하위 페이지](create-lp.md#configure-subpages) 표시되는 드롭다운 목록에서 선택합니다.

   ![](assets/lp_designer-form-error.png)

1. 양식을 제출할 때 추가 업데이트를 수행하려면 다음을 선택합니다 **[!UICONTROL 옵트인]** 또는 **[!UICONTROL 옵트아웃]**, 및에서 구독 목록, 채널 또는 사용된 이메일 주소를 업데이트할지 여부를 정의합니다.

   ![](assets/lp_designer-form-additionnal-update.png)

1. 컨텐츠를 저장하고 페이지 이름 옆에 있는 화살표를 클릭하여 로 돌아갑니다. [랜딩 페이지 속성](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

## 랜딩 페이지 양식 스타일 정의 {#lp-form-styles}

1. 양식 구성 요소 콘텐츠의 스타일을 수정하려면 언제든지 **[!UICONTROL 양식 스타일]** 탭.

   ![](assets/lp_designer-form-style.png)

1. 를 확장합니다. **[!UICONTROL 확인란]** 섹션을 클릭하여 확인란과 해당 텍스트의 모양을 정의합니다. 예를 들어 글꼴 패밀리나 크기, 확인란 테두리 색상을 조정할 수 있습니다.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. 를 확장합니다. **[!UICONTROL 단추]** 구성 요소 양식에서 단추 모양을 수정하는 섹션을 참조하십시오. 예를 들어 테두리를 추가하거나, 마우스로 가리키면 레이블 색상을 편집하거나, 단추 정렬을 조정할 수 있습니다.

   ![](assets/lp_designer-form-style-buttons.png)

   마우스로 가리키면 단추 레이블 색상과 같은 일부 설정을 **[!UICONTROL 미리 보기]** 버튼을 클릭합니다. 랜딩 페이지 테스트에 대해 자세히 알아보기 [여기](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. 를 확장합니다. **[!UICONTROL 양식 레이아웃]** 섹션에 배경색, 패딩 또는 여백과 같은 레이아웃 설정을 편집할 수 있습니다.

   ![](assets/lp_designer-form-style-layout.png)

1. 를 확장합니다. **[!UICONTROL 양식 오류]** 문제가 발생할 경우 표시되는 오류 메시지 표시를 조정하는 섹션을 추가했습니다. 해당 옵션을 선택하여 양식의 오류 텍스트를 미리 봅니다.

   ![](assets/lp_designer-form-error-preview.png)

## 기본 페이지 컨텍스트 사용 {#use-primary-page-context}

동일한 랜딩 페이지 내에서 다른 페이지에서 오는 컨텍스트 데이터를 사용할 수 있습니다.

예를 들어 확인란을 연결하는 경우<!-- or the submission of the page--> 변환 후 [구독 목록](subscription-list.md) 기본 랜딩 페이지에서 &quot;감사합니다&quot; 하위 페이지에서 해당 구독 목록을 사용할 수 있습니다.

기본 페이지의 두 확인란을 두 개의 다른 구독 목록에 연결한다고 가정합니다. 사용자가 이 중 하나를 구독하는 경우 선택한 확인란을 기준으로 양식을 제출할 때 특정 메시지를 표시할 수 있습니다.

이렇게 하려면 아래 절차를 따르십시오.

1. 기본 페이지에서 각 확인란을 관련 구독 목록에 연결합니다. [자세히 알아보기](#use-form-component).

   ![](assets/lp_designer-form-luma-newsletter.png)

1. 하위 페이지에서 텍스트를 삽입할 마우스 포인터를 놓고 선택합니다 **[!UICONTROL 개인화 추가]** 상황별 도구 모음

   ![](assets/lp_designer-form-subpage-perso.png)

1. 에서 **[!UICONTROL 개인화 편집]** 창, 선택 **[!UICONTROL 상황별 특성]** > **[!UICONTROL 랜딩 페이지]** > **[!UICONTROL 기본 페이지 컨텍스트]** > **[!UICONTROL 구독]**.

1. 기본 페이지에서 선택한 모든 구독 목록이 나열됩니다. + 아이콘을 사용하여 관련 항목을 선택합니다.

   ![](assets/lp_designer-form-add-subscription.png)

1. 표현식 편집기 도우미 함수를 사용하여 관련 조건을 추가합니다. [자세히 보기](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >표현식에 하이픈과 같은 특수 문자가 있으면 하이픈을 포함하는 텍스트를 이스케이프 처리해야 합니다.

1. 변경 내용을 저장합니다.

![](assets/lp_designer-form-preview-checked-box.png)

이제 사용자가 확인란 중 하나를 선택하면 양식 제출 시 선택한 확인란에 해당하는 메시지가 표시됩니다.

![](assets/lp_designer-form-thankyou-preview.png)

>[!NOTE]
>
>사용자가 두 개의 확인란을 선택하면 두 텍스트가 표시됩니다.

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [Expression editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->