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
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 12%

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

이러한 권장 사항을 사용하여 기다림을 예측 가능하고 안전하게 유지합니다.

### 여러 대기 활동 {#multiple-wait-activities}

여정에서 여러 **대기** 활동을 사용하는 경우 여정의 [전역 시간 초과](journey-properties.md#global_timeout)가 91일이므로 프로필이 입력한 후 항상 최대 91일 후에 여정에서 삭제됩니다. [이 페이지](journey-properties.md#global_timeout)에서 자세히 알아보십시오.

개인은 91일 여정 제한 시간 전에 대기 기간을 완료할 수 있는 충분한 시간이 여정에 남아 있는 경우에만 **대기** 활동을 입력할 수 있습니다.

### 대기 및 재입장 {#wait-reentrance}

**대기** 활동을 사용하여 다시 시작을 차단하지 않는 것이 좋습니다. 대신 여정 속성 수준에서 **재입력 허용** 옵션을 사용하십시오. [이 페이지](../building-journeys/journey-properties.md#entrance)에서 자세히 알아보십시오.

### 대기 및 테스트 모드 {#wait-test-mode}

테스트 모드에서 **[!UICONTROL 테스트의 대기 시간]** 매개 변수를 사용하면 각 **대기** 활동이 지속되는 시간을 정의할 수 있습니다. 기본 시간은 10초입니다. 이렇게 하면 테스트 결과를 빠르게 얻을 수 있습니다. [이 페이지](../building-journeys/testing-the-journey.md)에서 자세히 알아보십시오.

### 대기 및 모바일 채널 {#wait-mobile-channels}

[푸시 알림](../in-app/create-in-app.md)을 보낸 직후 [인앱 메시지](../../rp_landing_pages/push-landing-page.md)를 표시하려면 **대기** 활동을 사용하여 인앱 메시지 페이로드 시간을 전파하도록 허용하십시오. 일반적으로 5~15분 정도 기다리는 것이 좋지만 정확한 시간은 페이로드 복잡성과 개인화 요구 사항에 따라 달라질 수 있습니다.

## 구성 {#wait-configuration}

여기에서 대기 기간 및 시간을 구성합니다.

### 기간 대기 {#duration}

**Duration** 유형을 선택하여 다음 활동을 실행하기 전 대기 시간의 상대적 기간을 설정하십시오. 최대 기간은 **90일**&#x200B;입니다.

![대기 기간 정의](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)

-->

### 사용자 지정 대기 {#custom}

이벤트에서 가져온 필드 또는 사용자 지정 작업 응답을 기반으로 하는 고급 식을 사용하여 사용자 지정 날짜를 정의하려면 **Custom** 유형을 선택하십시오. 상대적 기간(예: 7일)을 직접 정의할 수는 없지만, 필요한 경우 함수를 사용하여 계산할 수 있습니다(예: 구매 후 2일).

![식을 사용하여 사용자 지정 대기 정의](assets/journey57.png)

편집기의 식은 `dateTimeOnly` 형식을 제공해야 합니다. [이 페이지](expression/expressionadvanced.md)를 참조하십시오. dateTimeOnly 형식에 대한 자세한 내용은 [이 페이지](expression/data-types.md)를 참조하세요.

가장 좋은 방법은 프로필에만 해당되는 사용자 지정 날짜를 사용하고 모든 항목에 동일한 날짜를 사용하지 않는 것입니다. 예를 들어 `toDateTimeOnly('2024-01-01T01:11:00Z')`을(를) 정의하지 않고 각 프로필에 해당하는 `toDateTimeOnly(@event{Event.productDeliveryDate})`을(를) 정의하십시오. 고정 날짜를 사용하면 여정 실행에 문제가 발생할 수 있습니다. [이 섹션](entry-management.md#wait-activities-impact)에서 대기 활동이 여정 처리 속도에 미치는 영향에 대해 자세히 알아보세요.


>[!NOTE]
>
>`dateTimeOnly` 식을 활용하거나 함수를 사용하여 `dateTimeOnly`(으)로 변환할 수 있습니다. 예: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`. 이벤트의 필드는 2023-08-12T09:46:06Z 형식입니다.
>
>여정 속성에 **표준 시간대**&#x200B;이(가) 필요합니다. 따라서 사용자 인터페이스에서 2023-08-12T09:46:06.982-05와 같이 전체 ISO-8601 타임스탬프 혼합 시간 및 시간대 오프셋을 직접 지정할 수 없습니다. [자세히 알아보기](../building-journeys/timezone-management.md).

>[!CAUTION]
>
>`toDateTimeOnly()`을(를) 사용하여 사용자 지정 대기 식을 만들 때 식 결과에 &#39;Z&#39; 또는 시간대 오프셋(예: &#39;-05:00&#39;)을 추가하지 마십시오. 명시적 시간대 지정자 없이 여정이 구성한 시간대를 참조하는 유효한 ISO 날짜/시간 구문을 표현식에 사용해야 합니다.
>
>**올바른 예:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))`
>
>**잘못된 예:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌(&#39;Z&#39; 포함)
>
>지원되지 않는 시간대 지정자를 사용하면 프로필이 예상대로 진행되지 않고 대기 활동에서 중단된 상태로 유지될 수 있습니다.

대기 활동이 예상대로 작동하는지 확인하려면 단계 이벤트를 사용할 수 있습니다. [자세히 알아보기](../reports/query-examples.md#common-queries).

## 대기 후 프로필 새로 고침 {#profile-refresh}

프로필이 **대상자 읽기** 활동으로 시작하는 여정의 **대기** 활동에 주차되어 있으면 여정은 UPS(통합 프로필 서비스)에서 프로필의 특성을 자동으로 새로 고쳐 사용 가능한 최신 데이터를 가져옵니다.

* **여정 항목에서**: 프로필은 여정 시작 시 평가된 대상 스냅숏의 특성 값을 사용합니다.
* **대기 노드 이후**: 여정이 조회를 수행하여 이전 스냅숏 데이터가 아닌 UPS에서 최신 프로필 데이터를 검색합니다. 즉, 여정이 시작된 후 프로필 속성이 변경되었을 수 있습니다.

이 비헤이비어는 다운스트림 활동이 대기 기간 후에 현재 프로필 정보를 사용하도록 합니다. 그러나 여정이 실행 전체에서 원본 스냅샷 데이터만 사용할 것으로 예상하면 예기치 않은 결과가 발생할 수 있습니다.

예: 여정 시작 시 프로필이 &quot;실버 고객&quot; 대상의 자격을 갖지만 3일 대기 동안 &quot;골드 고객&quot;으로 업그레이드하면 대기 후 활동에서 업데이트된 &quot;골드 고객&quot; 상태를 보게 됩니다.

## 자동 대기 노드  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="자동 대기 노드 정보"
>abstract="이 활동 뒤에 **대기** 활동이 자동으로 추가됩니다. 3일로 설정되어 있습니다. 필요에 따라 제거하거나 구성할 수 있습니다."

각 인바운드 경험 활동(인앱 메시지, 코드 기반 경험 또는 카드)에는 3일 **대기** 활동이 제공됩니다. 프로필이 여정 끝에 도달하면 인바운드 메시지가 자동으로 종료되므로 사용자가 적어도 3일 동안 이를 볼 수 있다고 가정합니다. 이 **대기** 활동을 제거하거나 필요한 경우 구성을 변경할 수 있습니다.
