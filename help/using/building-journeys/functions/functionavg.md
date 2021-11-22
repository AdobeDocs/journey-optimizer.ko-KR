---
product: adobe campaign
title: avg
description: 평균 함수에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# avg {#avg}

목록 또는 두 개의 표현식으로 제공되는 표현식 집합 간의 평균 값을 반환합니다. Null 값은 무시됩니다.


## 카테고리

집계

## 함수 구문

`avg(<parameter>)`

## 매개 변수

지원되는 유형:

* listInteger
* listDecimal
* 십진수
* 정수

## 서명 및 반환된 유형

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

소수점 반환

## 예시

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

7.0을 반환합니다.

`avg(10.2, 3)`

6.6을 반환합니다.
