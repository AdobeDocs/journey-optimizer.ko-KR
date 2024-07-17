---
title: 수학 함수 라이브러리
description: 수학 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 11%

---

# 수학 함수 {#math}

개인화 편집기에서 수학 함수를 사용하는 방법에 대해 알아봅니다.

## 절대 {#absolute}

`absolute` 함수는 숫자의 절대값을 변환하는 데 사용합니다.

**구문**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

`formatNumber` 함수는 숫자를 언어 구분 표현으로 서식을 지정하는 데 사용합니다.

숫자와 로케일을 나타내는 문자열을 수락하고 원하는 로케일에서 숫자의 서식 있는 문자열을 반환합니다.

**구문**

```sql
{%= formatNumber(number/double,string) %}: string
```

[Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}에 요약된 대로 서식 및 올바른 로케일을 사용할 수 있습니다.

**예**

이 쿼리는 입력 숫자로 123456.789에 해당하는 아랍어 형식의 문자열을 반환합니다.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## 무작위 {#random}

`random` 함수는 0과 1 사이의 임의의 값을 반환하는 데 사용됩니다.

**구문**

```sql
{%= random() %}: double
```

## 내림 {#round-down}

`roundDown` 함수는 숫자를 내림하는 데 사용됩니다.

**구문**

```sql
{%= roundDown(double) %}: double
```

## 올림 {#round-up}

`Count only null` 함수는 숫자를 반올림하는 데 사용됩니다.

**구문**

```sql
{%= roundUp(double) %}: double
```

## 16진수 문자열로 변환 {#to-hex-string}

`toHexString` 함수는 임의의 숫자를 16진수 문자열로 변환합니다.

**구문**

```sql
{%= toHexString(number) %}: string
```

**예**

이 쿼리는 158의 16진수 값, 즉 9e를 반환합니다.

```sql
{%= toHexString(158) %}
```

## 정수로 {#to-int}

`toInt` 함수는 이러한 형식(숫자, double, int, long, float, short, 바이트, 부울, 문자열)을 정수로 변환하는 데 사용합니다.

**구문**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**예**

이 쿼리는 42,6의 정수 값, 즉 42를 반환합니다.

```sql
{%= toInt(42.6) %}: integer
```

## 백분율로 변환 {#to-percentage}

`toPercentage` 함수는 숫자를 백분율로 변환하는 데 사용합니다.

**구문**

```sql
{%= toPercentage(double) %}: string
```

## 전체 자릿수로 변환 {#to-precision}

`toPrecision` 함수는 숫자를 필요한 전체 자릿수로 변환하는 데 사용합니다.

**구문**

```sql
{%= toPrecision(double,int) %}: string
```

## 대상 문자열 {#to-string}

**toString** 함수는 모든 숫자를 문자열 표시로 변환합니다.

**구문**

```sql
{%= toString(string) %}: string
```

**예**

이 쿼리는 &quot;12&quot;를 반환합니다.

```sql
{%= toString(12) %} 
```
