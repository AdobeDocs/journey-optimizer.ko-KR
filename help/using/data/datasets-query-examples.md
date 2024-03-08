---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 세트 쿼리 예
description: 데이터 세트 쿼리 예
feature: Journeys, Reporting, Use Cases, Datasets, Data Management
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 데이터 세트, 최적화 도구, 사용 사례
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: b3cb1a06b200961030ff22c2ee6f42173f83606f
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 2%

---

# 데이터 세트 사용 사례 {#tracking-datasets}

이 페이지에서는 Adobe Journey Optimizer 데이터 세트 목록 및 관련 사용 사례를 확인할 수 있습니다.

[이메일 추적 경험 이벤트 데이터 세트](#email-tracking-experience-event-dataset)
[메시지 피드백 이벤트 데이터 세트](#message-feedback-event-dataset)
[푸시 추적 경험 이벤트 데이터 세트](#push-tracking-experience-event-dataset)
[여정 단계 이벤트](#journey-step-event)
[의사 결정 이벤트 데이터 세트](#ode-decisionevents)
[BCC 피드백 이벤트 데이터 세트](#bcc-feedback-event-dataset)
[엔티티 데이터 세트](#entity-dataset)

각 스키마의 전체 필드와 속성 목록을 보려면 [Journey Optimizer 스키마 사전](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=ko){target="_blank"}을 찾아봅니다.

## 이메일 추적 경험 이벤트 데이터 세트{#email-tracking-experience-event-dataset}

_인터페이스의 이름 : CJM 이메일 추적 경험 이벤트 데이터 세트_

Journey Optimizer에서 이메일 추적 경험 이벤트를 수집하기 위한 시스템 데이터 세트입니다.

관련 스키마는 CJM 이메일 추적 경험 이벤트 스키마입니다.

이 쿼리는 지정된 메시지에 대한 다양한 이메일 상호 작용(열기, 클릭) 수를 보여 줍니다.

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

이 쿼리는 주어진 여정에 대해 메시지별로 서로 다른 이메일 상호 작용(열기, 클릭) 수의 분류를 보여줍니다.

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

Journey Optimizer에서 이메일 및 푸시 애플리케이션 피드백 이벤트를 수집하기 위한 데이터 세트입니다.

관련 스키마는 CJM 메시지 피드백 이벤트 스키마입니다.

이 쿼리는 지정된 메시지에 대한 다른 이메일 피드백 상태(보냄, 바운스 등)의 수를 보여줍니다.

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

이 쿼리는 지정된 여정에 대해 메시지별로 서로 다른 이메일 피드백 상태(보냄, 바운스 등)의 수 분류를 보여줍니다.

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

집계 수준에서 도메인 수준 보고서(최상위 도메인별로 정렬됨): 도메인 이름, 보낸 메시지, 반송

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

이메일은 매일 전송됩니다.

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

특정 이메일 ID가 이메일을 받았는지 여부를 확인하고, 받지 못했을 경우 오류, 반송 범주, 코드를 확인합니다.

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

지난 x시간/일 동안 특정 오류, 바운스 카테고리 또는 코드가 있거나 특정 메시지 게재와 연결된 모든 개별 이메일 ID 목록을 찾습니다.

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

집계 수준의 하드 바운스 비율:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

바운스 코드별로 그룹화된 영구 오류:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

### ISP 중단 후 격리된 주소 확인{#isp-outage-query}

인터넷 서비스 공급자(ISP) 가동이 중단된 경우 일정 기간 동안 특정 도메인에 대한 바운스 수(격리됨)로 잘못 매핑된 이메일 주소를 식별해야 합니다. 이러한 주소를 얻으려면 다음 쿼리를 사용하십시오.

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM cjm_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

여기서 날짜 형식은 다음과 같습니다. `YYYY-MM-DD HH:MM:SS`.

식별되면 Journey Optimizer 제외 목록에서 해당 주소를 제거합니다. [자세히 알아보기](../configuration/manage-suppression-list.md#remove-from-suppression-list).

## 푸시 추적 경험 이벤트 데이터 세트 {#push-tracking-experience-event-dataset}

_인터페이스의 이름: CJM 푸시 추적 경험 이벤트 데이터 세트_

Journey Optimizer에서 푸시할 모바일 추적 경험 이벤트를 수집하기 위한 데이터 세트입니다.

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

여정에서 단계 이벤트를 수집하기 위한 데이터 세트입니다.

관련 스키마는 Journey Orchestration에 대한 여정 단계 이벤트 스키마입니다.

이 쿼리는 주어진 여정에 대해 작업 레이블별 작업 성공 카운트 분류를 보여줍니다.

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

이 쿼리는 주어진 여정에 대해 nodeId 및 nodeLabel별로 단계 입력 카운트의 분류를 보여줍니다. nodeLabel이 다른 여정 노드에 대해 동일할 수 있으므로 nodeId가 여기에 포함됩니다.

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

## 의사 결정 이벤트 데이터 세트{#ode-decisionevents}

_인터페이스의 이름: ODE DecisionEvents(시스템 데이터 세트)_

사용자에게 오퍼 제안을 수집하기 위한 데이터 세트입니다.

관련 스키마는 ODE DecisionEvents입니다.

이 쿼리는 전날 반환된 모든 오퍼를 표시합니다.

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

이 쿼리는 특정 활동/의사 결정의 지난 30일 동안 오퍼가 제안된 횟수와 관련 오퍼 우선 순위를 보여 줍니다.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent Service Dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## BCC 피드백 이벤트 데이터 세트{#bcc-feedback-event-dataset}

_인터페이스의 이름: AJO BCC 피드백 이벤트 데이터 세트(시스템 데이터 세트)_

BCC 메시지에 대한 정보를 저장할 데이터 세트입니다.

2일 이내에 모든 BCC 메시지를 쿼리합니다(특정 캠페인의 경우).

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

피드백 데이터 세트를 사용하여 쿼리하여 받지 못한 사용자(모든 바운스 및 제외)와 특정 메시지에 대한 BCC 항목이 있는 사용자를 표시합니다.

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

## 엔티티 데이터 세트{#entity-dataset}

_인터페이스의 이름: ajo_entity_dataset(시스템 데이터 세트)_

최종 사용자에게 전송된 메시지의 엔티티 메타데이터를 저장하는 데이터 세트입니다.

관련 스키마는 AJO 엔티티 스키마입니다.

이 데이터 세트를 사용하면 마케터가 정의한 메타데이터에 액세스할 수 있으므로 외부 도구에서 보고 시각화를 위해 Journey Optimizer 데이터 세트를 내보낼 때 더 나은 보고 통찰력을 얻을 수 있습니다. 이는 메시지 피드백 데이터 세트 및 경험 이벤트 추적 데이터 세트와 같은 다양한 데이터 세트를 결합하여 프로필 수준에서 전송에서 추적에 이르기까지 메시지 게재의 세부 사항을 얻는 데 도움이 되는 messageID 속성을 사용하여 달성할 수 있습니다.

**중요 정보**

* 메시지에 대한 항목은 여정 또는 캠페인이 게시된 후에만 만들어집니다.

* 캠페인/여정이 게시되고 30분 후에 항목이 표시될 수 있습니다.

>[!NOTE]
>
>당분간 호환성을 위해 엔티티 데이터 세트에 각 메시지 게시에 대한 두 개의 항목이 있습니다. 이는 데이터 세트 간에 필요에 따라 조인 쿼리를 사용하여 원하는 정보를 가져오는 기능에 영향을 주지 않습니다.

보고서에서 특정 여정이 보낸 이메일을 전송한 작업에 따라 정렬하려는 경우 메시지 피드백 데이터 세트를 엔티티 데이터 세트와 결합할 수 있습니다. 사용할 필드는 다음과 같습니다. `_experience.decisioning.propositions.scopeDetails.correlationID` 및 `_id field in entity dataset`.

다음 쿼리는 주어진 캠페인에 대한 관련 메시지 템플릿을 가져오는 데 도움이 됩니다.

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

다음 쿼리는 모든 피드백 이벤트와 연결된 여정 세부 사항 및 이메일 제목을 가져오는 데 도움이 됩니다.

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

여정 단계 이벤트, 메시지 피드백 및 추적 데이터 세트를 연결하여 특정 프로필에 대한 상태를 가져올 수 있습니다.

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
