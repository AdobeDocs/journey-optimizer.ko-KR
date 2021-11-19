---
product: adobe campaign
title: distinctCountWithNull
description: distinctCountWithNull 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCountWithNull {#distinctCountWithNull}

null 값을 포함하여 다른 값의 수를 계산합니다.

## 카테고리

집계

## 함수 구문

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

정수를 반환합니다.

## 예

`distinctCountWithNull([10,2,10,null])`

3 반환.
