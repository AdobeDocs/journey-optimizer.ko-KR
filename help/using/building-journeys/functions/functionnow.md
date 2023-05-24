---
product: journey optimizer
title: now
description: 이제 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: now, 함수, 표현식, 여정
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 16%

---

# now {#now}

현재 날짜를 날짜 시간 형식으로 반환합니다. 데이터 유형에 대한 자세한 내용은 [이 페이지](../expression/data-types.md).

## 카테고리

날짜

## 함수 구문

`now(<parameter>)`

## 매개 변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 |  |

## 서명 및 반환된 유형

`now()`

`now("<timeZone id>")`

dateTime을 반환합니다.

## 예시

`now()`

2019-06-03T06:30Z를 반환합니다.

`toString(now())`

&quot;2019-06-03T06:30Z&quot; 반환

`now("Europe/Paris")`

2019-06-03T08:30+02:00을 반환합니다.
