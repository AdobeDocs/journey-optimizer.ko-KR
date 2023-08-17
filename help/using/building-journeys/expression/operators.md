---
solution: Journey Optimizer
product: journey optimizer
title: 연산자
description: 고급 표현식의 연산자에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 표현식, 구문, 연산자, 편집기, 여정
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 6%

---

# 연산자 {#operators}

연산자에는 단항 연산자와 이항 연산자의 두 종류가 있다. 왼쪽 단항 연산자와 오른쪽 단항 연산자가 있습니다.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 중요 정보{#important-notes}

* 곱셈 사용 시(`*`)에서 두 작업 필드는 정수나 십진수로 같은 형식을 가져야 합니다. 예 :
   * 다음 예는 올바릅니다. `3.0 * 4.0`
   * `3 * 4.0` 오류가 발생합니다.

## 논리적  {#logical}

### 및

```json
<expression1> and <expression2>
```

모두 &lt;expression1> 및 &lt;expression2> 은(는) 부울이어야 합니다. 결과는 부울입니다.

예:

```json
3.14 > 2 and 3.15 < 1
```

### 또는

```json
<expression1> or <expression2>
```

모두 &lt;expression1> 및 &lt;expression2> 은(는) 부울이어야 합니다. 결과는 부울입니다.

예:

```json
3.14 > 2 or 3.15 < 1
```

### 아님

```json
not <expression>
```

&lt;expression> 은(는) 부울이어야 합니다. 결과는 부울입니다.

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
@{BarBeacon.location} is null
```

### null이 아님

```json
<expression> is not null
```

결과는 부울입니다.

null은 표현식에 평가된 값이 없음을 의미합니다.

예:

```json
@{BarBeacon.location} is not null
```

### 이(가) null임

```json
<expression> has null
```

&lt;expression> 목록이어야 합니다. 결과는 부울입니다.

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
>대상 &lt;expression1> 및 &lt;expression2> 데이터 형식 컨트롤이 없습니다.

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
대상 &lt;expression1> 및 &lt;expression2> 데이터 형식 컨트롤이 없습니다.

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

&lt;expression2> 은(는) 0이 아니어야 합니다(반환 0).

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

&quot;현재 시간은 2019-09-23T09임&quot; 반환:30:06.693Z&quot;

```json
(now()) + " is the current time"
```

&quot;2019-09-23T09 반환:30:06.693Z는 현재 시간입니다.&quot;

```json
"a" + "b" + "c" + 1234
```

&quot;abc1234&quot;를 반환합니다.

## 날짜 {#date}

### +

```json
<expression> + <duration>
```

dateTime, dateTimeOnly 또는 duration에 duration을 추가합니다.

예:

```json
(toDateTime("2011-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

를 반환합니다. _dateTime_ 2011-12-03T15:30:30Z

```json
(toDateTimeOnly("2011-12-03T15:15:30")) + (toDuration("PT15M"))
```

를 반환합니다. _dateTimeOnly_ 2011-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

를 반환합니다. _dateTime_ (UTC 시간대 사용) 현재 시간으로부터 1시간 후

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

를 반환합니다. _지속 시간_ PT2H
