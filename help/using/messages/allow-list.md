---
title: 허용 목록
description: 허용 목록 사용 방법을 알아봅니다.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 4%

---

# 허용 목록 {#allow-list}

이제 에서 특정 전송 안전 목록을 정의할 수 있습니다 [샌드박스](../administration/sandboxes.md) 레벨, 테스트 목적으로 안전한 환경 실수가 발생할 수 있는 비프로덕션 인스턴스에서 허용 목록을 사용하면 고객에게 원치 않는 메시지를 보낼 위험이 없습니다.

허용 목록을 사용하면 특정 샌드박스에서 보내는 이메일을 받을 수 있는 권한이 있는 유일한 수신자 또는 도메인이 되는 개별 이메일 주소 또는 도메인을 지정할 수 있습니다. 따라서 테스트 환경에 있을 때 실수로 실제 고객 주소로 이메일을 보내지 않을 수 있습니다.

>[!CAUTION]
>
>이 기능은 다음과 같습니다 **not** 프로덕션 샌드박스에서 사용할 수 있습니다. 이메일 채널에만 적용됩니다.

## 허용 목록 활성화 {#enable-allow-list}

비프로덕션 샌드박스에서 허용 목록을 활성화하려면 메시지 사전 설정 서비스에서 해당 API 종료 지점을 사용하여 일반 설정을 업데이트해야 합니다.

* 이 API를 사용하면 언제든지 기능을 비활성화할 수도 있습니다.

* 기능을 활성화하기 전이나 후에 허용 목록을 업데이트할 수 있습니다.

* 기능이 활성화되어 있으면 허용 목록 논리가 적용됩니다 **및** 허용 목록이 **not** 비어 있습니다. 추가 정보 [이 섹션](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>활성화되면 여정을 실행할 때 허용 목록 기능이 허용되지만 [증명](preview.md#send-proofs) 및 를 사용하여 여정 테스트 [테스트 모드](../building-journeys/testing-the-journey.md).

## 허용 목록에 엔티티 추가 {#add-entities}

특정 샌드박스의 허용 목록에 새 이메일 주소 또는 도메인을 추가하려면 `ALLOWED` 값 `listType` 속성을 사용합니다. 예:

![](assets/allow-list-api.png)

다음을 수행할 수 있습니다 **추가**, **삭제** 및 **Get** 작업.

>[!NOTE]
>
>허용 목록은 최대 1,000개의 항목을 포함할 수 있습니다.

에서 API 호출을 작성하는 방법에 대해 자세히 알아보십시오 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;} 참조 설명서입니다.

## 허용 목록 논리 {#logic}

허용 목록이 **비어 있음**&#x200B;인 경우 허용 목록 논리가 적용되지 않습니다. 즉, 프로필에 게시되지 않은 경우 모든 프로필에 이메일을 보낼 수 있습니다 [제외 목록](suppression-list.md).

허용 목록이 **비어 있지 않음**&#x200B;로 지정하는 경우 허용 목록 논리가 적용됩니다.

* 엔티티가 **허용 목록에 없음**, 억제 목록이 아니라 해당 수신자가 이메일을 받지 못하므로 해당 수신자가 **[!UICONTROL Not allowed]**.

* 엔티티가 **허용 목록**&#x200B;제외 목록에서 제외하는 경우에는 해당 수신자에게 이메일을 보낼 수 있습니다. 그러나 엔티티가 [제외 목록](suppression-list.md)로 설정되면 해당 수신자가 전자 메일을 받지 않습니다. 그 이유는 다음과 같습니다 **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>다음 포함 **[!UICONTROL Not allowed]** 상태는 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서** 은(는) 이러한 프로필을 여정을 통해 이동했음을 나타냅니다([세그먼트 읽기](../building-journeys/read-segment.md) 및 [메시지](../building-journeys/journeys-message.md) 활동), **이메일 보고서** 에는 이러한 매개 변수가 포함되지 않습니다. **[!UICONTROL Sent]** 지표는 이메일 전송 전에 필터링됩니다.
>
>추가 정보 [라이브 보고서](../reports/live-report.md) 및 [글로벌 보고서](../reports/global-report.md).

## 제외 보고 {#reporting}

비프로덕션 샌드박스에서 이 기능을 활성화하면 허용 목록에 없어서 전송에서 제외된 이메일 주소 또는 도메인을 검색할 수 있습니다. 이렇게 하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} 를 사용하여 아래 API를 호출할 수 있습니다.

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
