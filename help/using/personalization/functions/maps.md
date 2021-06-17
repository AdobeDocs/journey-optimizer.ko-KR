---
title: 함수 라이브러리 매핑
description: 함수 라이브러리 매핑
feature: 개인화
topic: 개인화
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 8%

---

# 맵 함수{#maps}

개인화에서 맵 함수를 사용하여 맵과의 상호 작용을 더 쉽게 할 수 있습니다.

## 가져오기{#get}

`get` 함수는 지정된 키에 대한 맵 값을 검색하는 데 사용됩니다.

**형식**

```sql
{%= get(map, string) %}
```

**예**

다음 작업은 키 `example@example.com`에 대한 ID 맵의 값을 가져옵니다.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 키{#keys}

`keys` 함수는 지정된 맵에 대한 모든 키를 검색하는 데 사용됩니다.

**형식**

```sql
{%= keys(map) %}
```

**예**

다음 작업은 맵 `identityMap`에 대한 모든 키를 가져옵니다.

```sql
{%= keys(identityMap) %}
```

## 값{#values}

`values` 함수는 지정된 맵의 모든 값을 검색하는 데 사용됩니다.

**형식**

```sql
{%= values(map) %}
```

**예**

다음 작업은 맵 `identityMap`에 대한 모든 값을 가져옵니다.

```sql
{%= values(identityMap) %}
```
