---
solution: Journey Optimizer
product: journey optimizer
title: SMS Webhook 구성
description: 옵트인 및 옵트아웃 동의 관리를 위한 인바운드 응답을 캡처하도록 웹후크를 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: a0f3e385-934d-44d6-a487-6035161aef0e
source-git-commit: 2bd0048c356c668ce2611b923f126e2a4e2c8630
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# 웹후크 만들기 {#webhook}

>[!BEGINSHADEBOX]

옵트인 또는 옵트아웃 키워드가 제공되지 않으면 표준 동의 메시지가 사용자 개인 정보를 보장하는 데 사용됩니다. 사용자 지정 키워드를 추가하면 기본값이 자동으로 재정의됩니다.

**기본 키워드:**

* **옵트인**: 구독, 예, 중지 취소, 시작, 계속, 다시 시작, 시작
* **옵트아웃**: 중지, 종료, 취소, 종료, 구독 취소, 아니요
* **도움말**: 도움말

>[!ENDSHADEBOX]

API 자격 증명이 정상적으로 생성되면 이제 옵트인 및 옵트아웃 동의 관리를 위한 인바운드 응답을 캡처하고, 사용 가능한 경우 읽기 확인을 포함한 게재 보고서를 수신하도록 웹후크를 구성할 수 있습니다.

웹후크를 설정할 때 캡처할 데이터 유형을 기반으로 용도를 정의할 수 있습니다.

* **[!UICONTROL 인바운드]**: 옵트인 또는 옵트아웃과 같은 동의 응답을 캡처하고 사용자 환경 설정을 수집하려면 이 옵션을 사용합니다.

* **[!UICONTROL 피드백]**: 보고 및 분석을 지원하기 위해 읽기 확인 및 사용자 상호 작용을 포함한 게재 및 참여 이벤트를 추적하려면 이 옵션을 선택하십시오.

SMS 공급자에 따라 아래 탭을 탐색합니다.

>[!BEGINTABS]

>[!TAB 사용자 지정]

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동하고 **[!UICONTROL SMS 설정]**&#x200B;에서 **[!UICONTROL SMS 웹후크]** 메뉴를 선택한 다음 **[!UICONTROL 웹후크 만들기]** 단추를 클릭합니다.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 아래에 자세히 설명된 대로 Webhook 설정을 구성합니다.

   * **[!UICONTROL 이름]**: Webhook의 이름을 입력하십시오.

   * **[!UICONTROL SMS 공급업체 선택]**: 사용자 지정.

   * **[!UICONTROL 유형]**: 인바운드.

   * **[!UICONTROL API 자격 증명]**: 드롭다운에서 [이전에 구성한 API 자격 증명](sms-configuration-custom.md#api-credential)을 선택합니다.

   * **[!UICONTROL 보낸 사람 전화 번호{&#x200B;1}: 통신에 사용할 보낸 사람 전화 번호&#x200B;을 입력합니다.]**

     ![](assets/webhook-inbound.png){zoomable="yes"}

1. ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하여 키워드 범주를 추가한 다음 SMS 공급자에 따라 구성합니다.

   * **[!UICONTROL 인바운드 키워드 범주]**: 키워드 범주를 **[!UICONTROL 옵트인]**, **[!UICONTROL 옵트아웃]**, **[!UICONTROL 이중 옵트인]**, **[!UICONTROL 도움말]** 또는 **[!UICONTROL 사용자 지정]** 중에서 선택합니다.

   * **[!UICONTROL 키워드 입력]**: 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드를 추가하려면 ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하십시오.

     **[!UICONTROL 사용자 지정 키워드]**&#x200B;의 경우 여정 내의 일괄 처리 기반 작업에 동의 없는 관련 키워드를 사용하십시오.

   * **[!UICONTROL 응답 메시지]**: 자동으로 전송되는 사용자 지정 응답을 드롭다운에서 선택합니다.

   * **[!UICONTROL 유사 옵트아웃]**: 거의 일치하는 옵트아웃 키워드가 검색되면 자동 회신을 보내도록 이 옵션을 활성화합니다.

   ![](assets/sms_byo_6.png){zoomable="yes"}

1. 인바운드 메시지가 구성된 키워드 또는 범주와 일치하지 않을 때 자동으로 보내는 **[!UICONTROL 기본 회신 메시지]**&#x200B;를 입력하십시오.

1. 요청 페이로드의 유효성을 검사하고 사용자 지정하려면 **[!UICONTROL 페이로드 편집기 보기]**&#x200B;를 클릭하십시오.

   프로필 속성을 사용하여 페이로드를 동적으로 개인화할 수 있으며, 내장된 도우미 함수를 사용하여 처리 및 응답 생성을 위해 정확한 데이터가 전송되도록 할 수 있습니다.

1. Webhook 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 피드백]** 웹후크를 만들려면 위와 동일한 단계를 수행하여 **[!UICONTROL 피드백]**&#x200B;을(를) 웹후크 **[!UICONTROL 유형]**(으)로 선택합니다.

1. **[!UICONTROL 웹후크]** 메뉴에서 기존 웹후크를 편집 또는 삭제하거나 SMS 공급자와 통합하기 위해 **[!UICONTROL 웹후크 URL]**&#x200B;에 액세스하고 복사할 수 있습니다.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Webhook에 대한 설정을 만들고 구성한 후에는 SMS 메시지에 대해 [채널 구성](sms-configuration-surface.md)을 만들어야 합니다.

구성하고 나면 메시지 작성, 개인화, 링크 추적 및 보고와 같은 기본 제공 채널 기능을 모두 활용할 수 있습니다.

>[!TAB Infobip]

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동하고 **[!UICONTROL SMS 설정]**&#x200B;에서 **[!UICONTROL SMS 웹후크]** 메뉴를 선택한 다음 **[!UICONTROL 웹후크 만들기]** 단추를 클릭합니다.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 아래에 자세히 설명된 대로 Webhook 설정을 구성합니다.

   * **[!UICONTROL 이름]**: Webhook의 이름을 입력하십시오.

   * **[!UICONTROL SMS 공급업체 선택]**: Infobip.

   * **[!UICONTROL 유형]**: 인바운드.

   * **[!UICONTROL API 자격 증명]**: 드롭다운에서 [이전에 구성한 API 자격 증명](sms-configuration-infobip.md#api-credential)을 선택합니다.

   * **[!UICONTROL 보낸 사람 전화 번호{&#x200B;1}: 통신에 사용할 보낸 사람 전화 번호&#x200B;을 입력합니다.]**

     ![](assets/webhook-infobip-1.png){zoomable="yes"}

1. ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하여 키워드 범주를 추가한 다음 SMS 공급자에 따라 구성합니다.

   * **[!UICONTROL 인바운드 키워드 범주]**: 키워드 범주를 **[!UICONTROL 옵트인]**, **[!UICONTROL 옵트아웃]**, **[!UICONTROL 이중 옵트인]**, **[!UICONTROL 도움말]** 또는 **[!UICONTROL 사용자 지정]** 중에서 선택합니다.

   * **[!UICONTROL 키워드 입력]**: 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드를 추가하려면 ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하십시오.

     **[!UICONTROL 사용자 지정 키워드]**&#x200B;의 경우 여정 내의 일괄 처리 기반 작업에 동의 없는 관련 키워드를 사용하십시오.

   * **[!UICONTROL 응답 메시지]**: 자동으로 전송되는 사용자 지정 응답을 드롭다운에서 선택합니다.

   * **[!UICONTROL 유사 옵트아웃]**: 거의 일치하는 옵트아웃 키워드가 검색되면 자동 회신을 보내도록 이 옵션을 활성화합니다.

   ![](assets/webhook-infobip-2.png){zoomable="yes"}

1. 인바운드 메시지가 구성된 키워드 또는 범주와 일치하지 않을 때 자동으로 보내는 **[!UICONTROL 기본 회신 메시지]**&#x200B;를 입력하십시오.

1. Webhook 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 피드백]** 웹후크를 만들려면 위와 동일한 단계를 수행하여 **[!UICONTROL 피드백]**&#x200B;을(를) 웹후크 **[!UICONTROL 유형]**(으)로 선택합니다.

1. **[!UICONTROL 웹후크]** 메뉴에서 기존 웹후크를 편집 또는 삭제하거나 SMS 공급자와 통합하기 위해 **[!UICONTROL 웹후크 URL]**&#x200B;에 액세스하고 복사할 수 있습니다.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Webhook에 대한 인바운드 설정을 만들고 구성한 후 SMS 메시지에 대해 [채널 구성](sms-configuration-surface.md)을 만들어야 합니다.

구성하고 나면 메시지 작성, 개인화, 링크 추적 및 보고와 같은 기본 제공 채널 기능을 모두 활용할 수 있습니다.

>[!TAB Sinch]

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동하고 **[!UICONTROL SMS 설정]**&#x200B;에서 **[!UICONTROL SMS 웹후크]** 메뉴를 선택한 다음 **[!UICONTROL 웹후크 만들기]** 단추를 클릭합니다.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. 아래에 자세히 설명된 대로 Webhook 설정을 구성합니다.

   * **[!UICONTROL 이름]**: Webhook의 이름을 입력하십시오.

   * **[!UICONTROL SMS 공급업체 선택]**: Sinch.

   * **[!UICONTROL 유형]**: 인바운드.

   * **[!UICONTROL API 자격 증명]**: 드롭다운에서 [이전에 구성한 API 자격 증명](sms-configuration-sinch.md#create-api)을 선택합니다.

   * **[!UICONTROL 보낸 사람 전화 번호{&#x200B;1}: 통신에 사용할 보낸 사람 전화 번호&#x200B;을 입력합니다.]**

     ![](assets/webhook-sinch-1.png){zoomable="yes"}

1. ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하여 키워드 범주를 추가한 다음 SMS 공급자에 따라 구성합니다.

   * **[!UICONTROL 인바운드 키워드 범주]**: 키워드 범주를 **[!UICONTROL 옵트인]**, **[!UICONTROL 옵트아웃]**, **[!UICONTROL 이중 옵트인]**, **[!UICONTROL 도움말]** 또는 **[!UICONTROL 사용자 지정]** 중에서 선택합니다.

   * **[!UICONTROL 키워드 입력]**: 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드를 추가하려면 ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하십시오.

     **[!UICONTROL 사용자 지정 키워드]**&#x200B;의 경우 여정 내의 일괄 처리 기반 작업에 동의 없는 관련 키워드를 사용하십시오.

   * **[!UICONTROL 응답 메시지]**: 자동으로 전송되는 사용자 지정 응답을 드롭다운에서 선택합니다.

   * **[!UICONTROL 유사 옵트아웃]**: 거의 일치하는 옵트아웃 키워드가 검색되면 자동 회신을 보내도록 이 옵션을 활성화합니다.

   ![](assets/webhook-sinch-2.png){zoomable="yes"}

1. 인바운드 메시지가 구성된 키워드 또는 범주와 일치하지 않을 때 자동으로 보내는 **[!UICONTROL 기본 회신 메시지]**&#x200B;를 입력하십시오.

1. Webhook 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL Webhooks]** 메뉴에서 ![bin 아이콘](assets/do-not-localize/Smock_Delete_18_N.svg)을 클릭하여 Webhook을 삭제합니다.

1. 기존 구성을 수정하려면 원하는 웹후크를 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 내용을 변경합니다.

1. 이전에 제출한 **[!UICONTROL Webhook]**&#x200B;에서 새 **[!UICONTROL Webhook URL]**&#x200B;에 액세스하여 복사합니다.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Webhook에 대한 인바운드 설정을 만들고 구성한 후 SMS 메시지에 대해 [채널 구성](sms-configuration-surface.md)을 만들어야 합니다.

구성하고 나면 메시지 작성, 개인화, 링크 추적 및 보고와 같은 기본 제공 채널 기능을 모두 활용할 수 있습니다.

<!--
>[!TAB Twilio]

1. In the left rail, navigate to **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]**, select the **[!UICONTROL SMS Webhooks]** menu under **[!UICONTROL SMS settings]**, and click the **[!UICONTROL Create Webhook]** button.

    ![](assets/sms_byo_5.png){zoomable="yes"}

1. Configure your Webhook Settings, as detailed below:

    * **[!UICONTROL Name]**: Enter a name for your Webhook.

    * **[!UICONTROL Select SMS vendor]**: Twilio.

    * **[!UICONTROL Type]**: Inbound.

    * **[!UICONTROL API credentials]**: Choose from the drop-down you [previously configured API credentials](sms-configuration-twilio.md#create-api).

    * **[!UICONTROL Sender Phone Number ​]**: Enter the Sender phone number ​you want to use for your communications.
        
1. Click ![](assets/do-not-localize/Smock_Add_18_N.svg) to add your keywords categories, then, configure them depending on your SMS provider:

    * **[!UICONTROL Inbound Keyword Category]**: Choose your keyword categories either **[!UICONTROL Opt-In]**, **[!UICONTROL Opt-Out]**, **[!UICONTROL Double Opt-In]**, **[!UICONTROL Help]** or **[!UICONTROL Custom]**. 

    * **[!UICONTROL Enter a keyword]**: Enter the default or custom keywords that will automatically trigger your message. Click ![](assets/do-not-localize/Smock_Add_18_N.svg) to add multiple keywords.

        For **[!UICONTROL Custom keyword]**, use non-consent–related keywords for batch-based actions within a journey.

    * **[!UICONTROL Reply Message]**: Select from the drop-down the custom response that is automatically sent.

    * **[!UICONTROL Fuzzy Opt-out]**: Enable this option to send an automatic reply when a near-match opt-out keyword is detected.

1. Enter a **[!UICONTROL Default Reply Message]** automatically sent when an inbound message does not match any configured keyword or category.

1. Click **[!UICONTROL Submit]** when you finished the configuration of your Webhook.

1. In the **[!UICONTROL Webhooks]** menu, click the ![bin icon](assets/do-not-localize/Smock_Delete_18_N.svg) to delete your Webhook.

1. To modify existing configuration, locate the desired Webhook and click the **[!UICONTROL Edit]** option to make the necessary changes.

1. Access and copy your new **[!UICONTROL Webhook URL]** from your previously submitted **[!UICONTROL Webhook]**.

After creating and configuring the inbound settings for the Webhook, you now need to create a [channel configuration](sms-configuration-surface.md) for SMS messages. 

Once configured, you can leverage all out-of-the-box channel capabilities such as message authoring, personalization, link tracking, and reporting.
-->

>[!ENDTABS]


## 사용 방법 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
