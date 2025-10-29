---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 이벤트 작업 실행 필드
description: journeyStep 이벤트 작업 실행 필드
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

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

## actionOriginEndpoint {#actionoriginendpoint}

작업에 사용된 사용자 지정 작업 끝점의 URI입니다.

유형: 문자열

## actionOriginMethod {#actionoriginmethod}

HTTP 요청(GET 또는 POST)에 사용되는 메서드에 대해 설명합니다.

유형: 문자열

## actionOriginIsMTLS {#actionoriginismtls}

끝점에 대해 MTLS가 활성화되어 있는지 여부를 설명합니다.

유형: 부울

## actionIsProxy {#actionisproxy}

IP 주소 범위가 정의된 HTTP 프록시가 호출에 사용되는지 여부를 설명합니다.

유형: 부울

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

HTTP 요청이 시작되는 타임스탬프를 설명합니다. 다시 시도하는 경우 최종 다시 시도 시도가 시작되는 타임스탬프입니다. 타임스탬프는 UTC 시간대의 ISO8601 형식을 사용합니다.

이 타임스탬프는 일반적으로 프로필이 사용자 지정 작업 노드에 들어간 후 약간 지나거나, 제한이 있는 경우 노드에 들어간 후 상당히 지나야 합니다.

유형: 타임스탬프

## actionExecutionOriginTime {#actionexecutionorigintime}

HTTP 호출의 응답 시간을 설명합니다. 다시 시도하는 경우 최종 다시 시도 시 걸리는 시간입니다. HTTP 요청이 시작된 후부터 서버에서 전체 응답이 반환될 때까지의 시간을 측정합니다. 제한이 있는 경우 대기열에서 대기하는 데 걸린 시간은 제외됩니다.

유형: long

## actionIsThrottled {#actionisthrottled}

끝점에 대해 전송률 조절을 사용할지 여부를 설명합니다.

유형: 부울

## actionWaitTime {#actionwaittime}

스로틀 종단점에 대해 구성된 속도 제한에 도달하고 호출이 큐에 올라가 구성된 속도로 처리되는 경우를 설명합니다. 이 필드는 호출이 실행되기 전에 대기열에서 대기하는 데 걸린 시간을 보고합니다. actionIsThrottled가 true인 경우에만 ==.

유형: long

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
