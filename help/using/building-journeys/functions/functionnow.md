---
product: journey optimizer
title: now
description: 이제 함수에 대해 알아봅니다.
feature: Journeys
role: Engineer
level: Experienced
keywords: now, 함수, 표현식, 여정
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 14%

---

# now {#now}

현재 날짜를 날짜 시간 형식으로 반환합니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

## 카테고리

Date

## 함수 구문

`now(<parameter>)`

## 매개변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 시간대 식별자(선택 사항) |

## 서명 및 반환된 유형

`now()`

`now("<timeZone id>")`

dateTime을 반환합니다.

## 예

`now()`

2023-06-03T06:30Z을 반환합니다.

`toString(now())`

&quot;2023-06-03T06:30Z&quot; 반환

`now("Europe/Paris")`

2023-06-03T08:30+02:00을 반환합니다.
