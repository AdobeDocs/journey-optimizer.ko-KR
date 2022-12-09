---
product: journey optimizer
title: startWithIgnoreCase
description: startWithIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

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
| 접두사 | string |

## 서명 및 반환된 형식

`startWithIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`startWithIgnoreCase("rowing is great", "RO")`

true를 반환합니다.
