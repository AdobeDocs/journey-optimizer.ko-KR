---
product: journey optimizer
title: toBool
description: toBool 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool, function, expression, 여정
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# toBool {#toBool}

인수 유형에 따라 인수 값을 부울 값으로 변환합니다.

* From string: 문자열 값을 부울로 변환하고 문자열 값이 &quot;true&quot;이면 &quot;true&quot;를 반환하고 그렇지 않으면 false를 반환합니다
* 숫자에서: 숫자 값이 0이 아니면 true이고, 그렇지 않으면 false입니다

## 카테고리

전환

## 함수 구문

`toBool(<parameter>)`

## 매개 변수

* decimal
* 부울
* 문자열
* 정수

## 서명 및 반환된 유형

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

부울 반환.

## 예시

`toBool("true")`

`toBool(1)`

true를 반환합니다.

`toBool("this is not a boolean")`

false를 반환합니다.
