---
product: journey optimizer
title: toDateOnly
description: toDateOnly 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, 함수, 표현식, 여정
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

인수를 dateOnly 형식 값으로 변환합니다. 데이터 형식에 대한 자세한 내용은 이 [섹션](../expression/data-types.md)을 참조하세요.

## 카테고리

전환

## 함수 구문

`toDateOnly(<parameters>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜를 &quot;YYYY-MM-DD&quot;로 나타내는 문자열 표현(XDM 형식). 또한 ISO-8601 형식을 지원합니다. **전체 날짜** 부분만 고려됩니다([RFC 3339, 섹션 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) 참조). | 문자열 |
| 날짜 시간 | dateTime |
| 시간대 없는 날짜 시간 | dateTimeOnly |
| 에포크의 정수 값(밀리초) | 정수 |

## 서명 및 반환된 유형

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

dateOnly 형식 값을 반환합니다.

## 예시

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

all은 2023-08-18을 나타내는 dateOnly 개체를 반환합니다.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

dateOnly를 반환합니다.
