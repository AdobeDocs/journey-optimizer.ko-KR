---
solution: Journey Optimizer
product: journey optimizer
title: 연산자
description: 고급 표현식의 연산자에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 표현식, 구문, 연산자, 편집기, 여정
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# 연산자 {#operators}

연산자에는 단항 연산자와 이항 연산자의 두 종류가 있다. 왼쪽 단항 연산자와 오른쪽 단항 연산자가 있습니다.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 중요 정보{#important-notes}

* 곱셈(`*`)을 사용할 때는 두 연산 필드의 형식이 같아야 합니다(정수 또는 십진수). 예 :
   * 다음 예제는 올바릅니다. `3.0 * 4.0`
   * `3 * 4.0`에 오류가 발생합니다.

* `+` 연산자를 사용하는 경우 식을 괄호로 묶어야 합니다. 예:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))`이(가) 올바릅니다.
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))`에 오류가 발생합니다.

## 논리적  {#logical}

### 및

```json
<expression1> and <expression2>
```

&lt;expression1>과 &lt;expression2> 모두 부울이어야 합니다. 결과는 부울입니다.

예:

```json
3.14 > 2 and 3.15 < 1
```

### 또는

```json
<expression1> or <expression2>
```

&lt;expression1>과 &lt;expression2> 모두 부울이어야 합니다. 결과는 부울입니다.

예:

```json
3.14 > 2 or 3.15 < 1
```

### 아님

```json
not <expression>
```

&lt;expression>은(는) 부울이어야 합니다. 결과는 부울입니다.

예:

```json
not 3.15 < 1
```

## 비교 {#comparison}

### null임

```json
<expression> is null
```

결과는 부울입니다.

null은 표현식에 평가된 값이 없음을 의미합니다.

예:

```json
@event{BarBeacon.location} is null
```

### null이 아님

```json
<expression> is not null
```

결과는 부울입니다.

null은 표현식에 평가된 값이 없음을 의미합니다.

예:

```json
@event{BarBeacon.location} is not null
```

### 이(가) null임

```json
<expression> has null
```

&lt;expression>은(는) 목록이어야 합니다. 결과는 부울입니다.

목록에 Null 값이 하나 이상 포함되어 있음을 식별하는 데 유용합니다.

예:

```json
["foo", "bar", null] has null
```

true 반환

```json
["foo", "bar", ""] has null
```

&quot;&quot;가 null로 간주되지 않으므로 false를 반환합니다.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>&lt;expression1> 및 &lt;expression2>에 대한 데이터 형식 컨트롤이 없습니다.

예:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>&lt;expression1> 및 &lt;expression2>에 대한 데이터 형식 컨트롤이 없습니다.

결과는 부울입니다.

예:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datetime은 Datetime과 비교할 수 있습니다.

Datetimeonly는 Datetimeonly와 비교할 수 있습니다.

정수나 십진수는 모두 정수나 십진수와 비교할 수 있습니다.

다른 조합은 사용할 수 없습니다.

결과는 부울입니다.

예:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datetime은 Datetime과 비교할 수 있습니다.

Datetimeonly는 Datetimeonly와 비교할 수 있습니다.

정수나 십진수는 모두 정수나 십진수와 비교할 수 있습니다.

다른 조합은 사용할 수 없습니다.

결과는 부울입니다.

예:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datetime은 Datetime과 비교할 수 있습니다.

Datetimeonly는 Datetimeonly와 비교할 수 있습니다.

정수나 십진수는 모두 정수나 십진수와 비교할 수 있습니다.

다른 조합은 사용할 수 없습니다.

결과는 부울입니다.

예:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datetime은 Datetime과 비교할 수 있습니다.

Datetimeonly는 Datetimeonly와 비교할 수 있습니다.

정수나 십진수는 모두 정수나 십진수와 비교할 수 있습니다.

다른 조합은 사용할 수 없습니다.

결과는 부울입니다.

예:

```json
42 <= 3.14
```

## 산술 {#arithmetic}

### +

```json
<expression1> + <expression2>
```

두 표현식은 모두 숫자(정수 또는 십진수)여야 합니다.

결과도 숫자입니다.

예:

```json
1 + 2
```

반환 3

### -

```json
<expression1> - <expression2>
```

두 표현식은 모두 숫자(정수 또는 십진수)여야 합니다.

결과도 숫자입니다.

예:

```json
2 - 1 
```

1 반환

### /

```json
<expression1> / <expression2>
```

두 표현식은 모두 숫자(정수 또는 십진수)여야 합니다.

결과도 숫자입니다.

&lt;expression2>는 0이 아니어야 합니다(반환 0).

예:

```json
4 / 2
```

반환 2

### *

```json
<expression1> * <expression2>
```

두 표현식은 모두 숫자(정수 또는 십진수)여야 합니다.

결과도 숫자입니다.

예:

```json
3 * 4
```

12 반환

### %

```json
<expression1> % <expression2>
```

두 표현식은 모두 숫자(정수 또는 십진수)여야 합니다.

결과도 숫자입니다.

예:

```json
3 % 2
```

1을 반환합니다.

## 수학 {#math}

### 숫자임

```json
<expression> is numeric
```

식의 형식은 정수 또는 십진수입니다.

예:

```json
@ is numeric
```

### 정수

```json
<expression> is integer
```

식의 유형은 정수입니다.

예:

```json
@ is integer
```

### 소수임

```json
<expression> is decimal
```

식의 형식은 십진수입니다.

예:

```json
@ is decimal
```

## 문자열 {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

두 표현식을 연결합니다.

하나의 식은 체인 문자열이어야 합니다.

예:

```json
"the current time is " + (now())
```

&quot;현재 시간은 2023-09-23T09:30:06.693Z&quot;를 반환합니다.&quot;

```json
(now()) + " is the current time"
```

&quot;2023-09-23T09:30:06.693Z는 현재 시간&quot; 반환

```json
"a" + "b" + "c" + 1234
```

&quot;abc1234&quot;를 반환합니다.

## 일자 {#date}

### +

```json
<expression> + <duration>
```

dateTime, dateTimeOnly 또는 duration에 duration을 추가합니다.

예:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

_dateTime_ 2023-12-03T15:30:30Z 반환

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

_dateTimeOnly_ 2023-12-03T15:30:30 반환

```json
(now()) + (toDuration("PT1H"))
```

현재 시간으로부터 1시간 후 _dateTime_(UTC 시간대 포함)을 반환합니다.

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

_duration_ PT2H 반환

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지는 논리(`and`, `or`, `not`), 비교(`==`, `!=`, `>`, `>=`, `<`, `<=`, `is null`, `is not null`, `has null`, 산술(`+`, `-`, `/`, `*`, `%`), 연산 유형 검사(`is numeric`, `is integer`, `is decimal`), 문자열 연결 및 날짜 산술 연산자를 다루는 여정 고급 표현식 편집기에서 사용할 수 있는 연산자에 대한 전체 참조입니다.

**의도:**

* 논리 연산자 `and`, `or` 및 `not`을(를) 사용하여 부울 조건을 결합합니다.
* `is null` / `is not null`을(를) 사용하여 필드 또는 식 값이 null인지 여부를 확인합니다.
* `has null` 연산자를 사용하여 목록 내에서 null 값 감지
* `>`, `>=`, `<`, `<=`, `==` 및 `!=`을(를) 사용하여 숫자, datetime 및 datetimeonly 값 비교
* `+`, `-`, `/`, `*` 및 `%`을(를) 사용하여 숫자 값에 대한 산술 연산을 수행합니다.
* `+` 연산자를 사용하여 dateTime, dateTimeOnly 또는 duration 값에 duration을 추가합니다

**용어집:**

* **단항 연산자**: 단일 피연산자에 적용된 연산자입니다. 왼쪽(예: `not`) 또는 오른쪽(예: `is null`) *(제품별)*&#x200B;일 수 있습니다.
* **이진 연산자**: 두 피연산자(예: `and`, `==`, `+`) *(제품별)* 사이에 적용된 연산자
* **has null**: 목록에 하나 이상의 null 요소 *(제품별)이(가) 포함된 경우 true를 반환하는 오른쪽 단항 연산자*
* **은(는) 숫자/은(는) 정수/십진수입니다.**: 식 *(제품별)의 숫자 하위 유형에 따라 부울을 반환하는 유형 확인 연산자*

**보호 기능:**

* 곱셈(`*`)을 사용할 때 두 피연산자는 모두 같은 숫자 유형(정수 또는 소수점 모두)이어야 합니다. 이러한 경우 유형을 혼합하면 오류가 발생합니다
* 날짜 계산에 `+` 연산자를 사용할 때 구문 분석 오류를 방지하려면 식을 괄호로 묶어야 합니다
* 비교 연산자(`>`, `>=`, `<`, `<=`)는 호환 가능한 형식 간에 유효합니다. Datetime은 Datetime이고, DatetimeOnly는 DatetimeOnly이고, numeric은 Datetime이고, 다른 조합은 사용할 수 없습니다
* 빈 문자열 `""`은(는) null로 간주되지 않습니다. `has null`은(는) `""`이(가) 포함된 목록에 대해 false를 반환합니다.
* `==` 및 `!=` 연산자는 피연산자 간에 데이터 형식 제어를 수행하지 않습니다

**용어:**

* 정식 이름: 연산자 — 약어: 없음 — 변형: 표현식 연산자, 여정 연산자
* 동의어: `and` = &quot;logical AND&quot;; `or` = &quot;logical OR&quot;; `not` = &quot;logical NOT&quot;; `%` = &quot;modulo&quot;
* 혼동하지 마십시오. `is null`(식에 평가된 값이 없음) ≠ `== null`(올바른 구문이 아님); `has null`(목록에 null 포함) ≠ `is null`(식 자체가 null임)

**FAQ:**

* **Q: 정수에 십진수를 직접 곱할 수 있습니까?** — 아니요. `*`의 두 피연산자는 같은 형식이어야 합니다. `3.0 * 4.0`(십진수 모두) 또는 `3 * 4`(정수 모두)을(를) 사용합니다.
* **Q: dateTime에 15분을 추가하려면 어떻게 합니까?** — `(toDateTime("...")) + (toDuration("PT15M"))` 사용.
* **Q: `is null`과(와) `has null`의 차이점은 무엇입니까?** — `is null`은(는) 단일 식에 평가된 값이 없는지 확인하고, `has null`은(는) 목록에 null 요소가 하나 이상 있는지 확인합니다.
* **Q: `"" has null`이(가) true를 반환합니까?** — 아니요. 빈 문자열은 null로 간주되지 않으므로 결과는 false입니다.
* **Q: `3 * 4.0`에서 오류가 발생하는 이유는 무엇입니까?** — `*` 연산자를 사용하려면 두 피연산자가 동일한 숫자 유형이 되어야 합니다. 정수와 십진수를 혼합할 수 없습니다.

+++
