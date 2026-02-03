---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 시작
description: 매력적인 충성도 프로그램을 제작하기 위해 Adobe Journey Optimizer에서 충성도 문제를 만들고 관리하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 3%

---


# 충성도 문제 시작 {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

충성도 문제를 사용하면 고객을 위한 개인화된 참여 오퍼를 만들어 충성도 프로그램을 규모에 맞게 오케스트레이션할 수 있습니다. 특정 작업 및 이정표를 통해 문제를 디자인하고, 이를 완료한 고객에게 보상하며, Adobe Journey Optimizer 채널을 통해 경험을 전달할 수 있습니다.

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* **충성도 문제 시작** ◀︎**현재 상태** - 빠른 개요 및 다음 단계
* [충성도 문제 이해](get-started.md) - 기능, 워크플로, 사전 요구 사항
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

## 빠른 개요 {#quick-overview}

충성도 문제를 사용하여 다음을 수행할 수 있습니다.

* **세 가지 유형의 문제 만들기**: 표준(임의 작업), 연속(반복 작업) 또는 순차적(순차 작업)
* **과제 콘텐츠 디자인**: 콘텐츠 카드를 사용하여 고객 장치에서 과제를 표시합니다
* **작업 요구 사항 설정**: 보상이 있는 구매, 방문 또는 사용자 지정 이벤트와 같은 작업을 정의합니다.
* **다중 채널 알림 보내기**: 주요 단계에서 인앱, 이메일 및 푸시를 통해 메시지를 전달합니다.
* **성능 추적**: 자동 생성된 여정 및 기본 제공 보고서를 통해 모니터링

## 작동 방식 {#how-it-works-overview}

충성도 문제를 만드는 것은 다음 워크플로를 따릅니다.

1. **데이터 수집 설정** - 소스 커넥터를 구성하여 고객 작업을 추적합니다.
2. **과제 만들기** - 유형, 대상자 및 날짜 정의
3. **작업 추가** - 작업 및 보상 구성
4. **콘텐츠 디자인** - 콘텐츠 카드 및 선택적 메시지 만들기
5. **게시** - Journey Optimizer이 여정을 자동으로 생성하고 활성화합니다.
6. **모니터링** - 참여 및 성과 추적

>[!NOTE]
>
>자동 생성된 여정은 여정 인벤토리에 표시되며 필요한 경우 사용자 정의할 수 있습니다. 그러나 여정에 직접 적용한 변경 사항은 과제 구성에 다시 동기화되지 않습니다.

## 전제 조건 {#prerequisites-overview}

충성도 문제를 사용하기 전에:

* 충성도 이벤트 데이터를 수집하도록 Experience Platform 소스 커넥터(예: 모세관)를 구성합니다
* Journey Optimizer에서 적절한 권한이 있는지 확인합니다.
* Experience Platform에서 타겟 대상 만들기

자세한 전제 조건은 [충성도 과제 이해](get-started.md#prerequisites)를 참조하십시오.

## 중요한 제한 사항 {#limitations-overview}

* **원장 시스템 없음**: 충성도 문제에서 통화 가치 또는 포인트 잔액을 추적하지 않습니다. Journey Optimizer은 외부 충성도 관리 시스템을 호출하여 포인트 할당을 처리합니다.
* **대상 선택만**: 기존 대상을 선택할 수 있지만 충성도 문제 UI에서 새 대상을 만들 수는 없습니다.

## 다음 단계 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="이해" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>충성도 문제 이해</strong></a>
    </div>
    <p>
    <em>기능, 워크플로 및 기능에 대해 알아보기</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>문제 만들기</strong></a>
    </div>
    <p>
    <em>첫 번째 충성도 과제 구축 및 구성</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>문제 관리</strong></a>
    </div>
    <p>
    <em>문제 편집, 모니터링 및 최적화</em>
    <p>
  </td>
</tr>
</table>
