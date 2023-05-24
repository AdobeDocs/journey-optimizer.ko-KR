---
product: journey optimizer
title: distinctCount
description: distinctCount 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, 함수, 표현식, 여정
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

---

# distinctCount{#distinctCount}

null 값을 무시하는 다른 값의 수를 계산합니다.

## 카테고리

집계

## 함수 구문

`distinctCount(<listAny>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 목록 | list부울 |
| 목록 | list정수 |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

## 서명 및 반환된 유형

`distinctCount(<listAny>)`

정수 반환.

## 예

`distinctCount([10,2,10,null])`

2를 반환합니다.
