---
product: adobe campaign
title: inLastYears
description: LastYears의 기능에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
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
