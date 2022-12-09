---
product: journey optimizer
title: inLastDays
description: LastDays의 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

---

# inLastDays {#inLastDays}

주어진 날짜 또는 dateTime이 지금부터 현재 - 델타 일 사이에 있으면 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inLastDays(<dateTime>,<delta>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastDays(<dateTime>,<integer>)`

부울을 반환합니다.

## 예

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

true를 반환합니다.
