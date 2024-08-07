---
solution: Journey Optimizer
product: journey optimizer
title: 단계 이벤트 필드 목록
description: 단계 이벤트 필드 목록
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 18%

---

# 단계 이벤트 필드 목록 {#sharing-field-list}

단계 이벤트 필드는 카테고리별로 구성됩니다.

* 디버그 정보 필드
* 여정 필드
* 프로필 필드
* 서비스 이벤트 필드

identityMap 속성의 경우 기본 ID는 기본적으로 &quot;primary = true&quot;로 정의됩니다.

## debugInfo {#debuginfo-field}

| 필드 이름 | 유형 | 설명 |
|---|---|------------|
| requestId | 문자열 | Journey Optimizer에서 요청 흐름을 추적하는 데 사용하는 요청 ID입니다. |

## 여정 {#journey-field}

이 필드 그룹은 journeyStepEvent와 관련하여 여정 스키마에서 사용됩니다. 여기에는 다음 필드가 포함되어 있습니다.

| 필드 이름 | 유형 | 설명 |
|---|---|------------|
| ID | 문자열 | 지정된 여정의 식별자 |
| VersionID | 문자열 | 여정 버전 ID. 이 ID는 여정 ID를 나타냅니다. |
| 이름 | 문자열 | 여정 이름 |
| 설명 | 문자열 | 여정 설명 |
| 버전 | 문자열 | 버전, `major`.`minor`(으)로 표시됨 |

## 프로필 {#profile-field}

이 필드 그룹은 journeyStepEvent에만 해당됩니다. 이 이벤트는 여정과 관련되어 있으며 프로필 ID를 설명하는 identityMap이 없습니다(있는 경우).

journeyStepEvent의 경우 ID와 관련된 필드도 추가해야 합니다.

| 필드 이름 | 유형 | 설명 |
|---|---|------------|
| ID | 문자열 | 프로필 식별자는 여정에서 전송/사용되는 프로필을 식별합니다. 예: foo@adobe.com. |
| 네임스페이스 | 문자열 | 이 필드에서는 여정에 사용된 프로필에서 참조하는 네임스페이스에 대해 설명합니다. 예: 이메일, ECID |

## 서비스 이벤트 {#servicevents-field}

이 mixin에는 프로필 내보내기 작업에 해당하는 모든 필드가 포함되어 있습니다.

| 필드 이름 | 유형 | 설명 |
|---|---|------------|
| ID | 문자열 | 트리거된 대상자 내보내기 작업의 식별자 |
| 상태 | 문자열 | 대상자 내보내기 작업의 상태: 큐에 있음, 시작됨, 완료됨 |
| 내보내기 개수 합계 | 정수 | 대상 내보내기 작업의 가능한 최대 값 |
| exportCountImproved | 정수 | 작업을 통해 내보낸 실제 대상자 수 |
| exportCountFailed | 정수 | 작업을 통해 내보내는 동안 실패한 대상 수 |
| exportSegmentId | 문자열 | 내보내는 대상자의 식별자 |
| eventType | 문자열 | 정보 이벤트의 오류 이벤트인지 여부를 나타내는 이벤트 유형: 정보, 오류 |
| eventCode | 문자열 | 해당 eventType의 이유를 나타내는 오류 코드 |

## stepEvent {#stepevents-field}

이 카테고리에는 원래 단계 이벤트 필드가 포함되어 있습니다. 이 [섹션](../reports/sharing-legacy-fields.md)을 참조하십시오.
