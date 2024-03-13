---
product: journey optimizer
title: toString
description: 함수 toString에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, 함수, 표현식, 여정
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# toString {#toString}

인수 유형에 따라 인수 값을 문자열 값으로 변환합니다. 데이터 유형에 대한 자세한 내용은 [이 페이지](../expression/data-types.md).

## 카테고리

전환

## 함수 구문

`toString(<parameter>)`

## 매개 변수

| 매개변수 | 설명 |
|--- |--- |
| dateTime | 날짜를 UTC 날짜 형식으로 변환 |
| dateTimeOnly | 날짜를 UTC 날짜 형식으로 변환 |
| 지속 시간 | 문자열로 해당 시간(밀리초)으로 변환 |
| 정수 | 값의 문자열 표현으로 변환(1이 &quot;1&quot;이 됨) |
| decimal | 값의 문자열 표현으로 변환(1.5가 &quot;1.5&quot;가 됨) |
| 부울 | true이면 &#39;true&#39;로, false이면 &#39;false&#39;로 부울 값 변환 |

## 서명 및 반환된 유형

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

문자열을 반환합니다.

## 예

`toString(4)`

&quot;4&quot;를 반환합니다.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

지정된 dateOnly 필드(XDM 날짜 필드)의 문자열 표현을 반환합니다(예: &quot;2023-08-18&quot;).

`toString(toDuration(1520))`

&quot;PT1.52S&quot;를 반환합니다.
