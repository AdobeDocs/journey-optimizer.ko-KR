---
title: 맵 함수 라이브러리
description: 맵 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# 맵 함수{#maps}

개인화에 맵 함수를 사용하여 맵과의 상호 작용을 보다 쉽게 만듭니다.

## 다운로드{#get}

`get` 함수는 특정 키에 대한 맵의 값을 검색하는 데 사용됩니다.

**구문**

```sql
{%= get(map, string) %}
```

**예**

다음 작업은 키 `example@example.com`에 대한 ID 맵 값을 가져옵니다.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 키{#keys}

`keys` 함수는 특정 맵의 모든 키를 검색하는 데 사용됩니다.

**구문**

```sql
{%= keys(map) %}
```

**예**

다음 작업은 맵 `identityMap`의 모든 키를 가져옵니다.

```sql
{%= keys(identityMap) %}
```

## 값{#values}

`values` 함수는 지정된 맵의 모든 값을 검색하는 데 사용됩니다.

**구문**

```sql
{%= values(map) %}
```

**예**

다음 작업은 맵 `identityMap`의 모든 값을 가져옵니다.

```sql
{%= values(identityMap) %}
```
