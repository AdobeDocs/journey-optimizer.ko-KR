---
title: 오브젝트 함수 라이브러리
description: 오브젝트 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
TQID: https://experienceleague.adobe.com/EdvzBXdtv1Mm4yIZ8ehu4tx6uQBxnpcXTMVQIc1oQkI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 57
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
