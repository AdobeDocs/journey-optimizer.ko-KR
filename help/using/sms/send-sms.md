---
solution: Journey Optimizer
product: journey optimizer
title: SMS 메시지 미리 보기 및 테스트
description: Journey Optimizer에서 SMS 메시지를 미리 보고 테스트하는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# SMS 메시지 미리 보기 및 테스트 {#send-sms}

## SMS 미리 보기 {#preview-sms}

메시지가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 사용하여 이 콘텐츠가 메시지에 표시되는 방식을 확인할 수 있습니다.

1. 클릭 **[!UICONTROL 컨텐츠 시뮬레이션]**.

1. 클릭 **[!UICONTROL 테스트 프로필 관리]** 테스트 프로필을 추가하려면

1. 를 사용하여 테스트 프로필 찾기 **[!UICONTROL ID 네임스페이스]** 및 **[!UICONTROL ID 값]** 필드. 그런 다음 **[!UICONTROL 프로필 추가]**.

   ![](assets/sms_preview_3.png)

1. 테스트 프로필을 선택한 후에는 **[!UICONTROL 테스트 프로필 추가]** 창을 엽니다.

1. 에서 **미리 보기 및 테스트** 창의 테스트 프로필 데이터가 메시지 콘텐츠에 추가됩니다.

   ![](assets/sms_preview_2.png)


## SMS의 유효성 검사{#sms-validate}

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 다음 두 가지 유형의 경고가 발생할 수 있습니다. 경고 및 오류입니다.

* **경고** 권장 사항 및 우수 사례를 참조하십시오. 예를 들어 SMS 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류** 확인되지 않는 한 여정을 테스트하거나 활성화하거나 캠페인을 게시할 수 없습니다. 예를 들어, 제목 줄이 누락된 경우 오류 메시지가 표시됩니다.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 게재 능력을 향상하려면 공급자가 지원하는 형식으로 전화 번호를 사용하십시오. 예를 들어, Twilio 및 Sinch는 E.164 형식의 전화 번호만 지원합니다.

## SMS 보내기{#sms-send}

SMS 메시지가 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md) 전송하기 위해

**관련 항목**

* [SMS 채널 구성](sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [SMS 메시지 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
