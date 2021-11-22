---
title: 산술 함수 라이브러리
description: 산술 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 산술 함수 {#maths}

산술 함수는 값에 대한 기본 계산을 수행하는 데 사용됩니다.

## 이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에{#add}

다음 `+` (추가) 함수는 두 인수 표현식의 합계를 찾는 데 사용됩니다.

**포맷**

```sql
{%= double + double %}
```

**예**

다음 작업은 두 제품의 가격을 합합니다.

```sql
{%= product1.price + product2.price %}
```

## 곱하기{#multiply}

다음 `*` (곱하기) 함수는 두 인수 표현식의 제품을 찾는 데 사용됩니다.

**포맷**

```sql
{%= double * double %}
```

**예**

다음 공정은 제품의 총 가치를 찾기 위해 재고의 제품 및 제품의 가격을 찾습니다.

```sql
{%= product.inventory * product.price %}
```

## 빼기{#substract}

다음 `-` (빼기) 함수는 두 인수 표현식의 차이를 찾는 데 사용됩니다.

**포맷**

```sql
{%= double - double %}
```

**예**

다음 작업은 서로 다른 두 제품 간의 가격 차이를 찾습니다.

```sql
{%= product1.price - product2.price %}
```

## 나누기{#divide}

다음 `/` (division) 함수는 두 인수 표현식의 따옴표를 찾는 데 사용됩니다.

**포맷**

```sql
{%= double / double %}
```

**예**

다음 공정에서는 총 판매된 제품과 총 획득된 금액 사이의 수량을 찾아 항목당 평균 원가를 확인합니다.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 나머지{#remainder}

다음 `%` (modulo/additional) 함수는 두 인수 표현식을 나눈 후 나머지를 찾는 데 사용됩니다.

**포맷**

```sql
{%= double % double %}
```

**예**

다음 작업은 개인의 연령이 5세로 나눌 수 있는지 여부를 확인합니다.

```sql
{%= person.age % 5 = 0 %}
```
