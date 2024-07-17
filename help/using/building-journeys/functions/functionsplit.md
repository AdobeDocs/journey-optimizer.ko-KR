---
product: journey optimizer
title: split
description: 함수 분할에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: split, function, expression, 여정
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 14%

---

# split {#split}

첫 번째 인수 문자열을 구분 문자 문자열(정규 표현식일 수 있는 두 번째 인수 문자열)로 분할하여 문자열(토큰) 목록을 생성합니다.

## 카테고리

문자열

## 함수 구문

`split(<parameters>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 입력 문자열 | 문자열 |
| 구분 문자 문자열 | 문자열 |

## 서명 및 반환된 유형

`split(<input string>, <separator string>)`

listString을 반환합니다.

## 예

`split("A_B_C", "_")`

`["A","B","C"]` 반환

값이 &quot;20.45.2.3434&quot;인 이벤트 필드 &#39;event.appVersion&#39;이 있는 예

`split(@event{event.appVersion}, "\\.")`

`["20", "45", "2", "3434"]` 반환
