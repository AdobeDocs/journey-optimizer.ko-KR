---
product: journey optimizer
title: containIgnoreCase
description: containIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# containIgnoreCase {#containIgnoreCase}

대/소문자를 고려하지 않고 두 번째 인수 문자열이 첫 번째 인수 문자열에 포함되어 있는지 확인합니다.

## 카테고리

문자열

## 함수 구문

`containIgnoreCase(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| string | string |
| 검색된 문자열 | string |

## 서명 및 반환된 형식

`containIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`containIgnoreCase("rowing is great", "GREAT")`

true를 반환합니다.
