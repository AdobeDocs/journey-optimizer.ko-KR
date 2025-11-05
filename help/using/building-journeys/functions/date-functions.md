---
product: journey optimizer
title: 날짜 함수
description: 날짜 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 날짜, 함수, 표현식, 여정, 시간
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 12%

---

# 날짜 함수 {#date-functions}

날짜 함수를 사용하면 여정 표현식 내에서 날짜 및 시간 값을 조작하고 작업할 수 있습니다. 이러한 함수는 고객 여정에서 시간 기반 조건, 예약 및 임시 계산에 필수적입니다.

다음을 수행해야 하는 경우 날짜 함수 사용:

* 특정 시간대 처리([now](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))를 사용하여 현재 시간 또는 날짜 가져오기
* 날짜가 특정 시간 범위([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears)) 내에 있는지 확인
* 날짜 및 시간 구성 요소([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone)) 수정
* 시간 기반 계산 및 비교 수행
* 다양한 시간 형식과 표현 간 변환

날짜 함수를 사용하면 시간 논리를 정확하게 제어할 수 있으므로 특정 시간대 및 일정에 응답하는 시간 구분 여정 경로 및 조건을 만들 수 있습니다.

## currentTimeInMillis {#currentTimeInMillis}

에포크 밀리초로 현재 시간을 반환합니다.

+++구문

`currentTimeInMillis()`

+++

+++매개변수

이 함수는 매개 변수를 사용하지 않습니다.

+++

+++서명 및 반환된 유형

`currentTimeInMillis()`

정수 반환.

+++

+++예

`currentTimeInMillis()`

&quot;1544712617131&quot;를 반환합니다.

+++

## inLastDays {#inLastDays}

지정된 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 일).

+++구문

`inLastDays(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastDays(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inLastHours {#inLastHours}

지정된 날짜 시간이 지금부터 델타 시간 사이인 경우 true를 반환합니다.

+++구문

`inLastHours(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastHours(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

`inLastHours(@event{MyEvent.timestamp}, 4)`

true를 반환합니다.

+++

## inLastMonths {#inLastMonths}

지정된 date 또는 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 월).

+++구문

`inLastMonths(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastMonths(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inLastYears {#inLastYears}

지정된 date 또는 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 연도).

+++구문

`inLastYears(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastYears(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextDays {#inNextDays}

지정된 date 또는 dateTime이 now와 now + delta 일 사이인 경우 true를 반환합니다.

+++구문

`inNextDays(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextDays(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextHours {#inNextHours}

지정된 date 또는 dateTime이 now와 now + delta 시간 사이에 있으면 true를 반환합니다.

+++구문

`inNextHours(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextHours(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextMonths {#inNextMonths}

지정된 date 또는 dateTime이 now와 now + delta 개월 사이에 있으면 true를 반환합니다.

+++구문

`inNextMonths(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextMonths(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextYears {#inNextYears}

지정된 date 또는 dateTime이 now와 now + delta years 사이에 있으면 true를 반환합니다.

+++구문

`inNextYears(<dateTime>,<delta>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextYears(<dateTime>,<integer>)`

부울 반환.

+++

+++예

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## now {#now}

현재 날짜를 날짜 시간 형식으로 반환합니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

+++구문

`now(<parameter>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 시간대 식별자(선택 사항) |

+++

+++서명 및 반환된 유형

`now()`

`now("<timeZone id>")`

dateTime을 반환합니다.

+++

+++예

`now()`

2023-06-03T06:30Z을 반환합니다.

`toString(now())`

&quot;2023-06-03T06:30Z&quot; 반환

`now("Europe/Paris")`

2023-06-03T08:30+02:00을 반환합니다.

+++

## nowWithDelta {#nowWithDelta}

오프셋을 포함하여 현재 날짜/시간을 반환합니다. 시간대 ID를 지정하면 시간대 오프셋이 적용됩니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

+++구문

`nowWithDelta(<parameters>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| 델타 | 양의 정수 값 또는 음의 정수 값 |
| 날짜 부분 | years, months, days, hours, minutes 또는 seconds as a string |
| 시간대 id | 시간대 값의 문자열 표현입니다. 자세한 내용은 [데이터 형식](../expression/data-types.md)을 참조하세요. 시간대 ID는 문자열 상수여야 합니다. 필드 참조나 식이 될 수 없습니다. |

+++

+++서명 및 반환된 유형

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

dateTime을 반환합니다.

+++

+++예

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

정확히 2시간 전의 dateTime을 반환합니다.

+++

## setHours {#setHours}

날짜 시간 또는 날짜 시간의 시간만 설정합니다. 예를 들어 내일 특정 시간까지 기다리려면 시간을 강제로 지정할 수 있습니다.

+++구문

`setHours(<parameter>)`

+++

+++매개변수

| 매개변수 | 유형 |
|--- |--- |
| 날짜 시간 | dateTime |
| 시간대를 고려하지 않은 날짜 시간 | dateTimeOnly |
| 시간 | 정수 |

+++

+++서명 및 반환된 유형

`setHours(<dateTime>,<hours>)`

날짜/시간을 반환합니다.

`setHours(<dateTimeOnly>,<hours>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

+++

+++예

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

2023-12-12T04:11:00Z를 반환합니다.

`setHours(nowWithDelta(1, "days"), 20)`

내일 오후 8:XY에 반환합니다. XY는 현재 시간 평가 시점의 분입니다. 평가가 오전 2:45에 이루어지면 반환된 시간은 오후 8:45입니다.

+++

## setDays {#setDays}

날짜/시간 또는 날짜/시간만 설정합니다. 예를 들어, 특정 날짜까지 기다리려면 날짜를 강제로 지정할 수 있습니다.

+++구문

`setDays(<parameter>)`

+++

+++매개변수

| 매개변수 | 유형 |
|--- |--- |
| 날짜 시간 | dateTime |
| 시간대를 고려하지 않은 날짜 시간 | dateTimeOnly |
| 일 | 정수 |

+++

+++서명 및 반환된 유형

`setDays(<dateTime>,<days>)`

날짜/시간을 반환합니다.

`setDays(<dateTimeOnly>,<days>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

+++

+++예

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

2023-12-25T01:11:00Z를 반환합니다.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

같은 순간에 새 시간대와 함께 새 날짜 시간을 반환합니다.

+++구문

`updateTimeZone(<parameters>)`

+++

+++매개변수

* 시간대 id: 문자열
* dateTime

+++

+++서명 및 반환된 유형

`updateTimeZone(<dateTime>,<timeZone id>)`

날짜/시간을 반환합니다.

+++

+++예

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

2023-08-28T17:15:30.123+02:00을 반환합니다.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

타임스탬프 필드의 값이 `2021-11-16T16:55:12.939318+01:00`이면 함수는 `2021-11-17T02:55:12.942115+11:00`을(를) 반환합니다.

+++

