---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 이벤트 작업 실행 필드
description: journeyStep 이벤트 작업 실행 필드
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---

# journeyStep 이벤트 작업 실행 필드 {#sharing-execution-fields}

이 필드 그룹은 journeyStepEvent 및 journeyStepProfileEvent에서 공유됩니다.

단계에 처리할 작업이 있으면 해당 필드가 이벤트 페이로드에 추가됩니다.

## actionID {#actionid-field}

실행 중인 작업의 ID입니다.

유형: 문자열

## actionName {#actionname-field}

작업 이름. 설정된 이름이 없으면 stepName이 사용됩니다.

유형: 문자열

## actionType {#actionType-field}

작업 유형.

유형: 문자열

## actionParameterized {#actionparameterized-field}

작업이 매개 변수화되는지 여부를 나타냅니다.

유형: 부울

## actionExecutionTime {#actionexecutiontime-field}

현재 작업을 실행하는 데 걸린 시간(밀리초)입니다.

유형: long

`actionExecutionTime` 필드는 큐에 대기 중인 요청이 소요된 시간(제한이 구성되어 있고 속도 제한에 도달한 경우)과 실제 실행 시간(외부 끝점에 대한 네트워크 대기 시간 포함)을 포함하여 작업을 실행하는 데 소요되는 총 시간(밀리초)을 나타냅니다.

`Timestamp` 필드는 작업 실행의 종료 시간을 나타냅니다. 프로필이 사용자 지정 작업 노드에 언제 입력되었는지 확인하려면 `actionExecutionTime`에서 `Timestamp`을(를) 뺍니다.

예를 들어 `Timestamp`이(가) &quot;2025-02-04 09:39:03 UTC&quot;이고 `actionExecutionTime`이(가) 1,813,227ms(~31분)인 경우 프로필이 약 &quot;2025-02-04 09:08:32 UTC&quot;에 노드에 입장했습니다.




## actionExecutionError {#actionexecutionerror-field}

작업을 호출할 때 발생하는 오류 유형입니다.

유형: 문자열

값:

* http
* 캡핑
* timeout
* 오류

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

액션 실행 오류용 코드. 오류에 HTTP 코드와 같은 코드가 있을 경우 표시됩니다.

유형: 문자열

## actionExecutionOriginError {#actionexecutionoriginerror-field}

두 가지 경우 시간 초과가 발생할 수 있습니다.

* 첫 번째 시도에서 작업이 실행됩니다. 이 경우 실행이 완료되지 않으므로 기본 오류가 없습니다
* 재시도 시: 이 경우 actionExecOrigError/actionExecOrigErrorCode는 재시도 전에 시도에 발생한 오류를 설명합니다.

예를 들어 이메일이 전송되고 HTTP 500 오류가 첫 번째 시도에서 반환됩니다. 가져오기를 다시 시도하지만 2회 시도 기간이 시간 제한을 초과합니다. 그러면 작업 실행이 시간 초과로 태그가 지정됩니다. 작업 파트는 다음과 같이 표시됩니다.

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

유형: 문자열

## actionExecutionOriginCode {#actionexecutionorigincode-field}

actionExecOrigError의 오류 코드입니다.

유형: 문자열

## actionBusinessType {#actionbusinesstype-field}

작업 유형을 나타냅니다.

값:

* 기본
   * ACS 이메일
   * ACS SMS
   * ACS 푸시
* 고객
   * 엡실론
   * ...

유형: 문자열

## 배달 작업 ID {#deliveryjobid-field}

배치 여정의 게재 작업 ID에 대해 설명합니다.

유형: 문자열

## 일괄 게재 ID {#batchdeliveryid-field}

배치 여정의 게재 ID에 대해 설명합니다.

유형: 문자열

## fromSegmentTrigger {#fromsegmenttrigger-field}

이는 배치 세그먼트가 대상 여정에서 트리거되는지 여부를 설명합니다.

유형: 부울

## actionSchedulerCount {#actionschedulercount-field}

단계 처리 중 스케줄러 서비스로 전송된 스케줄러 알림 요청 개수입니다.

유형: long
