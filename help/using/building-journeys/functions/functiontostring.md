---
product: adobe campaign
title: toString
description: toString 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# toString {#toString}

인수 값을 유형에 따라 문자열 값으로 변환합니다. 데이터 유형에 대한 자세한 내용은 [이 페이지](../expression/data-types.md).

## 카테고리

전환

## 함수 구문

`toString(<parameter>)`

## 매개 변수

| 매개 변수 | 설명 |
|--- |--- |
| dateTime | 날짜를 UTC 날짜 형식으로 변환 |
| dateTimeOnly | 날짜를 UTC 날짜 형식으로 변환 |
| 기간 | 문자열로 해당 밀리초 수로 변환 |
| 시간대 | 표준 시간대 id 문자열 표시(JODA id)로 변환 |
| 정수 | 값의 문자열 표현으로 변환(1은 &quot;1&quot;이 됨) |
| 십진수 | 값의 문자열 표현으로 변환(1.5는 &quot;1.5&quot;가 됨) |
| 부울 | 부울 값을 true이면 &#39;true&#39;로, false이면 &#39;false&#39;로 변환합니다 |

## 서명 및 반환된 유형

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<timeZone>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

문자열을 반환합니다.

## 예

`toString(4)`

&quot;4&quot;를 반환합니다.
