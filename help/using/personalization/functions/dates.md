---
title: 날짜 시간 함수 라이브러리
description: 날짜 시간 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 11%

---

# 날짜 시간 함수{#date-time}

날짜 및 시간 함수는 Journey Optimizer 내의 값에 대해 날짜 및 시간 작업을 수행하는 데 사용됩니다.

## 일 추가 {#add-days}

`addDays` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 일수만큼 지정된 날짜를 조정합니다.

**구문**

```sql
{%= addDays(date, number) %}
```

+++예

* 입력: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 출력: `2024-11-11T17:19:51Z`

+++

## 시간 추가 {#add-hours}

`addHours` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 시간만큼 지정된 날짜를 조정합니다.

**구문**

```sql
{%= addHours(date, number) %}
```

+++예

* 입력: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* 출력: `2024-11-01T18:19:51Z`

+++

## 분 추가 {#add-minutes}

`addMinutes` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 시간(분)만큼 조정됩니다.

**구문**

```sql
{%= addMinutes(date, number) %}
```

+++예

* 입력: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* 출력: `2024-11-01T18:09:51Z`

+++

## 월 추가 {#add-months}

`addMonths` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 개월 수만큼 지정된 날짜를 조정합니다.

**구문**

```sql
{%= addMonths(date, number) %}
```

+++예

* 입력: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 출력: `2025-01-01T17:19:51Z`

+++

## 초 추가 {#add-seconds}

`addSeconds`은(는) 양수 값을 사용하여 증가 및 음수 값을 사용하여 지정된 시간(초)만큼 날짜를 조정합니다.

**구문**

```sql
{%= addSeconds(date, number) %}
```

+++예

* 입력: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 출력: `2024-11-01T17:20:01Z`

+++

## 년 추가 {#add-years}

`addYears`은(는) 양수 값을 사용하여 증가 값을 하고 음수 값을 사용하여 감소 값을 지정하여 지정된 연도 수만큼 날짜를 조정합니다.

**구문**

```sql
{%= addYears(date, number) %}
```

+++예

* 입력: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 출력: `2026-11-01T17:19:51Z`

+++

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

## 나이 (일 기준) {#age-days}

`ageInDays` 함수는 특정 날짜의 기간(예: 특정 날짜와 현재 날짜 사이에 경과된 일 수)을 계산합니다. 이후 날짜의 경우에는 음수이고 이전 날짜의 경우에는 양수입니다.

**구문**

```sql
{%= ageInDays(date) %}
```

+++예

currentDate = 2025-01-07T12:17:10.720122+05:30(아시아/콜카타)

* 입력: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* 출력: `5`

+++

## 나이 (월 기준) {#age-months}

`ageInMonths` 함수는 특정 날짜의 기간(예: 특정 날짜와 현재 날짜 사이에 경과된 개월 수)을 개월 단위로 계산합니다. 미래 날짜의 경우 음수, 과거 날짜의 경우 양수.

**구문**

```sql
{%= ageInMonths(date) %}
```

+++예

currentDate = 2025-01-07T12:22:46.993748+05:30(아시아/콜카타)

* 입력: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* 출력: `12`

+++

## 날짜 비교 {#compare-dates}

`compareDates` 함수는 첫 번째 입력 날짜와 다른 입력 날짜를 비교합니다. date1이 date2와 같으면 0을 반환하고, date1이 date2 전에 오면 -1을 반환하고, date1이 date2 후에 오면 1을 반환합니다.

**구문**

```sql
{%= compareDates(date1, date2) %}
```

+++예

* 입력: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* 출력: `-1`

+++

## ZonedDateTime 변환 {#convert-zoned-date-time}

`convertZonedDateTime` 함수는 날짜-시간을 지정된 시간대로 변환합니다.

**구문**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++예

* 입력: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* 출력: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

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

## 월일 {#day-month}

`dayOfWeek`은(는) 그 달의 요일을 나타내는 숫자를 반환합니다.

**구문**

```sql
{%= dayOfMonth(datetime) %}
```

+++예

* 입력: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* 출력: `5`

+++


## 요일 {#day-week}

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

## 초 단위 차이 {#diff-seconds}

`diffInSeconds` 함수는 두 날짜 간의 차이점을 초 단위로 반환합니다.

**구문**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++예

* 입력: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* 출력: `50`

+++

## 시간 추출 {#extract-hours}

`extractHours` 함수는 특정 타임스탬프에서 시간 구성 요소를 추출합니다.

**구문**

```sql
{%= extractHours(date) %}
```

+++예

* 입력: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `17`

+++

## 분 추출 {#extract-minutes}

`extractMinutes` 함수는 특정 타임스탬프에서 분 구성 요소를 추출합니다.

**구문**

```sql
{%= extractMinutes(date) %}
```

+++예

* 입력: `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `19`

+++

## 월 추출 {#extract-months}

`extractMonth` 함수는 지정된 타임스탬프에서 월 구성 요소를 추출합니다.

**구문**

```sql
{%= extractMonths(date) %}
```

+++예

* 입력: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `11`

+++

## 초 추출 {#extract-seconds}

`extractSeconds` 함수는 특정 타임스탬프에서 두 번째 구성 요소를 추출합니다.

**구문**

```sql
{%= extractSeconds(date) %}
```

+++예

* 입력: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `51`

+++

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

## CurrentZonedDateTime 가져오기 {#get-current-zoned-date-time}

`getCurrentZonedDateTime` 함수는 표준 시간대 정보와 함께 현재 날짜 및 시간을 반환합니다.

**구문**

```sql
{%= getCurrentZonedDateTime() %}
```

+++예

* 입력: `{%= getCurrentZonedDateTime() %}`
* 출력: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## 시간 차이 {#hours-difference}

`diffInHours` 함수는 시간 측면에서 두 날짜 간의 차이를 반환합니다.

**구문**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++예

* 입력: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* 출력: `10`

+++

## 분 차이{#diff-minutes}

`diffInMinutes` 함수는 분 단위로 두 날짜 간의 차이점을 반환하는 데 사용됩니다.

**구문**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++예

* 입력: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* 출력: `60`

+++

## 월 차이 {#months-difference}

`diffInMonths` 함수는 월 단위로 두 날짜 간의 차이점을 반환합니다.

**구문**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++예

* 입력: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* 출력: `3`

+++

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

## 날짜로 변환 {#to-date-time}

`ToDateTime` 함수는 문자열을 날짜로 변환합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.

**구문**

```sql
{%= toDateTime(string, string) %}
```

+++예

* 입력: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* 출력: `2024-11-01T17:19:51Z`

+++

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

## 일의 시작으로 잘라내기 {#truncate-day}

`truncateToStartOfDay` 함수는 특정 날짜-시간을 00:00으로 설정된 하루의 시작으로 설정하여 수정하는 데 사용됩니다.

**구문**

```sql
{%= truncateToStartOfDay(date) %}
```

+++예

* 입력: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* 출력: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

`truncateToStartOfQuarter` 함수는 00:00에 분기의 첫째 날(예: 1월 1일, 4월 1일, 7월 1일, 10월 1일)까지 날짜-시간을 자르는 데 사용됩니다.

**구문**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++예

* 입력: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

`truncateToStartOfWeek` 함수는 지정된 날짜-시간을 주의 시작(월요일 00:00)으로 설정하여 수정합니다.

**구문**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++예

* 입력: `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* 출력: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

`truncateToStartOfYear` 함수는 00:00에 연도의 첫째 날(1월 1일)로 잘라내어 지정된 날짜-시간을 수정하는 데 사용됩니다.

**구문**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++예

* 입력: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `2024-01-01T00:00Z`

+++

## 연간 주 {#week-of-year}

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

## 연도 차이 {#diff-years}

`diffInYears` 함수는 연도 단위로 두 날짜 간의 차이를 반환하는 데 사용됩니다.

**구문**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++예

* 입력: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* 출력: `5`

+++
