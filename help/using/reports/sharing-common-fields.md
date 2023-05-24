---
solution: Journey Optimizer
product: journey optimizer
title: journeysteps 이벤트 공통 필드
description: journeysteps 이벤트 공통 필드
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 9%

---

# journeysteps 이벤트 공통 필드 {#sharing-common-fields}

이 필드 그룹은 journeyStepEvent 및 journeyStepProfileEvent에서 공유됩니다.

이는 다음과 같은 일반적인 XDM 필드입니다. [!DNL Journey Optimizer] 는 Adobe Experience Platform으로 전송합니다. 여정에서 처리되는 모든 단계에 대해 공통 필드가 전송됩니다. 사용자 지정 작업 및 보강에는 더 구체적인 필드가 사용됩니다.

이러한 필드 중 일부는 특정 처리 패턴(작업 실행, 데이터 가져오기 등)에서만 사용할 수 있습니다 이벤트 크기를 제한하기 위해

## 입구 {#entrance-field}

사용자가 여정을 입력했는지 여부를 나타냅니다. 만약 존재하지 않는다면, 우리는 값이 false라고 가정한다.

유형: 부울

값: true/false

## 재진입 {#reentrance-field}

사용자가 동일한 인스턴스로 여정을 다시 입력했는지 여부를 나타냅니다. 만약 존재하지 않는다면, 우리는 값이 false라고 가정한다.

유형: 부울

값: true/false

## instanceEnd {#instance-ended-field}

인스턴스가 종료되었는지 여부를 나타냅니다.

유형: 부울

## eventID {#eventid-field}

처리 중인 이벤트 ID입니다(단계 처리 중). 이벤트가 외부 이벤트인 경우 값은 해당 eventId입니다. 이벤트가 내부 이벤트인 경우 값은 내부 eventId(예: scheduledNotificationReceived, executedAction 등)입니다.

유형: 문자열

## nodeID {#nodeid-field}

클라이언트 노드 ID(캔버스에서).

유형: 문자열

## stepID {#stepdid-field}

현재 처리 중인 단계에 대한 고유 ID.

유형: 문자열

## stepName {#stepname-field}

현재 처리 중인 단계의 이름입니다.

유형: 문자열

## stepType {#steptype-field}

단계 유형.

유형: 문자열

가능한 값:

* 조건
* 작업
* 예약
* 타이머

## stepStatus {#stepstatus-field}

단계가 처리되었으며(및 단계 이벤트가 실행됨) 단계 상태를 나타내는 단계 상태.

유형: 문자열

상태는 다음과 같을 수 있습니다.

* 종료: 단계에 전환이 없으며 처리가 정상적으로 종료되었습니다.
* error: 단계 처리에서 오류가 발생했습니다.
* 전환: 단계가 이벤트가 다른 단계로 전환되기를 기다리고 있습니다.
* 제한됨: 작업 또는 데이터 보강 중에 발생한 최대 가용량 오류에서 단계가 실패했습니다.
* 시간 초과: 작업 또는 데이터 보강 중에 발생한 시간 초과 오류로 인해 단계가 실패했습니다.
* instanceTimedout: 인스턴스가 시간 제한에 도달했기 때문에 단계가 처리를 중지했습니다.

## journeyID {#journeyid-field}

여정 ID.

유형: 문자열

## 여정 버전 ID {#journeyversionid-field}

여정 버전 ID. 이 ID는 journeyStepEvent의 경우 여정에 대한 ID 참조를 나타냅니다.

유형: 문자열

## 여정 버전 이름 {#journeyversionname-field}

여정 버전 이름.

유형: 문자열

## journeyVersion {#journeyversion-field}

여정 버전.

유형: 문자열

## instanceID {#instanceid-field}

여정 인스턴스의 내부 ID.

유형: 문자열

## externalKey {#externalkey-field}

처리할 이벤트에서 외부 키가 추출되었습니다.

유형: 문자열

## 상위 단계 ID {#parenstepid-field}

인스턴스에서 현재 처리된 단계의 상위 단계 ID.

유형: 문자열

## parentStepName {#parentstepname-field}

현재 단계 상위의 단계 이름입니다.

유형: 문자열

## parentTransitionID {#parenttransitionid-field}

인스턴스를 처리된 단계로 가져온 전환의 ID입니다.

유형: 문자열

## parentTransitionName {#parenttransitionname-field}

인스턴스를 처리된 단계로 가져온 전환의 이름입니다.

유형: 문자열

## inTest {#intest-field}

이 여정이 테스트 모드인지 여부를 나타냅니다.

유형: 부울

## processingTime {#processingtime-field}

인스턴스 단계 시작부터 처리 종료까지의 총 시간(밀리초).

유형: long

## instanceType {#instancetype-field}

인스턴스 유형이 일괄 처리이거나 단일 인스턴스인 경우 이를 나타냅니다.

유형: 문자열

값: 배치/단일

## recurrenceIndex {#recurrenceindex-field}

여정이 일괄 처리이고 반복인 경우 반복의 색인입니다(첫 번째 실행에는 recurrenceIndex = 1).

유형: long

## isBatchToUnitary {#isbatchtounitary-field}

이 단일 인스턴스가 일괄 처리 인스턴스에서 트리거되었는지 여부를 나타냅니다.

유형: 부울

## batchExternalKey {#batchexternalkey-field}

일괄 처리 이벤트에 대한 외부 키.

유형: 문자열

## 일괄 처리 인스턴스 ID {#batchinstanceid-field}

배치 인스턴스 ID입니다.

유형: 문자열

## batchUnitaryBranchID {#batchunitarybranchid-field}

인스턴스가 배치 인스턴스에서 트리거된 경우 단일 분기 ID입니다.

유형: 문자열
