---
product: adobe campaign
title: replace
description: 함수 바꾸기에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---

# replace {#replace}

대상 문자열과 일치하는 첫 번째 항목을 기본 문자열의 대체 문자열로 바꿉니다.

대체는 문자열 시작 부분부터 끝 부분까지 진행됩니다. 예를 들어 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아니라 &quot;ba&quot;가 됩니다.

## 카테고리

문자열

## 함수 구문

`replace(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|--------------|
| 기본 | string |
| target | string |
| 교체 | string |

## 서명 및 반환된 형식

`replace(<base>,<target>,<replacement>)`

문자열을 반환합니다.

## 예

`replace("Hello World", "l", "x")`

&quot;Hexlo World&quot;를 반환합니다.
