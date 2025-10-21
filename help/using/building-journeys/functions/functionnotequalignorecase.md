---
product: journey optimizer
title: notEqualIgnoreCase
description: notEqualIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Engineer
level: Experienced
keywords: notEqualIgnoreCase, 함수, 표현식, 여정
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

대/소문자 고려 사항을 무시한 채 첫 번째 인수 문자열과 두 번째 인수 문자열이 다른지 확인합니다.

## 카테고리

문자열

## 함수 구문

`notEqualIgnoreCase(<parameters>)`

## 매개변수

* 문자열

## 서명 및 반환된 유형

`notEqualIgnoreCase(<string>,<string>)`

부울 반환.

## 예

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
