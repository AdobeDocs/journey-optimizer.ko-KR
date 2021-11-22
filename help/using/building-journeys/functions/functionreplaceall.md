---
product: adobe campaign
title: replaceAll
description: 함수 replaceAll에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

---

# replaceAll {#replaceAll}

대상 문자열과 일치하는 모든 항목을 기본 문자열의 대체 문자열로 바꿉니다.

대체는 문자열 시작 부분부터 끝 부분까지 진행됩니다. 예를 들어 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아니라 &quot;ba&quot;가 됩니다.

## 카테고리

문자열

## 함수 구문

`replaceAll(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|--------------|
| 기본 | string |
| target | string |
| 교체 | string |

## 서명 및 반환된 형식

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

문자열을 반환합니다.

## 예

`replaceAll("Hello World", "l", "x")`

&quot;Hexxo Worxd&quot;를 반환합니다.
