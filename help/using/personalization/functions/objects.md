---
title: 객체 함수 라이브러리
description: 객체 함수 라이브러리
feature: 개인화
topic: 개인화
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

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
