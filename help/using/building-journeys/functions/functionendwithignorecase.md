---
product: journey optimizer
title: endWithIgnoreCase
description: 함수 endWithIgnoreCase에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase, 함수, 식, 여정
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

첫 번째 인수 문자열이 대/소문자를 고려하지 않고 특정 문자열(두 번째 인수 문자열)로 끝나는지 확인합니다.

## 카테고리

문자열

## 함수 구문

`endWithIgnoreCase(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 접미사 | 문자열 |

## 서명 및 반환된 형식

`endWithIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`endWithIgnoreCase("rowing is great", "AT")`

true를 반환합니다.
