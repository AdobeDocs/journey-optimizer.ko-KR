---
product: journey optimizer
title: min
description: min 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min, 함수, 표현식, 여정
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# min {#min}

목록 또는 두 표현식으로 지정된 표현식 세트 중 최소값을 반환합니다. Null 값은 무시됩니다.

## 카테고리

집계

## 함수 구문

`min(<parameters>)`

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

`min(<listDuration>)`

기간을 반환합니다.

`min(<listInteger>)`

기간을 반환합니다.

`min(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`min(<listDateTime>)`

날짜/시간을 반환합니다.

`min(<listDateOnly>)`

날짜를 반환합니다.

`min(<listDecimal>)`

십진수를 반환합니다.

`min(<decimal>,<decimal>)`

십진수를 반환합니다.

`min(<duration>,<duration>)`

기간을 반환합니다.

`min(<dateTime>,<dateTime>)`

날짜/시간을 반환합니다.

`min(<dateTimeOnly>,<dateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`min(<integer>,<integer>)`

정수 반환.

## 예시

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

3을 반환합니다.

`min([10,null,8])`

8을 반환합니다.
