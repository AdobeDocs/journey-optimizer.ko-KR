---
title: 전자 메일 설정 구성
description: 메시지 사전 설정 수준에서 이메일 설정을 구성하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: c48d083445d4e4c7cdbed1a61cee13ed3fcfcc8b
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 2%

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
* 전송 이메일(또는 &quot;회신&quot;) 주소가 사용될 사전 설정된 이름입니다.
* 현재 **[!UICONTROL Reply to (email)]** 미리 설정된 수준에서 설정된 주소입니다.

>[!NOTE]
>
>하위 도메인당 한 개의 순방향 이메일 주소만 있을 수 있습니다. 따라서 여러 사전 설정에서 동일한 하위 도메인을 사용하는 경우 모든 사전 설정에 동일한 순방향 이메일 주소를 사용해야 합니다.

전자 메일 전송 주소는 Adobe이 설정합니다. 3~4일 걸릴 수 있습니다.

## 숨은 참조 이메일 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="숨은 참조 이메일 주소 정의"
>abstract="보낸 전자 메일의 사본을 BCC 받은 편지함으로 보내어 유지할 수 있습니다. 보내는 모든 전자 메일이 이 BCC 주소로 블라인드(blind)되도록 선택한 전자 메일 주소를 입력합니다. 이 기능은 선택 사항입니다."

에서 보낸 이메일의 동일한 복사본(또는 블라인드 탄소 사본)을 보낼 수 있습니다 [!DNL Journey Optimizer] BCC 받은 편지함으로 이동합니다. 이 선택적 기능을 사용하면 규정 준수 및/또는 아카이브를 위해 사용자에게 보내는 이메일 통신 사본을 유지할 수 있습니다. 게재 수신자에게는 보이지 않습니다.

>[!CAUTION]
>
>이 기능은 시작할 때 사용할 수 있습니다 **5월 31일**.

### 숨은 참조 이메일 활성화 {#enable-bcc}

를 사용하려면 **[!UICONTROL BCC email]** 옵션을 선택한 경우 전용 필드에 원하는 이메일 주소를 입력합니다. 위임된 하위 도메인에 정의된 이메일 주소를 제외하고 올바른 형식으로 외부 주소를 지정할 수 있습니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*&#x200B;과 같은 모든 주소 *abc@marketing.luma.com* 는 금지됩니다.

>[!NOTE]
>
>숨은 참조 이메일 주소는 하나만 정의할 수 있습니다. 숨은 참조 주소에 현재 사전 설정을 사용하여 전송되는 모든 이메일을 저장할 수신 용량이 충분한지 확인합니다.
>
>추가 권장 사항은 [이 섹션](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

이 사전 설정을 사용하는 모든 이메일 메시지는 입력한 BCC 이메일 주소로 블라인드에 복사됩니다. 여기에서 외부 시스템을 사용하여 처리 및 보관할 수 있습니다.

>[!CAUTION]
>
>BCC 기능 사용량은 라이선스를 받은 메시지 수에 따라 계산됩니다. 따라서 보관하려는 중요한 통신에 사용되는 사전 설정에서만 활성화합니다. 라이선스가 부여된 볼륨이 있는지 계약을 확인합니다.

BCC 이메일 주소 설정이 즉시 저장되고 사전 설정된 수준에서 처리됩니다. 다음 경우에 [새 메시지 만들기](../messages/get-started-content.md#create-new-message) 이 사전 설정을 사용하면 숨은 참조 이메일 주소가 자동으로 표시됩니다.

![](assets/preset-bcc-in-msg.png)

그러나 아래 논리에 따라 BCC 주소가 통신을 전송하도록 선택됩니다.

* 배치 및 버스트 여정의 경우 BCC 설정이 만들어지기 전에 이미 시작된 일괄 처리 또는 버스트 실행에는 적용되지 않습니다. 변경 사항은 다음 되풀이 또는 새 실행 시 선택됩니다.

* 트랜잭션 메시지의 경우 변경 사항이 다음 커뮤니케이션에 대해 즉시 선택됩니다(최대 1분 지연).

>[!NOTE]
>
>선택할 BCC 설정에 대한 메시지나 여정을 다시 게시할 필요가 없습니다.

### Recommendations 및 제한 사항 {#bcc-recommendations-limitations}

* 개인 정보 보호 규정을 준수하려면 PII(보안 개인 식별 정보)를 저장할 수 있는 보관 시스템에서 BCC 이메일을 처리해야 합니다.

* 메시지에는 PII(개인 식별 정보)와 같은 중요 또는 개인 데이터가 포함될 수 있으므로 BCC 주소가 올바른지 확인하고 메시지에 대한 액세스를 보호합니다.

* 숨은 참조를 위해 사용되는 받은 편지함은 공간 및 게재에 대해 제대로 관리되어야 합니다. 받은 편지함이 바운스를 반환하는 경우 일부 이메일이 수신되지 않을 수 있으므로 보관되지 않습니다.

* 메시지는 대상 수신자가 되기 전에 BCC 전자 메일 주소로 배달될 수 있습니다. 원본 메시지가 전송되었을 수도 있지만 숨은 참조 메시지도 보낼 수 있습니다 [바운스](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* BCC 주소로 전송된 이메일은 전송 분석에서 총 열기 및 클릭 수를 고려하여 열지 않거나 클릭스루하지 마십시오. 이로 인해 일부 계산 오류가 발생할 수 있습니다. [보고서](../reports/message-monitoring.md).

* 이 주소로 전송된 다른 모든 이메일에 영향을 주므로 BCC 받은 편지함에서 메시지를 스팸으로 표시하지 마십시오.


>[!CAUTION]
>
>해당 수신자의 구독을 즉시 취소하므로 BCC 주소로 전송된 이메일에서 가입 해지 링크를 클릭하지 마십시오.

### GDPR 준수 {#gdpr-compliance}

GDPR과 같은 규정에서는 데이터 주체가 언제든지 동의를 수정할 수 있어야 합니다. Journey Optimizer으로 보내는 BCC 이메일에는 PII(보안 개인 식별 정보)가 포함되어 있으므로 **[!UICONTROL CJM Email BCC Feedback Event Schema]** gdpr 및 유사한 규정을 준수하여 이러한 PII를 관리할 수 있어야 합니다.

이렇게 하려면 아래 단계를 수행합니다.

1. 이동 **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** 을(를) 선택합니다. **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

   ![](assets/preset-bcc-schema.png)

1. 클릭하여 확장 **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** 그런 다음 **[!UICONTROL secondaryRecipientDetail]**.

1. **[!UICONTROL originalRecipientAddress]**&#x200B;를 선택합니다.

1. 에서 **[!UICONTROL Field properties]** 오른쪽에서 아래로 스크롤하여 **[!UICONTROL Identity]** 확인란을 선택합니다.

1. 선택하고 을(를) 선택합니다 **[!UICONTROL Primary identity]**.

1. 드롭다운 목록에서 네임스페이스를 선택합니다.

   ![](assets/preset-bcc-schema-identity.png)

1. **[!UICONTROL Apply]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>개인 정보 관리에 대한 자세한 내용 및 해당 규정은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko){target=&quot;_blank&quot;}를 참조하세요.

### 숨은 참조 보고 데이터 {#bcc-reporting}

숨은 참조를 통한 보고는 여정 및 메시지 보고서에서 사용할 수 없습니다. 하지만 정보는 **[!UICONTROL AJO BCC Feedback Event Dataset]**. 이 데이터 세트에 대한 쿼리를 실행하여 디버깅 목적에 유용한 정보를 찾을 수 있습니다.

사용자 인터페이스를 통해 이 데이터 세트에 액세스할 수 있습니다. 선택 **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** 그리고 **[!UICONTROL Show system datasets]** 필터에서 전환하여 시스템에서 생성한 데이터 세트를 표시합니다. 의 데이터 세트에 액세스하는 방법에 대해 자세히 알아보십시오 [이 섹션](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

이 데이터 세트에 대해 쿼리를 실행하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. 액세스하려면 다음을 선택합니다 **[!UICONTROL Data management]** > **[!UICONTROL Queries]** 을(를) 클릭합니다. **[!UICONTROL Create query]**. [자세히 보기](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

찾고 있는 정보에 따라 다음 쿼리를 실행할 수 있습니다.

1. 아래의 다른 모든 쿼리에 대해서는 여정 작업 ID가 필요합니다. 이 쿼리를 실행하여 지난 2일 내에 특정 여정 버전 ID와 연결된 모든 작업 ID를 가져옵니다.

       &quot;
       선택
       고유
       CAST(TIMESTAMP AS DATE) AS EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM 여정_step_events
       위치
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; 및
       _experience.journeyOrchestration.stepEvents.actionID가 NULL이 아니며,
       TIMESTAMP > NOW() - 간격 &#39;2&#39;일
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >를 가져오려면 `<journey version id>`매개 변수에서 해당 [여정 버전](../building-journeys/journey-versions.md) 에서 **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** 메뉴 아래의 제품에서 사용할 수 있습니다. 여정 버전 ID는 웹 브라우저에 표시되는 URL의 끝에 표시됩니다.
   >
   >![](assets/preset-bcc-action-id.png)

1. 지난 2일 이내에 특정 사용자를 타겟팅한 특정 메시지에 대해 생성된 모든 메시지 피드백 이벤트(특히 피드백 상태)를 가져오려면 이 쿼리를 실행하십시오.

       &quot;
       선택
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE_experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       &#39;sent&#39; THEN &#39;SENT&#39;
       &#39;delay&#39; THEN &#39;Retry&#39;
       &#39;out_of_band&#39; THEN &#39;반송&#39;
       &#39;바운스&#39; 후 &#39;바운스&#39;
       END AS FeedbackStatusCategory
       CJM_message_feedback_event_dataset에서
       위치
       timestamp > now() - 간격 &#39;2&#39;일 AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; 및
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39; 및
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>`
       ORDER BY EventTime DESC;
       &quot;
   
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
