---
title: 날짜 시간 함수 라이브러리
description: 날짜 시간 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 7%

---

# 날짜 시간 함수{#date-time}

날짜 및 시간 함수는 Journey Optimizer 내의 값에 대해 날짜 및 시간 작업을 수행하는 데 사용됩니다.

## 처리 시간{#age}

`age` 함수는 특정 날짜에서 기간을 검색하는 데 사용됩니다.

**구문**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## 현재 시간(밀리초){#current-time}

`currentTimeInMillis` 함수는 에포크 밀리초로 현재 시간을 검색하는 데 사용됩니다.

**구문**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## 날짜 차이{#date-diff}

`dateDiff` 함수는 일 수로 두 날짜 간의 차이를 검색하는 데 사용됩니다.

**구문**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## 요일{#day-week}

`dayOfWeek` 함수는 요일을 검색하는 데 사용됩니다.

**구문**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 연간 일자{#day-year}

`dayOfYear` 함수는 연간 일자를 검색하는 데 사용됩니다.

**구문**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 날짜 포맷{#format-date}

`formatDate` 함수는 날짜/시간 값의 형식을 지정하는 데 사용됩니다. 형식은 유효한 Java DateTimeFormat 패턴이어야 합니다.

**구문**

```sql
{%= formatDate(datetime, format) %}
```

여기서 첫 번째 문자열은 날짜 속성이고 두 번째 값은 날짜를 변환하여 표시하는 방식입니다.

>[!NOTE]
>
> 날짜 패턴이 올바르지 않으면 날짜는 ISO 표준 형식으로 대체됩니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}에 요약된 대로 Java 날짜 서식 함수를 사용할 수 있습니다.

**예**

다음 작업은 MM/DD/YY 형식으로 날짜를 반환합니다.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## 로케일 지원을 사용하여 날짜 형식 지정{#format-date-locale}

`formatDate` 함수는 날짜 시간 값의 형식을 해당 언어 구분 표시(즉, 원하는 로케일)로 지정하는 데 사용합니다. 형식은 유효한 Java DateTimeFormat 패턴이어야 합니다.

**구문**

```sql
{%= formatDate(datetime, format, locale) %}
```

여기서 첫 번째 문자열은 date 속성이고 두 번째 값은 날짜를 변환하여 표시하는 방식이며 세 번째 값은 로케일을 문자열 형식으로 나타냅니다.

>[!NOTE]
>
> 날짜 패턴이 올바르지 않으면 날짜는 ISO 표준 형식으로 대체됩니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)에 요약된 대로 Java 날짜 서식 함수를 사용할 수 있습니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)에 요약된 대로 서식 및 올바른 로케일을 사용할 수 있습니다.


**예**

다음 작업은 MM/DD/YY 및 로케일 프랑스 형식으로 날짜를 반환합니다.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 일 설정{#set-days}

`setDays` 함수는 특정 날짜-시간에 대한 날짜의 날짜를 설정하는 데 사용됩니다.

**구문**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 시간 설정{#set-hours}

`setHours` 함수는 날짜-시간의 시간을 설정하는 데 사용됩니다.

**구문**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## UTC로 변환{#to-utc}

`toUTC` 함수는 날짜/시간을 UTC로 변환하는 데 사용됩니다.


**구문**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## 주(UTC){#week-of-year}

`weekOfYear` 함수는 연간 주를 검색하는 데 사용됩니다.

**구문**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->