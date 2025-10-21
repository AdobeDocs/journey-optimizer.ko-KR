---
product: journey optimizer
title: concat
description: 함수 concat에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: concat, 함수, 표현식, 여정
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concat {#concat}

두 개의 문자열 매개 변수 또는 문자열 목록을 연결합니다.

## 카테고리

문자열

## 함수 구문

`concat(<parameters>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 문자열 | 문자열 |

## 서명 및 반환된 유형

`concat(<string>,<string>)`

`concat(<listString>)`

문자열을 반환합니다.

## 예

`concat("Hello","World")`

&quot;HelloWorld&quot;를 반환합니다.

`concat(["Hello"," ","World"])`

&quot;Hello World&quot;를 반환합니다.
