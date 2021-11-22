---
title: 집계 함수 라이브러리
description: 집계 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 8%

---

# 집계 함수 {#aggregation}

집계 함수는 여러 값을 함께 그룹화하여 단일 요약 값을 구성하는 데 사용됩니다.

## 카운트{#count}

다음 `count` 함수는 지정된 배열 내의 요소 수를 반환합니다.

**포맷**

```sql
{%= count(array) %}
```

**예**

다음 작업은 배열의 주문 수를 반환합니다.

```sql
{%= count(orders) %}
```

## 합계{#sum}

다음 `sum` 함수는 배열 내에서 선택한 모든 값의 합계를 반환합니다.

**포맷**

```sql
{%= sum(array) %}
```

**예**

다음 작업은 모든 주문 가격의 합계를 반환합니다.

```sql
{%=sum(orders.order.price)%}
```

## 평균{#average}

다음 `average` 함수는 배열 내에서 선택한 모든 값의 산술 평균을 반환합니다.

**포맷**

```sql
{%= average(array) %}
```

**예**

다음 작업은 모든 주문의 평균 가격을 반환합니다.

```sql
{%=average(orders.order.price)%}
```

## 최소값{#min}

다음 `min` 함수는 배열 내에서 선택한 모든 값 중 가장 작은 값을 반환합니다.

**포맷**

```sql
{%= min(array) %}
```

**예**

다음 작업은 모든 주문의 가장 낮은 가격을 반환합니다.

```sql
{%=min(orders.order.price)%}
```

## 최대값{#max}

다음 `max` 함수는 배열 내에서 선택한 모든 값 중 가장 큰 값을 반환합니다.

**포맷**

```sql
{%= max(array) %}
```

**예**

다음 작업은 모든 주문의 가장 높은 가격을 반환합니다.

```sql
{%=max(orders.order.price)%}
```
