---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 시작
description: Learn how to create and manage loyalty challenges in Adobe Journey Optimizer to build engaging loyalty programs.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 15%

---

# Get started with loyalty challenges {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* **Get started with Loyalty Challenges** ◀︎ **You are here**
* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](../rn/releases.md)를 참조하십시오.

## 개요 {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="충성도 챌린지"
>abstract="충성도 챌린지를 사용하면 고객 행동을 유도하고 브랜드 관계를 심화하는 매력적이고 게임화된 충성도 프로그램을 만들 수 있습니다. 구매 및 리뷰 작성부터 소셜 미디어 참여 및 친구 추천에 이르기까지 특정 액션에 대해 고객에게 보상해 주는 챌린지를 작성하십시오."

충성도 챌린지를 사용하면 고객 행동을 유도하고 브랜드 관계를 심화하는 매력적이고 게임화된 충성도 프로그램을 만들 수 있습니다. 구매 및 리뷰 작성부터 소셜 미디어 참여 및 친구 추천에 이르기까지 특정 액션에 대해 고객에게 보상해 주는 챌린지를 작성하십시오.

With Loyalty Challenges, you can:

* **Design flexible challenge types**: Create Standard, Streak, or Sequential challenges to match your business goals
* **Configure rewards strategically**: Deliver points at task milestones or upon full completion to maintain engagement
* **Personalize the experience**: Use content cards and multi-channel messaging to create immersive, branded experiences
* **Integrate seamlessly**: Connect with your existing loyalty providers and leverage Experience Platform data
* **Track automatically**: Monitor customer progress through auto-generated journeys without custom development

![](assets/challenges-gs.png)

You can create three types of challenge experiences:

* **Standard challenges**: Customers complete any specified number of tasks in any order. Use this type when you want flexibility and multiple paths to completion.\
  *Example: &quot;Summer Wellness Challenge&quot; - Complete 3 out of 5 tasks: buy health products, share on social media, refer a friend, write a review, or attend a virtual event*

* **Streak challenges**: Customers complete the same task multiple times consecutively. Use this type to encourage consistent, repeated behavior over time.\
  *예: &quot;커피 애호가 주간&quot; - 7일 연속으로 커피 제품을 구입하여 무료 음료 보상을 받으세요*

* **순차적인 문제**: 고객은 정의된 순서로 작업을 완료합니다. 이 유형을 사용하여 특정 여정 또는 온보딩 프로세스를 안내합니다.\
  *예: &quot;새 구성원 여정&quot; - 전자 메일→ 등록하여 첫 번째 구매 → 제품 리뷰 작성 → 친구 참조(이 순서로 완료)*

## 작동 방식 {#how-it-works}

충성도 문제를 만들고 실행하는 것은 다음 워크플로를 따릅니다.

1. **챌린지 만들기** - 이름, 유형(표준, 연속 또는 순차적), 날짜 범위를 포함한 기본 챌린지 속성을 정의합니다.

1. **작업 추가** - 작업 유형(구매, 지출), 수량, 제품 필터 및 보상을 포함하여 고객이 완료해야 하는 특정 작업을 정의합니다.

1. **콘텐츠 카드 디자인** - 고객 장치에 표시되는 Journey Optimizer 콘텐츠 카드를 사용하여 도전의 시각적 표현을 만듭니다. 콘텐츠 카드에는 도전 정보, 진행 상황, 보상 등이 표시된다.

1. **메시지 구성**(선택 사항) - 시작, 진행 중 및 완료와 같은 주요 라이프사이클 단계에 대한 멀티채널 메시지(인앱, 이메일, 푸시)를 설정합니다.

1. **대상 선택** - Adobe Experience Platform에서 대상을 선택하여 도전에 참여할 수 있는 고객을 정의합니다.

1. **챌린지 시작** - 챌린지를 게시한 다음 여정을 생성합니다. Journey Optimizer은 자동으로 문제를 해결할 여정을 생성합니다. 자동 생성된 여정을 게시하여 고객이 문제를 사용할 수 있도록 합니다.

자세한 단계별 지침은 [문제 만들기](create-challenges.md)를 참조하십시오.

## 전제 조건 {#prerequisites}

충성도 문제를 사용하기 전에 다음을 확인하십시오.

+++필요한 권한

충성도 문제를 사용하려면 Journey Optimizer 및 Adobe Experience Platform에서 적절한 권한이 필요합니다.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

기능에 액세스할 수 없거나 추가 권한이 필요한 경우 관리자에게 문의하십시오.

+++

+++타깃 대상자

과제를 만들기 전에 필요한 타겟 대상이 Adobe Experience Platform에 있는지 확인하십시오. 과제 구성 중에 참여할 수 있는 고객을 정의하는 대상을 선택합니다. [대상자를 사용하여 작업하는 방법을 알아봅니다](../audience/about-audiences.md).

+++

## 더 자세히 알아보기 {#lets-dive-deeper}

이제 충성도 문제가 무엇인지, 어떻게 작동하는지 알고 있으므로 세부 사항을 자세히 살펴볼 차례입니다. 다음 항목을 탐색하여 인터페이스에 액세스하고, 첫 번째 과제를 만들고, 고객이 완료할 작업을 정의합니다.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="액세스" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>문제 및 작업 액세스 및 관리</strong></a>
    </div>
    <p>
    <em>인벤토리에 액세스하고 문제 및 작업을 관리하는 방법을 알아봅니다.</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="만들기" src="assets/do-not-localize/icon-challenge.png" width="200"/>
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
      <img alt="작업" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>작업 만들기</strong></a>
    </div>
    <p>
    <em>고객이 어려움에 대해 완료하는 작업을 정의하는 방법을 알아보세요</em>
    </p>
  </td>
</tr>
</table>

## API 참조 {#api-reference}

충성도 문제를 프로그래밍 방식으로 관리하려면 [충성도 문제 API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}를 사용하십시오. API를 사용하면 REST 끝점을 통해 과제 및 작업을 만들고, 업데이트하고, 관리할 수 있습니다.
