---
product: adobe campaign
title: now
description: 지금 함수 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# now {#now}

현재 날짜를 날짜 시간 형식으로 반환합니다. 데이터 유형에 대한 자세한 내용은 [이 페이지](../expression/data-types.md).

## 카테고리

날짜

## 함수 구문

`now(<parameter>)`

## 매개 변수

| 매개 변수 | 설명 |
|--- |--- |
| string |  |

## 서명 및 반환된 유형

`now()`

`now("<timeZone id>")`

dateTime 반환

## 예시

`now()`

2019-06-03T06:30Z를 반환합니다.

`toString(now())`

반환: &quot;2019-06-03T06:30Z&quot;

`now("Europe/Paris")`

2019-06-03T08:30+02:00을 반환합니다.
