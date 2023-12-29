---
product: journey optimizer
title: toInteger
description: toInteger 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger, 함수, 표현식, 여정
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

---

# toInteger {#toInteger}

인수 값을 정수로 변환합니다.

## 카테고리

전환

## 함수 구문

`toInteger(<parameter>)`

## 매개 변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 문자열 값을 정수로 변환합니다. |
| dateTime | 날짜를 밀리초 단위로 변환(에포크 밀리초) |
| decimal | 소수 부분을 제거하여 정수로 변환합니다(예: 1.5가 1이 됨). |
| 부울 | true이면 부울 값을 1, false이면 부울 값으로 변환합니다. |

## 서명 및 반환된 유형

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

정수를 반환합니다.

## 예시

`toInteger("4")`

4를 반환합니다.
