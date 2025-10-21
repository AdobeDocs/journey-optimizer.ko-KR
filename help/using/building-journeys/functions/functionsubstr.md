---
product: journey optimizer
title: substr
description: 함수 substr에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: substr, 함수, 표현식, 여정
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

시작 색인과 끝 색인 사이에 있는 문자열 식의 하위 문자열을 반환합니다. 끝 색인이 정의되지 않으면 시작 색인과 끝 사이에 있습니다.

## 카테고리

문자열

## 함수 구문

`substr(<parameters>)`

## 매개변수

| 매개변수 | 유형 |
|-------------|----------|
| 문자열 | 문자열 |
| beginIndex | 정수 |
| endIndex | 정수 |

## 서명 및 반환된 유형

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

문자열을 반환합니다.

## 예

`substr("Hello World",6)`

&quot;World&quot;를 반환합니다.

`substr("Hello World", 0, 5)`

&quot;Hello&quot;를 반환합니다.
