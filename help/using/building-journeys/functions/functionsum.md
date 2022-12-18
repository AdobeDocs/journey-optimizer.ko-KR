---
product: journey optimizer
title: sum
description: 함수 합에 대해 알아봅니다
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---

# sum {#sum}

표현식 세트의 값 합계를 반환합니다. Null 값은 무시됩니다.

## 카테고리

집계

## 함수 구문

`sum(<parameters>)`

## 매개 변수

* listInteger
* listDecimal
* 기간
* 정수
* 십진수

## 서명 및 반환된 형식

`sum(<listDecimal>)`

소수점 반환

`sum(<listInteger>)`

정수를 반환합니다.

`sum(<integer>,<integer>)`

정수를 반환합니다.

`sum(<decimal>,<decimal>)`

소수점 반환

## 예시

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

21을 반환합니다.

`sum([10.5,null,8.1])`

18.6을 반환합니다.
