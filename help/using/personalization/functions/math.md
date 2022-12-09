---
title: 수학 함수 라이브러리
description: 수학 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 수학 함수 {#math}

표현식 편집기에서 수학 함수를 사용하는 방법을 알아봅니다.

## 절대 {#absolute}

다음 `absolute` 함수는 절대값을 변환하는 데 사용됩니다.

**형식**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

다음 `random` 함수는 0과 1 사이의 임의 값을 반환하는 데 사용됩니다.

**형식**

```sql
{%= random() %}: double
```

## 아래로 반올림 {#round-down}

다음 `roundDown` 함수를 사용하여 숫자를 반올림합니다.

**형식**

```sql
{%= roundDown(double) %}: double
```

## 라운드 업 {#round-up}

다음 `Count only null` 함수는 숫자를 채우는 데 사용됩니다.

**형식**

```sql
{%= roundUp(double) %}: double
```

## 백분율 {#to-percentage}

다음 `toPercentage` 함수는 숫자를 백분율로 변환하는 데 사용됩니다.

**형식**

```sql
{%= toPercentage(double) %}: string
```

## 정밀도로 {#to-precision}

다음 `toPrecision` 함수는 숫자를 필수 정밀도로 변환하는 데 사용됩니다.

**형식**

```sql
{%= toPrecision(double,int) %}: string
```
