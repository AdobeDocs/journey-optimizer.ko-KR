---
title: 집계 함수 라이브러리
description: 집계 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# 집계 함수 {#aggregation}

집계 함수는 여러 값을 함께 그룹화하여 단일 요약 값을 구성하는 데 사용됩니다.

## 평균{#average}

`average` 함수는 배열에서 선택한 모든 값의 산술 평균을 반환합니다.

**구문**

```sql
{%= average(array) %}
```

**예**

다음 작업은 모든 주문의 평균 가격을 반환합니다.

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

`count` 함수는 특정 배열의 요소 수를 반환합니다.

**구문**

```sql
{%= count(array) %}
```

**예**

다음 작업은 배열에 있는 주문 수를 반환합니다.

```sql
{%= count(orders) %}
```

## 최대{#max}

`max` 함수는 배열에서 선택한 모든 값 중 가장 큰 값을 반환합니다.

**구문**

```sql
{%= max(array) %}
```

**예**

다음 작업은 모든 주문의 가장 높은 가격을 반환합니다.

```sql
{%=max(orders.order.price)%}
```

## 최소{#min}

`min` 함수는 배열에서 선택한 모든 값 중 가장 작은 값을 반환합니다.

**구문**

```sql
{%= min(array) %}
```

**예**

다음 작업은 모든 주문의 최저 가격을 반환합니다.

```sql
{%=min(orders.order.price) %}
```

## Sum{#sum}

`sum` 함수는 배열에서 선택한 모든 값의 합계를 반환합니다.

**구문**

```sql
{%= sum(array) %}
```

**예**

다음 작업은 모든 주문 가격의 합계를 반환합니다.

```sql
{%=sum(orders.order.price)%}
```
