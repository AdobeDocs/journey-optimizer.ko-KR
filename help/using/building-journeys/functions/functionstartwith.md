---
product: journey optimizer
title: startWith
description: startWith 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: startWith, 함수, 표현식, 여정
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

두 번째 매개 변수가 첫 번째 매개 변수의 접두사인 경우 true를 반환합니다.

## 카테고리

문자열

## 함수 구문

`startWith(<parameters>)`

## 매개변수

| 매개변수 | 유형 |
|-------------|--------|
| 문자열 | 문자열 |
| 접두사 | 문자열 |

## 서명 및 반환된 유형

`startWith(<string>,<string>)`

부울 반환.

## 예

`startWith("Hello World", "Hello")`

true를 반환합니다.

`startWith("Hello World", "World")`

false를 반환합니다.
