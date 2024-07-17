---
product: journey optimizer
title: distinctCountWithNull
description: distinctCountWithNull 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, 함수, 표현식, 여정
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

null 값을 포함하여 다른 값의 수를 계산합니다.

`<listObject>` 매개 변수는 이 함수에서 지원되지 않습니다.

## 카테고리

집계

## 함수 구문

`distinctCountWithNull(<listAny>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## 서명 및 반환된 유형

`distinctCountWithNull(<listAny>)`

정수 반환.

## 예

`distinctCountWithNull([10,2,10,null])`

3을 반환합니다.
