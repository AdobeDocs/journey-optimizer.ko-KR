---
product: journey optimizer
title: distinct
description: 고유한 기능에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct, 함수, 표현식, 여정
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---

# distinct {#distinct}

지정된 목록의 고유 값 또는 개체를 반환합니다. Null 항목은 무시됩니다.

>[!NOTE]
>
>대상 목록이 listObject인 경우 이 함수는 사용자 지정 작업 표현식에서만 사용할 수 있습니다.

## 카테고리

목록

## 함수 구문

`distinct(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 선택 사항이며 listObject에만 사용됩니다. 매개 변수를 제공하지 않으면 모든 속성에 값이 동일한 경우 개체가 중복으로 간주됩니다. 그렇지 않으면 지정된 속성에 값이 동일한 경우 개체가 중복으로 간주됩니다. |

## 서명 및 반환된 형식

`distinct(<listInteger>)`

정수 목록을 반환합니다.

`distinct(<listDecimal>)`

소수 목록을 반환합니다.

`distinct(<listString>)`

문자열 목록을 반환합니다.

`distinct(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜 시간 목록을 반환합니다.

`distinct(<listDateTime>)`

datetime 목록을 반환합니다.

`distinct(<listDateOnly>)`

날짜 목록을 반환합니다.

`distinct(<listBoolean>)`

부울 목록을 반환합니다.

`distinct(<listDuration>)`

지속 시간 목록을 반환합니다.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

개체 목록을 반환합니다.


## 예시

`distinct([10,2,10,null])`

반환 `[10, 2]`.
