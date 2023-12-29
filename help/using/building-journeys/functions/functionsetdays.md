---
product: journey optimizer
title: setDays
description: setDays 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays, 함수, 표현식, 여정
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 11%

---

# setDays {#setDays}

날짜/시간 또는 날짜/시간만 설정합니다. 예를 들어, 특정 날짜까지 기다리려면 날짜를 강제로 지정할 수 있습니다.

## 카테고리

날짜

## 함수 구문

`setDays(<parameter>)`

## 매개 변수

| 매개변수 | 유형 |
|--- |--- |
| 날짜 시간 | dateTime |
| 시간대를 고려하지 않은 날짜 시간 | dateTimeOnly |
| 일 | 정수 |

## 서명 및 반환된 유형

`setDays(<dateTime>,<days>)`

날짜/시간을 반환합니다.

`setDays(<dateTimeOnly>,<days>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

## 예시

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

2010-12-25T01 반환:11:0Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
