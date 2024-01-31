---
product: journey optimizer
title: sum
description: 함수 합에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum, 함수, 표현식, 여정
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# sum {#sum}

표현식 집합의 값 합계를 반환합니다. Null 값은 무시됩니다.

## 카테고리

집계

## 함수 구문

`sum(<parameters>)`

## 매개 변수

* list정수
* listDecimal
* 지속 시간
* 정수
* decimal

## 서명 및 반환된 유형

`sum(<listDecimal>)`

십진수를 반환합니다.

`sum(<listInteger>)`

정수 반환.

`sum(<integer>,<integer>)`

정수 반환.

`sum(<decimal>,<decimal>)`

십진수를 반환합니다.

## 예시

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

21을 반환합니다.

`sum([10.5,null,8.1])`

18.6을 반환합니다.
