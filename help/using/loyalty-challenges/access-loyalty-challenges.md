---
solution: Journey Optimizer
product: journey optimizer
title: 액세스 충성도 문제
description: Adobe Journey Optimizer에서 충성도 문제를 액세스, 검색 및 필터링하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# 액세스 충성도 문제 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md) - 개요, 워크플로, 사전 요구 사항
* **충성도 문제 액세스** ◀︎**현재 상태** - 인벤토리 및 필터링
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [작업 만들기](create-tasks.md) - 과제 작업 정의
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 충성도 과제 인벤토리 액세스 {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

충성도 문제에 액세스하려면 Journey Optimizer으로 이동하여 **[!UICONTROL 고객 여정]** 섹션에서 **[!UICONTROL 충성도 문제]**&#x200B;를 선택하십시오.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

충성도 과제 페이지가 두 가지 탭과 함께 표시됩니다.

* **[!UICONTROL 과제]**: 모든 충성도 과제 보기 및 관리

* **[!UICONTROL 작업]**: 문제 발생 시 재사용할 수 있는 모든 작업을 보고 관리합니다.

## 과제 인벤토리 {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

과제 탭에는 마지막으로 수정한 날짜별로 정렬된 모든 과제가 표시되며, 가장 최근에 수정한 과제가 먼저 표시됩니다. 다음 정보가 표시됩니다.

* **[!UICONTROL 도전 이름]**: 도전에 할당한 이름
* **[!UICONTROL 상태]**: 현재 도전 상태(아래 상태 설명 참조)
* **[!UICONTROL 유형]**: 챌린지 유형(표준, 연속 또는 순차적)
* **[!UICONTROL 시작 날짜]**: 도전이 활성화될 때
* **[!UICONTROL 종료 날짜]**: 도전이 만료될 때
* **[!UICONTROL 작성자]**: 문제를 만든 사용자
* **[!UICONTROL 마지막 수정 날짜]**: 마지막 수정 날짜 및 시간
* **[!UICONTROL 태그]**: 조직의 챌린지에 적용되는 모든 태그

### 과제 상태 {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

문제는 라이프사이클에서 현재 상태를 나타내는 다양한 상태로 표시됩니다.

* **초안**: 문제를 만들거나 편집하는 중입니다.
* **예약됨**: 도전이 게시되며 시작 날짜에 활성화됩니다
* **Live**: 도전이 활성 상태이며 고객이 참여할 수 있습니다.
* **완료됨**: 도전 종료 날짜가 지났거나 목표를 달성했습니다.
* **중지됨**: 완료 전에 문제를 수동으로 중지했습니다.
* **보관됨**: 문제를 조직용으로 보관했습니다.

상태 전환 및 과제 주기에 대한 자세한 내용은 [과제 주기](manage-challenges.md#challenge-lifecycle)를 참조하십시오.

### 문제 검색 및 필터링 {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

검색 및 필터를 사용하여 문제를 신속하게 찾을 수 있습니다.

**검색:**

* 검색창을 사용하여 과제 이름 또는 설명에 키워드를 입력하여 과제를 찾습니다. 입력하면 검색 결과가 실시간으로 표시됩니다.

**필터:**

* 하나 이상의 필터를 적용하여 결과 범위를 좁힙니다.
   * **상태**: 문제 상태(초안, 예약됨, 라이브, 완료됨, 중지됨, 보관됨)별로 필터링합니다.
   * **유형**: 챌린지 유형(표준, 연속, 순차적)별로 필터링
   * **날짜**: 시작 날짜 또는 종료 날짜 범위별로 필터링
   * **태그**: 문제에 적용된 태그로 필터링

여러 필터를 동시에 결합할 수 있습니다. 예를 들어, &quot;2024년 여름&quot;으로 태그가 지정된 라이브 Standard 문제를 필터링하여 활성 시즌 캠페인을 신속하게 찾을 수 있습니다.

필터를 지우려면 **[!UICONTROL 모두 지우기]**&#x200B;를 선택하거나 개별 필터를 제거하십시오.

### 문제 해결 {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

과제 탭에서 다음과 같은 과제에 대해 빠른 작업을 수행할 수 있습니다.

* **도전 세부 정보 보기**: 도전 이름을 선택하여 세부 정보 페이지를 엽니다.
* **문제 편집**: **[!UICONTROL 추가 작업]** 메뉴(세 점)를 선택하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.
* **문제 복제**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* **실시간 챌린지 중지**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 중지]**&#x200B;를 선택하세요.
* **문제 보관**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 보관]** 선택
* **초안 과제 삭제**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 삭제]**(초안에만 사용 가능)을 선택합니다.

편집 제한 사항, 복제 전략, 성능 모니터링 및 문제 해결 등 생성 후 문제 관리에 대한 자세한 내용은 [문제 관리](manage-challenges.md)를 참조하십시오.

## 작업 인벤토리 {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

작업 탭에는 여러 어려움에 걸쳐 사용할 수 있는 재사용 가능한 모든 작업이 표시됩니다. 여기에서 만든 작업은 문제를 만들거나 편집할 때 선택할 수 있습니다.

작업 인벤토리에는 다음 정보가 표시됩니다.

* **[!UICONTROL 작업 이름]**: 작업에 할당한 이름
* **[!UICONTROL 작업 유형]**: 작업 유형(구매, 지출 금액, 방문, 참여, 사용자 지정 이벤트)
* **[!UICONTROL 설명]**: 작업에 필요한 사항에 대한 간략한 설명
* **[!UICONTROL 만든 사람]**: 작업을 만든 사용자
* **[!UICONTROL 마지막 수정 날짜]**: 마지막 수정 날짜 및 시간
* **[!UICONTROL 어려움에 사용됨]**: 현재 이 작업을 사용하는 문제 수

### 작업에 대한 작업 수행 {#tasks-actions}

작업 탭에서 작업에 대한 작업을 수행할 수 있습니다.

* **작업 세부 정보 보기**: 전체 구성을 보려면 작업 이름을 선택하십시오.
* **작업 편집**: **[!UICONTROL 추가 작업]** 메뉴(세 점)를 선택하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.
* **작업 복제**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 복제]** 선택
* **작업 삭제**: **[!UICONTROL 추가 작업]** 메뉴를 선택하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다(활성 문제에 사용되지 않는 경우에만).
* **사용량 보기**: 현재 작업을 사용 중인 문제 확인

## 다음 단계 {#next-steps}

이제 충성도 과제 인벤토리에 액세스하고 탐색하는 방법을 알았습니다.

* [과제 만들기](create-challenges.md) - 첫 번째 과제를 만들고 작업을 구성하는 방법에 대해 알아봅니다.
* [작업 만들기](create-tasks.md) - 문제에 대해 재사용 가능한 작업을 정의하는 방법을 알아봅니다.
* [문제 관리](manage-challenges.md) - 문제를 편집, 모니터링 및 최적화하는 방법을 알아봅니다.
