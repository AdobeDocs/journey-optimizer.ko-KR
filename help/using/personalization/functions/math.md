---
title: 수학 함수 라이브러리
description: 수학 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# 수학 함수 {#math}

표현식 편집기에서 수학 함수를 사용하는 방법을 알아봅니다.

## 절대 {#absolute}

다음 `absolute` 함수는 절대값을 변환하는 데 사용됩니다.

**구문**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

다음 `formatNumber` 함수는 숫자를 해당 언어에 맞는 표현으로 서식을 지정하는 데 사용됩니다.

숫자 및 로케일을 나타내는 문자열을 승인하고 원하는 로케일에서 숫자 형식의 문자열을 반환합니다.

**구문**

```sql
{%= formatNumber(number/double,string) %}: string
```

요약된 대로 형식 지정 및 유효한 로케일을 사용할 수 있습니다. [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**예**

이 쿼리는 123456.789에 해당하는 아랍어 형식의 문자열을 입력 번호로 반환합니다.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

다음 `random` 함수는 0과 1 사이의 임의 값을 반환하는 데 사용됩니다.

**구문**

```sql
{%= random() %}: double
```

## 아래로 반올림 {#round-down}

다음 `roundDown` 함수를 사용하여 숫자를 반올림합니다.

**구문**

```sql
{%= roundDown(double) %}: double
```

## 라운드 업 {#round-up}

다음 `Count only null` 함수는 숫자를 채우는 데 사용됩니다.

**구문**

```sql
{%= roundUp(double) %}: double
```

## 16진수 문자열 {#to-hex-string}

다음 `toHexString` 함수는 모든 숫자를 16진수 문자열로 변환합니다.

**구문**

```sql
{%= toHexString(number) %}: string
```

**예**

이 쿼리는 158i.e 9e의 16진수 값을 반환합니다.

```sql
{%= toHexString(158) %}
```

## 백분율 {#to-percentage}

다음 `toPercentage` 함수는 숫자를 백분율로 변환하는 데 사용됩니다.

**구문**

```sql
{%= toPercentage(double) %}: string
```

## 정밀도로 {#to-precision}

다음 `toPrecision` 함수는 숫자를 필수 정밀도로 변환하는 데 사용됩니다.

**구문**

```sql
{%= toPrecision(double,int) %}: string
```

## 대상 문자열 {#to-string}

다음 **toString** 함수는 숫자를 해당 문자열 표현으로 변환합니다.

**구문**

```sql
{%= toString(string) %}: string
```

**예**

이 쿼리는 &quot;12&quot;를 반환합니다.

```sql
{%= toString(12) %} 
```
