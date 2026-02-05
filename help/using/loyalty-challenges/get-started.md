---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 시작
description: 매력적인 충성도 프로그램을 구축하기 위해 Adobe Journey Optimizer에서 충성도 문제를 만들고 관리하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
source-git-commit: 6c6a1b31c81000877cea2af8bca0377264ec4833
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 2%

---


# 충성도 문제 시작 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* **충성도 문제 시작** ◀︎**현재 상태**
* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 개요 {#overview}

충성도 문제를 사용하면 고객 행동을 유도하고 브랜드 관계를 심화하는 매력적인 게임화된 충성도 프로그램을 만들 수 있습니다. 구매 및 리뷰 작성부터 소셜 미디어 참여 및 친구 추천에 이르기까지 특정 작업에 대해 고객에게 보상해 주는 문제를 제기하십시오.

충성도 문제를 통해 다음과 같은 작업을 수행할 수 있습니다.

* **유연한 과제 유형 디자인**: 비즈니스 목표에 맞게 표준, 연속 또는 순차적 과제 만들기
* **전략적으로 보상 구성**: 작업 마일스톤 또는 전체 완료 시 포인트를 전달하여 참여 유지
* **경험 개인화**: 콘텐츠 카드 및 다중 채널 메시지를 사용하여 몰입형 브랜드 경험을 만듭니다
* **원활하게 통합**: 기존 충성도 공급자와 연결하고 Experience Platform 데이터 활용
* **자동으로 추적**: 사용자 지정 개발 없이 자동 생성된 여정을 통해 고객 진행 상황을 모니터링합니다.

![](assets/challenges-gs.png)

다음과 같은 세 가지 유형의 과제 경험을 만들 수 있습니다.

* **표준 과제**: 고객은 순서에 관계없이 지정된 수의 작업을 완료합니다. 유연성과 여러 경로를 완성하려면 이 유형을 사용하십시오.\
  *예: &quot;Summer Wellness Challenge&quot; - 5가지 작업 중 3가지 완료: 건강 제품 구입, 소셜 미디어 공유, 친구 추천, 리뷰 작성 또는 가상 이벤트 참석*

* **연속 문제**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다. 이 유형을 사용하여 시간이 지남에 따라 일관되고 반복되는 동작을 장려합니다.\
  *예: &quot;커피 애호가 주간&quot; - 7일 연속으로 커피 제품을 구입하여 무료 음료 보상을 받으세요*

* **순차적인 문제**: 고객은 정의된 순서로 작업을 완료합니다. 이 유형을 사용하여 특정 여정 또는 온보딩 프로세스를 안내합니다.\
  *예: &quot;새 구성원 여정&quot; - 전자 메일→ 등록하여 첫 번째 구매 → 제품 리뷰 작성 → 친구 참조(이 순서로 완료)*

## 작동 방식 {#how-it-works}

충성도 문제를 만들고 실행하는 것은 다음 워크플로를 따릅니다.

1. **데이터 수집 설정** - 고객 작업 및 진행 상황을 추적하는 고객 충성도 이벤트 데이터를 수집하도록 Experience Platform 소스 커넥터(예: [Capillary 커넥터](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty))를 구성합니다. 이 데이터를 통해 과제 추적 및 작업 완료를 수행할 수 있습니다.

1. **챌린지 만들기** - 이름, 유형(표준, 연속 또는 순차적), 날짜 범위를 포함한 기본 챌린지 속성을 정의합니다.

1. **작업 추가** - 작업 유형(구매, 지출), 수량, 제품 필터 및 보상을 포함하여 고객이 완료해야 하는 특정 작업을 정의합니다.

1. **콘텐츠 카드 디자인** - 고객 장치에 표시되는 Journey Optimizer 콘텐츠 카드를 사용하여 도전의 시각적 표현을 만듭니다. 콘텐츠 카드에는 도전 정보, 진행 상황, 보상 등이 표시된다.

1. **메시지 구성**(선택 사항) - 시작, 진행 중 및 완료와 같은 주요 라이프사이클 단계에 대한 멀티채널 메시지(인앱, 이메일, 푸시)를 설정합니다.

1. **대상 선택** - Adobe Experience Platform에서 대상을 선택하여 도전에 참여할 수 있는 고객을 정의합니다.

1. **챌린지 시작** - 챌린지를 게시한 다음 여정을 생성합니다. Journey Optimizer은 자동으로 문제를 해결할 여정을 생성합니다. 자동 생성된 여정을 게시하여 고객이 문제를 사용할 수 있도록 합니다.

자세한 단계별 지침은 [문제 만들기](create-challenges.md)를 참조하십시오.

## 전제 조건 {#prerequisites}

충성도 문제를 사용하기 전에 다음을 확인하십시오.

+++데이터 수집 설정

충성도 문제는 Experience Platform 소스 커넥터를 통해 수집된 데이터를 사용하여 고객 진행 상황과 작업 완료를 추적합니다.

시작하기 전에 지원되는 소스 커넥터를 구성합니다. 현재 Capillary 커넥터를 사용할 수 있습니다. 추가 커넥터는 향후 릴리스에 제공될 예정입니다. [충성도 소스 커넥터에 대해 알아봅니다](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty).

+++

+++필요한 권한

충성도 문제를 사용하려면 Journey Optimizer에서 적절한 권한이 필요합니다. 필요한 권한은 다음과 같습니다.

* 추가 예정
* 추가 예정
* 추가 예정

기능에 액세스할 수 없거나 추가 권한이 필요한 경우 관리자에게 문의하십시오.

+++

+++타깃 대상자

과제를 만들기 전에 필요한 타겟 대상이 Adobe Experience Platform에 있는지 확인하십시오. 과제 구성 중에 참여할 수 있는 고객을 정의하는 대상을 선택합니다. [대상자를 사용하여 작업하는 방법을 알아봅니다](../audience/about-audiences.md).

+++

## 다음 단계 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>문제 및 작업 액세스 및 관리</strong></a>
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
    <em>첫 번째 충성도 과제를 만들고 구성하는 방법에 대해 알아봅니다.</em>
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
    <em>고객이 어려움에 대해 수행하는 작업을 구성하는 방법에 대해 알아봅니다.</em>
    </p>
  </td>
</tr>
</table>
