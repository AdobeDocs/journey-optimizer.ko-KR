---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 액세스 및 관리
description: Adobe Journey Optimizer에서 충성도 문제 및 작업에 액세스하고, 관리하고, 구성하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# 충성도 문제 액세스 및 관리 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md) - 개요, 워크플로, 사전 요구 사항
* **충성도 문제 액세스** ◀︎**현재 상태** - 인벤토리, 문제 및 작업 관리
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [작업 만들기](create-tasks.md) - 과제 작업 정의

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 단골 과제 액세스

충성도 문제에 액세스하려면 Journey Optimizer으로 이동하여 **[!UICONTROL 여정 관리]** 섹션에서 **[!UICONTROL 충성도 문제(Beta)]**&#x200B;을(를) 선택하십시오.

충성도 과제 인터페이스는 모든 과제와 작업을 중앙 집중식으로 보고, 관리하고, 구성할 수 있는 위치를 제공합니다. 다음 두 가지 기본 인벤토리에 액세스할 수 있습니다.

* **과제 인벤토리**: 모든 충성도 과제를 확인 및 관리하고, 상태를 모니터링하며, 빠른 작업을 수행합니다.
* **작업 인벤토리**: 여러 문제 간에 사용할 수 있는 재사용 가능한 작업을 찾아봅니다.

## 과제 인벤토리 {#challenges-tab}

**[!UICONTROL 과제]** 탭에는 마지막 수정 날짜별로 정렬된 모든 과제가 표시되며, 가장 최근에 수정된 과제가 먼저 표시됩니다.

![](assets/challenges-inventory.png)

표시되는 키 정보:

* **[!UICONTROL 도전]**: 도전 이름
* **[!UICONTROL 상태]**: 현재 도전 상태(초안 또는 게시됨)
* **[!UICONTROL 작업]**: 챌린지에 구성된 작업 수
* **[!UICONTROL 여정]**: 문제와 연결된 자동 생성된 여정에 대한 링크
* **[!UICONTROL 상태]**: 연결된 여정의 현재 상태(초안, 실시간, 중지됨 등)
* **[!UICONTROL 시작/종료 날짜(UTC)]**: 도전이 활성화되고 만료되는 시기

과제 탭에서 다음과 같은 과제에 대한 작업을 수행할 수 있습니다.

* **질문 보기**: 질문 이름을 선택하여 세부 정보 페이지를 엽니다.
* **문제 복제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다. 모든 작업, 콘텐츠 및 메시징이 그대로 유지되는 복사본이 만들어집니다.
* **챌린지 삭제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.
* **챌린지 편집**: 챌린지 이름을 선택하여 세부 정보 페이지를 열고 편집합니다.

  편집하기 위해 게시된 문제를 열면 먼저 문제를 초안 상태로 되돌려야 합니다.

   * 자동 생성된 여정에 직접 맞춤화된 내용은 손실됩니다
   * 문제가 초안 상태로 돌아갑니다.
   * 변경 후 문제를 저장하고 다시 게시해야 합니다
   * 업데이트된 문제를 고객에게 제공하려면 연결된 여정을 다시 게시해야 합니다

  >[!IMPORTANT]
  >
  >게시된 문제를 초안으로 되돌리는 작업은 실행 취소할 수 없습니다. 계속하기 전에 활성 여정에 미치는 영향을 고려하십시오.

## 작업 인벤토리 {#tasks-tab}

**[!UICONTROL 작업]** 탭에는 여러 문제에 걸쳐 사용할 수 있는 재사용 가능한 모든 작업이 표시됩니다. 여기에서 만든 작업은 문제를 만들거나 편집할 때 선택할 수 있습니다.

![](assets/tasks-inventory.png)

표시되는 키 정보:

* **[!UICONTROL 작업 이름]**: 작업에 할당한 이름
* **[!UICONTROL 설명]**: 작업에 필요한 사항에 대한 간략한 설명
* **[!UICONTROL 작업 활동]**: 활동 유형(구매, 지출)
* **[!UICONTROL SKU]**: 적격 및/또는 제외된 항목
* **[!UICONTROL 어려움에 사용됨]**: 현재 이 작업을 사용하는 문제 수

작업 탭에서 작업에 대한 작업을 수행할 수 있습니다.

* **작업 보기/편집**: 전체 구성을 보고 작업을 편집하려면 작업 이름을 선택하십시오.
* **작업 복제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* **작업 삭제**: ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.
