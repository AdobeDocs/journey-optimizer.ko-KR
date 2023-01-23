---
product: journey optimizer
title: limit
description: 함수 제한에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 제한, 함수, 표현식, 여정
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# limit {#limit}

목록의 첫 번째 또는 마지막 N 요소를 반환합니다.

>[!NOTE]
>
>대상 목록이 listObject인 경우 이 함수는 사용자 지정 작업 표현식에서만 사용할 수 있습니다.

## 카테고리

목록

## 함수 구문

`limit(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 정렬할 목록입니다. listObject의 경우 필드 참조여야 합니다. |
| numberOfItems | 정수 | 지정된 목록에서 반환할 항목 수입니다. |
| firstOrLastItems | 부울 | 이 매개 변수는 선택 사항입니다(기본적으로 true). true이면 첫 번째 항목이 반환됩니다. false는 마지막 항목을 반환합니다. |

## 서명 및 반환된 형식

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

문자열 목록을 반환합니다.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

정수 목록을 반환합니다.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

소수 목록을 반환합니다.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

부울 목록을 반환합니다.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

날짜 목록을 반환합니다.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

시간대를 고려하지 않고 날짜 시간 목록을 반환합니다.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

datetime 목록을 반환합니다.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

지속 시간 목록을 반환합니다.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

개체 목록을 반환합니다.

## 예

`limit(["A", "B", "C", "D", "E"], 3)`

반환 `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

반환 `["C","D","E"]`.
