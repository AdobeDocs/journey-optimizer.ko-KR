---
title: 전자 메일 설정 구성
description: 메시지 사전 설정 수준에서 이메일 설정을 구성하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 65c2ba7e0931f449a29d1e7ff01d6d68fccca448
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---

# 전자 메일 설정 구성 {#email-settings}

메시지 사전 설정 구성의 전용 섹션에서 전자 메일 설정을 정의합니다. 에서 메시지 사전 설정을 만드는 방법을 알아봅니다. [이 섹션](message-presets.md).

![](assets/preset-email.png)

## 이메일 유형 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="이메일 카테고리 정의"
>abstract="이 사전 설정을 사용할 때 전송할 메시지 유형을 선택합니다. 사용자 동의가 필요한 프로모션 메시지의 마케팅 또는 비상업용 메시지의 경우 트랜잭션용으로 특정 컨텍스트에서 가입 해지된 프로필에도 전송될 수 있습니다."

에서 **이메일 유형** 섹션에서 사전 설정으로 전송할 메시지 유형을 선택합니다. **마케팅** 또는 **트랜잭션**.

* 선택 **마케팅** 프로모션 메시지의 경우: 이러한 메시지에는 사용자의 동의가 필요합니다.

* 선택 **트랜잭션** 주문 확인, 암호 재설정 알림 또는 배달 정보와 같은 비상업적인 메시지의 경우,

>[!CAUTION]
>
>**트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필로 메시지를 보낼 수 있습니다. 이러한 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

When [메시지 만들기](../messages/get-started-content.md#create-new-message): 메시지에 대해 선택한 카테고리와 일치하는 유효한 메시지 사전 설정을 선택해야 합니다.

## 하위 도메인 및 IP 풀 {#subdomains-and-ip-pools}

에서 **하위 도메인 및 IP 풀 세부 정보** 섹션:

1. 이메일을 보내는 데 사용할 하위 도메인을 선택합니다. [자세히 보기](about-subdomain-delegation.md)

1. 사전 설정과 연결할 IP 풀을 선택합니다. [자세히 보기](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

선택한 IP 풀이 아래에 있는 동안에는 사전 설정을 만들 수 없습니다 [에디션](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** 상태) 및 을 선택한 하위 도메인과 연결한 적이 없습니다. 그렇지 않으면 가장 오래된 버전의 IP 풀/하위 도메인 연결이 계속 사용됩니다. 이 경우 사전 설정을 초안으로 저장하고 IP 풀에 **[!UICONTROL Success]** 상태.

>[!NOTE]
>
>비프로덕션 환경의 경우 Adobe은 기본 테스트 하위 도메인을 만들거나 공유 전송 IP 풀에 대한 액세스 권한을 부여하지 않습니다. 다음을 수행해야 합니다. [고유한 하위 도메인 위임](delegate-subdomain.md) 및 조직에 할당된 풀의 IP를 사용합니다.

## 목록 가입 해지 {#list-unsubscribe}

On [하위 도메인 선택](#subdomains-and-ip-pools) 목록에서 **[!UICONTROL Enable List-Unsubscribe]** 옵션이 표시됩니다.

![](assets/preset-list-unsubscribe.png)

이 옵션은 기본적으로 활성화되어 있습니다.

이 기능을 활성화한 상태로 두면 가입 해지 링크가 다음과 같이 이메일 헤더에 자동으로 포함됩니다.

![](assets/preset-list-unsubscribe-header.png)

이 옵션을 비활성화하면 이메일 헤더에 가입 해지 링크가 표시되지 않습니다.

가입 해지 링크는 다음 두 가지 요소로 구성됩니다.

* An **이메일 주소 가입**: 모든 구독 취소 요청을 전송하는 입니다.

   in [!DNL Journey Optimizer], 가입 해지 이메일 주소가 기본값입니다 **[!UICONTROL Mailto (unsubscribe)]** 메시지 사전 설정에 표시되는 주소 [선택한 하위 도메인](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* 다음 **구독 취소 URL**: 사용자가 가입 해지되면 리디렉션되는 랜딩 페이지의 URL입니다.

   를 추가할 경우 [옵트아웃 링크 1회 클릭](../messages/consent.md#one-click-opt-out) 이 사전 설정을 사용하여 만든 메시지에 대해 가입 해지 URL은 한 번의 클릭으로 옵트아웃 링크에 대해 정의된 URL입니다.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >메시지 콘텐츠에 원클릭 옵트아웃 링크를 추가하지 않으면 랜딩 페이지가 사용자에게 표시되지 않습니다.

에서 메시지에 헤더 가입 해지 링크를 추가하는 방법에 대해 자세히 알아보십시오 [이 섹션](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 헤더 매개 변수{#email-header}

에서 **[!UICONTROL HEADER PARAMETERS]** 섹션에서 해당 사전 설정을 사용하여 보낸 메시지 유형과 연관된 발신자 이름과 이메일 주소를 입력합니다.

>[!CAUTION]
>
>이메일 주소는 현재 선택한 주소를 사용해야 합니다 [위임된 하위 도메인](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: 브랜드 이름과 같은 발신자의 이름입니다.

* **[!UICONTROL Sender email]**: 통신에 사용할 이메일 주소입니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*, 다음 사용 가능 *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: 수신자가 **회신** 버튼을 클릭합니다.

* **[!UICONTROL Reply to (email)]**: 수신자가 **회신** 버튼을 클릭합니다. 위임된 하위 도메인에 정의된 주소를 사용해야 합니다(예: *reply@marketing.luma.com*). 그렇지 않으면 이메일이 삭제됩니다.

* **[!UICONTROL Error email]**: 이 주소에는 배달되는 며칠 후 ISP에서 생성한 모든 오류(비동기 바운스)가 수신됩니다.

![](assets/preset-header.png)

>[!NOTE]
>
>주소는 문자(A-Z)로 시작해야 하며 영숫자만 사용할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

### 이메일 전달 {#forward-email}

특정 이메일 주소로 전달하려는 경우 [!DNL Journey Optimizer] 위임된 하위 도메인은 Adobe 고객 지원 센터에 문의하십시오. 다음을 제공해야 합니다.

* 원하는 이메일 주소입니다. 전자 메일 주소 전달 도메인은 Adobe에 위임된 하위 도메인과 일치하지 않습니다.
* 샌드박스 이름입니다.
* 전자 메일 주소를 사용할 사전 설정된 이름입니다.
* 현재 **[!UICONTROL Reply to (email)]** 미리 설정된 수준에서 설정된 주소입니다.

>[!NOTE]
>
>하위 도메인당 한 개의 순방향 이메일 주소만 있을 수 있습니다. 따라서 여러 사전 설정에서 동일한 하위 도메인을 사용하는 경우 모든 사전 설정에 동일한 순방향 이메일 주소를 사용해야 합니다.

전자 메일 전송 주소는 Adobe이 설정합니다. 3~4일 걸릴 수 있습니다.

<!--
## BCC email {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Define a BCC email address"
>abstract="You can keep a copy of sent emails by sending them to a BCC inbox. Enter the email address of your choice so that every email sent is blind-copied to this BCC address. This feature is optional."

You can send an identical copy (or blind carbon copy) of an email sent by [!DNL Journey Optimizer] to a BCC inbox. This optional feature allows you to retain copies of email communications you send to your users for compliance and/or archival purposes. This will be invisible to the delivery recipients.

>[!CAUTION]
>
>This capability will be available starting **May, 31**.

### Enable BCC email {#enable-bcc}

To enable the **[!UICONTROL BCC email]** option, enter the email address of your choice in the dedicated field. You can specify any external address in correct format, except an email address defined on the delegated subdomain. For example, if the delegated subdomain is *marketing.luma.com*, any address like *abc@marketing.luma.com* is prohibited.

>[!NOTE]
>
>You can only define one BCC email address. Make sure the BCC address has enough reception capacity to store all the emails that are sent using the current preset.
>
>More recommendations are listed in [this section](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

All email messages using this preset will be blind-copied to the BCC email address you entered. From there, they can be processed and archived using an external system.

>[!CAUTION]
>
>Your BCC feature usage will be counted against the number of messages you are licensed for. Hence, only enable it in the presets used for critical communications that you wish to archive. Check your contract for licensed volumes.

The BCC email address setting is immediately saved and processed at the preset level. When you [create a new message](../messages/get-started-content.md#create-new-message) using this preset, the BCC email address is automatically displayed.

![](assets/preset-bcc-in-msg.png)

However, the BCC address gets picked up for sending communications following the logic below:

* For batch and burst journeys, it does not apply to batch or burst execution that had already started before the BCC setting is made. The change will be picked up at the next recurrence or new execution.

* For transactional messages, the change is picked up immediately for the next communication (up to one minute delay).

>[!NOTE]
>
>You do not need to republish a message or journey for the BCC setting to be picked up.

### Recommendations and limitations {#bcc-recommendations-limitations}

* To ensure your privacy compliance, BCC emails must be processed by an archiving system capable of storing securely personally identifiable information (PII).

* As messages can contain sensitive or private data, such as personally identifiable information (PII), make sure the BCC address is correct, and secure the access to messages.

* Your inbox used for BCC should be properly managed for space and delivery. If the inbox returns bounces, some emails may not be received and therefore will fail to get archived.

* Messages may be delivered to the BCC email address before the target recipients. BCC messages can also been sent even though the original messages may have [bounced](../reports/suppression-list.md#delivery-failures).

    //////OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK /////////

* Do not open or click through the emails sent to the BCC address as it is taken into account in the total opens and clicks from the send analysis, which could cause some miscalculations in [reports](../reports/message-monitoring.md). 

* Do not mark messages as spam in the BCC inbox, as it will impact all the other emails sent to this address.


>[!CAUTION]
>
>Do not click the unsubscribe link in the emails sent to the BCC address as you will immediately unsubscribe the corresponding recipients.

### GDPR compliance {#gdpr-compliance}

Regulations such as GDPR state that Data Subjects should be able to modify their consent at any time. Because the BCC emails you are sending with Journey Optimizer include securely personally identifiable information (PII), you must edit the **[!UICONTROL CJM Email BCC Feedback Event Schema]** to be able to manage these PII in compliance with GDPR and similar regulations.

To do this, follow the steps below.

1. Go to **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** and select **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

    ![](assets/preset-bcc-schema.png)

1. Click to expand **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]**.

1. Select **[!UICONTROL originalRecipientAddress]**.

1. In the **[!UICONTROL Field properties]** on the right, scroll down to the **[!UICONTROL Identity]** checkbox.

1. Select it and also select **[!UICONTROL Primary identity]**.

1. Select a namespace from the drop-down list.

    ![](assets/preset-bcc-schema-identity.png)

1. Click **[!UICONTROL Apply]**.

>[!NOTE]
>
>Learn more on managing Privacy and the applicable regulations in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target="_blank"}.

### BCC reporting data {#bcc-reporting}

Reporting as such on BCC is not available in the journey and message reports. However, information is stored on a system dataset called **[!UICONTROL AJO BCC Feedback Event Dataset]**. You can run queries against this dataset to find useful information for debugging purpose for example.

You can access this dataset through the user interface. Select **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** and enable the **[!UICONTROL Show system datasets]** toggle from the filter to display the system-generated datasets. Learn more on how to access datasets in [this section](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

To run queries against this dataset, you can use the Query Editor provided by the [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. To access it, select **[!UICONTROL Data management]** > **[!UICONTROL Queries]** and click **[!UICONTROL Create query]**. [Learn more](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Depending on what information you are looking for, you can run the following queries.

1. For all the other queries below, you will need the journey action ID. Run this query to fetch all action IDs associated with a particular journey version ID within the last 2 days:

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
    >To get the `<journey version id>`parameter, select the corresponding [journey version](../building-journeys/journey-versions.md) from the **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** menu. The journey version ID is displayed at the end of the URL displayed in your web browser.
    >
    >![](assets/preset-bcc-action-id.png)

1. Run this query to fetch all message feedback events (especially feedback status) generated for a particular message targeted to a specific user within the last 2 days:

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
    >To get the `<journey action id>` parameter, run the first query described above using the journey version id. The `<recipient email address>` parameter is the targeted or actual recipient's email address.

1. Run this query to fetch all BCC message feedback events generated for a particular message targeted to a specific user within the last 2 days:

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

1. Run this query to fetch all recipient addresses who have not received the message whereas its BCC entry exists within the last 30 days:

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
-->

## 전자 메일 다시 시도 매개 변수 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="다시 시도 기간 조정"
>abstract="임시 소프트 바운스 오류로 인해 이메일 메시지가 실패하면 3.5일(84시간) 동안 다시 시도가 수행됩니다. 이 기본 다시 시도 기간을 조정하여 사용자의 요구 사항에 맞게 조정할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="다시 시도 기본 정보"

을 구성할 수 있습니다 **전자 메일 다시 시도 매개 변수**.

![](assets/preset-retry-parameters.png)

기본적으로 [재시도 기간](retries.md#retry-duration) 은 84시간으로 설정되어 있지만 이 설정을 필요에 더 잘 맞게 조정할 수 있습니다.

다음 범위 내에 정수 값(시간 또는 분 단위)을 입력해야 합니다.

* 마케팅 이메일의 경우 최소 재시도 기간은 6시간입니다.
* 트랜잭션 전자 메일의 경우 최소 재시도 기간은 10분입니다.
* 두 이메일 유형의 경우 최대 다시 시도 기간은 84시간(또는 5040분)입니다.

에서 다시 시도하는 방법에 대해 자세히 알아보기 [이 섹션](retries.md).

## URL 추적 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="URL 추적 매개 변수"
>abstract="이 섹션을 사용하여 추적 매개 변수를 이메일 콘텐츠에 있는 캠페인 URL에 자동으로 추가합니다."

다음을 사용할 수 있습니다 **[!UICONTROL URL Tracking Parameters]** 를 사용하여 여러 채널에서 마케팅 활동의 효과를 측정할 수 있습니다. 이 기능은 선택 사항입니다.

이 섹션에 정의된 매개 변수가 이메일 메시지 콘텐츠에 포함된 URL의 끝에 추가됩니다. 그런 다음 Adobe Analytics 또는 Google Analytics과 같은 웹 분석 도구에서 이러한 매개 변수를 캡처하고 다양한 성능 보고서를 만들 수 있습니다.

![](assets/preset-url-tracking.png)

메시지 사전 설정을 만들 때 예로서 세 개의 URL 추적 매개 변수가 자동으로 채워집니다. 이러한 매개 변수를 편집하고 **[!UICONTROL Add new parameter]** 버튼을 클릭합니다.

URL 추적 매개 변수를 구성하려면 **[!UICONTROL Name]** 및 **[!UICONTROL Value]** 필드를 선택하거나 다음 객체로 이동하여 미리 정의된 값 목록에서 선택합니다.

* 여정 속성: **소스 ID**, **소스 이름**, **소스 버전 ID**
* 작업 속성: **작업 ID**, **작업 이름**
* Offer decisioning 속성: **오퍼 ID**, **오퍼 이름**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>폴더를 선택하지 마십시오: 필요한 폴더를 찾아 추적 매개 변수 값으로 사용할 프로필 속성을 선택해야 합니다.

다음은 Adobe Analytics 및 Google Analytics 호환 URL의 예입니다.

* Adobe Analytics 호환 URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics 호환 URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>텍스트 값을 입력하고 사전 정의된 값을 선택할 수 있습니다. 각 **[!UICONTROL Value]** 필드에는 총 255자가 포함될 수 있습니다.
