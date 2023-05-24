---
title: 산술 함수 라이브러리
description: 산술 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 산술 함수 {#maths}

산술 함수는 값에 대한 기본 계산을 수행하는 데 사용됩니다.

## 이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에{#add}

다음 `+` (추가) 함수는 두 인수 표현식의 합계를 찾는 데 사용합니다.

**구문**

```sql
{%= double + double %}
```

**예**

다음 연산은 서로 다른 두 제품의 가격을 합산합니다.

```sql
{%= product1.price + product2.price %}
```

## 곱하기{#multiply}

다음 `*` (곱하기) 함수는 두 인수 표현식의 곱을 찾는 데 사용된다.

**구문**

```sql
{%= double * double %}
```

**예**

다음 작업은 재고의 제품과 제품의 가격을 찾아 제품의 총액을 구합니다.

```sql
{%= product.inventory * product.price %}
```

## 빼기{#substract}

다음 `-` (빼기) 함수는 두 인수 표현식의 차이를 구하는 데 사용합니다.

**구문**

```sql
{%= double - double %}
```

**예**

다음 작업은 두 가지 다른 제품 간의 가격 차이를 확인합니다.

```sql
{%= product1.price - product2.price %}
```

## 나누기{#divide}

다음 `/` (나눗셈) 함수는 두 인수 표현식의 몫을 구하는 데 사용된다.

**구문**

```sql
{%= double / double %}
```

**예**

다음 작업은 품목당 평균 비용을 보기 위해 판매된 총 제품과 벌어들인 총 금액 사이의 몫을 구합니다.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 나머지{#remainder}

다음 `%` (modulo/remainder) 함수는 두 인수 표현식을 나눈 후 나머지를 구하는 데 사용된다.

**구문**

```sql
{%= double % double %}
```

**예**

다음 수술은 개인의 나이를 5로 나눌 수 있는지 확인합니다.

```sql
{%= person.age % 5 = 0 %}
```
