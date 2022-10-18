---
product: journey optimizer
title: matchRegExp
description: matchRegExp 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# matchRegExp {#matchRegExp}

첫 번째 매개 변수의 문자열이 두 번째 매개 변수의 정규 표현식과 일치하면 true를 반환합니다. 자세한 내용은 [이 페이지](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## 카테고리

문자열

## 함수 구문

`matchRegExp(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 |
|--- |--- |
| string | string |
| regexp | string |

## 서명 및 반환된 형식

`matchRegExp(<string>,<string>)`

부울을 반환합니다.

## 예

`matchRegExp("username@adobe.com", "*adobe")`

true를 반환합니다.
