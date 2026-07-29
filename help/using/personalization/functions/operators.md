---
title: 연산자 함수 라이브러리
description: 연산자 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
TQID: https://experienceleague.adobe.com/b4Tz4auDyWb-iaUYAie31DL5hlHh97n3rYm7EP-JjIw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 461
ht-degree: 9%

---

# 연산자 {#operators}

## 부울 함수 {#boolean-functions}

부울 함수는 다른 요소에 부울 로직을 수행하는 데 사용됩니다.

### And{#and}

`and` 함수는 논리 결합을 만드는 데 사용됩니다.

**구문**

```sql
{%= query1 and query2 %}
```

**예**

다음 작전은 프랑스와 1985년의 출생년도와 같은 본국과 함께 모든 사람들을 돌려보낼 것입니다.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Or{#or}

`or` 함수는 논리 분리를 만드는 데 사용됩니다.

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

`=`(equals) 함수는 하나의 값 또는 식이 다른 값 또는 식과 같은지 확인합니다.

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

`!=`(같지 않음) 함수는 하나의 값 또는 식이 다른 값 또는 식과 **같지 않음**&#x200B;인지 확인합니다.

**구문**

```sql
{%= expression != value %}
```

**예**

다음 작업에서는 홈 주소 국가가 프랑스가 아닌지 확인합니다.

```sql
{%= profile.homeAddress.country != "France" %}
```

### 다음보다 큼{#greaterthan}

`>`(큼) 함수는 첫 번째 값이 두 번째 값보다 큰지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 > expression2 %}
```

**예**

다음 수술은 1970년 이후 출생한 사람들을 엄격하게 정의합니다.

```sql
{%= profile.person.birthYear > 1970 %}
```

### 다음보다 크거나 같음{#greaterthanorequal}

`>=`(크거나 같음) 함수는 첫 번째 값이 두 번째 값보다 크거나 같은지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 >= expression2 %}
```

**예**

다음 수술은 1970년 이후 출생자를 정의합니다.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 다음보다 작음{#lessthan}

`<`(작음) 비교 함수는 첫 번째 값이 두 번째 값보다 작은지 확인하는 데 사용합니다.

**구문**

```sql
{%= expression1 < expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람들을 정의합니다.

```sql
{%= profile.person.birthYear < 2000 %}
```

### 다음보다 작거나 같음{#lessthanorequal}

`<=`(작거나 같음) 비교 함수는 첫 번째 값이 두 번째 값보다 작거나 같은지 확인하는 데 사용합니다.

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

## 템플릿 마이그레이션 기능 {#template-migration-functions}

템플릿 마이그레이션 기능은 개인화 편집기에서 사용할 수 있으며 기존 템플릿을 Journey Optimizer으로 마이그레이션하는 데 도움이 됩니다.

### 연산자를 통한 비교{#amp-compare}

`ampCompare` 함수는 지정된 비교 연산자를 사용하여 두 값을 비교합니다.

**구문**

```sql
{%= ampCompare(value1, value2, operator) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `value1` | 비교할 첫 번째 값. |
| `value2` | 비교할 두 번째 값입니다. |
| `operator` | 사용할 비교 연산자를 나타내는 정수입니다. |

**예**

```sql
{%= ampCompare(profile.person.age, 18, 4) %}
```

### 하위 문자열 범위{#amp-substr}

`ampSubstr` 함수는 지정된 시작 및 끝 인덱스 사이의 문자열 부분을 반환합니다.

**구문**

```sql
{%= ampSubstr(string, startIndex, endIndex) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `string` | 소스 문자열입니다. |
| `startIndex` | 하위 문자열의 시작 인덱스(정수). |
| `endIndex` | 하위 문자열의 끝 색인(정수). |

**예**

다음 표현식은 문자열 &quot;Hello World&quot;의 처음 5자를 반환합니다.

```sql
{%= ampSubstr("Hello World", 0, 5) %}
```

`Hello`을(를) 반환합니다

### 비교 대상{#compare-to}

`compareTo` 함수는 사전적으로 두 문자열을 비교합니다. 첫 번째 문자열이 두 번째 앞에 오면 음의 정수를 반환하고, 같으면 0을 반환하고, 첫 번째 문자열이 두 번째 뒤에 오면 양의 정수를 반환합니다.

**구문**

```sql
{%= compareTo(string1, string2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `string1` | 비교할 첫 번째 문자열입니다. |
| `string2` | 비교할 두 번째 문자열입니다. |

**예**

```sql
{%= compareTo("apple", "banana") %}
```
