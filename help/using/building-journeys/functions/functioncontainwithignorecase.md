---
product: journey optimizer
title: containIgnoreCase
description: containIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, 함수, 표현식, 여정
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

두 번째 인수 문자열이 대소문자를 고려하지 않고 첫 번째 인수 문자열에 포함되어 있는지 확인합니다.

## 카테고리

문자열

## 함수 구문

`containIgnoreCase(<parameters>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 문자열 검색됨 | 문자열 |

## 서명 및 반환된 유형

`containIgnoreCase(<string>,<string>)`

부울 반환.

## 예

`containIgnoreCase("rowing is great", "GREAT")`

true를 반환합니다.
