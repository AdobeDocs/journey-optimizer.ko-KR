---
product: journey optimizer
title: distinctCountWithNull
description: distinctCountWithNull 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, 함수, 식, 여정
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# distinctCountWithNull {#distinctCountWithNull}

null 값을 포함하여 다른 값의 수를 계산합니다.

>[!NOTE]
>
>대상 목록이 listObject인 경우 이 함수는 사용자 지정 작업 표현식에서만 사용할 수 있습니다.

## 카테고리

집계

## 함수 구문

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

정수를 반환합니다.

## 예

`distinctCountWithNull([10,2,10,null])`

3 반환.
