---
product: journey optimizer
title: max
description: 최대 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: max, 함수, 표현식, 여정
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

목록 또는 두 표현식으로 지정된 표현식 세트 중 최대값을 반환합니다. Null 값은 무시됩니다.

## 카테고리

집계

## 함수 구문

`max(<parameter>)`

## 매개 변수

* listDuration
* list정수
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 지속 시간
* 정수
* decimal
* dateTime
* dateTimeOnly

## 서명 및 반환된 유형

`max(<listDuration>)`

기간을 반환합니다.

`max(<listInteger>)`

기간을 반환합니다.

`max(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`max(<listDateTime>)`

날짜/시간을 반환합니다.

`max(<listDateOnly>)`

날짜를 반환합니다.

`max(<listDecimal>)`

십진수를 반환합니다.

`max(<decimal>,<decimal>)`

십진수를 반환합니다.

`max(<duration>,<duration>)`

기간을 반환합니다.

`max(<dateTime>,<dateTime>)`

날짜/시간을 반환합니다.

`max(<dateTimeOnly>,<dateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`max(<integer>,<integer>)`

정수 반환.

## 예시

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

10을 반환합니다.

`max([10,null,8])`

10을 반환합니다.
