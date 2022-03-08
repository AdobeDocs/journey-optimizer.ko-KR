---
product: adobe campaign
title: distinctCount
description: distinctCount 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCount{#distinctCount}

null 값을 무시하고 다른 값의 수를 계산합니다.

## 카테고리

집계

## 함수 구문

`distinctCount(<listAny>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 목록 | listBoolean |
| 목록 | listInteger |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

## 서명 및 반환된 형식

`distinctCount(<listAny>)`

정수를 반환합니다.

## 예

`distinctCount([10,2,10,null])`

2를 반환합니다.
