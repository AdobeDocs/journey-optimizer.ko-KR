---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer의 아카이빙 지원
description: 메시지 아카이브 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 아카이브, 메시지, HIPAA, BCC, 이메일
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 2%

---

# 아카이브 지원 {#archiving-support}

## 메시지 아카이브 방법 {#about-archiving}

HIPAA와 같은 규정에서는 [!DNL Journey Optimizer] 는 개인에게 전송된 메시지를 보관할 방법을 제공해야 합니다. 실제로 고객이 청구를 하는 경우 확인 목적으로 보낸 메시지 사본을 받을 수 있어야 합니다.

* 이메일 채널의 경우 [!DNL Journey Optimizer] 는 기본 제공 BCC 이메일 기능을 제공합니다. [자세히 알아보기](#bcc-email)

* 또한 모든 채널의 경우 **엔티티 데이터 세트**: 개인화되지 않은 메시지 템플릿에 대한 세부 정보를 포함합니다. 이 필드로 데이터 세트를 내보내어 다음과 같은 메타데이터를 저장합니다. 보낸 사람과 시기 개인화된 데이터는 내보내지지 않고 템플릿(메시지의 형식 및 구조)만 고려합니다. [자세히 알아보기](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] 은 SMS 아카이브 요구 사항을 지원하지 않습니다. 전용 아카이브 지원을 위해 SMS 공급업체(Synch 또는 Twilio)와 작업하십시오.

## 이메일에 BCC를 사용하는 방법 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="숨은 참조 이메일 주소 정의"
>abstract="보낸 전자 메일의 사본을 BCC 받은 편지함으로 보내어 유지할 수 있습니다. 보내는 모든 전자 메일이 이 BCC 주소로 블라인드(blind)되도록 선택한 전자 메일 주소를 입력합니다. BCC 주소 도메인은 Adobe에 위임된 하위 도메인과 동일하지 않아야 합니다. 이 기능은 선택 사항입니다."

에서 보낸 이메일의 동일한 복사본(또는 블라인드 탄소 사본)을 보낼 수 있습니다 [!DNL Journey Optimizer] BCC 받은 편지함으로 이동합니다. 이 선택적 기능을 사용하면 규정 준수 및/또는 아카이브를 위해 사용자에게 보내는 이메일 통신 사본을 유지할 수 있습니다. 게재 수신자에게는 보이지 않습니다.

### 숨은 참조 이메일 활성화 {#enable-bcc}

를 사용하려면 **[!UICONTROL 숨은 참조 이메일]** 옵션을 선택한 경우, [채널 표면](channel-surfaces.md) (즉, 메시지 사전 설정). Adobe에 위임된 하위 도메인에 정의된 이메일 주소를 제외하고 올바른 형식으로 외부 주소를 지정할 수 있습니다. 예를 들어 *marketing.luma.com* Adobe 하위 도메인, 다음과 같은 주소 *abc@marketing.luma.com* 는 금지됩니다.

>[!CAUTION]
>
>숨은 참조 이메일 주소는 하나만 정의할 수 있습니다. 숨은 참조 주소에 현재 채널 표면을 사용하여 전송되는 모든 이메일을 저장할 수신 용량이 충분한지 확인합니다.
>
>추가 권장 사항은 [이 섹션](#bcc-recommendations-limitations).

>[!NOTE]
>
>Healthcare Shield 추가 기능 서비스를 구입한 경우 BCC 주소의 ISP가 TLS 1.2 프로토콜을 지원하는지 확인해야 합니다.

![](assets/preset-bcc.png)

이 면을 사용하는 모든 이메일 메시지는 입력한 BCC 이메일 주소에 블라인드 복사됩니다. 여기에서 외부 시스템을 사용하여 처리 및 보관할 수 있습니다.

>[!CAUTION]
>
>BCC 기능 사용량은 라이선스를 받은 메시지 수에 따라 계산됩니다. 따라서 아카이브하려는 중요한 통신에 사용되는 표면에서만 활성화합니다. 라이선스가 부여된 볼륨이 있는지 계약을 확인합니다.

BCC 이메일 주소 설정이 즉시 저장되고 표면 수준에서 처리됩니다. 이 표면을 사용하여 새 메시지를 만들면 숨은 참조 이메일 주소가 자동으로 표시됩니다.

![](assets/preset-bcc-in-msg.png)

그러나 설명된 논리에 따라 숨은 참조 주소가 통신을 전송하도록 선택됩니다 [여기](../email/email-settings.md).

### Recommendations 및 제한 사항 {#bcc-recommendations-limitations}

* 개인 정보 보호 규정을 준수하려면 PII(보안 개인 식별 정보)를 저장할 수 있는 보관 시스템에서 BCC 이메일을 처리해야 합니다.

* 메시지에는 PII(개인 식별 정보)와 같은 중요 또는 개인 데이터가 포함될 수 있으므로 BCC 주소가 올바른지 확인하고 메시지에 대한 액세스를 보호합니다.

* 숨은 참조를 위해 사용되는 받은 편지함은 공간 및 게재에 대해 제대로 관리되어야 합니다. 받은 편지함이 바운스를 반환하는 경우 일부 이메일이 수신되지 않을 수 있으므로 보관되지 않습니다.

* 메시지는 대상 수신자가 되기 전에 BCC 전자 메일 주소로 배달될 수 있습니다. 원본 메시지가 전송되었을 수도 있지만 숨은 참조 메시지도 보낼 수 있습니다 [바운스](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* BCC 주소로 전송된 이메일은 전송 분석에서 총 열기 및 클릭 수를 고려하여 열지 않거나 클릭스루하지 마십시오. 이로 인해 일부 계산 오류가 발생할 수 있습니다. [보고서](../reports/global-report.md).

* 이 주소로 전송된 다른 모든 이메일에 영향을 주므로 BCC 받은 편지함에서 메시지를 스팸으로 표시하지 마십시오.

>[!CAUTION]
>
>해당 수신자의 구독을 즉시 취소하므로 BCC 주소로 전송된 이메일에서 가입 해지 링크를 클릭하지 마십시오.

### GDPR 준수 {#gdpr-compliance}

GDPR과 같은 규정에서는 데이터 주체가 언제든지 동의를 수정할 수 있어야 합니다. Journey Optimizer으로 보내는 BCC 이메일에는 PII(보안 개인 식별 정보)가 포함되어 있으므로 **[!UICONTROL CJM 이메일 BCC 피드백 이벤트 스키마]** gdpr 및 유사한 규정을 준수하여 이러한 PII를 관리할 수 있어야 합니다.

이렇게 하려면 아래 단계를 수행합니다.

1. 이동 **[!UICONTROL 데이터 관리]** > **[!UICONTROL 스키마]** > **[!UICONTROL 찾아보기]** 을(를) 선택합니다. **[!UICONTROL CJM 이메일 BCC 피드백 이벤트 스키마]**.

   ![](assets/preset-bcc-schema.png)

1. 클릭하여 확장 **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagement]** 그런 다음 **[!UICONTROL secondaryRecipientDetail]**.

1. 선택 **[!UICONTROL originalRecipientAddress]**.

1. 에서 **[!UICONTROL 필드 속성]** 오른쪽에서 아래로 스크롤하여 **[!UICONTROL ID]** 확인란을 선택합니다.

1. 선택하고 을(를) 선택합니다 **[!UICONTROL 기본 ID]**.

1. 드롭다운 목록에서 네임스페이스를 선택합니다.

   ![](assets/preset-bcc-schema-identity.png)

1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>개인 정보 관리 및 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko){target="_blank"}.

### 숨은 참조 보고 데이터 {#bcc-reporting}

숨은 참조를 통한 보고는 여정 및 메시지 보고서에서 사용할 수 없습니다. 하지만 정보는 **[!UICONTROL AJO BCC 피드백 이벤트 데이터 세트]**. 이 데이터 세트에 대한 쿼리를 실행하여 디버깅 목적에 유용한 정보를 찾을 수 있습니다.

사용자 인터페이스를 통해 이 데이터 세트에 액세스할 수 있습니다. 선택 **[!UICONTROL 데이터 관리]** > **[!UICONTROL 데이터 세트]** > **[!UICONTROL 찾아보기]** 그리고 **[!UICONTROL 시스템 데이터 세트 표시]** 필터에서 전환하여 시스템에서 생성한 데이터 세트를 표시합니다. 의 데이터 세트에 액세스하는 방법에 대해 자세히 알아보십시오 [이 섹션](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

이 데이터 세트에 대해 쿼리를 실행하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. 액세스하려면 다음을 선택합니다 **[!UICONTROL 데이터 관리]** > **[!UICONTROL 쿼리]** 을(를) 클릭합니다. **[!UICONTROL 쿼리 만들기]**. [자세히 알아보기](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

찾고 있는 정보에 따라 다음 쿼리를 실행할 수 있습니다.

1. 아래의 다른 모든 쿼리에 대해서는 여정 작업 ID가 필요합니다. 이 쿼리를 실행하여 지난 2일 내에 특정 여정 버전 ID와 연결된 모든 작업 ID를 가져옵니다.

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >를 가져오려면 `<journey version id>`매개 변수에서 해당 [여정 버전](../building-journeys/journey.md#journey-versions) 에서 **[!UICONTROL 여정 관리]** > **[!UICONTROL 여정]** 메뉴 아래의 제품에서 사용할 수 있습니다. 여정 버전 ID는 웹 브라우저에 표시되는 URL의 끝에 표시됩니다.
   >
   >![](assets/preset-bcc-action-id.png)

1. 지난 2일 이내에 특정 사용자를 타겟팅한 특정 메시지에 대해 생성된 모든 메시지 피드백 이벤트(특히 피드백 상태)를 가져오려면 이 쿼리를 실행하십시오.

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >를 가져오려면 `<journey action id>` 매개 변수에서 여정 버전 id를 사용하여 위에 설명된 첫 번째 쿼리를 실행합니다. 다음 `<recipient email address>` 매개 변수는 타겟팅된 또는 실제 수신자의 이메일 주소입니다.

1. 지난 2일 이내에 특정 사용자를 타겟팅한 특정 메시지에 대해 생성된 모든 숨은 참조 메시지 피드백 이벤트를 가져오려면 이 쿼리를 실행하십시오.

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. 이 쿼리를 실행하여 메시지를 받지 못한 모든 받는 사람 주소를 가져오지만 해당 BCC 항목은 지난 30일 내에 있습니다.

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
