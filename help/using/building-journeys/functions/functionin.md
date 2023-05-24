---
product: journey optimizer
title: in
description: 의 기능에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: in, 함수, 표현식, 여정
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 18%

---

# in {#in}

첫 번째 인수 값이 목록에 있는지 확인합니다. 각 인수 값에 대해 같음 을 통해 확인이 수행됩니다. 인수 값이 발견되면 true를 반환하고, 그렇지 않으면 false를 반환합니다.

의 유형입니다. `<expression>` 은(는) 목록의 항목과 일치해야 합니다. 미리 알림으로 목록의 항목 유형은 서로 일치해야 합니다.

## 카테고리

목록

## 함수 구문

`in(<parameters>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 부울 | 부울 |
| 정수 | 정수 |
| 10진수 | 10진수 |
| 기간 | 기간 |
| DateTime | DateTime |
| 날짜/시간만 | 날짜/시간만 |
| 목록 | listString |
| 목록 | list부울 |
| 목록 | list정수 |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

## 서명 및 반환된 유형

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

부울 반환.

## 예

`in(4,[4,5,3,4])`

true를 반환합니다.

`in(8,[4,5,3,4])`

false를 반환합니다.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
