---
product: adobe campaign
title: inNextMonths
description: NextMonths의 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

주어진 날짜 또는 dateTime이 now와 now + delta months 사이에 있으면 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inNextMonths(<dateTime>,<delta>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextMonths(<dateTime>,<integer>)`

부울을 반환합니다.

## 예시

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

true를 반환합니다.
