---
product: journey optimizer
title: endWith
description: 함수 끝에 대해 알아보기With
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, function, expression, 여정
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

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
| 문자열 | 문자열 |
| 접미사 | 문자열 |

## 서명 및 반환된 형식

`endWith(<string>,<string>)`

부울을 반환합니다.

## 예

`endWith("Hello World", "World")`

true를 반환합니다.

`endWith("Hello World", "Hello")`

false를 반환합니다.
