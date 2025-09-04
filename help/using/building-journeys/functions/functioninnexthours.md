---
product: journey optimizer
title: inNextHours
description: inNextHours 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, 함수, 표현식, 여정
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

지정된 date 또는 dateTime이 now와 now + delta 시간 사이에 있으면 true를 반환합니다.

## 카테고리

Date

## 함수 구문

`inNextHours(<dateTime>,<delta>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextHours(<dateTime>,<integer>)`

부울 반환.

## 예

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

true를 반환합니다.
