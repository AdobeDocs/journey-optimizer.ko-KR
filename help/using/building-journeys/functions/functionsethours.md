---
product: journey optimizer
title: setHours
description: setHours 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, 함수, 표현식, 여정
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 8%

---

# setHours {#setHours}

날짜 시간 또는 날짜 시간의 시간만 설정합니다. 예를 들어 내일 특정 시간까지 기다리려면 시간을 강제로 지정할 수 있습니다.

## 카테고리

날짜

## 함수 구문

`setHours(<parameter>)`

## 매개 변수

| 매개변수 | 유형 |
|--- |--- |
| 날짜 시간 | dateTime |
| 시간대를 고려하지 않은 날짜 시간 | dateTimeOnly |
| 시간 | 정수 |

## 서명 및 반환된 유형

`setHours(<dateTime>,<hours>)`

날짜/시간을 반환합니다.

`setHours(<dateTimeOnly>,<hours>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

## 예시

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

2023-12-12T04 반환:11:0Z.

`setHours(nowWithDelta(1, "days"), 20)`

내일 오후 8시(XY)에 를 반환합니다. XY는 현재 시간 평가 시점의 분입니다. 오전 2시 45분에 평가가 이뤄지면 돌아오는 시간은 오후 8시 45분이다.
