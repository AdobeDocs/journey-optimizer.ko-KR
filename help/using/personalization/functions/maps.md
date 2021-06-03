---
title: 함수 라이브러리
description: 함수 라이브러리
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# 맵 함수{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) 은 맵과 보다 쉽게 상호 작용할 수 있는 기능을 제공합니다.

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
