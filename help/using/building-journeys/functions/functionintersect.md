---
product: journey optimizer
title: intersect
description: 함수 intersect에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: intersect, 함수, 표현식, 여정
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# intersect{#intersect}

두 입력 목록의 공통 값을 반환합니다. 두 목록 중 하나가 null이면 빈 목록을 반환합니다.

## 카테고리

목록

## 함수 구문

`intersect(<parameters>)`

## 매개 변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 1 | list |
| 목록 2 | list |

## 서명 및 반환된 유형

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: list정수
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: list부울

목록을 반환합니다.

## 예시

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

[&quot;sports&quot;, &quot;news&quot;] 반환

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

프로필 속성과 지정된 범주 목록 간의 공통 항목을 반환합니다.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

프로필 속성과 지정된 이벤트 필드 간의 공통 항목을 반환합니다.
