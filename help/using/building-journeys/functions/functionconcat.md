---
product: adobe campaign
title: concat
description: 함수 개념에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 27%

---

# concat {#concat}

두 문자열 매개 변수 또는 문자열 목록을 연결합니다.

## 카테고리

문자열

## 함수 구문

`concat(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| string | string |

## 서명 및 반환된 형식

`concat(<string>,<string>)`

`concat(<listString>)`

문자열을 반환합니다.

## 예

`concat("Hello","World")`

&quot;HelloWorld&quot;를 반환합니다.

`concat(["Hello"," ","World"])`

&quot;Hello World&quot;를 반환합니다.
