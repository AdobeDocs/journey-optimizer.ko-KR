---
product: adobe campaign
title: notEqualIgnoreCase
description: notEqualIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

대/소문자 고려 사항을 무시하고 두 번째 인수 문자열이 들어 있는 첫 번째 인수 문자열이 다른지 확인하십시오.

## 카테고리

문자열

## 함수 구문

`notEqualIgnoreCase(<parameters>)`

## 매개 변수

* string

## 서명 및 반환된 형식

`notEqualIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
