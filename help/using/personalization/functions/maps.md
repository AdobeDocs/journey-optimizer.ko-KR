---
title: 함수 라이브러리 매핑
description: 함수 라이브러리 매핑
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# 맵 함수{#maps}

개인화에서 맵 함수를 사용하여 맵과의 상호 작용을 더 쉽게 할 수 있습니다.

## 가져오기{#get}

다음 `get` 함수는 지정된 키에 대한 맵 값을 검색하는 데 사용됩니다.

**형식**

```sql
{%= get(map, string) %}
```

**예**

다음 작업은 키에 대한 ID 맵의 값을 가져옵니다 `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 키{#keys}

다음 `keys` 함수는 지정된 맵에 대한 모든 키를 검색하는 데 사용됩니다.

**형식**

```sql
{%= keys(map) %}
```

**예**

다음 작업은 맵의 모든 키를 가져옵니다 `identityMap`.

```sql
{%= keys(identityMap) %}
```

## 값{#values}

다음 `values` 함수는 지정된 맵의 모든 값을 검색하는 데 사용됩니다.

**형식**

```sql
{%= values(map) %}
```

**예**

다음 작업은 맵의 모든 값을 가져옵니다 `identityMap`.

```sql
{%= values(identityMap) %}
```
