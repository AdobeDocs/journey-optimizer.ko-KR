---
product: journey optimizer
title: round
description: 함수 라운드에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: round, function, expression, 여정
exl-id: b9d5fd2f-9c7f-4811-b34f-23ce1d2c833f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 14%

---

# round {#round}

인수에 가장 가까운 정수 값을 반환하며, 인수는 양의 무한대로 반올림됩니다.

## 카테고리

계산

## 함수 구문

`round(<parameters>)`

## 매개 변수

* decimal
* 정수

## 서명 및 반환된 유형

`round(<decimal>)`

`round(<integer>)`

정수를 반환합니다.

## 예

`round(3.14)`

3을 반환합니다.

`round(3.54)`

4를 반환합니다.

`round(-3.14)`

-3을 반환합니다.

`round(3)`

3을 반환합니다.
