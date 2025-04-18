---
solution: Journey Optimizer
product: journey optimizer
title: 대기 활동
description: 대기 활동을 구성하는 방법 알아보기
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 대기, 활동, 여정, 다음, 캔버스
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: da7d895fcc724e6b1c0d6480f6a8693037a03752
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 15%

---

# 대기 활동 {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="대기 활동"
>abstract="경로에서 다음 활동을 실행할 때까지 대기하려면 대기 활동을 사용할 수 있습니다. 이를 통해 다음 활동이 실행되는 시점을 정의할 수 있습니다. 지속 기간과 사용자 정의와 같은 두 가지 옵션을 사용할 수 있습니다."

다음 활동을 실행하기 전에 **[!UICONTROL 대기]** 활동을 사용하여 기간을 정의할 수 있습니다.  최대 대기 기간은 **90일**&#x200B;입니다.

두 가지 유형의 **대기** 활동을 설정할 수 있습니다.

* 상대적 기간을 기반으로 한 대기. [자세히 알아보기](#duration)
* 함수를 사용하여 계산하는 사용자 지정 날짜입니다. [자세히 알아보기](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 추천 {#wait-recommendations}

### 여러 대기 활동 {#multiple-wait-activities}

여정에서 여러 **대기** 활동을 사용하는 경우 여정의 [전역 시간 초과](journey-properties.md#global_timeout)가 91일이므로 프로필이 입력한 후 항상 최대 91일 후에 여정에서 삭제됩니다. [이 페이지](journey-properties.md#global_timeout)에서 자세히 알아보세요.

개인은 91일 여정 제한 시간 전에 대기 기간을 완료할 수 있는 충분한 시간이 여정에 남아 있는 경우에만 **대기** 활동을 입력할 수 있습니다.

### 대기 및 재입장 {#wait-reentrance}

**대기** 활동을 사용하여 다시 시작을 차단하지 않는 것이 좋습니다. 대신 여정 속성 수준에서 **재입력 허용** 옵션을 사용하십시오. [이 페이지](../building-journeys/journey-properties.md#entrance)에서 자세히 알아보세요.

### 대기 및 테스트 모드 {#wait-test-mode}

테스트 모드에서 **[!UICONTROL 테스트의 대기 시간]** 매개 변수를 사용하면 각 **대기** 활동이 지속되는 시간을 정의할 수 있습니다. 기본 시간은 10초입니다. 이렇게 하면 테스트 결과를 빠르게 얻을 수 있습니다. [이 페이지](../building-journeys/testing-the-journey.md)에서 자세히 알아보세요.

### 대기 및 모바일 채널 {#wait-mobile-channels}

[푸시 알림](../push/get-started-push.md)을 보낸 직후 [인앱 메시지](../in-app/create-in-app.md)를 표시하려면 **대기** 활동을 사용하여 인앱 메시지 페이로드 시간을 전파하도록 허용하십시오. 일반적으로 5~15분 정도 기다리는 것이 좋지만 정확한 시간은 페이로드 복잡성과 개인화 요구 사항에 따라 달라질 수 있습니다.

## 구성 {#wait-configuration}

### 기간 대기 {#duration}

**Duration** 유형을 선택하여 다음 활동을 실행하기 전 대기 시간의 상대적 기간을 설정하십시오. 최대 기간은 **90일**&#x200B;입니다.

![대기 기간 정의](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### 사용자 지정 대기 {#custom}

이벤트에서 가져온 필드 또는 사용자 지정 작업 응답을 기반으로 하는 고급 식을 사용하여 사용자 지정 날짜를 정의하려면 **Custom** 유형을 선택하십시오. 상대적 기간(예: 7일)을 직접 정의할 수는 없지만, 필요한 경우 함수를 사용하여 계산할 수 있습니다(예: 구매 후 2일).

![식을 사용하여 사용자 지정 대기 정의](assets/journey57.png)

편집기의 식은 `dateTimeOnly` 형식을 제공해야 합니다. [이 페이지](expression/expressionadvanced.md)를 참조하십시오. dateTimeOnly 형식에 대한 자세한 내용은 [이 페이지](expression/data-types.md)를 참조하세요.

가장 좋은 방법은 프로필에만 해당되는 사용자 지정 날짜를 사용하고 모든 항목에 동일한 날짜를 사용하지 않는 것입니다. 예를 들어 `toDateTimeOnly('2024-01-01T01:11:00Z')`을(를) 정의하지 않고 각 프로필에 해당하는 `toDateTimeOnly(@event{Event.productDeliveryDate})`을(를) 정의하십시오. 고정 날짜를 사용하면 여정 실행에 문제가 발생할 수 있습니다.


>[!NOTE]
>
>`dateTimeOnly` 식을 활용하거나 함수를 사용하여 `dateTimeOnly`(으)로 변환할 수 있습니다. 예: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`. 이벤트의 필드는 2023-08-12T09:46:06Z 형식입니다.
>
>여정 속성에 **표준 시간대**&#x200B;이(가) 필요합니다. 따라서 사용자 인터페이스에서 2023-08-12T09:46:06.982-05와 같이 전체 ISO-8601 타임스탬프 혼합 시간 및 시간대 오프셋을 직접 지정할 수 없습니다. [자세히 알아보기](../building-journeys/timezone-management.md).


대기 활동이 예상대로 작동하는지 확인하려면 단계 이벤트를 사용할 수 있습니다. [자세히 알아보기](../reports/query-examples.md#common-queries).

## 자동 대기 노드  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="자동 대기 노드 정보"
>abstract="이 활동 뒤에 **대기** 활동이 자동으로 추가됩니다. 3일로 설정되어 있습니다. 필요에 따라 제거하거나 구성할 수 있습니다."

각 인바운드 메시지 활동(인앱 메시지, 코드 기반 경험 또는 카드)에는 3일 **대기** 활동이 제공됩니다. 프로필이 여정 끝에 도달하면 인바운드 메시지가 자동으로 종료되므로 사용자가 적어도 3일 동안 이를 볼 수 있다고 가정합니다. 이 **대기** 활동을 제거하거나 필요한 경우 구성을 변경할 수 있습니다.