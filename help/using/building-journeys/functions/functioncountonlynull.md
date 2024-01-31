---
product: journey optimizer
title: countOnlyNull
description: countOnlyNull 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, 함수, 표현식, 여정
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

목록의 null 값 수를 계산합니다.

매개 변수는 `<listObject>` 은(는) 이 함수에서 지원되지 않습니다.

## 카테고리

집계

## 함수 구문

`countOnlyNull(<listAny>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## 서명 및 반환된 유형

`countOnlyNull(<listAny>)`

정수 반환.

## 예

`countOnlyNull([10,2,10,null])`

1을 반환합니다.
