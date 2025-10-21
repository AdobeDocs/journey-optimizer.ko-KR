---
product: journey optimizer
title: updateTimeZone
description: updateTimeZone 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: updateTimeZone, 함수, 표현식, 여정
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 9%

---

# updateTimeZone {#updateTimeZone}

같은 순간에 새 시간대와 함께 새 날짜 시간을 반환합니다.

## 카테고리

Date

## 함수 구문

`updateTimeZone(<parameters>)`

## 매개변수

* 시간대 id: 문자열
* dateTime

## 서명 및 반환된 유형

`updateTimeZone(<dateTime>,<timeZone id>)`

날짜/시간을 반환합니다.

## 예

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

2023-08-28T17:15:30.123+02:00을 반환합니다.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

타임스탬프 필드의 값이 `2021-11-16T16:55:12.939318+01:00`이면 함수는 `2021-11-17T02:55:12.942115+11:00`을(를) 반환합니다.
