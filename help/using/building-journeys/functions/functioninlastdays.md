---
product: journey optimizer
title: inLastDays
description: inLastDays 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, 함수, 표현식, 여정
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: e0a942f4dc84b41882b3c12dd47f5931a8a34a2b
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

지정된 dateTime이 now와 now 사이에 있으면 true를 반환합니다(델타 일).

## 카테고리

날짜

## 함수 구문

`inLastDays(<dateTime>,<delta>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inLastDays(<dateTime>,<integer>)`

부울 반환.

## 예시

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.
