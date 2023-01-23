---
product: journey optimizer
title: startWithIgnoreCase
description: startWithIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase, 함수, 식, 여정
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 25%

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
| 문자열 | 문자열 |
| prefix로 인해 영구적으로 지정되는 Mbox 매개 변수입니다 | 문자열 |

## 서명 및 반환된 형식

`startWithIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`startWithIgnoreCase("rowing is great", "RO")`

true를 반환합니다.
