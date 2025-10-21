---
title: 오브젝트 함수 라이브러리
description: 오브젝트 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 개체 함수 {#objects}

## null임{#isNull}

`isNull` 함수는 개체 참조가 없는지 확인합니다.

**구문**

```sql
{%= isNull(object) %}
```

**예**

다음 작업은 해당 사용자의 홈 주소가 존재하지 않는지 확인합니다.

```sql
{%= isNull(person.homeAddress) %}
```

## null이 아님{#isNotNull}

`isNotNull` 함수는 개체 참조가 있는지 확인합니다.

**구문**

```sql
{%= isNotNull(object) %}
```

**예**

다음 작업은 해당 사용자의 집 주소가 있는지 확인합니다.

```sql
{%= isNotNull(person.homeAddress) %}
```
