---
product: journey optimizer
title: count
description: 함수 개수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, function, expression, 여정
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# count {#count}

null 값을 고려하지 않는 목록의 요소를 계산합니다.

## 카테고리

집계

## 함수 구문

`count(<listAny>)`

`count(<listObject>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. listObject는 null 개체를 포함할 수 없습니다. |

## 서명 및 반환된 유형

`count(<listAny>)`

정수 반환.

## 예

`count([10,2,10,null])`

3을 반환합니다.

`count(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에 있는 개체 수를 반환합니다. 비고: listObject는 null 개체를 포함할 수 없습니다.
