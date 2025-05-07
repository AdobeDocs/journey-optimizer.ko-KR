---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 정의 공급자 구성
description: 사용자 지정 공급자를 통해 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: fc78fcfb0f2ce3616cb8b1df44dda2cfd66262fe
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 9%

---

# 사용자 지정 SMS 공급자 구성 {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="공급자 URL"
>abstract="외부 API에 연결할 URL을 지정합니다. 이 URL은 API의 기능과 기능에 접근하는 엔드포인트로 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="헤더 매개변수"
>abstract="적절한 인증, 콘텐츠 형식 지정 및 효과적인 API 통신을 위해 추가 헤더의 레이블, 유형 및 값을 지정합니다. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="공급자 페이로드"
>abstract="올바른 데이터가 처리 및 응답 생성에 사용될 수 있도록 요청 페이로드를 제공합니다."

>[!AVAILABILITY]
>
>사용자 지정 공급자는 현재 선택한 사용자만 베타 버전으로 사용할 수 있습니다. Beta에 포함하려면 Adobe 담당자에게 문의하십시오.
>이 Beta은 옵트인/옵트아웃 동의 관리 및 게재 보고에 대한 인바운드 메시지를 지원하지 않습니다.


이 기능을 사용하면 자체 SMS 공급자를 통합 및 구성할 수 있으므로 기본 공급자(Sinch, Twilio 및 Infobip) 이상의 유연성을 제공합니다. 이를 통해 SMS 작성, 전달, 보고 및 동의 관리를 원활하게 수행할 수 있습니다.

SMS에 대한 사용자 정의 공급자 구성을 통해 다음을 수행할 수 있습니다.

* Journey Optimizer 내에서 직접 사용자 지정 SMS 공급자를 구성합니다.
* 다이내믹 메시징에 고급 페이로드 사용자 지정을 사용합니다.
* 동의 환경 설정(옵트인/옵트아웃)을 관리하여 규정 준수를 보장합니다.

## API 자격 증명 만들기 {#api-credential}

Adobe에서 즉시 사용할 수 없는 사용자 지정 공급자(예: Sinch, Infobip, Twilio)를 사용하여 Journey Optimizer에서 메시지를 보내려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동하고 **[!UICONTROL API 자격 증명]** 메뉴를 선택한 다음 **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_byo_1.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: 사용자 지정입니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 입력하십시오.

   * **[!UICONTROL 공급자 AppId]**: SMS 공급자가 제공한 응용 프로그램 ID를 입력하십시오.

   * **[!UICONTROL 공급자 이름]**: SMS 공급자의 이름을 입력하십시오.

   * **[!UICONTROL 공급자 URL]**: SMS 공급자의 URL을 입력하십시오.

   * **[!UICONTROL 인증 유형{&#x200B;1}: 인증 유형을 선택하고 [선택한 인증 방법에 따라 해당 필드를 완료](#auth-options)합니다.]**

     ![](assets/sms-byop.png)

1. **[!UICONTROL Headers]** 섹션에서 **[!UICONTROL 새 매개 변수 추가]**&#x200B;를 클릭하여 외부 서비스로 전송될 요청 메시지에 대한 HTTP 헤더를 지정합니다.

   **Content-Type** 및 **Charset** 헤더 필드는 기본적으로 설정되며 삭제할 수 없습니다.

   ![](assets/sms_byo_2.png)

1. **[!UICONTROL 공급자 페이로드]**&#x200B;를 추가하여 요청 페이로드의 유효성을 검사하고 사용자 지정합니다.

   프로필 속성을 사용하여 페이로드를 동적으로 개인화할 수 있으며, 내장된 도우미 함수를 사용하여 처리 및 응답 생성을 위해 정확한 데이터가 전송되도록 할 수 있습니다.
<!--
1. Add your **Inbound settings** to determine how your system handles incoming messages and subscriber preferences: 

    * **[!UICONTROL Inbound Webhook URL]**: Specify the endpoint URL where inbound messages (e.g. replies or new messages from users) are sent.
    * **[!UICONTROL Opt-in Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-In Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-in Message]**: Enter the custom response that is automatically sent as your Opt-In Message.
    * **[!UICONTROL Opt-out Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-Out Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-out Message]**: Enter the custom response that is automatically sent as your Opt-Out Message.
-->

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

   ![](assets/sms_byo_3.png)

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

   ![](assets/sms_byo_4.png)

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

구성하고 나면 메시지 작성, 개인화, 링크 추적 및 보고와 같은 기본 제공 채널 기능을 모두 활용할 수 있습니다.

### 사용자 지정 SMS 공급자에 대한 인증 옵션 {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="인증 유형"
>abstract="API에 액세스하는 데 필요한 인증 방법을 지정하십시오. 이렇게 하면 외부 서비스와 안전하고 승인된 통신을 수행할 수 있습니다."

>[!BEGINTABS]

>[!TAB API 키]

API 자격 증명이 만들어지면 API 키 인증에 필요한 필드를 작성합니다.

* **[!UICONTROL 이름]**&#x200B;: API 키 구성의 이름을 입력하십시오.
* **[!UICONTROL API 토큰]**&#x200B;: SMS 공급자가 제공한 API 토큰을 입력하십시오.

![](assets/sms-byop-api-key.png)

>[!TAB MAC 인증]

API 자격 증명이 만들어지면 MAC 인증에 필요한 필드를 작성합니다.

* **[!UICONTROL 이름]**&#x200B;: MAC 인증 구성의 이름을 입력하십시오.
* **[!UICONTROL API 토큰]**&#x200B;: SMS 공급자가 제공한 API 토큰을 입력하십시오.
* **[!UICONTROL API 암호 키]**: SMS 공급자가 제공한 API 암호 키를 입력하십시오. 이 키는 보안 통신을 위한 MAC(메시지 인증 코드)를 생성하는 데 사용됩니다.
* **[!UICONTROL Mac 인증 해시 형식]**: MAC 인증에 대한 해시 형식을 선택합니다.

![](assets/sms-byop-mac.png)

>[!TAB OAuth 인증]

API 자격 증명이 생성되면 OAuth 인증에 필요한 필드를 작성합니다.

* **[!UICONTROL 이름]**&#x200B;: OAuth 인증 구성의 이름을 입력합니다.

* **[!UICONTROL API 토큰]**&#x200B;: SMS 공급자가 제공한 API 토큰을 입력하십시오.

* **[!UICONTROL OAuth URL]**&#x200B;: OAuth 토큰을 가져올 URL을 입력합니다.

* **[!UICONTROL OAuth 본문]**&#x200B;: `grant_type`, `client_id` 및 `client_secret` 등의 매개 변수를 포함하여 JSON 형식으로 OAuth 요청 본문을 제공합니다.

![](assets/sms-byop-oauth.png)

>[!TAB JWT 인증]

API 자격 증명이 생성되면 JWT 인증에 필요한 필드를 작성합니다.

* **[!UICONTROL 이름]**&#x200B;: JWT 인증 구성의 이름을 입력하십시오.

* **[!UICONTROL API 토큰]**&#x200B;: SMS 공급자가 제공한 API 토큰을 입력하십시오.

* **[!UICONTROL JWT 페이로드]**&#x200B;: 발급자, 제목, 대상 및 만료와 같이 JWT에 필요한 클레임이 들어 있는 JSON 페이로드를 입력합니다.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## 사용 방법 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
