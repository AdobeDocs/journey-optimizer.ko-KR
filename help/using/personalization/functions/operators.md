---
title: 연산자 함수 라이브러리
description: 연산자 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 연산자 {#operators}

## 부울 함수 {#boolean-functions}

부울 함수는 다른 요소에서 부울 논리를 수행하는 데 사용됩니다.

### 및{#and}

다음 `and` 함수를 사용하여 논리 연결을 만듭니다.

**형식**

```sql
{%= query1 and query2 %}
```

**예**

다음 작전은 1985년 프랑스의 출생연도, 본국에 있는 모든 사람들을 돌려줄 것입니다.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 또는{#or}

다음 `or` 함수는 논리 분리를 만드는 데 사용됩니다.

**형식**

```sql
{%= query1 or query2 %}
```

**예**

다음 작전은 1985년의 프랑스 또는 출생년으로 고국을 가진 모든 사람들을 돌려줄 것입니다.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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

비교 함수는 다른 표현식과 값 간을 비교하고 그에 따라 true 또는 false를 반환하는 데 사용됩니다.

### 다음과 같음{#equals}

다음 `=` (equals) 함수는 한 값 또는 표현식이 다른 값 또는 표현식과 같은지 여부를 확인합니다.

**형식**

```sql
{%= expression = value %}
```

**예**

다음 작업은 홈 주소 국가가 프랑스인지 확인합니다.

```sql
{%= profile.homeAddress.country = "France" %}
```

### 같지 않음{#notequal}

다음 `!=` (같지 않음) 함수는 값 또는 표현식이 있는지 여부를 확인합니다 **not** 다른 값 또는 표현식과 같음.

**형식**

```sql
{%= expression != value %}
```

**예**

다음 작업은 홈 주소 국가가 프랑스가 아닌지 확인합니다.

```sql
{%= profile.homeAddress.country != "France" %}
```

### 보다 큼{#greaterthan}

다음 `>` (보다 큼) 함수는 첫 번째 값이 두 번째 값보다 커야 하는지 확인하는 데 사용됩니다.

**형식**

```sql
{%= expression1 > expression2 %}
```

**예**

다음 작업은 1970년 이후에 태어난 사람을 엄격하게 정의합니다.

```sql
{%= profile.person.birthYear > 1970 %}
```

### 크거나 같음{#greaterthanorequal}

다음 `>=` (크거나 같음) 함수는 첫 번째 값이 두 번째 값보다 크거나 같은지 확인하는 데 사용됩니다.

**형식**

```sql
{%= expression1 >= expression2 %}
```

**예**

다음 작업은 1970년 또는 그 이후에 태어난 사람을 정의한다.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 미만{#lessthan}

다음 `<` (보다 작음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작은지 확인합니다.

**형식**

```sql
{%= expression1 < expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람을 정의합니다.

```sql
{%= profile.person.birthYear < 2000 %}
```

### 작거나 같음{#lessthanorequal}

다음 `<=` (작거나 같음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작거나 같은지 확인합니다.

**형식**

```sql
{%= expression1 <= expression2 %}
```

**예**

다음 작업은 2000년 또는 그 이전에 태어난 사람을 정의합니다.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**숫자를 사용하는 작업**
