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
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# 이메일에 시각적 개체 조각 추가 {#use-visual-fragments}

에서 시각적 조각을 사용할 수 있습니다. [이메일](get-started-email-design.md) 여정, 캠페인 내 또는 [콘텐츠 템플릿](../content-management/content-templates.md).

>[!NOTE]
>
>에서 조각을 만들고 관리하는 방법 알아보기 [이 섹션](../content-management/fragments.md).

➡️ [이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다.](../content-management/fragments.md#video-fragments)

## 조각 사용 {#use-fragment}

1. 을(를) 사용하여 이메일 또는 템플릿 콘텐츠를 엽니다. [이메일 디자이너](get-started-email-design.md).

1. 다음 항목 선택 **[!UICONTROL 조각]** 왼쪽 레일의 아이콘

   ![](assets/fragments-in-designer.png)

1. 현재 샌드박스에서 만든 모든 시각적 조각 목록이 표시됩니다. 다음과 같은 작업을 수행할 수 있습니다.

   * 레이블 입력을 시작하여 특정 조각을 검색합니다.
   * 오름차순 또는 내림차순으로 조각을 정렬합니다.
   * 조각이 표시되는 방법(카드 또는 목록 보기)을 변경합니다.

   >[!NOTE]
   >
   >조각은 생성 날짜별로 정렬됩니다. 최근에 추가된 시각적 조각이 목록에 먼저 표시됩니다.

1. 목록을 검색하고 새로 고칠 수 있습니다.

   >[!NOTE]
   >
   >콘텐츠를 편집하는 동안 일부 조각이 수정되거나 추가된 경우 목록이 최신 변경 내용으로 업데이트됩니다.

1. 목록의 조각을 삽입할 영역으로 끌어다 놓습니다.

   ![](assets/fragment-insert.png)

1. 다른 구성 요소와 마찬가지로 콘텐츠에서 조각을 이동할 수 있습니다.

1. 조각을 선택하여 오른쪽에 해당 창을 표시합니다. 여기에서 콘텐츠에서 조각을 삭제하거나 복제할 수 있습니다. 조각 위에 표시되는 상황별 메뉴에서 직접 이러한 작업을 수행할 수도 있습니다.

   ![](assets/fragment-right-pane.png)

1. 다음에서 **[!UICONTROL 설정]** 탭에서 다음 작업을 수행할 수 있습니다.

   * 조각을 표시할 장치를 선택합니다.
   * 필요한 경우 새 탭에서 조각을 열어 편집합니다. [자세히 알아보기](../content-management/fragments.md#edit-fragments)
   * 참조 살펴보기. [자세히 알아보기](../content-management/fragments.md#explore-references)

1. 다음을 사용하여 조각을 추가로 사용자 정의할 수 있습니다. **[!UICONTROL 스타일]** 탭.

1. 필요한 경우 원본 조각으로 상속을 중단할 수 있습니다. [자세히 알아보기](#break-inheritance)

1. 원하는 만큼 조각을 추가하고 **[!UICONTROL 저장]** 변경 사항.

## 상속 중단 {#break-inheritance}

시각적 조각을 편집하면 변경 사항이 동기화됩니다. 모든 사용자에게 자동으로 전파됩니다 **[!UICONTROL 초안]** 여정/캠페인 및 해당 조각을 포함하는 콘텐츠 템플릿.

>[!NOTE]
>
>변경 사항은에서 사용하는 이메일에 전파되지 않습니다. **[!UICONTROL 라이브]** 여정 또는 캠페인.

이메일 또는 콘텐츠 템플릿에 추가되면 조각은 기본적으로 동기화됩니다.

그러나 원본 조각에서 상속을 중단할 수 있습니다. 이 경우 조각의 콘텐츠가 현재 디자인에 복사되며, 변경 사항은 더 이상 동기화되지 않습니다.

상속을 중단하려면 아래 단계를 수행합니다.

1. 조각을 선택합니다.

1. 상황별 툴바에서 잠금 해제 아이콘을 클릭합니다.

   ![](assets/fragment-break-inheritance.png)

1. 해당 조각은 원래 조각에 더 이상 연결되지 않는 독립 실행형 요소가 됩니다. 콘텐츠의 다른 콘텐츠 구성 요소로 편집합니다. [자세히 알아보기](content-components.md)
