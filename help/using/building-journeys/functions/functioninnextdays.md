---
product: journey optimizer
title: inNextDays
description: inNextDays 함수에 대해 알아보기
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextDays, 함수, 표현식, 여정
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

지정된 date 또는 dateTime이 now와 now + delta 일 사이인 경우 true를 반환합니다.

## 카테고리

Date

## 함수 구문

`inNextDays(<dateTime>,<delta>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextDays(<dateTime>,<integer>)`

부울 반환.

## 예

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.
