---
product: journey optimizer
title: countWithNull
description: countWithNull 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, 함수, 표현식, 여정
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 29%

---

# countWithNull {#countWithNull}

null 값을 포함하여 목록의 모든 요소를 계산합니다.

## 카테고리

집계

## 함수 구문

`countWithNull(<listAny>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 목록 | list부울 |
| 목록 | list정수 |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

## 서명 및 반환된 유형

`countWithNull(<listAny>)`

정수 반환.

## 예

`countWithNull([10,2,10,null])`

4를 반환합니다.
