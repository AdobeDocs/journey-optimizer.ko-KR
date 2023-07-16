---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 항목 관리
description: 프로필 항목 관리 방법 알아보기
feature: Journeys
role: User
level: Intermediate
keywords: 재입력, 여정, 프로필, 반복
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 15%

---


# 프로필 항목 관리 {#entry-management}

기본적으로 새 여정은 다시 입력할 수 있습니다. 예를 들어 한 사람이 상점에 들어갈 때 일회성 선물을 제공하려는 경우 &quot;한 방&quot; 여정에 대한 옵션을 선택 취소할 수 있습니다. 이 경우 고객이 여정에 다시 입장하여 오퍼를 다시 받을 수 없도록 해야 합니다.

![](assets/journey-re-entrance.png)

여정이 종료되면 상태는 다음과 같습니다. **[!UICONTROL 종료됨]**. 새 사용자는 더 이상 여정에 들어갈 수 없습니다. 여정에 이미 있는 사람은 여정을 정상적으로 완료합니다.

기본 전역 시간 제한 30일 후 여정이 로 전환됩니다. **완료됨** 상태.  [자세히 알아보기](journey-gs.md#global_timeout).


## 단일 여정{#entry-unitary}

단일 여정(이벤트 또는 대상 자격으로 시작)에는 동일한 이벤트에 대해 여정이 여러 번 잘못 트리거되는 것을 방지하는 보호가 포함됩니다. 프로필 재입력은 기본적으로 5분 동안 일시적으로 차단됩니다. 예를 들어 이벤트가 특정 프로필에 대해 12:01에 여정을 트리거하고 다른 이벤트가 12:03에 도착하는 경우(동일한 이벤트이든 동일한 여정을 트리거하는 다른 이벤트이든) 해당 여정은 이 프로필에 대해 다시 시작되지 않습니다.

또한:

* 재입력이 활성화된 경우 프로필은 여정을 여러 번 입력할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 입력할 수 없습니다.

* 재입력이 비활성화된 경우 프로필은 동일한 여정을 여러 번 입력할 수 없습니다

## 대상자 여정 읽기{#entry-read-segment}

대상자 읽기 여정:

* 반복되지 않는 여정의 경우: 프로필은 여정에 한 번만 입력합니다.

* 반복 여정의 경우: 프로필이 대상자 예상 상태인 경우 각 반복에 대한 여정에 들어갑니다. 이전 반복에서 여정에 있었던 경우 처음부터 다시 시작합니다.

비즈니스 이벤트 여정 **대상자 읽기** 활동: 이 여정은 비즈니스 이벤트 수신을 기반으로 한다는 것을 알고 있는 경우 프로필이 예상 대상에서 자격을 부여받으면 수신된 각 비즈니스 이벤트에 대한 여정을 입력합니다. 즉, 이 프로필은 동일한 여정에서 동시에 여러 번, 하지만 다른 비즈니스 이벤트의 컨텍스트에서 제공될 수 있습니다.

<!--
# Profile entry management {#entry-management}

There are two main types of journeys:

* event-based journeys: starting with an event, these journeys are unitary, they are associated to one individual. When the event is received, the individual enters the journey. [Read more](#entry-unitary)
* read segment journeys: starting with a read segment, these are batch journeys. Individuals belonging to the segment all enter the same journey. These journeys can be recurring or one-shot. [Read more](#entry-read-segment)

In both journey types, a profile cannot be present multiple times in the same journey, at the same time.


## Unitary journeys{#entry-unitary}

In unitary journeys, you can enable or disable re-entrance:

* If re-entrance is enabled, a profile can enter a journey several times, but cannot do it until he fully exited that previous instance of the journey.

* If re-entrance is disabled, a profile cannot enter multiple times the same journey

By default, new journeys allow re-entrance. You can uncheck the option for “one shot” journeys, for example if you want to offer a one-time gift when a person enters a shop. In that case, you don't want the customer to be able to re-enter the journey and receive the offer again. When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally. [Learn more](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

After the default global timeout of 30 days, the journey switches to the **Finished** status. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally.Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. [Learn more](journey-gs.md#global_timeout).

Unitary journeys (starting with an event or a segment qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.

The key is also used to check that a person is in a journey. Indeed, a person cannot be at two different places in the same journey. As a result, the system does not allow the same key, for example the key CRMID=3224, to be at different places in the same journey.

## Read segment journeys{#entry-read-segment}

In a read segment journey:

* For non-recurring journeys: the profile enters once and only once the journey.

* For recurring journeys: by default, all the profiles belonging to the segment enters the journey on each recurrence. They must finish the journey before they can reenter in another occurrence. 

>[!NOTE]
>
>Two options are available for recurring read segment journeys. The **Force reentrance on recurrence** option makes all the profiles still present in the journey automatically exit it on the next execution. The **Incremental read** option only targets the individuals who entered the segment since the last execution of the journey. Refer to this [section](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

In business event journeys starting with a **Read segment** activity: knowing that this journey is based on the reception of a business event, if the profile is qualified in the expected segment, they will enter the journey for each business event received, meaning that this profile can be multiple times in the same journey, at the same time, but in the context of different business events.
-->