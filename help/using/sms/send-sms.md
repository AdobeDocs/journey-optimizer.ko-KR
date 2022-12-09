---
solution: Journey Optimizer
product: journey optimizer
title: SMS 메시지 미리 보기
description: Journey Optimizer에서 SMS 메시지를 미리 보고 테스트하는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# SMS 메시지 보내기 {#send-sms}

## SMS 메시지 미리 보기 {#preview-sms}

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 표시되는 방식을 확인할 수 있습니다.

1. 클릭 **[!UICONTROL Simulate content]**.

1. 클릭 **[!UICONTROL Manage test profiles]** 테스트 프로필을 추가하려면

1. 를 사용하여 테스트 프로필 찾기 **[!UICONTROL Identity namespace]** 및 **[!UICONTROL Identity value]** 필드. 그런 다음 **[!UICONTROL Add profile]**.

   ![](assets/sms_preview_3.png)

1. 테스트 프로필을 선택한 후에는 **[!UICONTROL Add test profile]** 창을 엽니다.

   ![](assets/sms_preview_1.png)

1. 미리 보기 및 테스트 창에서 테스트 프로필 데이터를 메시지 콘텐츠에서 활용합니다.

   예를 들어 이 SMS 메시지의 경우 두 메시지 콘텐츠가 모두 개인화됩니다.

   ![](assets/sms_preview_2.png)

## SMS의 유효성 검사{#sms-preview}

>[!NOTE]
>
> 보다 나은 게재 능력을 위해 항상 공급자가 지원하는 형식으로 전화 번호를 사용해야 합니다. 예를 들어, Twilio 및 Sinch는 E.164 형식의 전화 번호만 지원합니다.

편집기의 상단 섹션에서도 경고를 확인해야 합니다.  일부 경고는 간단한 경고이지만 일부 사용자는 메시지를 사용하지 못하도록 할 수 있습니다. 다음 두 가지 유형의 경고가 발생할 수 있습니다.

* **경고** 권장 사항 및 우수 사례를 참조하십시오. 예를 들어 SMS 메시지가 비어 있는 경우 메시지가 표시됩니다.

* **오류** 확인되지 않는 한 여정을 테스트하거나 활성화하지 않도록 합니다. 예를 들어 제목 줄이 누락되었다는 메시지가 표시됩니다.

![](assets/sms-alert-button.png)

SMS 메시지가 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md) 전송하기 위해

**관련 항목**

* [SMS 채널 구성](sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [SMS 메시지 만들기](create-sms.md)
* [여정에서 메시지 추가](../building-journeys/journeys-message.md)
