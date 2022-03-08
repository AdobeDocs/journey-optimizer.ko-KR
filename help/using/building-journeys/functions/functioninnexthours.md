---
product: adobe campaign
title: inNextHours
description: 다음 시간의 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextHours {#inNextHours}

주어진 날짜 또는 dateTime이 now와 now + delta 시간 사이에 있으면 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inNextHours(<dateTime>,<delta>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextHours(<dateTime>,<integer>)`

부울을 반환합니다.

## 예시

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

true를 반환합니다.
