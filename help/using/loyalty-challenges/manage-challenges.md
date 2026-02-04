---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 관리
description: Adobe Journey Optimizer에서 발생하는 충성도 문제를 관리, 모니터링 및 최적화하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---


# 과제 관리 {#manage-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md) - 개요, 워크플로, 사전 요구 사항
* [충성도 문제 액세스](access-loyalty-challenges.md) - 인벤토리 및 필터링
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [작업 만들기](create-tasks.md) - 과제 작업 정의
* **문제 관리** ◀︎**현재 상태** - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 과제 관리 {#manage-challenges-section}

### 과제 라이프사이클 {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

과제는 라이프사이클 동안 다양한 상태로 이동합니다.

* **초안**: 도전이 만들어지거나 편집되고 있으며 아직 고객에게 제공되지 않습니다.
* **게시됨**: 도전이 활성 상태이므로 연결된 여정이 생성되었습니다.

### 문제 편집 {#edit-challenges}

과제 인벤토리에서 과제를 열어 과제를 편집할 수 있습니다. 편집 동작은 과제 상태에 따라 다릅니다.

**초안 문제**: 전체 편집 기능이 있습니다. 모든 속성, 작업, 콘텐츠 및 메시징은 제한 없이 수정할 수 있습니다.

**게시된 문제**: 편집을 위해 게시된 문제를 열면 먼저 문제를 초안 상태로 되돌려야 합니다.

* 자동 생성된 여정에 직접 맞춤화된 내용은 손실됩니다
* 문제가 초안 상태로 돌아갑니다.
* 변경 후 문제를 저장하고 다시 게시해야 합니다
* 업데이트된 문제를 고객에게 제공하려면 연결된 여정을 다시 활성화해야 합니다

>[!IMPORTANT]
>
>게시된 문제를 초안으로 되돌리는 작업은 실행 취소할 수 없습니다. 계속하기 전에 활성 여정에 미치는 영향을 고려하십시오.

### 과제 복제 {#duplicate-challenges}

문제를 복제하면 모든 작업, 콘텐츠 및 메시징이 그대로 유지되는 정확한 복사본이 만들어지므로 처음부터 새로 시작하지 않고도 신속하게 새 버전을 만들 수 있습니다.

문제를 복제하려면 다음을 수행하십시오.

1. **[!UICONTROL 과제]** 탭으로 이동하여 복제할 과제를 찾습니다.

1. 해당 챌린지 옆에 있는 ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.

1. 문제 사본이 생성됩니다. 복제된 문제를 열고 필요한 속성을 수정합니다.

1. 복제된 문제를 저장하고 관련 여정을 생성합니다.

### 성능 모니터링 {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

주요 지표를 통해 과제 성과를 추적합니다.

* **기여도 지표**:
   * 등록: 과제에 참여한 고객 수
   * 활성 참가자: 현재 이 문제에 관여하는 고객
* **완료 지표**:
   * 완료율: 문제를 완료한 등록된 고객의 백분율
   * 평균 완료 시간: 모든 작업을 완료하는 데 걸린 평균 시간
* **보상 지표**:
   * 분배된 총 보상: 주어진 모든 보상의 값을 집계합니다.
   * 유형별 보상: 보상 범주별 보상 분류
* **참여 지표**:
   * 콘텐츠 카드 노출 횟수: 챌린지 콘텐츠 카드가 표시된 횟수
   * 메시지 게재: 모든 채널에서 성공적으로 전송된 메시지 수

성능 데이터에 액세스하려면:

1. 충성도 과제 인벤토리의 **[!UICONTROL 과제]** 탭으로 이동합니다.

1. 모니터링할 문제를 선택합니다.

1. 실시간 지표 및 분석을 보려면 **[!UICONTROL 성능]** 탭을 여십시오.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

또한 [자동 생성된 여정 보고서](../reports/journey-global-report-cja.md)에서 자세한 성능 데이터에 액세스하여 추가적인 통찰력과 이전 추세를 확인할 수 있습니다.

## 작업 관리 {#manage-tasks}

작업은 여러 어려움에 걸쳐 사용할 수 있는 재사용 가능한 구성 요소입니다. 작업을 효과적으로 관리하면 충성도 프로그램 전반에서 일관성을 유지할 수 있으며 작업 정의를 중앙에서 더 쉽게 업데이트할 수 있습니다. 하나의 과제에서 생성된 작업은 다른 과제에서 재사용할 수 있어 중복을 줄이고 표준화를 유지할 수 있다.

### 작업 편집 {#edit-tasks}

작업 인벤토리에서 기존 작업을 편집할 수 있습니다. 다음 사항을 고려하십시오.

* **활성 작업에 사용되지 않는 작업**: 자유롭게 편집할 수 있습니다. 영향을 주지 않고 모든 속성을 수정할 수 있습니다.
* **실시간 어려움에 사용되는 작업**: 변경 사항은 작업을 사용하는 모든 어려움에 영향을 미치므로 주의하십시오. 수정 사항은 참조하는 모든 어려움에 즉시 적용됩니다

작업을 편집하려면:

1. 충성도 과제 인벤토리의 **[!UICONTROL 작업]** 탭으로 이동합니다.

1. 편집할 작업을 찾습니다.

1. 작업 이름을 선택하여 편집 모드로 엽니다.

1. 필요에 따라 작업 속성을 수정합니다.
   * 작업 이름 또는 설명 업데이트
   * 활동 유형 또는 속성 변경
   * 적격 항목 및 제외 조정
   * 수량 또는 금액 소요량 수정

1. 변경 내용을 저장합니다.

>[!WARNING]
>
>라이브 카피에서 활발하게 사용되는 작업을 편집할 때 원본을 수정하지 않고 새 버전으로 중복 항목을 만드는 것이 좋습니다. 이렇게 하면 활성 문제에 대한 의도하지 않은 변경이 방지되며 수정 사항을 적용하기 전에 테스트할 수 있습니다.

### 작업 삭제 {#delete-tasks}

작업은 현재 어려움에 사용되지 않는 경우에만 삭제할 수 있습니다. 작업을 삭제하기 전에:

* 작업 인벤토리에서 **[!UICONTROL 어려움에 사용됨]** 수를 확인합니다.
* 작업을 참조하는 초안, 예약됨 또는 라이브 과제 없음

작업을 삭제하려면 다음을 수행하십시오.

1. 충성도 과제 인벤토리의 **[!UICONTROL 작업]** 탭으로 이동합니다.

1. 삭제할 작업을 찾습니다.

1. **[!UICONTROL 어려움에 사용됨]** 수가 0으로 표시되는지 확인하십시오. 카운트가 0보다 큰 경우 삭제하기 전에 먼저 모든 도전에서 작업을 제거해야 합니다.

1. 작업 옆에 있는 ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 선택합니다.

1. **[!UICONTROL 삭제]**&#x200B;를 선택하세요.

1. 대화 상자에서 삭제를 확인합니다.

>[!NOTE]
>
>작업이 모든 과제(초안, 예약됨 또는 라이브)에서 사용되는 경우 삭제하려면 먼저 모든 과제에서 해당 과제를 제거해야 합니다. 나중에 필요할 수 있는 경우 작업을 삭제하지 않고 보관하거나 복제하는 것이 좋습니다.
