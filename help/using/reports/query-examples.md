---
solution: Journey Optimizer
product: journey optimizer
title: 쿼리 예제
description: 쿼리 예제
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 2%

---

# 쿼리 예제{#query-examples}

이 섹션에는 데이터 레이크에서 여정 단계 이벤트를 쿼리하는 데 일반적으로 사용되는 몇 가지 예가 나와 있습니다.

쿼리에 사용된 필드에 해당 스키마의 관련 값이 있는지 확인하십시오.

**ID, instanceid 및 profileid 간의 차이점은 무엇입니까**

* id: 모든 단계 이벤트 항목에 대해 고유합니다. 서로 다른 두 단계 이벤트는 동일한 ID를 가질 수 없습니다.
* instanceId: instanceID는 여정 실행 내의 프로필에 연결된 모든 단계 이벤트에 대해 동일합니다. 프로필이 여정을 다시 입력하면 다른 instanceId가 사용됩니다. 이 새 instanceId는 다시 입력한 인스턴스의 모든 단계 이벤트(처음부터 끝까지)에 대해 동일합니다.
* profileID: 여정 네임스페이스에 해당하는 프로필의 ID입니다.

## 기본 사용 사례/일반 쿼리 {#common-queries}

**특정 시간대에 여정에 입력한 프로필 수**

이 쿼리는 주어진 시간대에 주어진 여정에 들어간 고유 프로필 수를 제공합니다.

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND _experience.journeyOrchestration.stepEvents.instanceType = 'unitary'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

**특정 시간 동안 특정 여정의 각 노드에서 발생한 오류 수**

_데이터 레이크 쿼리_

```sql
SELECT
_experience.journeyOrchestration.stepEvents.nodeName,
count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersiionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (_experience.journeyOrchestration.stepEvents.actionExecutionError not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginCode not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginError not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchError not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchErrorCode  not NULL
  )
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**특정 시간대에 특정 여정에서 삭제된 이벤트 수**

_데이터 레이크 쿼리_

```sql
SELECT
count(_id) AS NUMBER_OF_EVENTS_DISCARDED
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersiionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

**특정 시간대의 특정 여정에서 특정 프로필에 발생하는 결과**

_데이터 레이크 쿼리_

이 쿼리는 지정된 시간 동안 지정된 프로필과 여정에 대한 모든 단계 이벤트와 서비스 이벤트를 시간 순서대로 반환합니다.

```sql
SELECT
timestamp,
_experience.journeyOrchestration.stepEvents.journeyVersionID,
_experience.journeyOrchestration.stepEvents.profileID,
_experience.journeyOrchestration.stepEvents.nodeName,
_experience.journeyOrchestration.stepEvents.journeyNodeProcessed,
_experience.journeyOrchestration.serviceType,
to_json(_experience.journeyOrchestration.profile),
to_json(_experience.journeyOrchestration.serviceEvents)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (
    _experience.journeyOrchestration.stepEvents.profileID='<profileID>'
    OR _experience.journeyOrchestration.profile.ID='<profileID>'
  );
ORDER BY timestamp;
```

**두 노드 사이에 경과된 시간**

예를 들어 이러한 쿼리는 대기 활동에 소요된 시간을 예상하는 데 사용할 수 있습니다. 대기 활동이 올바르게 구성되었는지 확인할 수 있습니다.

_데이터 레이크 쿼리_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    T1.INSTANCE_ID AS INSTANCE_ID,
    T1.NODE_NAME AS START_NODE_NAME,
    T2.NODE_NAME AS END_NODE_NAME,
    DATEDIFF(millisecond,T1.TS_START,T2.TS_END) AS ELAPSED_TIME_MS
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

_데이터 레이크 쿼리_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    AVG(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS AVERAGE_ELAPSED_TIME,
    MIN(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MIN_ELAPSED_TIME,
    MAX(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MAX_ELAPSED_TIME
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

**serviceEvent 세부 사항을 확인하는 방법**

여정 단계 이벤트 데이터 세트에는 모든 stepEvents 및 serviceEvents가 포함되어 있습니다. stepEvents는 활동(이벤트, 작업 등)과 관련하여 보고에 사용됩니다. 여정 내 프로필 개수 serviceEvents는 동일한 데이터 세트에 저장되며 디버깅 목적을 위한 추가 정보(예: 경험 이벤트가 삭제되는 이유)를 나타냅니다.

다음은 serviceEvent의 세부 사항을 확인하는 쿼리의 예입니다.

_데이터 레이크 쿼리_

```sql
SELECT

     _experience.journeyOrchestration.profile.ID, 
     _experience.journeyOrchestration.journey.versionID, 
     to_json(_experience.journeyOrchestration.serviceEvents) 

FROM journey_step_event 

WHERE _experience.journeyOrchestration.serviceType is not null;
```

## 메시지/작업 오류 {#message-action-errors}

**여정에서 발생한 각 오류 목록**

이 쿼리를 사용하면 메시지/작업을 실행하는 동안 여정에서 발생하는 각 오류를 나열할 수 있습니다.

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName=<'message-name'>
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

_예_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName='Message - 100KB Email with Gateway and Kafkav2'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

이 쿼리는 여정에서 작업을 실행하는 동안 발생한 다른 모든 오류와 발생한 횟수를 반환합니다.

## 프로필 기반 쿼리 {#profile-based-queries}

**프로필이 특정 여정을 입력했는지 확인**

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_예_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = 'ec9efdd0-8a7c-4d7a-a765-b2cad659fa4e' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

결과는 0보다 커야 합니다. 이 쿼리는 프로필이 여정을 입력한 정확한 횟수를 반환합니다.

**프로필에 특정 메시지가 전송되었는지 확인**

방법 1: 메시지 이름이 여정에서 고유하지 않은 경우(여러 위치에서 사용됨).

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='<NodeId in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_예_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='17ae65a1-02dd-439d-b54e-b56a78520eba' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

결과는 0보다 커야 합니다. 이 쿼리는 메시지 작업이 여정 측에서 성공적으로 실행되었는지 여부만 알려줍니다.

방법 2: 메시지 이름이 여정에서 고유한 경우.

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeName='<NodeName in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_예_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='Message- 100KB Email' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

이 쿼리는 선택한 프로필에 대해 호출된 카운트와 함께 모든 메시지 목록을 반환합니다.

**지난 30일 동안 프로필에서 받은 모든 메시지 찾기**

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

_예_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

이 쿼리는 선택한 프로필에 대해 호출된 카운트와 함께 모든 메시지 목록을 반환합니다.

**지난 30일 동안 프로필이 입력한 모든 여정 찾기**

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

_예_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

쿼리는 모든 여정 이름 목록과 함께 쿼리된 프로필이 여정을 입력한 횟수를 반환합니다.

**매일 여정에 적합한 프로필 수**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_예_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

정의된 기간 동안 매일 여정에 입력한 프로필 수가 다시 표시됩니다. 프로필이 여러 ID를 통해 입력된 경우 두 번 계산됩니다. 재입력이 활성화된 경우 다른 날에 여정에 다시 입력한 경우 다른 날에 프로필 수가 중복될 수 있습니다.

## 세그먼트 읽기 관련 쿼리 {#read-segment-queries}

**세그먼트 내보내기 작업을 완료하는 데 걸린 시간**

_데이터 레이크 쿼리_

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

_예_

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

쿼리는 세그먼트 내보내기 작업이 큐에 추가된 시간과 최종적으로 종료되는 시간 사이의 시간 차이를 분 단위로 반환합니다.

**중복 항목이므로 여정에서 버린 프로필 수입니다.**

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

_예_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

쿼리는 여정이 중복되었기 때문에 삭제한 모든 프로필 ID를 반환합니다.

**잘못된 네임스페이스로 인해 여정에서 삭제된 프로필 수입니다.**

_데이터 레이크 쿼리_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

_예_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

이 쿼리는 잘못된 네임스페이스가 있거나 해당 네임스페이스에 대한 ID가 없기 때문에 여정에서 삭제된 모든 프로필 ID를 반환합니다.

**ID 맵이 없어 여정에서 삭제된 프로필 수입니다.**

_데이터 레이크 쿼리_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

_예_

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

이 쿼리는 ID 맵이 누락되었기 때문에 여정이 삭제한 모든 프로필 ID를 반환합니다.

**여정이 테스트 여정에 있고 프로필이 테스트 프로필이 아니기 때문에 테스트 노드에서 삭제된 프로필 수입니다**

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

_예_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

내보내기 작업이 테스트 모드에서 실행되었지만 프로필에 testProfile 특성이 true로 설정되지 않았으므로 여정에서 삭제된 모든 프로필 ID가 쿼리에서 반환됩니다.

**내부 오류로 인해 여정에서 삭제된 프로필 수입니다**

_데이터 레이크 쿼리_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

_예_

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

이 쿼리는 일부 내부 오류로 인해 여정에서 삭제된 모든 프로필 ID를 반환합니다.

**주어진 여정 버전에 대한 세그먼트 읽기 개요**

_데이터 레이크 쿼리_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator'
```

지정된 여정 버전과 관련된 모든 서비스 이벤트를 반환합니다. 다음과 같은 작업 체인을 따를 수 있습니다.

* 주제 만들기
* 내보내기 작업 생성
* 내보내기 작업 종료(내보낸 프로필에 대한 지표 사용)
* 작업자 처리 종료

또한 다음과 같은 문제도 감지할 수 있습니다.

* 주제 또는 내보내기 작업 생성 오류(세그먼트 내보내기 API 호출에 대한 시간 초과 포함)
* 중단 가능한 내보내기 작업(주어진 여정 버전에 대해 내보내기 작업 종료와 관련된 이벤트가 없는 경우)
* 작업자 문제, 내보내기 작업 종료 이벤트를 수신했지만 작업자 처리 종료 이벤트가 없는 경우

중요: 이 쿼리에서 반환된 이벤트가 없는 경우 다음 이유 중 하나가 원인일 수 있습니다.

* 여정 버전이 일정에 도달하지 않았습니다.
* 여정 버전이 orchestrator를 호출하여 내보내기 작업을 트리거해야 하는 경우 업그레이드 플로우에서 문제가 발생했습니다. 여정 배포 문제, 비즈니스 이벤트 또는 스케줄러 문제.

**지정된 여정 버전에 대한 세그먼트 읽기 오류 가져오기**

_데이터 레이크 쿼리_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'ERROR_TOPIC_CREATION',
        'ERROR_EXPORTJOB_APICALL',
        'ERROR_EXPORTJOB_APICALL_TIMEOUT',
        'ERROR_EXPORTJOB_FAILED'
    )
```

**내보내기 작업 처리 상태 가져오기**

_데이터 레이크 쿼리_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT 
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'INFO_EXPORTJOB_SUCCEEDED',
        'ERROR_EXPORTJOB_FAILED'
    )
```

레코드가 반환되지 않으면 다음 중 하나를 의미합니다.

* 주제 또는 내보내기 작업을 만드는 동안 오류가 발생했습니다.
* 내보내기 작업이 아직 실행 중입니다.

**각 내보내기 작업에 대한 디스카드 및 내보내기 작업 지표를 포함하여 내보낸 프로필에 대한 지표를 가져옵니다**

_데이터 레이크 쿼리_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
 
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
  
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.EXPORTJOB_ID = T2.EXPORTJOB_ID
```

**모든 내보내기 작업에서 집계된 지표(세그먼트 내보내기 작업 및 카드) 가져오기**

_데이터 레이크 쿼리_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.journey.versionID
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
          _experience.journeyOrchestration.journey.versionID
 
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.JOURNEYVERSION_ID = T2.JOURNEYVERSION_ID
```

이 쿼리는 이전 쿼리와 다릅니다.

지정된 여정 버전에 대한 전체 지표를 반환합니다(반복 여정의 경우 비즈니스 이벤트가 항목 재사용을 활용하여 트리거됨).

## 세그먼트 자격 관련 쿼리 {#segment-qualification-queries}

**구성된 것과 다른 세그먼트 실현으로 인해 프로필이 삭제되었습니다.**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

_예_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = 'a868f3c9-4888-46ac-a274-94cdf1c4159d' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

이 쿼리는 잘못된 세그먼트 실현으로 인해 여정 버전에서 삭제된 모든 프로필 ID를 반환합니다.

**특정 프로필에 대한 다른 이유로 삭제된 세그먼트 자격 이벤트**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = '<profile-id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_예_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

이 쿼리는 프로필에 대한 다른 이유로 인해 삭제된 모든 이벤트(외부 이벤트/세그먼트 자격 이벤트)를 반환합니다.

## 이벤트 기반 쿼리 {#event-based-queries}

**여정에 대한 비즈니스 이벤트가 수신되었는지 확인**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.nodeName = '<node-name-corresponding-to-business-event>' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '<last x hours>' hour)
```

_예_

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = 'b1093bd4-11f3-44cc-961e-33925cc58e18' AND
_experience.journeyOrchestration.stepEvents.nodeName = 'TEST_MLTrainingSession' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '6' hour)
```

**관련 여정을 찾을 수 없어 프로필의 외부 이벤트가 삭제되었는지 확인**

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '<eventId>' AND
_experience.journeyOrchestration.profile.ID = '<profileId>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

_예_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '515bff852185e434ca5c83bcfc4f24626b1545ca615659fc4cfff91626ce61a6' AND
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

**다른 이유로 인해 프로필의 외부 이벤트가 무시되었는지 확인**

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='<eventID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_예_

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='81c51be978d8bdf9ef497076b3e12b14533615522ecea9f5080a81c736491656' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

**errorCode로 stateMachine에서 삭제한 모든 이벤트 수를 확인합니다.**

_데이터 레이크 쿼리_

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

_예_

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

**재입력이 허용되지 않아 삭제된 모든 이벤트 확인**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

_예_

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

## 일반적인 여정 기반 쿼리 {#journey-based-queries}

**일별 활성 여정 수**

_데이터 레이크 쿼리_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_예_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

쿼리는 정의된 기간 동안 매일 트리거된 고유한 여정 수를 반환합니다. 여러 날에 트리거되는 단일 여정은 하루에 한 번 계산됩니다.

## 여정 인스턴스의 쿼리 {#journey-instances-queries}

**특정 시간 동안 특정 상태에 있는 프로필 수**

_데이터 레이크 쿼리_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = '<specific node name>' AND
        <filter on time for profile in specific node>
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in (<list of next node names from the specific node>)
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'<date pattern>') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_예_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = 'slack_bso_tests - test1' AND
        T1.TS > (now() - interval '18 hour')
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in ('slack_bso_tests - test2')
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

**특정 기간에 여정을 종료한 프로필 수입니다.**

_데이터 레이크 쿼리_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_예_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

**노드/상태에서 특정 기간 동안 여정을 종료한 프로필 수입니다.**

_데이터 레이크 쿼리_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

_예_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```
