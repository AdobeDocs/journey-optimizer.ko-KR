---
product: adobe campaign
title: endWith
description: 함수 끝에 대해 알아보기With
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# endWith {#endWith}

두 번째 매개 변수가 첫 번째 매개 변수의 접미사이면 true를 반환합니다.

## 카테고리

문자열

## 함수 구문

`endWith(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| string | string |
| 접미사 | string |

## 서명 및 반환된 형식

`endWith(<string>,<string>)`

부울을 반환합니다.

## 예

`endWith("Hello World", "World")`

true를 반환합니다.

`endWith("Hello World", "Hello")`

false를 반환합니다.
