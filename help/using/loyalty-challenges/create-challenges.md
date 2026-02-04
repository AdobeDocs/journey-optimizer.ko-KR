---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 만들기
description: Adobe Journey Optimizer에서 충성도 문제를 만들고 구성하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---


# 과제 만들기 {#create-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md) - 개요, 워크플로, 사전 요구 사항
* [충성도 문제 액세스](access-loyalty-challenges.md) - 인벤토리 및 필터링
* **과제 만들기** ◀︎**현재 상태** - 과제 빌드 및 구성
* [작업 만들기](create-tasks.md) - 과제 작업 정의
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 작동 방식 {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

충성도 문제를 만들고 실행하는 것은 다음 워크플로를 따릅니다.

1. **챌린지 만들기** - 이름, 유형(표준, 연속 또는 순차적), 대상 및 날짜 범위를 포함한 기본 챌린지 속성을 정의합니다.

1. **작업 추가** - 작업 유형(구매, 지출, 방문 등), 수량, 제품 필터 및 보상을 포함하여 고객이 완료해야 하는 특정 작업을 정의합니다.

1. **콘텐츠 카드 디자인** - 고객 장치에 표시되는 Journey Optimizer 콘텐츠 카드를 사용하여 도전의 시각적 표현을 만듭니다.

1. **메시지 구성**(선택 사항) - 시작, 진행 중 및 완료와 같은 주요 단계에 대해 멀티채널 메시지(인앱, 이메일, 푸시, SMS)를 설정합니다.

1. **검토 및 게시** - 테스트 프로필로 문제를 테스트한 다음 게시하여 대상 대상자가 사용할 수 있도록 합니다.

## 과제 만들기 {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

새로운 충성도 과제를 만들려면:

1. Journey Optimizer의 **[!UICONTROL 충성도 과제]**(으)로 이동합니다.

1. **[!UICONTROL 과제]** 탭을 선택하십시오.

1. **[!UICONTROL 질문 만들기]**&#x200B;를 선택하십시오.

1. 과제 속성을 구성합니다.

   **도전 이름**: 도전의 수사적 이름을 입력하십시오. 이 이름은 과제 인벤토리에 표시되며 과제를 식별하는 데 도움이 됩니다.

   **도전 유형**: 다음 유형 중 하나를 선택하십시오.
   * **[!UICONTROL 표준]**: 고객은 지정된 수의 작업을 순서에 관계없이 완료합니다
   * **[!UICONTROL 연속]**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다
   * **[!UICONTROL 순차적]**: 고객은 정의된 순서로 작업을 완료합니다

   **대상**: 이 문제에 참여할 수 있는 사용자를 정의하는 대상 세그먼트를 선택하십시오. 문제를 만들려면 먼저 Experience Platform에서 대상을 만들어야 합니다. 자세한 내용은 [대상자 시작](../audience/about-audiences.md)을 참조하세요.

   **시작 날짜**: 고객이 도전을 사용할 수 있게 되면 설정합니다.

   **종료 날짜**: 문제가 만료되어 더 이상 새 완료를 허용하지 않는 시기를 설정합니다.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### 작업 추가 {#add-tasks}

작업은 고객이 보상을 받기 위해 완료해야 하는 특정 작업 또는 이정표를 정의합니다. 작업 유형(구매, 지출, 방문, 참여, 사용자 정의 이벤트), 수량, 제품 필터 및 보상을 구성합니다.

과제 유형에 따라 고객은 다르게 작업을 완료합니다.

* **표준 과제**: 순서에 관계없이 지정된 수의 작업을 완료하십시오.
* **연속 문제**: 동일한 작업을 여러 번 연속적으로 완료하십시오.
* **순차적인 문제**: 정의된 순서로 작업 완료

작업에 작업을 추가하려면 작업 섹션에서 **[!UICONTROL 작업 추가]**&#x200B;를 선택하고 작업 속성을 구성하십시오.

작업 만들기 및 구성에 대한 자세한 지침은 [작업 만들기](create-tasks.md)를 참조하세요.

### 콘텐츠 카드 구성 {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

콘텐츠 카드는 고객 디바이스에 대한 도전을 시각적으로 표현하여 도전 정보, 진행 상황 및 보상을 표시합니다. [콘텐츠 카드](../content-card/create-content-card.md)에 대해 자세히 알아보세요.

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

과제에 맞게 콘텐츠 카드를 구성하려면 다음을 수행하십시오.

1. 과제 편집기에서 **[!UICONTROL 콘텐츠 카드]** 섹션으로 이동합니다.

1. **[!UICONTROL 콘텐츠 카드 만들기]**&#x200B;를 선택하거나 기존 템플릿을 선택하십시오.

1. 콘텐츠 카드 디자인:
   * 이미지, 텍스트 및 브랜딩 요소 추가
   * 고객별 정보를 표시하려면 [개인화 토큰](../personalization/personalization-syntax.md)을 포함하십시오.
   * 과제 진행 표시기 표시
   * 보상 및 인센티브 표시

1. 콘텐츠 카드가 표시될 시기를 구성합니다.
   * **챌린지 시작**: 챌린지를 사용할 수 있게 되면 표시
   * **진행 중**: 고객이 적극적으로 참여하는 동안 표시
   * **완료**: 고객이 모든 작업을 완료한 후 표시

1. 제대로 표시되도록 하려면 다른 장치에서 컨텐츠 카드를 미리 봅니다.

1. 콘텐츠 카드 구성을 저장합니다.

콘텐츠 카드 디자인 및 개인화에 대한 자세한 내용은 [콘텐츠 카드 디자인](../content-card/design-content-card.md)을 참조하세요.

### 메시징 구성 {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

멀티채널 메시지를 설정하여 과제 라이프사이클의 주요 단계에서 고객을 참여시킵니다.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

당면 과제에 대한 메시지를 구성하려면 다음을 수행하십시오.

1. 과제 편집기에서 **[!UICONTROL 메시징]** 섹션으로 이동합니다.

1. 각 라이프사이클 단계에 대한 메시지를 구성합니다.

   **시작 메시지** - 도전이 시작되면 고객에게 알림:
   * 채널 선택: [앱 내](../in-app/get-started-in-app.md), [이메일](../email/get-started-email.md), [푸시 알림](../push/get-started-push.md) 또는 [SMS](../sms/get-started-sms.md)
   * 과제 세부 정보 및 call-to-action을 사용하여 메시지 디자인
   * 시간 설정: 도전이 실행되거나 특정 시간 동안 예약되면 즉시 전송

   **진행 중인 메시지** - 문제 중에 고객 참여 유지:
   * 트리거 조건 정의(예: 50% 완료, 특정 작업 완료됨)
   * 지속적인 참여를 독려하는 알림 메시지 만들기
   * 진행 상황 업데이트 및 다음 단계 포함

   **완료 메시지** - 성공을 축하하고 보상을 제공합니다.
   * 고객의 도전 완료를 축하합니다.
   * 보상 할당 확인
   * 보상 청구에 대한 지침 제공
   * 다음 과제 또는 작업 제안

특정 채널을 위한 메시지를 만드는 방법에 대한 자세한 내용은 다음을 참조하십시오.

* [인앱 메시지 설명서](../in-app/get-started-in-app.md)
* [이메일 메시지 설명서](../email/get-started-email.md)
* [푸시 알림 설명서](../push/get-started-push.md)
* [SMS 메시지 설명서](../sms/get-started-sms.md)

## 과제 검토 및 게시 {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

문제를 게시하기 전에:

1. **모든 구성 요소 검토**: 과제 속성, 작업, 보상, 콘텐츠 카드 및 메시징 구성을 확인합니다.

1. **경험 테스트**: [테스트 프로필](../content-management/test-profiles.md)을 사용하여 콘텐츠 카드 표시 및 작업 트리거 동작의 유효성을 검사하십시오.

1. **게시**: **[!UICONTROL 게시]**&#x200B;를 선택하여 대상 대상자에게 문제를 제공할 수 있습니다.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

문제를 게시하면 Journey Optimizer에서 초안 상태로 [여정](../building-journeys/journey-gs.md)을(를) 자동으로 만듭니다. 자동 생성된 여정이 &quot;도전: [도전 이름]&quot; 이름 형식으로 여정 인벤토리에 표시됩니다.

고객이 문제를 해결할 수 있도록 하려면 다음을 수행하십시오.

1. Journey Optimizer의 **[!UICONTROL 여정]** 인벤토리로 이동합니다.

1. 자동 생성된 여정(이름에 접두사로 &quot;Challenge:&quot;가 있음)를 찾습니다.

1. [여정 활성화](../building-journeys/publish-journey.md).

여정은 지정된 챌린지 시작 날짜에 자동으로 시작됩니다.

>[!NOTE]
>
>자동 생성된 여정은 여정 인벤토리에 표시되며 필요한 경우 사용자 정의할 수 있습니다. 그러나 여정에 직접 적용한 변경 사항은 과제 구성에 다시 동기화되지 않습니다.

## 다음 단계 {#next-steps}

* [문제 관리](manage-challenges.md) - 문제를 편집, 모니터링 및 최적화하는 방법을 알아봅니다.
* [충성도 문제 이해](get-started.md) - 기능 검토

