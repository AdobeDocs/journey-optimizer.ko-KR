---
product: journey optimizer
title: toDateOnly
description: toDateOnly 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---

# toDateOnly{#toDateOnly}

인수를 dateOnly 형식 값으로 변환합니다. 데이터 유형에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../expression/data-types.md).

## 카테고리

전환

## 함수 구문

`toDateOnly(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| 날짜를 &quot;YYYY-MM-DD&quot;(XDM 형식)로 나타내는 문자열 표현입니다. 또한 ISO-8601 형식을 지원합니다. 전용 **전체 날짜** 부품이 고려됩니다(참조: [RFC 3339, 섹션 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| 날짜 시간 | dateTime |
| 시간대 없는 날짜 시간 | dateTimeOnly |
| epoch의 정수 값(밀리초) | 정수 |

## 서명 및 반환된 형식

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

dateOnly 유형 값을 반환합니다.

## 예시

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

모두 2016-08-18을 나타내는 dateOnly 개체를 반환합니다.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

dateOnly를 반환합니다.
