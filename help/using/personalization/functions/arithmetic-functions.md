---
title: 산술 함수 라이브러리
description: 산술 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
TQID: https://experienceleague.adobe.com/vQcfLG40Xhz4-ebm--J875oU4o-6BXC0SvNq24OOyTk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 7%

---

# 산술 함수 {#maths}

산술 함수는 값에 대한 기본 계산을 수행하는 데 사용됩니다.

## 이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에{#add}

`+`(추가) 함수는 두 인수 표현식의 합계를 찾는 데 사용됩니다.

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

`*`(곱하기) 함수는 두 인수 표현식의 곱을 찾는 데 사용됩니다.

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

`-`(빼기) 함수는 두 인수 표현식의 차이를 찾는 데 사용됩니다.

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

`/`(나눗셈) 함수는 두 인수 표현식의 몫을 찾는 데 사용됩니다.

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

`%`(modulo/remainder) 함수는 두 인수 표현식을 나눈 후 나머지를 찾는 데 사용됩니다.

**구문**

```sql
{%= double % double %}
```

**예**

다음 수술은 개인의 나이를 5로 나눌 수 있는지 확인합니다.

```sql
{%= person.age % 5 = 0 %}
```
