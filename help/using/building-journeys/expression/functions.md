---
solution: Journey Optimizer
product: journey optimizer
title: 함수
description: 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 함수, 표현식, 편집기, 여정
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 7d75abf6b428becc8b535a63421e85cca417daac
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# 함수 {#functions}

함수에는 서로 다른 서명(순서가 지정된 매개 변수의 다른 세트)이 있을 수 있습니다. 함수 시그니처에는 순서가 지정된 매개 변수로 0-N 표현식이 있을 수 있습니다.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

각 함수에는 특정 반환 유형이 있습니다.

다음은 지원되는 함수 목록입니다.

## 기본 함수

| 카테고리 | 함수 |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| 집계 | [avg](../functions/aggregation-functions.md#avg) |
| 집계 | [count](../functions/aggregation-functions.md#count) |
| 집계 | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| 집계 | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| 집계 | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| 집계 | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| 집계 | [max](../functions/aggregation-functions.md#max) |
| 집계 | [min](../functions/aggregation-functions.md#min) |
| 집계 | [sum](../functions/aggregation-functions.md#sum) |
| 전환 | [toBool](../functions/conversion-functions.md#toBool) |
| 전환 | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| 전환 | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| 전환 | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| 전환 | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| 전환 | [toDuration](../functions/conversion-functions.md#toDuration) |
| 전환 | [toInteger](../functions/conversion-functions.md#toInteger) |
| 전환 | [toString](../functions/conversion-functions.md#toString) |
| Date | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Date | [inLastDays](../functions/functioninlastdays.md) |
| Date | [inLastHours](../functions/functioninlasthours.md) |
| Date | [inLastMonths](../functions/functioninlastmonths.md) |
| Date | [inLastYears](../functions/functioninlastyears.md) |
| Date | [inNextDays](../functions/functioninnextdays.md) |
| Date | [inNextHours](../functions/functioninnexthours.md) |
| Date | [inNextMonths](../functions/functioninnextmonths.md) |
| Date | [inNextYears](../functions/functioninnextyears.md) |
| Date | [now](../functions/functionnow.md) |
| Date | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Date | [setHours](../functions/functionsethours.md) |
| Date | [setDays](../functions/functionsetdays.md) |
| Date | [updateTimeZone](../functions/functionupdatetimezone.md) |
| 목록 | [distinct](../functions/functiondistinct.md) |
| 목록 | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| 목록 | [필터](../functions/functionfilter.md) |
| 목록 | [getListItem](../functions/functiongetlistitem.md) |
| 목록 | [in](../functions/functionin.md) |
| 목록 | [교차](../functions/functionintersect.md) |
| 목록 | [제한](../functions/functionlimit.md) |
| 목록 | [listSize](../functions/functionlistsize.md) |
| 목록 | [serializeList](../functions/functionserializelist.md) |
| 목록 | [sort](../functions/functionsort.md) |
| 수학 | [random](../functions/functionrandom.md) |
| 수학 | [round](../functions/functionround.md) |
| 문자열 | [concat](../functions/functionconcat.md) |
| 문자열 | [contain](../functions/functioncontain.md) |
| 문자열 | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| 문자열 | [endWith](../functions/functionendwith.md) |
| 문자열 | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| 문자열 | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| 문자열 | [indexOf](../functions/functionindexof.md) |
| 문자열 | [isEmpty](../functions/functionisempty.md) |
| 문자열 | [isNotEmpty](../functions/functionisnotempty.md) |
| 문자열 | [lastIndexOf](../functions/functionlastindexof.md) |
| 문자열 | [length](../functions/functionlength.md) |
| 문자열 | [lower](../functions/functionlower.md) |
| 문자열 | [matchRegExp](../functions/functionmatchregexp.md) |
| 문자열 | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| 문자열 | [replace](../functions/functionreplace.md) |
| 문자열 | [replaceAll](../functions/functionreplaceall.md) |
| 문자열 | [split](../functions/functionsplit.md) |
| 문자열 | [startWith](../functions/functionstartwith.md) |
| 문자열 | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| 문자열 | [substr](../functions/functionsubstr.md) |
| 문자열 | [trim](../functions/functiontrim.md) |
| 문자열 | [upper](../functions/functionupper.md) |
| 문자열 | [uuid](../functions/functionuuid.md) |
