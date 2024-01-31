---
product: journey optimizer
title: serializeList
description: serializeList 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, 함수, 표현식, 여정
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

지정된 목록(listObject를 제외한 모든 유형)을 문자열로 변환합니다.

## 카테고리

목록

## 함수 구문

`serializeList(<parameters>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | 문자열로 변환할 목록입니다. |
| 분리자 | 문자열 | 출력 문자열에서 각 목록 요소 사이의 구분 기호입니다. |
| addQuotes | 부울 | 이 매개 변수는 출력 문자열의 각 요소에 따옴표(true)를 포함해야 하는지 여부를 나타냅니다(false). |

## 서명 및 반환된 유형

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

문자열을 반환합니다.

## 예

`serializeList(["Hello","World"], " ", false)`

&quot;Hello World&quot;를 반환합니다.

`serializeList(["Hello", "World"], ",", true)`

&quot;&quot;Hello&quot;,&quot;World&quot;&quot;를 반환합니다.
