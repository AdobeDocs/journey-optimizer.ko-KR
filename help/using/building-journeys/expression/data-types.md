---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 유형
description: 고급 표현식의 데이터 유형에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 표현식, 데이터, 데이터 유형, 여정
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 3%

---

# 데이터 유형 {#data-types}

기술적으로, 상수는 항상 데이터 형식을 포함합니다. 리터럴 표현식에서는 값만 지정합니다. 값(예: 문자열, 정수, 십진수 등)에서 데이터 형식을 유추할 수 있습니다. 날짜 시간과 같은 특정한 경우에, 우리는 표현에 전용 함수를 사용한다.

아래 섹션에서는 다양한 데이터 유형 표현식과 표현식을 표시하는 방법에 대한 정보를 제공합니다.

## 문자열 {#string}

**설명**

일반적인 문자 시퀀스. 사용 가능한 메모리 양과 같은 환경에서 발생하는 암시적 크기 외에는 특정 크기가 없습니다.

JSON 형식: 문자열

직렬화 형식: UTF-8

**리터럴 표시**

```json
"<value>"
```

```json
'<value>'
```

**예**

```json
"hello world"
```

```json
'hello world'
```

## 정수 {#integer}

**설명**

-2^63부터 2^63-1까지의 정수 값입니다.

JSON 형식: 숫자

**리터럴 표시**

```json
<integer value>
```

**예**

```json
42
```

## decimal {#decimal}

**설명**

10진수입니다. 부동 값을 나타냅니다.

* double 유형의 가장 큰 양의 유한 값, (2-2^-52)x2^1023
* double 유형의 가장 작은 양의 정규 값, 2-1022
* double, 2 p-1074 유형의 가장 작은 양수 nonzero 값

JSON 형식: 숫자

직렬화 형식: 소수점 구분 기호로 &#39;.&#39;를 사용합니다.

**리터럴 표시**

```json
<integer value>.<integer value>
```

**예**

```json
3.14
```

## 부울 {#boolean}

**설명**

소문자로 작성된 부울 값: true 또는 false

JSON 형식: 부울

**리터럴 표시**

```json
true
```

```json
false
```

**예**

```json
true
```

## dateOnly {#date-only}

**설명**

표준 시간대 없이 1년 1개월로 표시된 날짜만 나타냅니다.

생일에 사용되는 날짜에 대한 설명입니다.

JSON 형식: 문자열.

형식은 YYYY-MM-DD(ISO-8601)입니다(예: &quot;2021-03-11&quot;).

toDateOnly 함수에 캡슐화할 수 있습니다.

DateTimeFormatter ISO_LOCAL_DATE_TIME을 사용하여 값을 deserialize 및 serialize합니다. [자세히 알아보기](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**리터럴 표시**

```json
date("<dateOnly in ISO-8601 format>")  
```

**예**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**설명**

표준 시간대 없이 연-월-일-시간-분-초(밀리초)로 표시되는 날짜 시간을 나타냅니다.

JSON 형식: 문자열.

시간대를 저장하거나 나타내지 않습니다. 대신, 월시계에서 본 현지 시간과 결합하여 생일 때 사용되는 날짜의 설명입니다.

오프셋이나 시간대와 같은 추가 정보 없이 타임라인에서 순간을 나타낼 수 없습니다.

toDateTimeOnly 함수에 캡슐화할 수 있습니다.

직렬화 포맷: ISO-8601 확장 오프셋 날짜-시간 포맷.

DateTimeFormatter ISO_LOCAL_DATE_TIME을 사용하여 값을 deserialize 및 serialize합니다. [자세히 알아보기](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME"){_blank}

**리터럴 표시**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**예**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**설명**

시간대도 고려하는 날짜 시간 상수입니다. UTC의 오프셋이 있는 날짜-시간을 나타냅니다.

오프셋의 추가적 정보를 가지고 순간적으로 볼 수 있다. 세계의 일정한 장소에서 특정한 &#39;순간&#39;을 나타내는 방법이다.

JSON 형식: 문자열.

toDateTime 함수에 캡슐화할 수 있습니다.

직렬화 포맷: ISO-8601 확장 오프셋 날짜-시간 포맷.

DateTimeFormatter ISO_OFFSET_DATE_TIME을 사용하여 값을 deserialize 및 serialize합니다. [자세히 알아보기](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}

에포크 값을 전달하는 정수를 전달할 수도 있습니다. [자세히 보기](https://www.epochconverter.com){_blank}.

시간대는 오프셋 또는 시간대 코드(예: 유럽/파리, Z - UTC 의미)로 지정할 수 있습니다.

**리터럴 표시**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**예**

```json
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## 지속 시간 {#duration}

**설명**

이는 &#39;34.5초&#39;와 같이 시간 기반 시간을 나타냅니다. 그것은 밀리초로 수량이나 시간을 모델링한다.

지원되는 시간 단위는 밀리초, 초, 분, 시간, 일수가 24시간과 같은 경우입니다. 연도 및 월은 고정된 시간이 아니므로 지원되지 않습니다.

JSON 형식: 문자열.

toDuration 함수에 캡슐화해야 합니다.

직렬화 형식: 시간대 ID를 역직렬화하려면 java 함수 java.time을 사용합니다.

Duration.parse: 허용되는 형식은 ISO-8601 기간 형식 PnDTnHnMn.nS를 기반으로 하며, 일은 정확히 24시간으로 간주됩니다. [자세히 알아보기](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}

**리터럴 표시**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**예**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## list {#list}

**설명**

대괄호를 구분 기호로 사용하여 쉼표로 구분된 표현식 목록입니다.

다형성은 지원되지 않으므로 목록에 포함된 모든 표현식의 유형이 같아야 합니다.

**리터럴 표시**

```json
[<expression>, <expression>, ... ]
```

**예**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 JSON 형식, 직렬화 규칙 및 리터럴 표현 구문과 함께 여정 고급 표현식 편집기에서 지원되는 모든 데이터 형식(문자열, 정수, 십진수, 부울, dateOnly, dateTimeOnly, dateTime, duration 및 목록)에 대해 설명합니다.

**의도:**

* 여정 표현식을 작성할 때 각 데이터 유형에 대한 올바른 리터럴 구문을 식별합니다
* `dateOnly`, `dateTimeOnly` 및 `dateTime` 형식 간의 차이점 및 각 형식을 사용할 시기를 파악합니다.
* `toDuration()` 함수와 함께 ISO-8601 형식 또는 밀리초를 사용하여 기간 값을 나타냅니다.
* 컬렉션 작업에 사용할 대괄호 구문을 사용하여 목록 식을 구성합니다.
* 변환 함수(`toDateTime`, `toDateTimeOnly`, `toDuration`, `toDateOnly`)를 사용하여 형식화된 상수를 만드십시오.

**용어집:**

* **dateOnly**: 표준 시간대 또는 표준 시간대 없이 YYYY-MM-DD 형식의 날짜로, 생일이나 달력 날짜에 적합합니다. *(제품별)*
* **dateTimeOnly**: 시간대 정보가 없는 날짜 및 시간입니다. 오프셋 *(제품별)* 없이 특정 인스턴스를 표시할 수 없습니다.
* **dateTime**: 특정 인스턴스를 나타내는 UTC 오프셋을 포함하는 날짜-시간 상수입니다. epoch 정수 *(제품별)*&#x200B;에서도 만들 수 있습니다.
* **duration**: 시간 기반 금액(밀리초)입니다. ISO-8601 `PnDTnHnMn.nS` 형식을 사용합니다. 연도 및 월은 지원되지 않습니다. *(제품별)*
* **list**: 대괄호 *(제품별)로 구분된 동일한 형식의 쉼표로 구분된 컬렉션입니다.*

**보호 기능:**

* 기간은 밀리초, 초, 분, 시간 및 일만 지원합니다. 연도 및 월은 고정된 시간이 아니므로 지원되지 않습니다
* `duration` 값은 `toDuration()`에 래핑해야 합니다. 리터럴로 표현할 수 없습니다.
* `list`에 있는 모든 식의 형식이 같아야 합니다. 다형성은 지원되지 않습니다.
* `dateTimeOnly`은(는) 추가 오프셋이나 표준 시간대 없이 인스턴트 인타임을 표시할 수 없습니다.

**용어:**

* 정식 이름: 데이터 유형 — 약어: 없음 — 변형: 표현식 데이터 유형, 여정 데이터 유형
* 동의어: &quot;dateTime&quot; = &quot;date-time with timezone&quot;; &quot;dateTimeOnly&quot; = &quot;local date-time&quot;
* 혼동하지 마십시오. `dateOnly`(시간 없음) ≠ `dateTimeOnly`(날짜 + 시간, 시간대 없음) ≠ `dateTime`(날짜 + 시간 + 시간대/오프셋)

**FAQ:**

* **Q: `dateTimeOnly`과(와) `dateTime`의 차이점은 무엇입니까?** — `dateTimeOnly`에는 표준 시간이나 오프셋이 없으므로 정확한 순간을 나타낼 수 없습니다. `dateTime`에는 UTC 오프셋이 포함되며 특정 시간을 나타냅니다.
* **Q: 2일 3시간의 기간을 표현하려면 어떻게 해야 합니까?** — `toDuration("P2DT3H")` 사용.
* **Q: 목록 식에서 정수와 문자열을 혼합할 수 있습니까?** — 아니요. 목록에 있는 모든 표현식은 같은 형식이어야 합니다.
* **Q: Epoch 타임스탬프(밀리초)에서 `dateTime`을(를) 만들려면 어떻게 합니까?** — `toDateTime(<epoch in milliseconds>)`(예: `toDateTime(1560762190189)`)을(를) 사용합니다.
* **Q: `true` 또는 `True`이(가) 올바른 부울 리터럴입니까?** — 소문자 `true` 또는 `false`을(를) 사용합니다. 대문자인 변형이 잘못되었습니다.

+++
