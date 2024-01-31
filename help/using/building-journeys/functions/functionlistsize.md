---
product: journey optimizer
title: listSize
description: listSize 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, 함수, 표현식, 여정
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# listSize {#listSize}

목록의 요소 수를 계산합니다.

## 카테고리

목록

## 함수 구문

`listSize(<parameters>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. listObject는 null 개체를 포함할 수 없습니다. |

## 서명 및 반환된 유형

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

정수를 반환합니다.

`listSize(<listObject>)`

## 예

`listSize([10,2,3])`

3을 반환합니다.

`listSize(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에 있는 개체 수를 반환합니다.
