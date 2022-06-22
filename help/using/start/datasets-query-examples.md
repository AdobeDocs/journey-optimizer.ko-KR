---
title: 데이터 집합 쿼리 예
description: 데이터 집합 쿼리 예
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 1de18fa479a54c09751324a67793ce50e5657ce3
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# 데이터 집합 사용 사례 {#tracking-datasets}

이 페이지에서는 Adobe Journey Optimizer 데이터 세트 및 관련 사용 사례 목록을 확인할 수 있습니다.

[이메일 추적 경험 이벤트 데이터 세트](../start/datasets-query-examples.md#email-tracking-experience-event-dataset)
[메시지 피드백 이벤트 데이터 세트](../start/datasets-query-examples.md#message-feedback-event-dataset)
[푸시 추적 경험 이벤트 데이터 세트](../start/datasets-query-examples.md#push-tracking-experience-event-dataset)
[여정 단계 이벤트](../start/datasets-query-examples.md#journey-step-event)
[Offer Decisioning 이벤트 데이터 세트](../start/datasets-query-examples.md#ode-decisionevents)
[동의 서비스 데이터 세트](../start/datasets-query-examples.md#consent-service-dataset)
[숨은 참조 피드백 이벤트 데이터 세트](../start/datasets-query-examples.md#bcc-feedback-event-dataset)

## 이메일 추적 경험 이벤트 데이터 세트{#email-tracking-experience-event-dataset}

_인터페이스의 이름: CJM 이메일 추적 경험 이벤트 데이터 세트_

Journey Optimizer에서 이메일 추적 경험 이벤트를 수집하기 위한 시스템 데이터 세트입니다.

관련 스키마는 CJM 이메일 추적 경험 이벤트 스키마입니다.

이 쿼리는 주어진 메시지에 대한 다른 이메일 상호 작용(열기, 클릭) 수를 보여줍니다.

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

이 쿼리는 지정된 여정에 대한 메시지별 다른 이메일 상호 작용(열기, 클릭) 수의 분류를 표시합니다.

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## 메시지 피드백 이벤트 데이터 세트{#message-feedback-event-dataset}

_인터페이스의 이름: CJM 메시지 피드백 이벤트 데이터 세트_

Journey Optimizer에서 전자 메일을 수집하고 애플리케이션 피드백 이벤트를 푸시하기 위한 데이터 집합입니다.

관련 스키마는 CJM 메시지 피드백 이벤트 스키마입니다.

이 쿼리는 주어진 메시지에 대한 다른 이메일 피드백 상태(전송됨, 바운스 등)의 수를 보여줍니다.

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

이 쿼리는 지정된 여정에 대한 메시지별 다른 이메일 피드백 상태(보낸 사람, 바운스 등) 수의 분류를 표시합니다.

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

합계 수준에서 도메인 수준 보고서(최상위 도메인별로 정렬): 도메인 이름, 메시지 전송, 바운스 수

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

이메일은 매일 전송됩니다.

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

특정 이메일 ID가 이메일을 수신했는지 여부를 확인하고 수신하지 않은 경우 오류, 바운스 카테고리, 코드:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

지난 x시간/일 동안 특정 오류, 바운스 카테고리 또는 코드가 있거나 특정 메시지 배달과 연결된 모든 개별 이메일 ID 목록을 찾습니다.

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

합계 수준의 하드 바운스 비율:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

바운스 코드별로 그룹화된 영구 오류:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## 푸시 추적 경험 이벤트 데이터 세트 {#push-tracking-experience-event-dataset}

_인터페이스의 이름: CJM 푸시 추적 경험 이벤트 데이터 세트_

Journey Optimizer에서 푸시할 모바일 추적 경험 이벤트를 수집하기 위한 데이터 집합입니다.

관련 스키마는 CJM 푸시 추적 경험 이벤트 스키마입니다.

쿼리 예:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```
## 여정 단계 이벤트{#journey-step-event}

_내부 이름: 여정 단계 이벤트(시스템 데이터 세트)_

여정에서 단계 이벤트를 수집하기 위한 데이터 집합입니다.

관련 스키마는 Journey Orchestration을 위한 여정 단계 이벤트 스키마입니다.

이 쿼리는 지정된 여정에 대한 작업 레이블별 작업 성공 카운트의 분류를 표시합니다.

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

이 쿼리는 지정된 여정에 대해 nodeId 및 nodeLabel별로 입력한 단계 카운트의 분류를 표시합니다. nodeId는 여기에 포함됩니다. nodeLabel은 다른 여정 노드에 대해 동일할 수 있습니다.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## Offer Decisioning 이벤트 데이터 세트{#ode-decisionevents}

_인터페이스의 이름: ODE DecisionEvents(시스템 데이터 세트)_

사용자에게 오퍼 제안을 수집하기 위한 데이터 세트입니다.

관련 스키마는 ODE DecisionEvents입니다.

이 쿼리는 이전 날짜에 반환된 모든 오퍼를 보여줍니다.

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

이 쿼리는 특정 활동/결정 중 최근 30일 동안 오퍼가 제안된 횟수와 해당 관련 오퍼 우선 순위를 보여줍니다.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## 동의 서비스 데이터 세트{#consent-service-dataset}

_인터페이스의 이름: CJM 동의 서비스 데이터 세트(시스템 데이터 세트)_

Journey Optimizer 동의 서비스에 대한 데이터 집합입니다.

관련 스키마는 CJM 동의 서비스 스키마입니다.

이메일 수신을 동의한 이메일 ID를 나열하는 쿼리입니다.

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

이메일 ID가 입력되는 이메일 ID에 대한 동의 값을 반환하도록 쿼리합니다.

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## 숨은 참조 피드백 이벤트 데이터 세트{#bcc-feedback-event-dataset}

_인터페이스의 이름: AJO BCC 피드백 이벤트 데이터 세트(시스템 데이터 세트)_

숨은 참조 메시지에 대한 정보를 저장하는 데이터 집합입니다.

2일 이내(특정 캠페인의 경우) 모든 BCC 메시지를 쿼리합니다.

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

피드백 데이터 세트로 쿼리하여 수신하지 않은 사용자(모든 바운스 및 지원) 및 특정 메시지에 대한 숨은 참조 항목이 있는 사용자를 표시합니다.

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```
