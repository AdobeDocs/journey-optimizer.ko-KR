---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 이벤트 데이터 가져오기 필드
description: journeyStep 이벤트 데이터 가져오기 필드
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 377
ht-degree: 4%

---

# journeyStep 이벤트 데이터 가져오기 필드 {#sharing-fetch-fields}

이 필드 그룹은 journeyStepEvent 및 journeyStepProfileEvent에서 공유됩니다.

단계 처리 중에 필드 그룹에서 N개의 데이터를 가져올 수 있습니다.

## fetchTotalTime {#fetchtotaltime-field}

단계 처리 중 데이터 가져오기에 소요된 총 시간(밀리초)입니다.

유형: long

## fetchTypeInError {#fetchtypeinerror-field}

가져오기 오류가 Adobe Experience Platform 또는 사용자 지정 데이터 소스에 있는지 정의합니다.

유형: 문자열

값:

* aep
* 사용자 정의

## fetchError {#fetcherror-field}

데이터 가져오기를 처리할 때 발생하는 오류 유형.

유형: 문자열

값:

* http
* 캡핑
* 시간 초과
* 오류

## fetchErrorCode {#fetcherrorcode-field}

가져오기 오류 코드. 오류에 HTTP 코드와 같은 코드가 있을 경우 표시됩니다. 예를 들어 actionExecError 가 http 이면 코드 404 는 HTTP 404 오류를 나타냅니다.

유형: 문자열

## fetchOriginError {#fetchoriginerror-field}

두 가지 경우 시간 초과가 발생할 수 있습니다.

* 첫 번째 시도에서 작업이 실행됩니다. 이 경우 실행이 완료되지 않으므로 기본 오류가 없습니다
* 재시도 시: 이 경우 actionExecOrigError/actionExecOrigErrorCode는 재시도 전에 시도에 발생한 오류를 설명합니다.

예를 들어 통합 프로필 서비스에서 데이터를 가져오고 첫 번째 시도에서 HTTP 500 오류가 반환됩니다. 가져오기를 다시 시도하지만 2회 시도 기간이 시간 제한을 초과합니다. 그러면 작업 실행이 시간 초과로 태그가 지정됩니다. 작업 파트는 다음과 같이 표시됩니다.

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

시스템 [!DNL Journey Optimizer]에서 제공한 오류 코드를 쿼리하는 중입니다. 예를 들어 404, 500 등이 될 수 있습니다.

유형: 문자열

## fetchCount {#fetchcount-field}

소스 유형에 관계없이 데이터를 가져오는 횟수.

유형: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Adobe Experience Platform에서 데이터를 가져오는 데 걸린 총 시간(밀리초)입니다. 비고: 이 시간은 엔진이 데이터 보강 서비스로 데이터 보강 이벤트를 보내고 응답을 받은 시간부터 계산됩니다.

유형: long

## fetchPlatformCount {#fetchplatformcount-field}

Adobe Experience Platform에서 데이터를 가져오는 횟수.

유형: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

사용자 정의 데이터를 가져오는 데 걸리는 시간(밀리초)입니다. 비고: 이 시간은 엔진이 데이터 보강 서비스로 데이터 보강 이벤트를 보내고 응답을 받은 시간부터 계산됩니다

유형: long

## fetchCustomCount {#fetchcustomcount-field}

외부 시스템에서 사용자 정의 데이터를 가져오는 횟수.

유형: long
