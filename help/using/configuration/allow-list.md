---
solution: Journey Optimizer
product: journey optimizer
title: 허용 목록
description: 허용 목록 사용 방법 알아보기
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: 허용 목록, 목록, 안전, 구성
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 6%

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

허용되는 이메일 주소 및 도메인의 세부 목록에 액세스하려면 다음 위치로 이동하십시오. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]**, 을(를) 선택하고 을(를) 선택합니다. **[!UICONTROL 허용 목록]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>허용 목록 보기, 내보내기 및 관리를 위한 권한은 [여정 관리자](../administration/ootb-product-profiles.md#journey-administrator). 관리에 대해 자세히 알아보기 [!DNL Journey Optimizer] 사용자 액세스 권한 [이 섹션](../administration/permissions-overview.md).

허용 목록을 CSV 파일로 내보내려면 **[!UICONTROL CSV 다운로드]** 버튼을 클릭합니다.

를 사용하십시오 **[!UICONTROL 삭제]** 단추를 클릭하여 항목을 영구적으로 제거합니다.

이메일 주소 또는 도메인을 검색하고 **[!UICONTROL 주소 유형]**. 선택한 후에는 목록 위에 표시된 필터를 지울 수 있습니다.

![](assets/allowed-list-filtering-example.png)

## 허용 목록 활성화 {#enable-allow-list}

허용 목록을 활성화하려면 아래 단계를 수행하십시오.

1. 액세스 권한  **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]** > **[!UICONTROL 허용 목록]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 전환 단추를 선택합니다.

   ![](assets/allow-list-edit.png)

1. 선택 **[!UICONTROL 허용 목록 활성화]**. 이제 허용 목록이 활성 상태입니다.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >허용 목록을 활성화한 후 여정 및 캠페인에서가 적용되기 위한 5분 지연이 있습니다.

허용 목록 논리는 기능이 활성 상태일 때 적용됩니다. 자세한 내용은 [이 섹션](#logic)을 참조하십시오.

>[!NOTE]
>
>활성화되면 여정을 실행할 때에도 허용 목록 기능이 적용되지만 [증명](../email/preview.md#send-proofs) 및 를 사용하여 여정 테스트 [테스트 모드](../building-journeys/testing-the-journey.md).

## 허용 목록 비활성화 {#deactivate-allow-list}

허용 목록을 비활성화하려면 아래 단계를 수행하십시오.

1. 액세스 권한  **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]** > **[!UICONTROL 허용 목록]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 전환 단추를 선택합니다.

   ![](assets/allow-list-edit-active.png)

1. 선택 **[!UICONTROL 허용 목록 비활성화]**. 허용 목록이 더 이상 활성 상태가 아닙니다.

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
>id="ajo_admin_allowed_list_add_header"
>title="허용 목록에 주소 또는 도메인 추가"
>abstract="새 이메일 주소 또는 도메인을 하나씩 선택하여 허용 목록에 수동으로 추가할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="허용 목록에 주소 또는 도메인 추가"
>abstract="새 이메일 주소 또는 도메인을 하나씩 선택하여 허용 목록에 수동으로 추가할 수 있습니다."

수동으로 [!DNL Journey Optimizer] 사용자 인터페이스를 통해 이메일 주소 또는 도메인을 추가하여 허용 목록.

>[!NOTE]
>
>한 번에 하나의 이메일 주소나 도메인만 추가할 수 있습니다.

이렇게 하려면 아래 단계를 수행합니다.

1. 을(를) 선택합니다 **[!UICONTROL 이메일 또는 도메인 추가]** 버튼을 클릭합니다.

   ![](assets/allowed-list-add-email.png)

1. 주소 유형을 선택합니다. **[!UICONTROL 이메일 주소]** 또는 **[!UICONTROL 도메인 주소]**.

1. 전자 메일을 보낼 전자 메일 주소 또는 도메인을 입력합니다.

   >[!NOTE]
   >
   >유효한 이메일 주소(예: abc@company.com) 또는 도메인(예: abc.company.com)을 입력했는지 확인합니다.

1. 필요한 경우 이유를 지정합니다.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >32-126 사이의 모든 ASCII 문자는 **[!UICONTROL 이유]** 필드. 전체 목록은 [이 페이지](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}에서 확인할 수 있습니다.

1. **[!UICONTROL 제출을 클릭합니다]**.

### API 호출을 사용하여 엔티티 추가 {#api-call-allowed-list}

허용 목록을 채우기 위해 `ALLOWED` 값 `listType` 속성을 사용합니다. 예:

![](assets/allow-list-api.png)

다음을 수행할 수 있습니다 **추가**, **삭제** 및 **Get** 작업.

에서 API 호출을 작성하는 방법에 대해 자세히 알아보십시오 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} 참조 설명서.

## 허용 목록 다운로드 {#download-allowed-list}

허용 목록을 CSV 파일로 내보내려면 아래 단계를 수행하십시오.

1. 을(를) 선택합니다 **[!UICONTROL CSV 다운로드]** 버튼을 클릭합니다.

   ![](assets/allowed-list-download-csv.png)

1. 파일이 생성될 때까지 기다립니다.

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >다운로드 시간은 파일 크기에 따라 다릅니다. 즉, 허용 목록에 있는 주소 수입니다.
   >
   >지정된 샌드박스에 대해 한 번에 하나의 다운로드 요청을 처리할 수 있습니다.

1. 파일이 생성되면 알림을 받게 됩니다. 화면 오른쪽 위의 벨 아이콘을 클릭하여 표시합니다.

1. 알림 자체를 클릭하여 파일을 다운로드합니다.

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >링크는 24시간 동안 유효합니다.

## 허용 목록 논리 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="허용 목록 관리"
>abstract="허용 목록이 활성화되면 허용 목록에 포함된 수신자만 이 샌드박스에서 이메일 메시지를 수신하게 됩니다. 비활성화되면 모든 수신자는 이메일을 수신하게 됩니다."

허용 목록이 [활성](#enable-allow-list), 다음 논리가 적용됩니다.

* 허용 목록이 **비어 있음**: 이메일을 전송하지 않습니다.

* 엔티티가 **허용 목록**&#x200B;제외 목록에 없으면 이메일이 해당 수신자에게 전송됩니다. 그러나 엔티티가 [제외 목록](../reports/suppression-list.md)로 설정되면 해당 수신자가 이메일을 받지 못합니다. 이유 **[!UICONTROL 억제됨]**.

* 엔티티가 **허용 목록에 없음** (또한 제외 목록에 없음) 해당 수신자가 이메일을 받지 못하므로 해당 수신자가 **[!UICONTROL 허용되지 않음]**.

>[!NOTE]
>
>다음 포함 **[!UICONTROL 허용되지 않음]** 상태는 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서** 은(는) 이러한 프로필을 여정을 통해 이동했음을 나타냅니다([세그먼트 읽기](../building-journeys/read-segment.md) 및 [메시지 활동](../building-journeys/journeys-message.md)), **이메일 보고서** 에는 이러한 매개 변수가 포함되지 않습니다. **[!UICONTROL 전송]** 지표는 이메일 전송 전에 필터링됩니다.
>
>추가 정보 [라이브 보고서](../reports/live-report.md) 및 [글로벌 보고서](../reports/global-report.md).

허용 목록이 [비활성화됨](#deactivate-allow-list), 현재 샌드박스에서 보내는 모든 이메일은 실제 고객 주소를 포함하여 모든 수신자(제외 목록에 없는 경우)에게 전송됩니다.

## 제외 보고 {#reporting}

허용 목록이 활성화되면 허용 목록에 없어서 전송에서 제외된 이메일 주소 또는 도메인을 검색할 수 있습니다. 이렇게 하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} 아래에 API를 호출하십시오.

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
