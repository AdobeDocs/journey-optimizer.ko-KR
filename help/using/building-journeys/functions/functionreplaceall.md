---
product: journey optimizer
title: replaceAll
description: replaceAll 함수에 대해 알아봅니다.
feature: Journeys
role: Developer
level: Experienced
keywords: replaceAll, 함수, 표현식, 여정
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

대상 문자열과 일치하는 모든 발생 항목을 기본 문자열의 대체 문자열로 바꿉니다.

교체는 문자열 시작부터 끝까지 진행됩니다. 예를 들어, 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아닌 &quot;ba&quot;가 생성됩니다.

## 카테고리

문자열

## 함수 구문

`replaceAll(<parameters>)`

## 매개변수

| 매개변수 | 유형 |
|-----------|--------------|
| 기본 | 문자열 |
| 대상 | 문자열(RegExp) |
| 교체 | 문자열 |

## 서명 및 반환된 유형

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

문자열을 반환합니다.

## 예{#example}

`replaceAll("Hello World", "l", "x")`

&quot;Hexxo Worxd&quot;를 반환합니다.

대상 매개 변수는 RegExp이므로 바꿀 문자열에 따라 일부 문자를 이스케이프해야 할 수 있습니다. [이 페이지](../functions/functionreplace.md#example_2)의 예제를 참조하십시오.
