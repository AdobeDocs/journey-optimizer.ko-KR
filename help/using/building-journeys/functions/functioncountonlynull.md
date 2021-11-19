---
product: adobe campaign
title: countOnlyNull
description: 함수 countOnlyNull에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 33%

---

# countOnlyNull {#countOnlyNull}

목록에서 null 값 수를 계산합니다.

## 카테고리

집계

## 함수 구문

`countOnlyNull(<listAny>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 목록 | listBoolean |
| 목록 | listInteger |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

## 서명 및 반환된 형식

`countOnlyNull(<listAny>)`

정수를 반환합니다.

## 예

`countOnlyNull([10,2,10,null])`

1 반환.
