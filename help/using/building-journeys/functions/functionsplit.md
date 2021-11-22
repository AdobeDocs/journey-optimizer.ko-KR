---
product: adobe campaign
title: split
description: 함수 분할에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---

# split {#split}

첫 번째 인수 문자열을 구분 기호 문자열(정규 표현식일 수 있는 두 번째 인수 문자열)로 분할하여 문자열(토큰) 목록을 만듭니다.

## 카테고리

문자열

## 함수 구문

`split(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 입력 문자열 | string |
| 구분 문자열 | string |

## 서명 및 반환된 유형

`split(<input string>, <separator string>)`

listString을 반환합니다.

## 예

`split(["A_B_C"], "_")`

반환 `["A","B","C"]`

값이 있는 이벤트 필드 &#39;event.appVersion&#39;이 있는 예: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

반환 `["20", "45", "2", "3434"]`
