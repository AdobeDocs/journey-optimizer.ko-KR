---
product: journey optimizer
title: startWith
description: 함수 startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, function, expression, 여정
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 25%

---

# startWith {#startWith}

두 번째 매개 변수가 첫 번째 매개 변수의 접두사이면 true를 반환합니다.

## 카테고리

문자열

## 함수 구문

`startWith(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-------------|--------|
| 문자열 | 문자열 |
| prefix로 인해 영구적으로 지정되는 Mbox 매개 변수입니다 | 문자열 |

## 서명 및 반환된 형식

`startWith(<string>,<string>)`

부울을 반환합니다.

## 예

`startWith("Hello World", "Hello")`

true를 반환합니다.

`startWith("Hello World", "World")`

false를 반환합니다.
