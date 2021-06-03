---
title: 함수 라이브러리
description: 함수 라이브러리
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# 개체 함수 {#objects}

![](../../assets/do-not-localize/badge.png)

## null임{#isNull}

`isNull` 함수는 개체 참조가 없는지 확인합니다.

**형식**

```sql
{%= isNull(object) %}
```

**예**

다음 작업은 개인의 집 주소가 존재하지 않는지 확인합니다.

```sql
{%= isNull(person.homeAddress) %}
```

## null이 아님{#isNotNull}

`isNotNull` 함수는 개체 참조가 있는지 여부를 결정합니다.

**형식**

```sql
{%= isNotNull(object) %}
```

**예**

다음 작업은 개인의 집 주소가 있는지 확인합니다.

```sql
{%= isNotNull(person.homeAddress) %}
```
