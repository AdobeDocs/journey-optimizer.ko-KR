---
solution: Journey Optimizer
product: journey optimizer
title: 조건 만들기
description: 조건을 만드는 방법을 알아봅니다
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 조건부, 규칙
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 8%

---

# 조건부 규칙 작업 {#conditions}

조건부 규칙은 프로필의 속성, 세그먼트 멤버십 또는 상황별 이벤트와 같은 다양한 기준에 따라 메시지에 표시할 콘텐츠를 정의하는 규칙 세트입니다.

조건부 규칙은 표현식 편집기를 사용하여 작성되며 컨텐츠에서 재사용하려는 경우 저장할 수 있습니다. [조건부 규칙을 라이브러리에 저장하는 방법 알아보기](#save)

>[!NOTE]
>
>개인에게는 [라이브러리 항목 관리](../administration/ootb-product-profiles.md) 조건부 규칙을 저장하거나 삭제할 수 있는 권한. 저장된 조건은 조직 내의 모든 사용자가 사용할 수 있습니다.

## 조건부 규칙 빌더 액세스 {#access}

조건부 규칙은 **[!UICONTROL 조건]** 표현식 편집기 내의 메뉴로서 다음 중 하나에 액세스할 수 있습니다.

* 이메일 디자이너에서 전자 메일 본문의 구성 요소에 대한 동적 콘텐츠를 활성화하는 경우. [이메일에 다이내믹 콘텐츠를 추가하는 방법 알아보기](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 을 사용하여 개인화를 추가할 수 있는 모든 필드에서 [표현식 편집기](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## 조건부 규칙 만들기 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="조건 만들기"
>abstract="프로필 속성, 상황별 이벤트 또는 대상자를 결합하여 메시지에 표시되어야 하는 콘텐츠를 정의하는 규칙을 작성합니다."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="조건 만들기"
>abstract="프로필 속성, 상황별 이벤트 또는 대상자를 결합하여 메시지에 표시되어야 하는 콘텐츠를 정의하는 규칙을 작성합니다."

조건부 규칙을 만드는 단계는 다음과 같습니다.

1. 액세스 권한 **[!UICONTROL 조건]** 표현식 편집기 또는 이메일 디자이너에서 메뉴를 클릭한 다음 **[!UICONTROL 새로 만들기]**.

1. 필요에 따라 조건부 규칙을 만듭니다. 이렇게 하려면 왼쪽 메뉴에서 원하는 속성을 캔버스로 드래그하여 놓습니다.

   속성을 캔버스에 결합하는 단계는 세그먼트 작성 경험과 유사합니다. 규칙 빌더 캔버스로 작업하는 방법에 대한 자세한 내용은 [이 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   속성은 다음 세 개의 탭으로 구성됩니다.

   * **[!UICONTROL 프로필]**:
      * **[!UICONTROL 세그먼트 멤버십]** 모든 세그먼트 속성(예: 상태, 버전 등)을 나열합니다 대상 [Adobe Experience Platform 세그멘테이션 서비스](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL XDM 개별 프로필]** 에는 [XDM(경험 데이터 모델) 스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR) Adobe Experience Platform에 정의됩니다.
   * **[!UICONTROL 상황별]**: 여정에서 메시지를 사용하는 경우 이 탭을 통해 컨텍스트 여정 필드를 사용할 수 있습니다.
   * **[!UICONTROL 대상]**: 에서 만들어진 세그먼트에서 생성된 모든 대상을 나열합니다. [Adobe Experience Platform 세그멘테이션 서비스](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. 조건부 규칙이 준비되면 메시지에 추가하여 동적 콘텐츠를 만들 수 있습니다. [다이내믹 컨텐츠를 추가하는 방법 알아보기](dynamic-content.md)

   규칙을 저장하여 다시 사용할 수도 있습니다. [조건을 저장하는 방법 알아보기](#save)

## 조건부 규칙 저장 {#save}

자주 다시 사용할 조건 규칙이 있는 경우 조건 라이브러리에 해당 규칙을 저장할 수 있습니다. 저장된 모든 규칙은 공유되며 조직 내의 개인이 액세스하여 사용할 수 있습니다.

>[!NOTE]
>
>여정 컨텍스트 특성을 활용하는 조건부 규칙은 라이브러리에 저장할 수 없습니다.

1. 조건 편집 화면에서 **[!UICONTROL 조건 저장]** 버튼을 클릭합니다.

1. 규칙에 이름과 설명(선택 사항)을 지정한 다음 **[!UICONTROL 추가]**.

   ![](assets/conditions-name-description.png)

1. 조건부 규칙이 라이브러리에 저장됩니다. 이제 이 콘텐츠를 사용하여 메시지에 동적 콘텐츠를 만들 수 있습니다. [다이내믹 컨텐츠를 추가하는 방법 알아보기](dynamic-content.md)

## 저장된 조건부 규칙 편집 및 삭제 {#edit-delete}

줄임표 단추를 사용하여 언제든지 조건부 규칙을 삭제할 수 있습니다.

![](assets/conditions-open.png)

라이브러리에 저장된 조건부 규칙은 수정할 수 없습니다. 그러나 여전히 이 매개 변수를 사용하여 새 규칙을 만들 수 있습니다. 이렇게 하려면 조건부 규칙을 열고 원하는 대로 변경한 다음 라이브러리에 저장합니다. [라이브러리에 조건을 저장하는 방법을 알아봅니다](#save)
