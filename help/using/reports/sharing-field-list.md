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
source-git-commit: f9102c10aa58be0e1a7280aa53fd97b3f792b9e9
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 10%

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
| eventType | 문자열 | 오류 이벤트인지 정보 이벤트인지를 나타내는 이벤트 유형: 정보, 오류 |
| eventCode | 문자열 | 해당 eventType의 이유를 나타내는 오류 코드 |

이 섹션[에서 eventTypes ](#discarded-events)에 대해 자세히 알아보세요.

## stepEvent {#stepevents-field}

이 카테고리에는 원래 단계 이벤트 필드가 포함되어 있습니다. 이 [섹션](../reports/sharing-legacy-fields.md)을 참조하십시오.


## 여정 단계 이벤트에서 삭제된 이벤트 유형 문제 해결  {#discarded-events}

`eventCode = 'discard'`이(가) 있는 레코드에 대해 여정 단계 이벤트를 쿼리하는 경우 여러 eventTypes가 발생할 수 있습니다.

다음은 가장 자주 삭제되는 `eventTypes`에 대한 정의, 일반적인 원인 및 문제 해결 단계입니다.

* EXTERNAL_KEY_COMPUTATION_ERROR: 시스템이 이벤트 데이터에서 고객에 대한 고유 식별자(외부 키)를 계산할 수 없습니다.

|---|---|
| **일반적인 원인** | 이벤트 페이로드에 누락되었거나 잘못된 고객 식별자(예: 이메일, 고객 ID). |
| **문제 해결** | 이벤트 구성에 필요한 식별자가 있는지 확인하고 이벤트 데이터가 완전하고 형식이 올바른지 확인합니다. |

* NO_INTEREST_SEGMENTS_FOR_SEGMENTMEMBERSHIP_EVENT: 여정 자격 이벤트를 받았지만 이 여정에 응답하도록 구성된 세그먼트가 없습니다.


|---|---|
| **일반적인 원인** | 세그먼트를 트리거로 사용하는 여정이 없거나, 여정이 초안/중단됨 상태이거나, 세그먼트 ID가 일치하지 않습니다. |
| **문제 해결** | 최소 1개의 세그먼트가 라이브이고 여정에 대해 구성되어 있는지 확인하고 세그먼트 ID를 확인하십시오. |

### 여정_인스턴스_ID_NOT_CREATE: 시스템이 고객에 대한 여정 인스턴스를 생성하지 못했습니다.

|---|---|
| **일반적인 원인** | 중복 이벤트, 높은 이벤트 볼륨, 시스템 리소스 제한. |
| **문제 해결** | 중복 제거 구현, 트래픽 급증 방지, 여정 설계 최적화, 영구적 인 경우 지원 센터에 문의 |

### EVENT_WITH_NO_EVENT: 여정을 받았지만 이 이벤트에 응답하도록 구성된 활성 여정이 없습니다.

|---|---|
| **일반적인 원인** | 여정 이름/ID 불일치, 이벤트가 게시되지 않음, 잘못된 샌드박스/조직, 테스트 모드/프로필 불일치. |
| **문제 해결** | 이벤트 및 여정 구성을 확인하고 여정 상태를 확인한 다음 디버깅 도구를 사용합니다. |

일시 중지된 여정에서 발생하는 폐기물의 경우:

* **PAUSED_DISPATCHER_VERSION**: 여정 시작 지점에서 발생한 여정을 버립니다.
* **여정_IN_PAUSED_STATE**: 프로필이 여정 상태일 때 발생한 항목을 삭제합니다.

[여정 일시 중지](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys)에서 이러한 이벤트와 문제를 해결하는 방법에 대해 자세히 알아보세요.

## 추가 리소스

* [데이터 집합 쿼리 샘플 - 여정 단계 이벤트](../data/datasets-query-examples.md#journey-step-event).
* [쿼리의 예 - 이벤트 기반 쿼리](query-examples.md#event-based-queries).
* [기본 제공 스키마 사전](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=ko)

