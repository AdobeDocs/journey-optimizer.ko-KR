---
solution: Journey Optimizer
product: journey optimizer
title: 평일에만 이메일 보내기
description: Adobe Journey Optimizer에서 평일에만 이메일을 전송하도록 여정을 구성하는 방법 알아보기
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 사용 사례, 평일, 조건, 이메일, 예약
version: Journey Orchestration
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 1%

---

# 평일에만 이메일 보내기 {#send-emails-only-on-weekdays}

이 사용 사례에서는 평일(월요일부터 금요일까지)에만 이메일을 보내는 Adobe Journey Optimizer의 여정을 구성하는 방법을 보여 줍니다. 주말(토요일 또는 일요일)에 여정을 입력하는 프로필의 경우 전자 메일은 지정된 시간에 자동으로 큐에 올라가 월요일에 전송됩니다. 이렇게 하면 주 중에 메시지를 전달하여 최적의 참여를 보장합니다.

## 사용 사례 개요

**과제**: 프로필이 주말에 여정에 들어갈 수 있더라도 이메일이 평일에만 전송되도록 합니다. 주말 게시물의 경우, 이메일은 특정 시간에 큐에 올라가 월요일에 전송되어야 합니다.

**솔루션**: 조건 활동을 사용하여 요일을 식별합니다. 주말 항목의 경우, 사용자 정의 수식이 있는 대기 활동이 이메일을 월요일까지 지연시킵니다. 평일 항목은 이메일 전송 단계로 직접 진행됩니다.

이 접근 방법에서는 조건 활동을 사용하여 현재 요일이 토요일이나 일요일인지 확인하고, 주말 항목에 대해 사용자 지정 수식으로 대기 활동을 구현하고, 특정 시간에 월요일 배달에 대해 주말 이메일 대기열을 만들고, 평일 항목(월요일-금요일)에 대해 즉시 이메일을 보내는 방법을 보여 줍니다.

이 접근 방식은 B2B(기업 간) 이메일 캠페인, 전문 뉴스레터 및 커뮤니케이션, 비즈니스 관련 공지 사항, 작업 관련 제품 업데이트 및 주말 배송을 원하지 않는 모든 마케팅 캠페인에 이상적입니다.

>[!NOTE]
>
>이 사용 사례를 구현하려면 구성된 [이메일 채널 표면](../configuration/channel-surfaces.md), 여정을 트리거할 [대상](../audience/about-audiences.md) 또는 [이벤트](../event/about-events.md)를 사용하는 활성 Adobe Journey Optimizer 인스턴스와 [여정 조건](condition-activity.md) 및 [표현식](expression/expressionadvanced.md)에 대한 기본 이해가 필요합니다.


## 구현 단계

### 1단계: 여정 만들기

1. Adobe Journey Optimizer의 **[!UICONTROL 여정 관리]** > **[!UICONTROL 여정]**(으)로 이동합니다.

1. **[!UICONTROL 여정 만들기]**&#x200B;를 클릭하여 [새 여정 만들기](journey-gs.md)를 클릭합니다.

1. [여정 속성](journey-properties.md)을 구성하십시오.

1. 여정 진입점을 선택합니다.
   * **[대상자 읽기](read-audience.md)**: 특정 대상자를 타겟팅하는 일괄 캠페인의 경우
   * **[이벤트](../event/about-events.md)**: 고객 행동에 따라 실시간으로 트리거되는 여정

### 2단계: 요일을 확인하는 조건 활동 추가

여정 시작 직후 **[!UICONTROL 조건]** 활동을 추가하여 현재 날짜가 토요일이나 일요일인지 확인하십시오. 이에 따라 워크플로우가 분기됩니다.

1. 진입점 뒤에 [**[!UICONTROL 조건&#x200B;]**활동](condition-activity.md)을 캔버스로 끌어서 놓습니다.

1. **[!UICONTROL 조건]** 활동을 클릭하여 구성 패널을 엽니다.

1. 조건 유형으로 **[!UICONTROL 시간 조건]**&#x200B;을(를) 선택하십시오.

1. 시간 필터링 옵션으로 **[!UICONTROL 요일]**&#x200B;을(를) 선택합니다.

1. **첫 번째 경로(토요일)**&#x200B;에 대해 **토요일**&#x200B;만 선택하십시오. 이 경로의 레이블을 &quot;Saturday&quot;로 지정합니다.

1. 두 번째 조건을 만들려면 **[!UICONTROL 경로 추가]**&#x200B;를 클릭합니다.

1. **초 경로(일요일)**&#x200B;에 대해 **[!UICONTROL 요일]**&#x200B;을 선택하고 **일요일**&#x200B;만 선택합니다. 이 경로의 레이블을 &quot;Sunday&quot;로 지정합니다.

   ![식 편집기에서 토요일 및 일요일 조건 구성](assets/weekday-email-uc-condition-expression.png)


1. **[!UICONTROL 경로 표시]**&#x200B;을(를) 선택하여 평일 항목(월요일-금요일)에 대한 경로를 만듭니다.

>[!NOTE]
>
>요일 평가에 사용되는 시간대는 조건 수준이 아닌 여정 속성의 여정 수준에서 정의됩니다. 수식에 사용된 여정 [표준 시간대](timezone-management.md)은(는) 수신자의 표준 시간대가 아니라 여정의 구성된 표준 시간대입니다.

### 3단계: 주말 항목에 대한 대기 활동 구성

토요일 또는 일요일에 입력한 프로필의 경우, 사용자 지정 수식이 있는 **[!UICONTROL 대기]** 활동을 사용하여 이메일을 원하는 시간대의 월요일까지 지연하십시오.

**[!UICONTROL 대기]** 활동에서 다음 수식을 사용합니다.

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

위치:

* **X**&#x200B;은(는) 대기할 일 수입니다.
   * 토요일은 **2** 사용(월요일까지 대기)
   * 일요일에는 **1** 사용(월요일까지 대기)
* **시간**&#x200B;은(는) 보낼 시간입니다(예: 오전 9시 **9**).


토요일의 **예:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**일요일의 예:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

여정에서 이를 구현하려면 다음을 수행하십시오.

1. **토요일 경로**&#x200B;에서 조건 뒤에 **[!UICONTROL 대기]** 활동을 추가합니다.

1. 대기 유형으로 **[!UICONTROL 기간]**&#x200B;을(를) 선택하십시오.

1. 사용자 지정 수식을 입력하려면 **[!UICONTROL 고급 모드]**&#x200B;를 클릭하십시오.

1. 입력: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![토요일, 일요일, 평일 등 세 가지 조건 경로가 있는 여정](assets/weekday-email-uc-paths.png)

1. **을(를) 사용하여**&#x200B;일요일 경로`toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`에 대해 동일한 단계를 반복합니다.

>[!TIP]
>
>더 복잡한 업무 시간(예: 평일 오전 9시에서 오후 5시 사이에만 전송)의 경우 공식 및 조건을 더욱 향상시킬 수 있습니다.

### 4단계: 평일 분기

월요일부터 금요일까지 입력하는 프로필의 경우 평소대로 이메일 전송 단계로 진행합니다.

1. **평일 경로**(&quot;기타 사례&quot; 경로)에서 **[!UICONTROL 전자 메일]** 작업 활동을 추가하도록 직접 진행하십시오. 평일 항목에는 **[!UICONTROL 대기]** 활동이 필요하지 않습니다.

1. 필요에 따라 이메일 메시지를 구성합니다.

### 5단계: 여정 흐름 완료

토요일과 일요일 경로 모두에서 **[!UICONTROL 대기]** 활동이 끝나면 세 경로(토요일, 일요일, 평일)가 모두 동일한 **[!UICONTROL 이메일]** 작업 활동으로 이동해야 합니다. 전자 메일 뒤에 **[!UICONTROL End]** 활동을 추가합니다.

### 시각적 워크플로우 개요

전체 여정 워크플로우는 다음 논리를 따릅니다.

* **시작** → **[!UICONTROL 조건]**: 토요일입니까, 일요일입니까?
   * **예(토요일):** **[!UICONTROL 월요일 오전 9시까지 대기]** → **[!UICONTROL 이메일 보내기]**
   * **예(일요일):** **[!UICONTROL 월요일 오전 9시까지 대기]** → **[!UICONTROL 이메일 보내기]**
   * **아니요(월요일~금요일):** **[!UICONTROL 즉시 메일 보내기]**

이렇게 하면 모든 이메일이 평일에만 전송되고, 주말 항목이 월요일 배달을 위해 자동으로 큐에 올라갑니다.

### 6단계: 여정 테스트

게시하기 전에 Adobe Journey Optimizer의 테스트 모드에서 여정 논리를 철저히 테스트하여 모든 것이 예상대로 작동하는지 확인하십시오.

1. 오른쪽 상단의 **[!UICONTROL 테스트]** 단추를 클릭합니다.

1. [테스트 모드](testing-the-journey.md)를 사용하도록 설정합니다.

1. 다른 요일에 시뮬레이션된 시작 시간을 사용하여 [테스트 프로필](../audience/creating-test-profiles.md)을 만듭니다.
   * **Saturday entry**: 프로필이 Saturday 경로를 따르고, 기다리고, 월요일에 지정된 시간에 이메일을 받는지 확인합니다.
   * **Sunday entry**: 프로필이 Sunday 경로를 따라 지정되는 시간에 기다렸다가 월요일에 이메일을 수신하는지 확인합니다.
   * **월요일-금요일 항목**: 전자 메일이 대기 없이 즉시 전송되는지 확인

1. 여정 시각화를 검토하여 프로필이 올바른 조건부 경로(토요일, 일요일 또는 평일)를 따르는지 확인하십시오.

1. 여정에서 [오류 또는 경고](troubleshooting.md)를 확인하십시오.

1. 대기 공식이 원하는 월요일 배달 시간에 대한 올바른 기간을 계산하는지 확인합니다.

>[!IMPORTANT]
>
>항상 테스트 모드에서 여정 논리를 테스트하여 대기 활동이 예상대로 작동하는지 확인하십시오. 테스트 모드를 사용하여 다양한 시작 시나리오를 시뮬레이션하고 주말 항목이 월요일 게재를 위해 올바르게 큐에 있는지 확인하십시오. 자세한 내용은 [여정 테스트 모범 사례](testing-the-journey.md)를 참조하세요.

### 7단계: 여정 게시

테스트가 완료되면:

1. 오른쪽 상단 모서리에서 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

1. [게시](publish-journey.md)를 확인합니다.

1. [여정 보고](report-journey.md) 및 [실시간 보고서](../reports/journey-live-report.md)를 사용하여 여정 성능을 모니터링합니다.


## 관련 항목

* [조건 활동](condition-activity.md) - 여정에서 다양한 경로를 만드는 방법을 알아봅니다.
* [여정에서 조건 사용](conditions.md) - 여정 조건에 대한 세부 안내서
* [대기 활동](wait-activity.md) - 대기 기간 및 수식 구성
* [날짜 함수](functions/date-functions.md) - 날짜 및 시간 함수에 대한 전체 참조
* [식 편집기](expression/expressionadvanced.md) - 복잡한 식을 빌드합니다.
* [여정 모범 사례](journey-gs.md#best-practices) - 여정 디자인에 대한 권장 접근 방식
