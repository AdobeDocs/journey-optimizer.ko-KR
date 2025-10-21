---
product: journey optimizer
title: inNextMonths
description: inNextMonths 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: inNextMonths, 함수, 표현식, 여정
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

지정된 date 또는 dateTime이 now와 now + delta 개월 사이에 있으면 true를 반환합니다.

## 카테고리

Date

## 함수 구문

`inNextMonths(<dateTime>,<delta>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextMonths(<dateTime>,<integer>)`

부울 반환.

## 예

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

true를 반환합니다.
