---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 개체 함수 {#objects}

![](../../assets/do-not-localize/badge.png)

## null임

`isNull` 함수는 개체 참조가 있는지 확인합니다.

**형식**

```sql
isNull({OBJECT})
```

**예**

다음 PQL 쿼리는 개인의 홈 주소가 존재하지 않는지 확인합니다.

```sql
isNull(person.homeAddress)
```

## null이 아님

`isNotNull` 함수는 개체 참조가 있는지 확인합니다.

**형식**

```sql
isNotNull({OBJECT})
```

**예**

다음 PQL 쿼리는 개인의 홈 주소가 있는지 확인합니다.

```sql
isNotNull(person.homeAddress)
```
