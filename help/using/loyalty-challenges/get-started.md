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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 1%

---


# 충성도 문제 시작 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* **충성도 문제 시작** ◀︎**현재 상태** - 개요, 워크플로, 사전 요구 사항
* [충성도 문제 액세스](access-loyalty-challenges.md) - 인벤토리 및 필터링
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [작업 만들기](create-tasks.md) - 과제 작업 정의
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 개요 {#overview}

충성도 과제는 작업과 이정표 정의에서 채널 전반에 걸쳐 콘텐츠 전달 및 성능 추적에 이르기까지 규모에 맞는 충성도 프로그램을 제작할 수 있는 완벽한 솔루션을 제공합니다.

다음과 같은 세 가지 유형의 과제 경험을 만들 수 있습니다.

* **표준 과제**: 고객은 순서에 관계없이 지정된 수의 작업을 완료합니다
* **연속 문제**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다
* **순차적 문제**: 고객은 정의된 순서로 작업을 완료합니다

충성도 문제를 사용하면 외부 충성도 관리 시스템과의 통합을 유지하면서 보상을 구성하고, 주요 라이프사이클 단계에서 다중 채널 알림을 전송하고, 자동으로 생성된 여정을 통해 성능을 모니터링할 수 있습니다.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## 작동 방식 {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

충성도 문제를 만들고 실행하는 것은 다음 워크플로를 따릅니다.

1. **데이터 수집 설정** - 고객 작업 및 진행 상황을 추적하는 고객 충성도 이벤트 데이터를 수집하도록 Experience Platform 소스 커넥터(예: Capillary 커넥터)를 구성합니다. 이 데이터를 통해 과제 추적 및 작업 완료를 수행할 수 있습니다.

1. **챌린지 만들기** - 이름, 유형(표준, 연속 또는 순차적), 대상 및 날짜 범위를 포함한 기본 챌린지 속성을 정의합니다. 자세한 단계는 [문제 만들기](create-challenges.md)를 참조하십시오.

1. **작업 추가** - 작업 유형(구매, 지출, 방문, 참여, 사용자 지정 이벤트), 수량, 제품 필터 및 보상을 포함하여 고객이 완료해야 하는 특정 작업을 정의합니다. 자세한 지침은 [작업 만들기](create-tasks.md)를 참조하세요.

1. **콘텐츠 카드 디자인** - 고객 장치에 표시되는 Journey Optimizer [콘텐츠 카드](../content-card/create-content-card.md)를 사용하여 도전의 시각적 표현을 만듭니다. 콘텐츠 카드에는 도전 정보, 진행 상황, 보상 등이 표시된다.

1. **메시지 구성**(선택 사항) - 시작, 진행 중 및 완료와 같은 주요 라이프사이클 단계에 대해 다중 채널 메시지([인앱](../in-app/get-started-in-app.md), [이메일](../email/get-started-email.md), [푸시](../push/get-started-push.md))를 설정합니다.

1. **검토 및 게시** - [테스트 프로필](../content-management/test-profiles.md)을 사용하여 도전을 테스트한 다음 게시하여 대상 대상자가 사용할 수 있도록 합니다.

1. **여정 활성화** - 문제를 게시하면 Journey Optimizer에서 콘텐츠 카드 게재 및 메시지를 조정하는 초안 상태의 [여정](../building-journeys/journey-gs.md)을(를) 자동으로 만듭니다. 여정 인벤토리로 이동하고 자동으로 생성된 여정(&quot;과제: [과제 이름]&quot;)를 찾은 다음 [활성화](../building-journeys/publish-journey.md)하여 고객이 과제를 사용할 수 있도록 합니다.

1. **성능 모니터링** - 기본 제공 보고서 및 여정 캔버스를 통해 기여도, 완료율, 보상 배포 및 메시지 참여를 추적합니다. 모니터링 세부 정보는 [문제 관리](manage-challenges.md)를 참조하십시오.

## 전제 조건 {#prerequisites}

충성도 문제를 사용하기 전에 다음을 확인하십시오.

+++데이터 수집 설정

충성도 문제는 Experience Platform 소스 커넥터를 통해 수집된 데이터를 사용하여 고객 진행 상황과 작업 완료를 추적합니다.

1. **지원되는 소스 커넥터를 구성하십시오**: 현재 Capillary 커넥터는 일반적으로 사용할 수 있습니다. 추가 커넥터는 향후 릴리스에 제공될 예정입니다.

1. **데이터 수집 유효성 검사**: 충성도 이벤트 및 고객 데이터가 Experience Platform으로 유입되어 Journey Optimizer에서 사용할 수 있는지 확인하십시오. 데이터 스키마에 고객 작업 및 진행 상황을 추적하는 데 필요한 필드가 포함되어 있는지 확인합니다.

자세한 지침은 다음을 참조하십시오.

* [Experience Platform 소스 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Journey Optimizer에서 소스 커넥터 구성](../start/get-started-sources.md)

+++

+++필요한 권한

충성도 문제를 사용하려면 Journey Optimizer에서 적절한 권한이 필요합니다. 필요한 권한은 다음과 같습니다.

* **[!UICONTROL 충성도 문제(Beta)]** 기능에 액세스
* 여정 만들기 및 관리 권한
* 콘텐츠 카드를 만들고 관리할 수 있는 권한
* 대상자를 만들고 관리할 수 있는 권한

기능에 액세스할 수 없거나 추가 권한이 필요한 경우 관리자에게 문의하십시오.

+++

+++타깃 대상자

충성도 도전에 참여할 수 있는 고객을 지정하는 타겟 대상을 정의합니다. 기존 대상을 선택하거나 과제 생성 인터페이스에서 직접 새 대상을 만들 수 있습니다. 대상자를 사용하여 작업하는 방법에 대한 자세한 내용은 [대상자 시작](../audience/about-audiences.md)을 참조하세요.

+++

## 다음 단계 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>충성도 문제 액세스</strong></a>
    </div>
    <p>
    <em>인벤토리 및 필터링 문제 액세스 방법 알아보기</em>
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>작업 만들기</strong></a>
    </div>
    <p>
    <em>어려움에 대한 조치 및 보상 정의</em>
    </p>
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
    </p>
  </td>
</tr>
</table>
