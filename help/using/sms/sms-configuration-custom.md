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
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# 사용자 정의 공급자 구성 {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="공급자 URL"
>abstract="외부 API에 연결할 URL을 지정합니다. 이 URL은 API의 기능과 기능에 접근하는 엔드포인트로 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="인증 유형"
>abstract="API에 액세스하는 데 필요한 인증 방법(OAuth 또는 Bearer 토큰)을 지정합니다. 이를 통해 외부 서비스와의 안전하고 승인된 통신이 보장됩니다."

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
>
>이 Beta은 옵트인/옵트아웃 동의 관리 및 게재 보고에 대한 인바운드 메시지를 지원하지 않습니다.

Adobe에서 즉시 사용할 수 없는 사용자 지정 공급자(예: Sinch, Infobip, Twilio)를 사용하여 Journey Optimizer에서 메시지를 보내려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택합니다.

1. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_byo_1.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: 사용자 지정입니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 입력하십시오.

   * **[!UICONTROL 공급자 AppId]**: SMS 공급자가 제공한 응용 프로그램 ID를 입력하십시오.

   * **[!UICONTROL 공급자 이름]**: SMS 공급자의 이름을 입력하십시오.

   * **[!UICONTROL 공급자 URL]**: SMS 공급자의 URL을 입력하십시오.

   * **[!UICONTROL 인증 유형{&#x200B;1}: 인증 유형을 선택합니다.]** 지원되는 인증 유형은 **Bearer App** 또는 **Basic**&#x200B;입니다.

   * **[!UICONTROL API 토큰]**: SMS 공급자가 제공한 API 토큰을 입력하십시오.

   * **[!UICONTROL 공급자 페이로드]**: 공급자 페이로드(예: `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`)를 추가하십시오.

     페이로드에 `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`이(가) 포함되어 있는지 확인하십시오.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

구성하고 나면 메시지 작성, 개인화, 링크 추적 및 보고와 같은 기본 제공 채널 기능을 모두 활용할 수 있습니다.

## 사용 방법 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
