---
product: journey optimizer
title: distinctWithNull
description: distinctWithNull 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, 함수, 식, 여정
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---

# distinctWithNull {#distinctWithNull}

지정된 목록의 고유 값 또는 개체를 반환합니다. 목록에 Null 항목이 하나 이상 있으면 반환된 목록에 Null 항목이 표시됩니다.

## 카테고리

목록

## 함수 구문

`distinctWithNull(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 선택 사항이며 listObject에만 사용됩니다. 매개 변수를 제공하지 않으면 모든 속성에 값이 동일한 경우 개체가 중복으로 간주됩니다. 그렇지 않으면 지정된 속성에 값이 동일한 경우 개체가 중복으로 간주됩니다. |

## 서명 및 반환된 형식

`distinctWithNull(<listInteger>)`

정수 목록을 반환합니다.

`distinctWithNull(<listDecimal>)`

소수 목록을 반환합니다.

`distinctWithNull(<listString>)`

문자열 목록을 반환합니다.

`distinctWithNull(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜 시간 목록을 반환합니다.

`distinctWithNull(<listDateTime>)`

datetime 목록을 반환합니다.

`distinctWithNull(<listDateOnly>)`

날짜 목록을 반환합니다.

`distinctWithNull(<listBoolean>)`

부울 목록을 반환합니다.

`distinctWithNull(<listDuration>)`

지속 시간 목록을 반환합니다.

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

개체 목록을 반환합니다.

## 예시

`distinctWithNull([10,2,10,null])`

반환 [10, 2, null]
