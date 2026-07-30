---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 과제 API
description: Adobe Journey Optimizer에서 충성도 과제 REST API를 사용하여 도전을 프로그래밍 방식으로 관리하고 프로필 참여 상태를 쿼리하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# 충성도 과제 API {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**이 페이지에서:** 충성도 문제 REST API를 사용하여 프로그래밍 방식으로 문제를 만들고 관리하고 개별 프로필에 대한 문제 참여 상태를 쿼리하고 업데이트하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

## 빠른 액세스 {#quick-access}

충성도 문제에 두 가지 REST API를 사용할 수 있습니다.

* **[충성도 챌린지 메타데이터 API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}** - 프로그래밍 방식으로 도전을 만들고, 검색하고, 업데이트하고, 게시하고, 보관하고, 복제합니다.
* **[충성도 도전 상태 API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}** — 개별 프로필에 대한 도전 참가 상태를 쿼리하고 업데이트합니다.

## 충성도 챌린지 메타데이터 API {#metadata-api}

충성도 문제 메타데이터 API를 사용하면 Journey Optimizer UI 외부의 전체 문제 라이프사이클을 관리할 수 있습니다. 이를 사용하여 과제 운영을 자동화하거나 충성도 프로그램 관리를 고유한 도구 및 워크플로우에 통합합니다. 예를 들어, 문제를 만들고, 게시하고, 보관하고, 필터링 및 정렬로 모든 문제를 검색하거나, 여정 메타데이터 및 캠페인을 포함하여 기존 문제를 복제할 수 있습니다.

➡️ [충성도 챌린지 메타데이터 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## 충성도 챌린지 상태 API {#state-api}

충성도 챌린지 상태 API를 사용하면 프로필 수준에서 챌린지 참여 레코드와 상호 작용할 수 있습니다. 프로필의 현재 참여 상태, 진행 상황 및 작업 완료를 질의하는 데 사용합니다. 예를 들어, 프로필에 대한 모든 참여 레코드를 검색하거나, 과제 내의 특정 작업의 상태를 확인하거나, 하나 이상의 과제에서 프로필을 회수할 수 있습니다.

➡️ [충성도 챌린지 상태 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## 인증 {#authentication}

모든 충성도 과제 API 호출에는 다음 헤더가 필요합니다.

| Header | 설명 |
|---|---|
| `Authorization` | IMS 액세스 토큰의 전달자 토큰 |
| `x-gw-ims-org-id` | IMS 조직 ID |
| `x-api-key` | 클라이언트 ID(API 키) |
| `x-sandbox-name` | 타깃팅할 샌드박스의 이름 |

이러한 자격 증명을 검색하려면 [인증 자습서](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}를 따르십시오.
