---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# 수학 함수 {#math}

![](../../assets/do-not-localize/badge.png)

산술 함수는 [!DNL Profile Query Language](PQL)의 값에 대한 기본 계산을 수행하는 데 사용됩니다.

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
