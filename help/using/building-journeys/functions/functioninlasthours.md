---
product: journey optimizer
title: inLastHours
description: inLastHours 함수에 대해 알아보기
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastHours, 함수, 표현식, 여정
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

지정된 날짜 시간이 지금부터 델타 시간 사이인 경우 true를 반환합니다.

## 카테고리

Date

## 함수 구문

`inLastHours(<dateTime>,<delta>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastHours(<dateTime>,<integer>)`

부울 반환.

## 예

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.

`inLastHours(@event{MyEvent.timestamp}, 4)`

true를 반환합니다.
