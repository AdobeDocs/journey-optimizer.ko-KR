---
product: adobe campaign
title: startWith
description: 함수 startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 27%

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
| string | string |
| prefix로 인해 영구적으로 지정되는 Mbox 매개 변수입니다 | string |

## 서명 및 반환된 형식

`startWith(<string>,<string>)`

부울을 반환합니다.

## 예

`startWith("Hello World", "Hello")`

true를 반환합니다.

`startWith("Hello World", "World")`

false를 반환합니다.
