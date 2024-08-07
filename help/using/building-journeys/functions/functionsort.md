---
product: journey optimizer
title: sort
description: 함수 정렬에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sort, function, expression, 여정
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 7%

---

# sort {#sort}

값 또는 개체 목록을 원래 순서로 정렬합니다.

## 카테고리

목록

## 함수 구문

`sort(<parameters>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 정렬할 목록입니다. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 listObject에만 사용할 수 있습니다. 해당 목록의 개체에 있는 특성 이름은 정렬의 키로 사용됩니다. |
| 정렬 순서 | 부울 | 오름차순(true) 또는 내림차순(false) |

## 서명 및 반환된 유형

`sort(<listInteger>,<boolean>)`

정수 목록을 반환합니다.

`sort(<listDecimal>,<boolean>)`

소수점 목록을 반환합니다.

`sort(<listString>,<boolean>)`

문자열 목록을 반환합니다.

`sort(<listDateTimeOnly>,<boolean>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`sort(<listDateTime>,<boolean>)`

날짜/시간 목록을 반환합니다.

`sort(<listDateOnly>,<boolean>)`

날짜 목록을 반환합니다.

`sort(<listBoolean>,<boolean>)`

부울 목록을 반환합니다.

`sort(<listObject>,<string>,<boolean>)`

개체 목록을 반환합니다.

## 예

`sort(["A", "C", "B"], true)`

`["A","B","C"]`을(를) 반환합니다

`sort([1, 3, 2], false)`

`[3, 2, 1]`을(를) 반환합니다

`sort(@event{my_event.productListItems}, "SKU", true)`

SKU 속성으로 정렬된 listObject 반환(오름차순)

