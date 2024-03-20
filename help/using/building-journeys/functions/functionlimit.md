---
product: journey optimizer
title: limit
description: 기능 제한에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: limit, function, expression, 여정
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# limit {#limit}

목록의 첫 번째 또는 마지막 N 요소를 반환합니다.

## 카테고리

목록

## 함수 구문

`limit(<parameters>)`

## 매개 변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 고려할 목록입니다. listObject의 경우 필드 참조여야 합니다. |
| numberOfItems | 정수 | 해당 목록에서 반환할 항목 수. |
| 첫 번째 또는 마지막 항목 | 부울 | 이 매개 변수는 선택 사항입니다(기본값: true). true는 첫 번째 항목을 반환합니다. false는 마지막 항목을 반환합니다. |

## 서명 및 반환된 유형

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

문자열 목록을 반환합니다.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

정수 목록을 반환합니다.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

소수점 목록을 반환합니다.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

부울 목록을 반환합니다.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

날짜 목록을 반환합니다.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

날짜/시간 목록을 반환합니다.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

기간 목록을 반환합니다.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

개체 목록을 반환합니다.

## 예

`limit(["A", "B", "C", "D", "E"], 3)`

반환 `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

반환 `["C","D","E"]`.
