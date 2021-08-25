---
title: 허용 목록
description: 허용 목록 사용 방법을 알아봅니다.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 2edb3535c50f83d18ce4d6429a6d76f44b694ac6
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# 허용 목록 {#allow-list}

이제 [sandbox](administration/sandboxes.md) 수준에서 특정 전송 안전 목록을 정의하여 테스트 목적으로 안전한 환경을 가질 수 있습니다. 허용 목록이 실수가 발생할 수 있는 비프로덕션 인스턴스에서 고객에게 원치 않는 메시지를 보낼 위험이 없습니다.

허용 목록을 사용하면 특정 샌드박스에서 보내는 이메일을 받을 수 있는 권한이 있는 유일한 수신자 또는 도메인이 되는 개별 이메일 주소 또는 도메인을 지정할 수 있습니다. 따라서 테스트 환경에 있을 때 실수로 실제 고객 주소로 이메일을 보내지 않을 수 있습니다.

>[!CAUTION]
>
>이 기능은 프로덕션 샌드박스에서 사용할 수 있는 **이 아닙니다.** 이메일 채널에만 적용됩니다.

## 허용 목록 활성화 {#enable-allow-list}

비프로덕션 샌드박스에서 허용 목록을 활성화하려면 메시지 사전 설정 서비스에서 해당 API 종료 지점을 사용하여 일반 설정을 업데이트해야 합니다.

* 이 API를 사용하면 언제든지 기능을 비활성화할 수도 있습니다.

* 기능을 활성화하기 전이나 후에 허용 목록을 업데이트할 수 있습니다.

* 허용 목록 로직은 기능이 활성화될 때 **및** 허용 목록이 비어 있지 않은 경우 적용됩니다.**비어 있지 않은 경우** 자세한 내용은 [이 섹션](#logic)을 참조하십시오.

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>활성화되면 여정을 실행할 때 허용 목록 기능이 적용되지만 [증명](preview.md#send-proofs)으로 메시지를 테스트하고 [테스트 모드](building-journeys/testing-the-journey.md)를 사용하여 여정을 테스트할 때에도 이 기능이 적용됩니다.

## 허용 목록에 엔티티 추가 {#add-entities}

특정 샌드박스의 허용 목록에 새 이메일 주소 또는 도메인을 추가하려면 `listType` 속성에 대해 `ALLOWED` 값이 있는 제외 API를 호출해야 합니다. 예:

![](assets/allow-list-api.png)

**추가**, **삭제** 및 **Get** 작업을 수행할 수 있습니다.

>[!NOTE]
>
>허용 목록은 최대 1,000개의 항목을 포함할 수 있습니다.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 허용 목록 논리 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

허용 목록이 **비어 있으면 허용 목록 논리가 적용되지 않습니다.** 즉, [제외 목록](suppression-list.md)에 없는 경우 모든 프로필에 이메일을 보낼 수 있습니다.

허용 목록이 **비어 있지 않으면 허용 목록 논리가 적용됩니다.**

* 엔티티가 허용 목록&#x200B;**에 없고 제외 목록에 없는**&#x200B;인 경우 해당 수신자는 이메일을 받지 못합니다. 이유는 **[!UICONTROL Not allowed]**.

* 엔티티가 허용 목록&#x200B;**에서**&#x200B;이고 제외 목록에 없으면 이메일을 해당 수신자에게 보낼 수 있습니다. 그러나 엔티티가 [제외 목록](suppression-list.md)에도 있는 경우 해당 수신자가 이메일을 받지 못합니다. 이유는 **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>**[!UICONTROL Not allowed]** 상태가 있는 프로필은 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서**&#x200B;는 여정([세그먼트 읽기](building-journeys/read-segment.md) 및 [메시지](building-journeys/journeys-message.md) 활동)를 통해 이동한 것으로 표시되지만 **이메일 보고서**&#x200B;는 전자 메일 보내기 전에 필터링되므로 이 프로필을 **[!UICONTROL Sent]** 지표에 포함하지 않습니다.
>
>[라이브 보고서](reports/live-report.md) 및 [글로벌 보고서](reports/global-report.md)에 대해 자세히 알아보십시오.

## 제외 보고 {#reporting}

비프로덕션 샌드박스에서 이 기능을 활성화하면 허용 목록에 없어서 전송에서 제외된 이메일 주소 또는 도메인을 검색할 수 있습니다. 이렇게 하려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html)를 사용하여 아래에서 API를 호출할 수 있습니다.

수신자가 허용 목록에 없어서 전송되지 않은 **개의 전자 메일**&#x200B;을(를) 가져오려면 다음 쿼리를 사용하십시오.

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

수신자가 허용 목록에 없어서 전송되지 않은 **전자 메일 주소 목록을 가져오려면 다음 쿼리를 사용하십시오.**

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

