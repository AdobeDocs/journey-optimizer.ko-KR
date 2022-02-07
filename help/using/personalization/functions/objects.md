---
title: 객체 함수 라이브러리
description: 객체 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 개체 함수 {#objects}

## null임{#isNull}

다음 `isNull` 함수는 개체 참조가 존재하지 않는지 확인합니다.

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

다음 `isNotNull` 함수는 개체 참조가 있는지 여부를 결정합니다.

**형식**

```sql
{%= isNotNull(object) %}
```

**예**

다음 작업은 개인의 집 주소가 있는지 확인합니다.

```sql
{%= isNotNull(person.homeAddress) %}
```
