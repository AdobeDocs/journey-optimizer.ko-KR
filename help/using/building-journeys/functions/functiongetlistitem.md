---
product: journey optimizer
title: getListItem
description: gstListItem 함수에 대해 알아봅니다
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# getListItem {#gestListItem}

지정된 인덱스에서 목록의 항목을 반환합니다.

## 카테고리

목록

## 함수 구문

`getListItem(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| 색인 | 정수 |

## 서명 및 반환된 유형

`getListItem(<listInteger>,<index>)`

정수를 반환합니다.

`getListItem(<listDecimal>,<index>)`

소수점 반환

`getListItem(<listString>,<index>)`

문자열을 반환합니다.

`getListItem(<listDateTimeOnly>,<index>)`

시간대를 고려하지 않고 datetime을 반환합니다.

`getListItem(<listDateTime>,<index>)`

datetime을 반환합니다.

`getListItem(<listDateOnly>,<index>)`

날짜 목록을 반환합니다.

`getListItem(<listBoolean>,<index>)`

부울을 반환합니다.

`getListItem(<listDuration>,<index>)`

지속 시간을 반환합니다.

## 예

`getListItem([10, 2, 3], 1)`

&quot;2&quot;를 반환합니다.

`getListItem(["A", "B", "C"], 2)`
&quot;C&quot;를 반환합니다.

값이 있는 이벤트 필드 &#39;event.appVersion&#39;의 예: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

반환 `["20", "45", "2", "3434"]`

`getListItem(split(@{event.appVersion}, "\\."), 0)`

&quot;20&quot;을 반환합니다.
