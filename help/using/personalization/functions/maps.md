---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

---

# 맵 함수 {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)은 맵과의 상호 작용을 용이하게 하는 기능을 제공합니다.

## 가져오기

`get` 함수는 지정된 키에 대한 맵 값을 검색하는 데 사용됩니다.

**형식**

```sql
get({MAP},{STRING})
```

**예**

다음 PQL 쿼리는 `example@example.com` 키의 ID 맵 값을 가져옵니다.

```sql
get(identityMap,"example@example.com")
```

## 키

`keys` 함수는 지정된 맵에 대한 모든 키를 검색하는 데 사용됩니다.

**형식**

```sql
keys({MAP})
```

**예**

다음 PQL 쿼리는 `identityMap` 맵에 대한 모든 키를 가져옵니다.

```sql
keys(identityMap)
```

## 값

`values` 함수는 지정된 맵의 모든 값을 검색하는 데 사용됩니다.

**형식**

```sql
values({MAP})
```

**예**

다음 PQL 쿼리는 `identityMap` 맵에 대한 모든 값을 가져옵니다.

```sql
values(identityMap)
```
