---
product: journey optimizer
title: 날짜 함수
description: 날짜 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 날짜, 함수, 표현식, 여정, 시간
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1275
ht-degree: 7%

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

>[!NOTE]
>
>이 페이지의 함수는 여정 표현식에서 사용할 수 있습니다. `now()`과(와) 같은 일부 함수는 전자 메일 콘텐츠의 개인화 편집기에서 사용할 수 없습니다. [자세히 알아보기](../../personalization/functions/dates.md)

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

+++예시

`currentTimeInMillis()`

&quot;1544712617131&quot;를 반환합니다.

+++

## inLastDays {#inLastDays}

지정된 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 일).

+++구문

`inLastDays(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastDays(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inLastHours {#inLastHours}

지정된 날짜 시간이 지금부터 델타 시간 사이인 경우 true를 반환합니다.

+++구문

`inLastHours(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastHours(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

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

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastMonths(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inLastYears {#inLastYears}

지정된 date 또는 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 연도).

+++구문

`inLastYears(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inLastYears(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextDays {#inNextDays}

지정된 date 또는 dateTime이 now와 now + delta 일 사이인 경우 true를 반환합니다.

+++구문

`inNextDays(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextDays(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextHours {#inNextHours}

지정된 date 또는 dateTime이 now와 now + delta 시간 사이에 있으면 true를 반환합니다.

+++구문

`inNextHours(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextHours(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextMonths {#inNextMonths}

지정된 date 또는 dateTime이 now와 now + delta 개월 사이에 있으면 true를 반환합니다.

+++구문

`inNextMonths(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextMonths(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## inNextYears {#inNextYears}

지정된 date 또는 dateTime이 now와 now + delta years 사이에 있으면 true를 반환합니다.

+++구문

`inNextYears(<dateTime>,<delta>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

+++

+++서명 및 반환된 유형

`inNextYears(<dateTime>,<integer>)`

부울 반환.

+++

+++예시

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

true를 반환합니다.

+++

## now {#now}

현재 날짜를 날짜 시간 형식으로 반환합니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

>[!NOTE]
>
>이 함수는 여정 표현식에서만 사용할 수 있습니다. 전자 메일 개인화 및 기타 콘텐츠의 경우 `getCurrentZonedDateTime()`을(를) 대신 사용하십시오. [자세히 알아보기](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++구문

`now(<parameter>)`

+++

+++매개변수

| 매개 변수 | 설명 |
|--- |--- |
| 문자열 | 시간대 식별자(선택 사항) |

+++

+++서명 및 반환된 유형

`now()`

`now("<timeZone id>")`

dateTime을 반환합니다.

+++

+++예시

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

| 매개 변수 | 설명 |
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

+++예시

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

| 매개 변수 | 유형 |
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

+++예시

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

| 매개 변수 | 유형 |
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

+++예시

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

+++예시

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

2023-08-28T17:15:30.123+02:00을 반환합니다.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

타임스탬프 필드의 값이 `2021-11-16T16:55:12.939318+01:00`이면 함수는 `2021-11-17T02:55:12.942115+11:00`을(를) 반환합니다.

+++

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 AJO 여정 표현식에서 사용할 수 있는 모든 날짜 및 시간 함수를 문서화하고, 현재 시간을 얻는 방법을 다루고, 날짜가 상대 시간 기간에 속하는지 여부를 확인하고, 날짜/시간 구성 요소를 수정하는 방법을 설명합니다.

**의도:**
* `now` 또는 `nowWithDelta`을(를) 사용하여 현재 날짜/시간(선택적 시간대 포함) 가져오기
* `currentTimeInMillis`을(를) 사용하여 현재 시간을 에포크 정수로 검색
* 날짜/시간이 `inLastDays`, `inLastHours`, `inLastMonths`, `inLastYears`을(를) 사용하여 최근 N일, 시간, 월 또는 년 이내에 속하는지 확인
* `inNextDays`, `inNextHours`, `inNextMonths`, `inNextYears`을(를) 사용하여 날짜/시간이 다음 N일, 시간, 월 또는 년 이내에 속하는지 확인
* `setHours` 또는 `setDays`을(를) 사용하여 datetime 값에 특정 시간 또는 월 일 강제 적용
* `updateTimeZone`을(를) 사용하여 동일한 인스턴스를 유지하면서 날짜/시간을 다른 시간대로 변환

**용어집:**
* **dateTime**: 시간대 오프셋 정보 *(제품별)가 포함된 날짜-시간 값*
* **dateTimeOnly**: 시간대 정보가 없는 날짜-시간 값 *(제품별)*
* **epoch 밀리초**: 1970-01-01T00:00:00Z 이후 경과된 시간(밀리초)을 나타내는 정수
* **delta**: 현재 시간을 년, 월, 일, 시간, 분 또는 초로 보내기 위해 `nowWithDelta`과(와) 함께 사용되는 정수 오프셋(양수 또는 음수)입니다.

**보호 기능:**
* `now()`은(는) 여정 식에서만 사용할 수 있습니다. 전자 메일 개인화를 위해 `getCurrentZonedDateTime()`을(를) 대신 사용하십시오.
* `nowWithDelta`의 시간대 ID는 문자열 상수여야 합니다. 필드 참조 및 동적 식은 지원되지 않습니다.
* `updateTimeZone`의 시간대 ID는 문자열 상수여야 합니다.

**용어:**
* 정식 이름: 날짜 함수 — 약어: 없음 — 변형: 날짜-시간 함수, 임시 함수
* 동의어: &quot;now()&quot; = &quot;current datetime&quot;; &quot;currentTimeInMillis()&quot; = &quot;current epoch milliseconds&quot;
* 혼동하지 마십시오. &quot;inLastDays&quot;(시간 후 전환) ≠ &quot;inNextDays&quot;(시간 후 전환)
* 혼동하지 마십시오. &quot;setHours&quot;(시간 구성 요소 대체) ≠ &quot;nowWithDelta&quot;(현재 시간 오프셋)
* 혼동하지 마십시오. &quot;updateTimeZone&quot;(같은 인스턴트, 다른 시간대 표시) ≠ &quot;setHours&quot;(시간 값 자체를 변경)

**FAQ:**
* **Q: 전자 메일 개인화 콘텐츠에서 `now()`을(를) 사용할 수 있습니까?** — 아니요. `now()`은(는) 여정 식에서만 사용할 수 있습니다. 전자 메일 개인화에 `getCurrentZonedDateTime()`을(를) 사용합니다.
* **Q: 지난 24시간 동안 이벤트가 발생했는지 어떻게 확인할 수 있습니까?** — `inLastHours(@event{MyEvent.timestamp}, 24)` 사용.
* **Q: 지난 2시간 동안 현재 시간 오프셋을 가져오려면 어떻게 해야 합니까?** — `nowWithDelta(-2, "hours")` 사용.
* **Q: `updateTimeZone`이(가) `setHours`과(와) 다르게 수행하는 작업** — `updateTimeZone`은(는) 같은 시간을 유지하지만 다른 시간대에 표시하는 반면 `setHours`은(는) 실제로 datetime 값의 hour 구성 요소를 변경합니다.
* **Q: `nowWithDelta`의 시간대 매개 변수가 프로필 필드일 수 있습니까?** — 아니요. 시간대 ID는 문자열 상수여야 합니다. 필드 참조는 지원되지 않습니다.

+++
