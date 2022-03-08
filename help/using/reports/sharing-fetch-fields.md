---
title: journeyStep 이벤트 데이터 가져오기 필드
description: journeyStep 이벤트 데이터 가져오기 필드
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---

# journeyStep 이벤트 데이터 가져오기 필드 {#sharing-fetch-fields}

이 필드 그룹은 journeyStepEvent 및 journeyStepProfileEvent가 공유합니다.

단계 처리 중에 필드 그룹에서 N 데이터를 가져오도록 할 수 있습니다.

## fetchTotalTime {#fetchtotaltime-field}

단계 처리 중 데이터 가져오기에 소요된 총 시간입니다.

유형: 장기간

## fetchTypeInError {#fetchtypeinerror-field}

오류 가져오기가 Adobe Experience Platform 또는 사용자 지정 데이터 소스에 있는지 정의합니다.

유형: 문자열

값:
* aep
* 사용자 지정

## fetchError {#fetcherror-field}

데이터 가져오기가 처리될 때 발생하는 오류 유형입니다.

유형: 문자열

값:
* http
* 최대 가용량
* 시간 초과
* 라는 오류가 표시됩니다

## fetchErrorCode {#fetcherrorcode-field}

가져오기 오류 코드. 오류에 HTTP 코드와 같은 코드가 있을 경우 표시됩니다. 예를 들어 actionExecError가 http인 경우 코드 404는 HTTP 404 오류를 나타냅니다.

유형: 문자열

## fetchOriginError {#fetchoriginerror-field}

시간 초과는 다음 두 가지 경우에 발생할 수 있습니다.

* 첫 번째 시도에서 작업이 실행됩니다. 이 경우 실행이 완료되지 않았으므로 기본 오류가 없습니다
* 다시 시도 시: 이 경우 actionExecOrigError/actionExecOrigErrorCode는 재시도 전에 발생한 오류에 대해 설명합니다.

예를 들어 데이터를 통합 프로필 서비스에서 가져오고 있으며 첫 번째 시도에서 HTTP 500 오류가 반환됩니다. 가져오기가 다시 시도되지만, 두 번의 시도 기간이 시간 제한을 초과합니다. 그런 다음 작업 실행에 시간 제한으로 태그가 지정됩니다. 작업 부분은 다음과 같습니다.

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

유형: 문자열

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

시스템에서 제공한 오류 코드 [!DNL Journey Orchestration] 쿼리 중입니다. 예를 들어 404, 500 등이 될 수 있습니다.

유형: 문자열

## fetchCount {#fetchcount-field}

소스 유형에 관계없이 데이터를 가져오는 횟수입니다.

유형: 장기간

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Adobe Experience Platform에서 데이터를 밀리로 가져오는 데 걸린 총 시간입니다. 참고: 이 시간은 엔진이 데이터 보강 서비스로 데이터 보강 이벤트를 보내고 응답을 받은 시점부터 계산됩니다.

유형: 장기간

## fetchPlatformCount {#fetchplatformcount-field}

Adobe Experience Platform에서 데이터를 가져오는 횟수입니다.

유형: 장기간

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

사용자 지정 데이터를 밀리로 가져오는 데 걸리는 시간입니다. 참고: 이 시간은 엔진이 데이터 보강 이벤트를 데이터 보강 서비스로 보내고 응답을 받는 시점부터 계산됩니다

유형: 장기간

## fetchCustomCount {#fetchcustomcount-field}

외부 시스템에서 사용자 지정 데이터를 가져오는 횟수입니다.

유형: 장기간
