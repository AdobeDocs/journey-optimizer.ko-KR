---
title: 연산자 함수 라이브러리
description: 연산자 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 6%

---

# 연산자 {#operators}

## 부울 함수 {#boolean-functions}

부울 함수는 다른 요소에 부울 로직을 수행하는 데 사용됩니다.

### 및{#and}

다음 `and` 함수는 논리 결합을 만드는 데 사용됩니다.

**구문**

```sql
{%= query1 and query2 %}
```

**예**

다음 작전은 프랑스와 1985년의 출생년도와 같은 본국과 함께 모든 사람들을 돌려보낼 것입니다.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 또는{#or}

다음 `or` 함수는 논리적 분리를 만드는 데 사용됩니다.

**구문**

```sql
{%= query1 or query2 %}
```

**예**

다음 작전은 프랑스와 같은 본국 또는 1985년의 출생년도에 있는 모든 사람들을 돌려보낼 것입니다.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## 비교 함수 {#comparison-functions}

비교 함수는 다른 표현식과 값을 비교하는 데 사용되며, 그에 따라 true 또는 false를 반환합니다.

### 다음과 같음{#equals}

다음 `=` (같음) 함수는 하나의 값 또는 표현식이 다른 값 또는 표현식과 같은지 확인합니다.

**구문**

```sql
{%= expression = value %}
```

**예**

다음 작업에서는 홈 주소 국가가 프랑스인지 확인합니다.

```sql
{%= profile.homeAddress.country = "France" %}
```

### 같지 않음{#notequal}

다음 `!=` (같지 않음) 함수는 하나의 값 또는 표현식이 **아님** 다른 값 또는 표현식과 같습니다.

**구문**

```sql
{%= expression != value %}
```

**예**

다음 작업에서는 홈 주소 국가가 프랑스가 아닌지 확인합니다.

```sql
{%= profile.homeAddress.country != "France" %}
```

### 보다 큼{#greaterthan}

다음 `>` (큼) 함수는 첫 번째 값이 두 번째 값보다 큰지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 > expression2 %}
```

**예**

다음 수술은 1970년 이후 출생한 사람들을 엄격하게 정의합니다.

```sql
{%= profile.person.birthYear > 1970 %}
```

### 크거나 같음{#greaterthanorequal}

다음 `>=` (크거나 같음) 함수는 첫 번째 값이 두 번째 값보다 크거나 같은지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 >= expression2 %}
```

**예**

다음 수술은 1970년 이후 출생자를 정의합니다.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 보다 작음{#lessthan}

다음 `<` (작음) 비교 함수는 첫 번째 값이 두 번째 값보다 작은지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 < expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람들을 정의합니다.

```sql
{%= profile.person.birthYear < 2000 %}
```

### 작거나 같음{#lessthanorequal}

다음 `<=` (작거나 같음) 비교 함수는 첫 번째 값이 두 번째 값보다 작거나 같은지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 <= expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람들을 정의합니다.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**숫자가 있는 작업**
