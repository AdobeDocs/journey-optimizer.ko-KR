---
product: journey optimizer
title: distinctCount
description: distinctCount 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, 함수, 표현식, 여정
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

null 값을 무시하는 다른 값의 수를 계산합니다.

## 카테고리

집계

## 함수 구문

`distinctCount(<listAny>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 선택 사항이며 listObject에만 사용됩니다. 매개변수를 제공하지 않으면 모든 속성의 값이 동일한 경우 객체가 복제된 것으로 간주됩니다. 그렇지 않으면, 지정된 속성에 동일한 값이 있으면 객체가 복제된 것으로 간주됩니다. |

## 서명 및 반환된 유형

`distinctCount(<listAny>)`

정수 반환.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

개체 목록을 반환합니다.


## 예

`distinctCount([10,2,10,null])`

2를 반환합니다.

`distinctCount(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에서 엄격히 구별되는 개체 수를 반환합니다.

`distinctCount(@event{my_event.productListItems}, "SKU")`

고유한 &quot;SKU&quot; 특성 값 {}이(가) 있는 개체 수를 반환합니다.
