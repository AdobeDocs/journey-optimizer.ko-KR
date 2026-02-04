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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '483'
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

충성도 문제에 액세스하려면 Journey Optimizer으로 이동하여 **[!UICONTROL 여정 관리]** 섹션에서 **[!UICONTROL 충성도 문제(Beta)]**&#x200B;을(를) 선택하십시오.

## 과제 인벤토리 {#challenges-tab}

**[!UICONTROL 과제]** 탭에는 마지막 수정 날짜별로 정렬된 모든 과제가 표시되며, 가장 최근에 수정된 과제가 먼저 표시됩니다.

![](assets/challenges-inventory.png)

다음 정보가 표시됩니다.

* **[!UICONTROL 도전]**: 도전에 할당한 이름
* **[!UICONTROL 상태]**: 현재 도전 상태입니다. 상태 전환 및 과제 주기에 대한 자세한 내용은 [과제 주기](manage-challenges.md#challenge-lifecycle)를 참조하십시오.
* **[!UICONTROL 설명]**: 도전 목적에 대한 간략한 설명
* **[!UICONTROL 작업]**: 챌린지에 구성된 작업 수
* **[!UICONTROL 여정]**: 문제와 연결된 자동 생성된 여정에 대한 링크
* **[!UICONTROL 상태]**: 연결된 여정의 현재 상태(초안, 실시간, 중지됨 등)
* **[!UICONTROL 시작 날짜(UTC)]**: 챌린지가 활성화될 때
* **[!UICONTROL 종료 날짜(UTC)]**: 챌린지가 만료될 때
* **[!UICONTROL 마지막 수정 날짜]**: 마지막 수정 날짜 및 시간
* **[!UICONTROL 만든 날짜]**: 문제를 만든 날짜
* **[!UICONTROL 작성자]**: 문제를 만든 사용자

과제 탭에서 다음과 같은 과제에 대해 빠른 작업을 수행할 수 있습니다.

* **도전 세부 정보 보기**: 도전 이름을 선택하여 세부 정보 페이지를 엽니다.
* **문제 복제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* **초안 챌린지 삭제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.

생성 후 문제 관리에 대한 자세한 내용은 [문제 및 작업 관리](manage-challenges.md)를 참조하십시오.

## 작업 인벤토리 {#tasks-tab}

작업 탭에는 여러 어려움에 걸쳐 사용할 수 있는 재사용 가능한 모든 작업이 표시됩니다. 여기에서 만든 작업은 문제를 만들거나 편집할 때 선택할 수 있습니다.

![](assets/tasks-inventory.png)

작업 인벤토리에는 다음 정보가 표시됩니다.

* **[!UICONTROL 작업 이름]**: 작업에 할당한 이름
* **[!UICONTROL 설명]**: 작업에 필요한 사항에 대한 간략한 설명
* **[!UICONTROL 작업 활동]**: 활동 유형(구매, 지출)
* **[!UICONTROL SKU]**: 적격 및/또는 제외된 항목
* **[!UICONTROL 마지막 수정 날짜]**: 마지막 수정 날짜 및 시간
* **[!UICONTROL 마지막으로 수정한 사람]**: 작업을 수정한 마지막 사용자
* **[!UICONTROL 만든 날짜]**: 작업을 만든 날짜
* **[!UICONTROL 만든 사람]**: 작업을 만든 사용자

작업 탭에서 작업에 대한 빠른 작업을 수행할 수 있습니다.

* **작업 세부 정보 보기**: 전체 구성을 보려면 작업 이름을 선택하십시오.
* **작업 복제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* **작업 삭제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.

생성 후 작업 관리에 대한 자세한 내용은 [문제 및 작업 관리](manage-challenges.md)를 참조하십시오.

## 다음 단계 {#next-steps}

이제 충성도 과제 인벤토리에 액세스하고 탐색하는 방법을 알았습니다.

* [과제 만들기](create-challenges.md) - 첫 번째 과제를 만들고 작업을 구성하는 방법에 대해 알아봅니다.
* [작업 만들기](create-tasks.md) - 문제에 대해 재사용 가능한 작업을 정의하는 방법을 알아봅니다.
* [문제 관리](manage-challenges.md) - 문제를 편집, 모니터링 및 최적화하는 방법을 알아봅니다.
