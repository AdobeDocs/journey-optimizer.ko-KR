---
product: journey optimizer
title: toDecimal
description: toDecimal 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: decimal, function, expression, 여정
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# toDecimal {#toDecimal}

인수 유형에 따라 인수 값을 십진수 값으로 변환합니다.

## 카테고리

전환

## 함수 구문

`toDecimal(<parameter>)`

## 매개 변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 문자열 값을 소수로 변환합니다. |
| dateTime | 날짜를 밀리초 단위로 변환(에포크 밀리초) |
| 부울 | true이면 부울 값을 1, false이면 부울 값으로 변환합니다. |
| 정수 | 소수로 변환합니다(예: ).: 1이 1.0이 됨) |

## 서명 및 반환된 유형

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

십진수를 반환합니다.

## 예시

`toDecimal("4.0")`

4.0을 반환합니다
