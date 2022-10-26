---
solution: Journey Optimizer
product: journey optimizer
title: SMS 메시지 만들기
description: Journey Optimizer에서 SMS 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 13%

---

# SMS 메시지 만들기 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS 만들기"
>abstract="텍스트 메시지를 추가하고 표현식 편집기를 사용하여 개인화를 시작합니다."

사용 [!DNL Journey Optimizer] 을 눌러 모바일 장치에서 고객에게 텍스트 메시지를 보냅니다. SMS 편집기에서 텍스트 형식으로 메시지를 만들고, 개인화하고, 미리 볼 수 있습니다.

>[!NOTE]
>
>업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. [옵트아웃을 관리하는 방법 알아보기](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

SMS 게재를 만들 수 있습니다.

* 다음 **여정**: 여정에 SMS 활동을 추가하고 기본 설정을 정의하면, **[!UICONTROL 작업: SMS]** 오른쪽 창에서 SMS 메시지의 콘텐츠를 작성합니다.

   여정 구성 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../building-journeys/journey-gs.md).

* 다음 **캠페인**: 캠페인을 만든 후 SMS를 작업으로 선택하고 기본 설정을 정의합니다.

   캠페인 구성 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../campaigns/create-campaign.md#configure).

SMS 메시지를 처음 만드는 경우 SMS 채널이 구성되었는지 확인하십시오. [자세히 알아보기](../configuration/sms-configuration.md).

## SMS 콘텐츠 정의{#sms-content}

SMS 메시지 개인화를 시작하려면 다음 단계를 수행합니다.

1. 을(를) 클릭합니다. **[!UICONTROL 메시지]** 필드 를 클릭하여 표현식 편집기를 엽니다.

   ![](assets/sms-content.png)

1. 표현식 편집기를 사용하여 컨텐츠를 정의하고 동적 컨텐츠를 추가합니다. 프로필 이름 또는 구/군/시 등의 속성을 사용할 수 있습니다. 추가 정보 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md) 를 입력합니다.

1. 클릭 **[!UICONTROL 저장]** 미리 보기에서 메시지를 확인합니다.

   ![](assets/sms-content-preview.png)

## SMS의 유효성 검사{#sms-preview}

>[!NOTE]
>
> 보다 나은 게재 능력을 위해 항상 공급자가 지원하는 형식으로 전화 번호를 사용해야 합니다. 예를 들어, Twilio 및 Sinch는 E.164 형식의 전화 번호만 지원합니다.

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 삽입한 경우 [개인화된 콘텐츠](../personalization/personalize.md)테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

모바일 장치에서 SMS 메시지가 표시되는 방식을 시각화하려면, **[!UICONTROL 컨텐츠 시뮬레이션]** 탭. 에서 콘텐츠 시뮬레이션에 대해 자세히 알아보기 [이 섹션](../design/preview.md).

편집기의 상단 섹션에서도 경고를 확인해야 합니다.  일부 경고는 간단한 경고이지만 일부 사용자는 메시지를 사용하지 못하도록 할 수 있습니다. 자세한 내용은 [이 섹션](alerts.md)을 참조하십시오.

![](assets/sms-alert-button.png)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**관련 항목**

* [SMS 채널 구성](../configuration/sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [새 메시지 만들기](get-started-content.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
