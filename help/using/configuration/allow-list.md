---
title: 허용 목록
description: 허용 목록 사용 방법을 알아봅니다.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 3%

---

# 허용 목록 {#allow-list}

에서 특정 전송 안전 목록을 정의할 수 있습니다 [샌드박스](../administration/sandboxes.md) 수준.

이 허용 목록을 사용하면 특정 샌드박스에서 보내는 이메일을 받을 수 있는 권한이 있는 유일한 수신자 또는 도메인이 되는 개별 이메일 주소 또는 도메인을 지정할 수 있습니다.

>[!NOTE]
>
>이 기능은 프로덕션 및 비프로덕션 샌드박스에서 사용할 수 있습니다.

예를 들어, 오류가 발생할 수 있는 비프로덕션 인스턴스의 경우 허용 목록은 실제 고객 주소로 원치 않는 메시지를 보낼 위험이 없으므로 테스트 목적으로 안전한 환경을 제공합니다.

또한 허용 목록이 활성화되었지만 비어 있으면 메일이 발송되지 않습니다. 따라서 중요한 문제가 발생하면 이 기능을 사용하여 나가는 모든 통신을 [!DNL Journey Optimizer] 문제를 해결할 때까지 추가 정보 [허용 목록 논리](#logic).

>[!CAUTION]
>
>이 기능은 이메일 채널에만 적용됩니다.

## 허용 목록 액세스 {#access-allowed-list}

허용되는 이메일 주소 및 도메인의 세부 목록에 액세스하려면 다음 위치로 이동하십시오. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**, 을(를) 선택하고 을(를) 선택합니다. **[!UICONTROL Allowed list]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>허용 목록 보기, 내보내기 및 관리를 위한 권한은 [여정 관리자](../administration/ootb-product-profiles.md#journey-administrator). 관리에 대해 자세히 알아보기 [!DNL Journey Optimizer] 사용자 액세스 권한 [이 섹션](../administration/permissions-overview.md).

허용 목록을 CSV 파일로 내보내려면 **[!UICONTROL Download CSV]** 버튼을 클릭합니다.

를 사용하십시오 **[!UICONTROL Delete]** 단추를 클릭하여 항목을 영구적으로 제거합니다.

이메일 주소 또는 도메인을 검색하고 **[!UICONTROL Address type]**. 선택한 후에는 목록 위에 표시된 필터를 지울 수 있습니다.

![](assets/allowed-list-filtering-example.png)

## 허용 목록 활성화 {#enable-allow-list}

허용 목록을 활성화하려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** 메뉴에 액세스합니다.

1. **[!UICONTROL Deactivated]**&#x200B;을(를) 클릭합니다.

   ![](assets/allow-list-edit.png)

1. **[!UICONTROL Activate allowed list]**&#x200B;를 선택합니다. 이제 허용 목록이 활성 상태입니다.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >허용 목록을 활성화한 후 여정 및 캠페인에서가 적용되기 위한 5분 지연이 있습니다.

허용 목록 논리는 기능이 활성 상태일 때 적용됩니다. 자세한 내용은 [이 섹션](#logic)을 참조하십시오.

>[!NOTE]
>
>활성화되면 여정을 실행할 때에도 허용 목록 기능이 적용되지만 [증명](../design/preview.md#send-proofs) 및 를 사용하여 여정 테스트 [테스트 모드](../building-journeys/testing-the-journey.md).

## 허용 목록 비활성화 {#deactivate-allow-list}

허용 목록을 비활성화하려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** 메뉴에 액세스합니다.

1. **[!UICONTROL Active]**&#x200B;을(를) 클릭합니다.

   ![](assets/allow-list-edit-active.png)

1. **[!UICONTROL Deactivate allowed list]**&#x200B;를 선택합니다. 허용 목록이 더 이상 활성 상태가 아닙니다.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >허용 목록을 비활성화한 후 여정 및 캠페인에서가 적용되려면 5분 지연이 있습니다.

기능이 비활성화되면 허용 목록 논리가 적용되지 않습니다. 자세한 내용은 [이 섹션](#logic)을 참조하십시오.

## 허용 목록에 엔티티 추가 {#add-entities}

특정 샌드박스의 허용 목록에 새 이메일 주소 또는 도메인을 추가하려면 다음 중 하나를 수행할 수 있습니다 [수동으로 목록 채우기](#manually-populate-list), 또는 [API 호출](#api-call-allowed-list).

>[!NOTE]
>
>허용 목록은 최대 1,000개의 항목을 포함할 수 있습니다.

### 수동으로 허용 목록 채우기 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="허용 목록에 주소 또는 도메인 추가"
>abstract="새 이메일 주소 또는 도메인을 하나씩 선택하여 허용 목록에 수동으로 추가할 수 있습니다."

수동으로 [!DNL Journey Optimizer] 사용자 인터페이스를 통해 이메일 주소 또는 도메인을 추가하여 허용 목록.

>[!NOTE]
>
>한 번에 하나의 이메일 주소나 도메인만 추가할 수 있습니다.

이렇게 하려면 아래 단계를 수행합니다.

1. **[!UICONTROL Add email or domain]** 버튼을 선택합니다.

   ![](assets/allowed-list-add-email.png)

1. 주소 유형을 선택합니다. **[!UICONTROL Email address]** 또는 **[!UICONTROL Domain address]**.

1. 전자 메일을 보낼 전자 메일 주소 또는 도메인을 입력합니다.

   >[!NOTE]
   >
   >올바른 이메일 주소(예: abc@company.com) 또는 도메인(예: abc.company.com)을 입력해야 합니다.

1. 필요한 경우 이유를 지정합니다.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >32-126 사이의 모든 ASCII 문자는 **[!UICONTROL Reason]** 필드. 전체 목록은 [이 페이지](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)예를 들어 {target=&quot;_blank&quot;} 입니다.

1. **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

### API 호출을 사용하여 엔티티 추가 {#api-call-allowed-list}

허용 목록을 채우기 위해 `ALLOWED` 값 `listType` 속성을 사용합니다. 예:

![](assets/allow-list-api.png)

다음을 수행할 수 있습니다 **추가**, **삭제** 및 **Get** 작업.

에서 API 호출을 작성하는 방법에 대해 자세히 알아보십시오 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;} 참조 설명서입니다.

## 허용 목록 논리 {#logic}

허용 목록이 [활성](#enable-allow-list), 다음 논리가 적용됩니다.

* 허용 목록이 **비어 있음**: 이메일을 전송하지 않습니다.

* 엔티티가 **허용 목록**&#x200B;제외 목록에 없으면 이메일이 해당 수신자에게 전송됩니다. 그러나 엔티티가 [제외 목록](../reports/suppression-list.md)로 설정되면 해당 수신자가 이메일을 받지 못합니다. 이유 **[!UICONTROL Suppressed]**.

* 엔티티가 **허용 목록에 없음** (또한 제외 목록에 없음) 해당 수신자가 이메일을 받지 못하므로 해당 수신자가 **[!UICONTROL Not allowed]**.

>[!NOTE]
>
>다음 포함 **[!UICONTROL Not allowed]** 상태는 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서** 은(는) 이러한 프로필을 여정을 통해 이동했음을 나타냅니다([세그먼트 읽기](../building-journeys/read-segment.md) 및 [메시지 활동](../building-journeys/journeys-message.md)), **이메일 보고서** 에는 이러한 매개 변수가 포함되지 않습니다. **[!UICONTROL Sent]** 지표는 이메일 전송 전에 필터링됩니다.
>
>추가 정보 [라이브 보고서](../reports/live-report.md) 및 [글로벌 보고서](../reports/global-report.md).

허용 목록이 [비활성화됨](#deactivate-allow-list), 현재 샌드박스에서 보내는 모든 이메일은 실제 고객 주소를 포함하여 모든 수신자(제외 목록에 없는 경우)에게 전송됩니다.

## 제외 보고 {#reporting}

허용 목록이 활성화되면 허용 목록에 없어서 전송에서 제외된 이메일 주소 또는 도메인을 검색할 수 있습니다. 이렇게 하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} 를 사용하여 아래 API를 호출할 수 있습니다.

를 가져오려면 **이메일 수** 수신자가 허용 목록에 없어서 전송되지 않은 경우 다음 쿼리를 사용하십시오.

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

를 가져오려면 **이메일 주소 목록** 수신자가 허용 목록에 없어서 전송되지 않은 경우 다음 쿼리를 사용하십시오.

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
