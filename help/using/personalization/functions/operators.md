---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# 연산자 {#operators}

![](../../assets/do-not-localize/badge.png)

## 그리고

`and` 함수는 논리 연결을 만드는 데 사용됩니다.

**형식**

```sql
{QUERY} and {QUERY}
```

**예**

다음 PQL 쿼리는 1985년 캐나다와 출생년으로 본국에 있는 모든 사람을 반환합니다.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## 또는

`or` 함수는 논리적 분리를 만드는 데 사용됩니다.

**형식**

```sql
{QUERY} or {QUERY}
```

**예**

다음 PQL 쿼리는 1985년 캐나다나 출생년으로 본국에 있는 모든 사람을 반환합니다.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## 아님

`not`(또는 `!`) 함수를 사용하여 논리적 부정을 만듭니다.

**형식**

```sql
not ({QUERY})
!({QUERY})
```

**예**

다음 PQL 쿼리는 본국이 없는 모든 사람을 캐나다로 반환합니다.

```sql
not (homeAddress.countryISO = "CA")
```

## If

`if` 함수는 지정된 조건이 true인지 여부에 따라 표현식을 해결하는 데 사용됩니다.

**형식**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | 테스트할 부울 표현식입니다. |
| `{TRUE_EXPRESSION}` | `{TEST_EXPRESSION}`이(가) true인 경우 값이 사용될 표현식입니다. |
| `{FALSE_EXPRESSION}` | `{TEST_EXPRESSION}`이(가) false인 경우 값을 사용할 표현식입니다. |

**예**

다음 PQL 쿼리는 홈 국가가 캐나다인 경우 `1` 값을 설정하고, 홈 국가가 캐나다가 아닌 경우에는 `2` 값을 설정합니다.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## 다음과 같음

`=`(같음) 함수는 한 값 또는 표현식이 다른 값 또는 표현식과 같은지 여부를 확인합니다.

**형식**

```sql
{EXPRESSION} = {VALUE}
```

**예**

다음 PQL 쿼리는 홈 주소 국가가 캐나다인지 확인합니다.

```sql
homeAddress.countryISO = "CA"
```

## 같지 않음

`!=`(같지 않음) 함수는 한 값 또는 표현식이 다른 값 또는 표현식과 동일한지 **not**&#x200B;인지 확인합니다.

**형식**

```sql
{EXPRESSION} != {VALUE}
```

**예**

다음 PQL 쿼리는 홈 주소 국가가 캐나다에 있지 않은지 확인합니다.

```sql
homeAddress.countryISO != "CA"
```

## 보다 큼

`>`(보다 큼) 함수는 첫 번째 값이 두 번째 값보다 큰지 확인하는 데 사용됩니다.

**형식**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**예**

다음 PQL 쿼리는 1월 또는 2월에 생일을 맞지 않는 사람을 정의합니다.

```sql
person.birthMonth > 2
```

## 크거나 같음

`>=`(보다 크거나 같음) 함수는 첫 번째 값이 두 번째 값보다 크거나 같은지 확인하는 데 사용됩니다.

**형식**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**예**

다음 PQL 쿼리는 1월 또는 2월에 생일을 맞지 않는 사람을 정의합니다.

```sql
person.birthMonth >= 3
```

## 보다 작음

`<`(보다 작음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작은지 확인합니다.

**형식**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**예**

다음 PQL 쿼리는 1월에 생일을 사용하는 사람을 정의합니다.

```sql
person.birthMonth < 2
```

## 작거나 같음

`<=`(작거나 같음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작거나 같은지 확인합니다.

**형식**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**예**

다음 PQL 쿼리는 1월 또는 2월에 생일을 사용하는 사람을 정의합니다.

```sql
person.birthMonth <= 2
```

## 이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에

`+`(추가) 함수는 두 인수 표현식의 합계를 찾는 데 사용됩니다.

**형식**

```sql
{NUMBER} + {NUMBER}
```

**예**

다음 PQL 쿼리는 서로 다른 두 제품의 가격을 합합니다.

```sql
product1.price + product2.price
```

## 곱하기

`*`(곱하기) 함수는 두 인수 표현식의 제품을 찾는 데 사용됩니다.

**형식**

```sql
{NUMBER} * {NUMBER}
```

**예**

다음 PQL 쿼리는 재고 제품 및 제품 가격을 검색하여 제품의 총값을 찾습니다.

```sql
product.inventory * product.price
```

## 빼기

`-`(빼기) 함수는 두 인수 표현식의 차이를 찾는 데 사용됩니다.

**형식**

```sql
{NUMBER} - {NUMBER}
```

**예**

다음 PQL 쿼리는 서로 다른 두 제품 간의 가격 차이를 찾습니다.

```sql
product1.price - product2.price
```

## 나누기

`/`(나누기) 함수는 두 인수 표현식의 인용 부분을 찾는 데 사용됩니다.

**형식**

```sql
{NUMBER} / {NUMBER}
```

**예**

다음 PQL 쿼리는 총 판매 제품과 총 수입 간 견적 정보를 검색하여 품목당 평균 비용을 확인합니다.

```sql
totalProduct.price / totalProduct.sold
```

## 나머지 항목

`%`(모듈형/나머진) 함수는 두 인수 표현식을 나눈 후 나머지를 찾는 데 사용됩니다.

**형식**

```sql
{NUMBER} % {NUMBER}
```

**예**

다음 PQL 쿼리는 개인의 연령이 5로 구분되었는지 확인합니다.

```sql
person.age % 5 = 0
```
