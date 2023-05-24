---
product: journey optimizer
title: inNextYears
description: inNextYears 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears, 함수, 표현식, 여정
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

지정된 date 또는 dateTime이 now와 now + delta years 사이에 있으면 true를 반환합니다.

## 카테고리

날짜

## 함수 구문

`inNextYears(<dateTime>,<delta>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜 시간 | dateTime |
| 델타 | 정수 |

## 서명 및 반환된 유형

`inNextYears(<dateTime>,<integer>)`

부울 반환.

## 예시

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

true를 반환합니다.
