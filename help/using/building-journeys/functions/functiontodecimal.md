---
product: journey optimizer
title: toDecimal
description: toDecimal 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: decimal, 함수, 표현식, 여정
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 14%

---

# toDecimal {#toDecimal}

인수 값을 유형에 따라 십진수 값으로 변환합니다.

## 카테고리

전환

## 함수 구문

`toDecimal(<parameter>)`

## 매개 변수

| 매개 변수 | 설명 |
|--- |--- |
| 문자열 | 문자열 값을 십진수로 변환 |
| dateTime | 날짜를 밀리초(epoch 밀리초)로 변환 |
| 부울 | 부울 값을 true면 1로, false이면 0으로 변환합니다 |
| 정수 | 소수점(예)으로 변환합니다.: 1.0이 됨 |

## 서명 및 반환된 형식

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

소수점 반환

## 예시

`toDecimal("4.0")`

4.0을 반환합니다.
