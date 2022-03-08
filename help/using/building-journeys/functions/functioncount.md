---
product: adobe campaign
title: count
description: 함수 개수에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# count {#count}

null 값을 고려하지 않는 목록의 요소를 계산합니다.

## 카테고리

집계

## 함수 구문

`count(<listAny>)`

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

## 서명 및 반환된 유형

`count(<listAny>)`

정수를 반환합니다.

## 예

`count([10,2,10,null])`

3 반환.
