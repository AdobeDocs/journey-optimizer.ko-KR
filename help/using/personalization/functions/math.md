---
title: 수학 함수 라이브러리
description: 수학 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# 수학 함수 {#math}

표현식 편집기에서 수학 함수를 사용하는 방법에 대해 알아봅니다.

## 절대 {#absolute}

다음 `absolute` 함수는 숫자를 숫자의 절대값으로 변환하는 데 사용됩니다.

**구문**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

다음 `formatNumber` 함수는 숫자를 언어에 민감한 표현으로 서식을 지정하는 데 사용됩니다.

숫자와 로케일을 나타내는 문자열을 수락하고 원하는 로케일에서 숫자의 서식 있는 문자열을 반환합니다.

**구문**

```sql
{%= formatNumber(number/double,string) %}: string
```

에 요약된 대로 형식 지정 및 유효한 로케일을 사용할 수 있습니다. [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**예**

이 쿼리는 입력 숫자로 123456.789에 해당하는 아랍어 형식의 문자열을 반환합니다.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

다음 `random` 함수는 0과 1 사이의 임의의 값을 반환하는 데 사용됩니다.

**구문**

```sql
{%= random() %}: double
```

## 내림 {#round-down}

다음 `roundDown` 함수는 숫자를 내림하는 데 사용됩니다.

**구문**

```sql
{%= roundDown(double) %}: double
```

## 올림 {#round-up}

다음 `Count only null` 함수는 숫자를 올림하는 데 사용됩니다.

**구문**

```sql
{%= roundUp(double) %}: double
```

## 16진수 문자열로 변환 {#to-hex-string}

다음 `toHexString` 함수는 임의의 숫자를 16진수 문자열로 변환합니다.

**구문**

```sql
{%= toHexString(number) %}: string
```

**예**

이 쿼리는 158의 16진수 값, 즉 9e를 반환합니다.

```sql
{%= toHexString(158) %}
```

## 백분율로 변환 {#to-percentage}

다음 `toPercentage` 함수는 숫자를 백분율로 변환하는 데 사용합니다.

**구문**

```sql
{%= toPercentage(double) %}: string
```

## 전체 자릿수로 {#to-precision}

다음 `toPrecision` 함수는 숫자를 필요한 전체 자릿수로 변환하는 데 사용합니다.

**구문**

```sql
{%= toPrecision(double,int) %}: string
```

## 대상 문자열 {#to-string}

다음 **toString** 함수는 임의의 숫자를 문자열 표현으로 변환합니다.

**구문**

```sql
{%= toString(string) %}: string
```

**예**

이 쿼리는 &quot;12&quot;를 반환합니다.

```sql
{%= toString(12) %} 
```
