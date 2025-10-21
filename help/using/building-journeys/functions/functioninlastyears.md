---
product: journey optimizer
title: inLastYears
description: inLastYears 함수에 대해 알아보기
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastYears, 함수, 표현식, 여정
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

지정된 date 또는 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 연도).

## 카테고리

Date

## 함수 구문

`inLastYears(<dateTime>,<delta>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastYears(<dateTime>,<integer>)`

부울 반환.

## 예

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.
