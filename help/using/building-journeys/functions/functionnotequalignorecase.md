---
product: journey optimizer
title: notEqualIgnoreCase
description: notEqualIgnoreCase 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, 함수, 식, 여정
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

대/소문자 고려 사항을 무시하고 두 번째 인수 문자열이 들어 있는 첫 번째 인수 문자열이 다른지 확인하십시오.

## 카테고리

문자열

## 함수 구문

`notEqualIgnoreCase(<parameters>)`

## 매개 변수

* 문자열

## 서명 및 반환된 형식

`notEqualIgnoreCase(<string>,<string>)`

부울을 반환합니다.

## 예

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
