---
product: journey optimizer
title: countOnlyNull
description: 함수 countOnlyNull에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

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
