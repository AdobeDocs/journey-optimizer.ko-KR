---
product: journey optimizer
title: substr
description: Function substr에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr, 함수, 표현식, 여정
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

시작 인덱스와 끝 인덱스 사이에 문자열 식의 하위 문자열을 반환합니다. 끝 인덱스가 정의되지 않으면 시작 색인과 끝 사이의 인덱스입니다.

## 카테고리

문자열

## 함수 구문

`substr(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-------------|----------|
| 문자열 | 문자열 |
| beginIndex | 정수 |
| endIndex | 정수 |

## 서명 및 반환된 형식

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

문자열을 반환합니다.

## 예

`substr("Hello World",6)`

&quot;World&quot;를 반환합니다.

`substr("Hello World", 0, 5)`

&quot;Hello&quot;를 반환합니다.
