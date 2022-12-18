---
product: journey optimizer
title: inLastYears
description: LastYears의 기능에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastYears {#inLastYears}

주어진 날짜 또는 dateTime이 지금부터 현재 - 델타 연도 사이에 있으면 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inLastYears(<dateTime>,<delta>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastYears(<dateTime>,<integer>)`

부울을 반환합니다.

## 예시

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

true를 반환합니다.
