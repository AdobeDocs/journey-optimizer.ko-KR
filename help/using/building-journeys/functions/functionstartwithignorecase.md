---
product: adobe campaign
title: startWithIgnoreCase
description: startWithIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 27%

---

# startWithIgnoreCase {#startWithIgnoreCase}

두 번째 매개 변수가 대/소문자를 고려하지 않고 첫 번째 매개 변수의 접두사이면 true를 반환합니다.

## 카테고리

문자열

## 함수 구문

`startWithIgnoreCase(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-------------|--------|
| string | string |
| prefix로 인해 영구적으로 지정되는 Mbox 매개 변수입니다 | string |

## 서명 및 반환된 형식

`startWithIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`startWithIgnoreCase("rowing is great", "RO")`

true를 반환합니다.
