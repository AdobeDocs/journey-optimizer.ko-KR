---
solution: Journey Optimizer
product: journey optimizer
title: 시각적 조각 사용
description: Journey Optimizer 캠페인 및 여정에서 이메일을 만들 때 시각적 조각을 사용하는 방법을 알아봅니다
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 7a8a0c133318b0bfc33b0fdb294e5b9ef53de9a5
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 2%

---

# 이메일에 비주얼 조각 추가 {#use-visual-fragments}

조각은 Journey Optimizer 캠페인, 여정 또는 콘텐츠 템플릿 간의 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다. 이 기능을 사용하면 마케팅 사용자가 향상된 디자인 프로세스에서 이메일 콘텐츠를 빠르게 조합하는 데 사용할 수 있는 여러 사용자 지정 콘텐츠 블록을 미리 빌드할 수 있습니다. [조각을 만들고 관리하는 방법을 알아보세요](../content-management/fragments.md).

➡️ [이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다.](../content-management/fragments.md#video-fragments)

## 조각 사용 {#use-fragment}

이메일에 조각을 사용하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>주어진 게재에서 최대 30개의 조각을 추가할 수 있습니다. 조각은 최대 1개 수준까지만 중첩할 수 있습니다.


1. [전자 메일 Designer](get-started-email-design.md)을(를) 사용하여 전자 메일 또는 템플릿 콘텐츠를 엽니다.

1. 왼쪽 레일에서 **[!UICONTROL 조각]** 아이콘을 선택합니다.

   ![](assets/fragments-in-designer.png)

1. 현재 샌드박스에서 만든 모든 시각적 조각 목록이 표시됩니다. 만든 날짜별로 정렬됩니다. 최근에 추가된 시각적 조각이 목록에 먼저 표시됩니다. 다음과 같은 작업을 수행할 수 있습니다.

   * 레이블 입력을 시작하여 특정 조각을 검색합니다.
   * 오름차순 또는 내림차순으로 조각을 정렬합니다.
   * 조각이 표시되는 방법(카드 또는 목록 보기)을 변경합니다.
   * 목록을 새로 고칩니다.

   >[!NOTE]
   >
   >콘텐츠를 편집하는 동안 일부 조각이 수정되거나 추가된 경우 목록이 최신 변경 내용으로 업데이트됩니다.

1. 목록의 조각을 삽입할 영역으로 끌어다 놓습니다.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >콘텐츠에 **초안** 또는 **라이브** 조각을 추가할 수 있습니다. 하지만 초안 상태의 조각을 사용 중인 경우에는 여정 또는 캠페인을 활성화할 수 없습니다. 여정 또는 캠페인 게시 시 초안 조각에 오류가 표시되며 이를 승인해야 게시할 수 있습니다.

1. 다른 구성 요소와 마찬가지로 콘텐츠에서 조각을 이동할 수 있습니다.

1. 조각을 선택하여 오른쪽에 해당 창을 표시합니다. 여기에서 콘텐츠에서 조각을 삭제하거나 복제할 수 있습니다. 조각 위에 표시되는 상황별 메뉴에서 직접 이러한 작업을 수행할 수도 있습니다.

   ![](assets/fragment-right-pane.png)

1. **[!UICONTROL 설정]** 탭에서 다음을 수행할 수 있습니다.

   * 조각을 표시할 장치를 선택합니다.
   * 필요한 경우 새 탭에서 조각을 열어 편집합니다. [자세히 알아보기](../content-management/fragments.md#edit-fragments)
   * 참조 살펴보기. [자세히 알아보기](../content-management/fragments.md#explore-references)

1. **[!UICONTROL 스타일]** 탭을 사용하여 조각을 추가로 사용자 지정할 수 있습니다.

1. 필요한 경우 원본 조각으로 상속을 중단할 수 있습니다. [자세히 알아보기](#break-inheritance)

1. 원하는 만큼 조각을 추가하고 변경 내용을 **[!UICONTROL 저장]**&#x200B;합니다.

## 암시적 변수 사용 {#implicit-variables-in-fragments}

암시적 변수는 기존 조각 기능을 향상시켜 콘텐츠 재사용 가능성 및 스크립팅 사용 사례의 효율성을 개선합니다. 조각은 입력 변수를 사용하고 캠페인 및 여정 콘텐츠에 사용할 수 있는 출력 변수를 만들 수 있습니다.

[이 섹션](../personalization/use-expression-fragments.md#implicit-variables)에서 암시적 변수를 사용하는 방법을 알아봅니다.

## 편집 가능한 필드 사용자 지정 {#customize-fields}

선택한 조각의 특정 부분을 편집할 수 있게 만든 경우 조각을 콘텐츠에 추가한 후 기본값을 무시할 수 있습니다. [조각을 사용자 지정할 수 있게 만드는 방법을 알아보세요](../content-management/customizable-fragments.md)

조각에서 편집 가능한 필드를 사용자 정의하려면 다음 단계를 수행합니다.

1. 콘텐츠에 조각을 추가합니다.

1. 오른쪽의 속성 창을 열려면 이 옵션을 선택합니다.

   조각에서 편집 가능한 모든 필드는 **조각** 섹션 아래의 **설정** 탭에 표시됩니다.

1. 오른쪽 창에서 편집 가능한 필드를 선택하면 중앙 미리 보기 창에 녹색으로 강조 표시되어 콘텐츠에서 해당 위치를 쉽게 식별할 수 있습니다.

   아래 예제에서 **소스** 및 **대체 텍스트** 이미지와 &quot;여기를 클릭하세요&quot; 단추 **URL**&#x200B;을(를) 편집할 수 있습니다.

   ![](assets/fragment-editable.png)

## 상속 중단 {#break-inheritance}

시각적 조각을 편집하면 변경 사항이 동기화됩니다. 모든 초안 또는 라이브 여정/캠페인 및 해당 조각을 포함하는 콘텐츠 템플릿에 자동으로 전파됩니다.

이메일 또는 콘텐츠 템플릿에 추가되면 조각은 기본적으로 동기화됩니다. 그러나 원본 조각에서 상속을 중단할 수 있습니다. 이 경우 조각의 콘텐츠가 현재 디자인에 복사되며, 변경 사항은 더 이상 동기화되지 않습니다.

상속을 중단하려면 아래 단계를 수행합니다.

1. 조각을 선택합니다.

1. 상황별 툴바에서 잠금 해제 아이콘을 클릭합니다.

   ![](assets/fragment-break-inheritance.png)

1. 해당 조각은 원래 조각에 더 이상 연결되지 않는 독립 실행형 요소가 됩니다. 콘텐츠의 다른 콘텐츠 구성 요소로 편집합니다. [자세히 알아보기](content-components.md)
