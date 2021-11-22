---
product: adobe campaign
title: inLastHours
description: LastHours의 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---

# inLastHours {#inLastHours}

주어진 날짜 시간이 지금부터 현재 - 델타 시간 사이에 있는 경우 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inLastHours(<dateTime>,<delta>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastHours(<dateTime>,<integer>)`

부울을 반환합니다.

## 예시

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

true를 반환합니다.

`inLastHours(@{MyEvent.timestamp}, 4)`

true를 반환합니다.
