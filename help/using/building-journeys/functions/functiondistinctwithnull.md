---
product: journey optimizer
title: distinctWithNull
description: distinctWithNull 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, 함수, 표현식, 여정
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

주어진 목록의 고유 값 또는 개체를 반환합니다. 목록에 null 항목이 하나 이상 있으면 반환된 목록에 null 항목이 표시됩니다.

매개 변수는 `<listObject>` 은(는) 이 함수에서 지원되지 않습니다.

## 카테고리

목록

## 함수 구문

`distinctWithNull(<parameters>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | 처리할 목록. |

## 서명 및 반환된 유형

`distinctWithNull(<listInteger>)`

정수 목록을 반환합니다.

`distinctWithNull(<listDecimal>)`

소수점 목록을 반환합니다.

`distinctWithNull(<listString>)`

문자열 목록을 반환합니다.

`distinctWithNull(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`distinctWithNull(<listDateTime>)`

날짜/시간 목록을 반환합니다.

`distinctWithNull(<listDateOnly>)`

날짜 목록을 반환합니다.

`distinctWithNull(<listBoolean>)`

부울 목록을 반환합니다.

`distinctWithNull(<listDuration>)`

기간 목록을 반환합니다.

## 예시

`distinctWithNull([10,2,10,null])`

반환 [10, 2, null]
