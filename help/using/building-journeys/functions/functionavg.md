---
product: journey optimizer
title: avg
description: 함수 avg에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: avg, 함수, 표현식, 여정
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# avg {#avg}

목록 또는 두 표현식으로 지정된 표현식 세트 중 평균 값을 반환합니다. Null 값은 무시됩니다.


## 카테고리

집계

## 함수 구문

`avg(<parameter>)`

## 매개변수

지원되는 유형:

* list정수
* listDecimal
* decimal
* 정수

## 서명 및 반환된 유형

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

십진수를 반환합니다.

## 예

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

7.0을 반환합니다

`avg(10.2, 3)`

6.6 반환.
