---
title: 집계 함수 라이브러리
description: 집계 함수 라이브러리
feature: 개인화
topic: 개인화
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 9%

---

# 집계 함수 {#aggregation}

![](../../assets/do-not-localize/badge.png)

집계 함수는 여러 값을 함께 그룹화하여 단일 요약 값을 구성하는 데 사용됩니다.

## 카운트{#count}

`count` 함수는 지정된 배열 내의 요소 수를 반환합니다.

**형식**

```sql
{%= count(array) %}
```

**예**

다음 작업은 배열의 주문 수를 반환합니다.

```sql
{%= count(orders) %}
```

## 합계{#sum}

`sum` 함수는 배열 내에서 선택한 모든 값의 합계를 반환합니다.

**형식**

```sql
{%= sum(array) %}
```

**예**

다음 작업은 모든 주문 가격의 합계를 반환합니다.

```sql
{%=sum(orders.order.price)%}
```

## 평균{#average}

`average` 함수는 배열 내에서 선택한 모든 값의 산술 평균을 반환합니다.

**형식**

```sql
{%= average(array) %}
```

**예**

다음 작업은 모든 주문의 평균 가격을 반환합니다.

```sql
{%=average(orders.order.price)%}
```

## 최소값{#min}

`min` 함수는 배열 내에서 선택한 모든 값 중 가장 작은 값을 반환합니다.

**형식**

```sql
{%= min(array) %}
```

**예**

다음 작업은 모든 주문의 가장 낮은 가격을 반환합니다.

```sql
{%=min(orders.order.price)%}
```

## 최대값{#max}

`max` 함수는 배열 내에서 선택한 모든 값 중 가장 큰 값을 반환합니다.

**형식**

```sql
{%= max(array) %}
```

**예**

다음 작업은 모든 주문의 가장 높은 가격을 반환합니다.

```sql
{%=max(orders.order.price)%}
```
