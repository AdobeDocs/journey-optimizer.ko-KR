---
solution: Journey Optimizer
product: journey optimizer
title: SMS 채널 구성
description: Journey Optimizer에서 SMS를 전송하도록 환경을 구성하는 방법 알아보기
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: e2851c97dd14577a992625bcfd60fc7300b432d3
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 17%

---

# SMS 채널 구성 {#sms-configuration}

[!DNL Journey Optimizer] 을(를) 통해 여정을 만들고 타겟팅된 대상자에게 메시지를 보낼 수 있습니다.

SMS를 보내기 전에 인스턴스를 구성합니다. 다음을 수행해야 합니다. [공급자 설정 통합](#create-api) Journey Optimizer 및 [sms 표면 만들기](#message-preset-sms) (예: SMS 사전 설정). 이 단계는 [Adobe Journey Optimizer 시스템 관리자](../start/path/administrator.md)가 수행해야 합니다.

## 전제 조건{#sms-prerequisites}

Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 독립적으로 SMS 서비스를 제공하는 Sinch, Twilio 및 Infobip과 같은 서드파티 공급자와 통합됩니다.

SMS를 구성하기 전에 이러한 SMS 공급자 중 하나로 계정을 만들어 API 토큰 및 서비스 ID를 받아야 Adobe Journey Optimizer과 해당 SMS 공급자 간의 연결을 설정할 수 있습니다.

SMS 서비스 사용에는 해당 SMS 공급자의 추가 약관이 적용됩니다. Sinch 및 Twilio가 통합을 통해 Adobe Journey Optimizer 사용자가 사용할 수 있는 서드파티 제품인 경우 SMS 서비스와 관련된 문제 또는 질문이 발생하면 Sinch 또는 Twilio 사용자는 해당 SMS 공급자에게 지원을 요청해야 합니다. Adobe은 타사 제품을 제어하지 않으며 책임도 지지 않습니다.

>[!CAUTION]
>
>SMS 하위 도메인에 액세스하고 편집하려면 **[!UICONTROL SMS 하위 도메인 관리]** 프로덕션 샌드박스에 대한 권한.

## 새 API 자격 증명 만들기 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Journey Optimizer로 SMS 공급업체 구성"
>abstract="공급업체를 선택하고 SMS API 자격 증명을 채웁니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Journey Optimizer로 SMS 공급업체 구성"
>abstract="SMS를 보내기 전에 공급자 설정을 Journey Optimizer와 통합해야 합니다. 완료되면 SMS 표면을 만들어야 합니다. 이 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=ko-KR#message-preset-sms" text="SMS 채널 표면 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="SMS 공급업체 구성 선택"
>abstract="SMS 공급업체에 맞게 구성된 API 자격 증명을 선택합니다."

Journey Optimizer을 사용하여 SMS 공급업체를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. SMS API 자격 증명을 구성합니다.

   * 대상 **[!DNL Sinch]**:

      * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

      * **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]**: API 페이지에 액세스하면 SMS 탭 아래에서 자격 증명을 찾을 수 있습니다.  [자세히 알아보기](https://developers.sinch.com/docs/sms/getting-started/)

      * **[!UICONTROL 옵트인 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트인 메시지]**.

      * **[!UICONTROL 도움말 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 도움말 메시지]**.

   * 대상 **[!DNL Twilio]**:

      * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

      * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]**: Twilio 콘솔 대시보드 페이지의 계정 정보 창에 액세스하여 자격 증명을 찾을 수 있습니다.

      * **[!UICONTROL 메시지 SID]**: Twilio의 API에서 만든 모든 메시지에 할당된 고유 식별자를 입력합니다. [자세히 알아보기](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-)

   * 대상 **[!DNL Infobip]**:

      * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

      * **[!UICONTROL API 기본 URL]** 및 **[!UICONTROL API 토큰]**: 웹 인터페이스 홈 페이지 또는 API 키 관리 페이지에 액세스하여 자격 증명을 찾을 수 있습니다. [자세히 알아보기](https://www.infobip.com/docs/api)

   ![](assets/sms_7.png)

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

## SMS 표면 만들기 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="SMS 범주 정의"
>abstract="이 표면을 사용하여 SMS 메시지 유형 선택: 사용자 동의가 필요한 프로모션 SMS 메시지를 위한 마케팅 또는 암호 재설정과 같은 비상업적 SMS 메시지를 위한 트랜잭션."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=ko-KR#sms-opt-out-management" text="마케팅 SMS 메시지 옵트아웃"

SMS 채널이 구성되면 SMS 메시지를 보낼 수 있는 채널 표면을 만들어야 합니다. **[!DNL Journey Optimizer]**.

채널 표면을 만들려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 표면]**. 다음을 클릭합니다. **[!UICONTROL 채널 표면 만들기]** 단추를 클릭합니다.

   ![](assets/preset-create.png)

1. 표면에 대한 이름과 설명(선택 사항)을 입력한 다음 SMS 채널을 선택합니다.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 다음을 정의합니다. **SMS 설정**.

   ![](assets/preset-sms.png)

   * 다음 항목 선택 **[!UICONTROL SMS 유형]** 이 데이터는 표면과 함께 전송됩니다. **[!UICONTROL 트랜잭션]** 또는 **[!UICONTROL 마케팅]**.

      * 선택 **마케팅** 프로모션 SMS의 경우: 이러한 메시지에는 사용자의 동의가 필요합니다.
      * 선택 **트랜잭션** 예를 들어 주문 확인, 암호 재설정 알림 또는 게재 정보와 같은 비상업적인 메시지의 경우.

     >[!CAUTION]
     >
     >**트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필에 SMS 메시지를 보낼 수 있습니다. 이러한 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

     SMS 메시지를 만들 때 메시지에 대해 선택한 카테고리와 일치하는 유효한 채널 표면을 선택해야 합니다.

   * 다음 항목 선택 **[!UICONTROL SMS 구성]** 서피스와 연관시킬 수 있습니다.

     SMS 메시지를 보내도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](#create-api).

   * 다음을 입력합니다. **[!UICONTROL 발신자 번호]** 통신&#x200B;에 을 사용하려고 합니다.

   * 다음 항목 선택 **[!UICONTROL SMS 실행 필드]** 을(를) 선택하려면 **[!UICONTROL 프로필 속성]** 프로필의 전화 번호와 연결됩니다.

1. SMS 메시지에서 URL 단축 기능을 사용하려면 **[!UICONTROL 하위 도메인]** 목록을 표시합니다.

   >[!NOTE]
   >
   >하위 도메인을 선택하려면 최소 하나 이상의 SMS 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](sms-subdomains.md)

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인할 수 있습니다. 채널 서피스를 구배로 저장하고 나중에 구성을 재개할 수도 있습니다.

   ![](assets/sms_preset_2.png)

1. 채널 표면이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 처리 중]** 상태.

   >[!NOTE]
   >
   >검사가 실패한 경우 다음에서 가능한 실패 이유에 대해 자세히 알아보십시오. [이 섹션](#monitor-channel-surfaces).

1. 검사가 성공하면 채널 표면이 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

이제 Journey Optimizer에서 SMS 메시지를 보낼 준비가 되었습니다.

**관련 항목**

* [SMS 메시지 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
* [캠페인에 메시지 추가](../campaigns/create-campaign.md)

