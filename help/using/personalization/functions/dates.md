---
title: 날짜 시간 함수 라이브러리
description: 날짜 시간 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# 날짜 시간 함수{#date-time}

날짜 및 시간 함수는 Journey Optimizer 내의 값에 대한 날짜 및 시간 작업을 수행하는 데 사용됩니다.

## 연령{#age}

다음 `age` 함수는 지정된 날짜에서 페이지를 검색하는 데 사용됩니다.

**형식**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## 현재 시간(밀리초){#current-time}

다음 `currentTimeInMillis` 함수는 epoch 밀리초 단위의 현재 시간을 검색하는 데 사용됩니다.

**형식**

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

다음 `dateDiff` 함수는 일 수로 두 날짜 간의 차이를 검색하는 데 사용됩니다.

**형식**

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

다음 `dayOfWeek` 함수는 요일을 검색하는 데 사용됩니다.

**형식**

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

## 일(한 해 기준){#day-year}

다음 `dayOfYear` 함수는 날짜를 검색하는 데 사용됩니다.

**형식**

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

## 날짜 형식 지정{#format-date}

다음 `formatDate` 함수는 날짜 시간 값의 형식을 지정하는 데 사용됩니다. 형식은 유효한 Java DateTimeFormat 패턴이어야 합니다.

**형식**

```sql
{%= formatDate(date, format) %}
```

여기서 첫 번째 문자열은 날짜 속성이고 두 번째 값은 날짜를 변환하여 표시하는 방법입니다.

>[!NOTE]
>
> 날짜 패턴이 올바르지 않으면 날짜가 ISO 표준 형식으로 대체됩니다.
>
> 요약된 대로 Java 날짜 형식 기능을 사용할 수 있습니다 [oracle 설명서에서](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**예**

다음 작업은 날짜를 다음 형식으로 반환합니다. MM/DD/YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 설정 일{#set-days}

다음 `setDays` 함수는 지정된 날짜 시간에 대한 월의 일을 설정하는 데 사용됩니다.

**형식**

```sql
{%= setDays(date, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 시간 설정{#set-hours}

다음 `setHours` 함수는 날짜-시간의 시간을 설정하는 데 사용됩니다.

**형식**

```sql
{%= setHours(date, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## UTC로{#to-utc}

다음 `toUTC` 함수에서 datetime을 UTC로 변환하는 데 사용됩니다.


**형식**

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


## Week of Year UTC{#week-of-year}

다음 `weekOfYear` 함수는 요일을 검색하는 데 사용됩니다.

**형식**

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
