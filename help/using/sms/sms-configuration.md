---
solution: Journey Optimizer
product: journey optimizer
title: SMS 구성
description: Journey Optimizer에서 SMS를 전송하도록 환경을 구성하는 방법을 알아봅니다
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---

# SMS 채널 구성 {#sms-configuration}

[!DNL Journey Optimizer] 에서는 여정을 만들고 타겟팅된 대상자에게 메시지를 전송할 수 있습니다.

SMS를 보내기 전에 인스턴스를 구성합니다. 다음을 수행해야 합니다. [공급자 설정 통합](#create-api) Journey Optimizer 및 [sms 서피스 만들기](#message-preset-sms) (즉, SMS 사전 설정). 이러한 단계는 [Adobe Journey Optimizer 시스템 관리자](../start/path/administrator.md).

>[!IMPORTANT]
>
>Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 별도로 SMS 서비스를 제공하는 Sinch, Twilio 등 타사 공급자와 통합됩니다.  SMS를 구성하기 전에 Adobe Journey Optimizer과 해당 SMS 공급자 간의 연결을 설정할 수 있는 API 토큰 및 서비스 ID를 수신하려면 이러한 SMS 공급자 중 하나와 계정을 만들어야 합니다. SMS 서비스 사용은 해당 SMS 공급자의 추가 약관을 따릅니다. Sinch 및 Twilio는 Adobe Journey Optimizer 사용자가 통합을 통해 사용할 수 있는 타사 제품이므로 SMS 서비스와 관련된 문제 또는 문의 사항은 Sinch 또는 Twilio 사용자가 해당 SMS 공급자에게 문의하여 도움을 받아야 합니다. Adobe은 제어하지 않으며 타사 제품에 대한 책임이 없습니다.

## 새 API 자격 증명 만들기 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Journey Optimizer을 사용하여 SMS 공급업체 구성"
>abstract="공급업체 를 선택하고 SMS API 자격 증명을 입력합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Journey Optimizer을 사용하여 SMS 공급업체 구성"
>abstract="SMS를 전송하기 전에 공급자 설정을 Journey Optimizer과 통합해야 합니다. 완료되면 SMS 표면을 만들어야 합니다. 이러한 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/sms-configuration.html#message-preset-sms" text="SMS 채널 서피스 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="SMS 공급업체 구성을 선택합니다"
>abstract="SMS 공급업체용으로 구성된 API 자격 증명을 선택합니다."

Journey Optimizer을 사용하여 SMS 공급업체를 구성하려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL API 자격 증명]** 메뉴를 클릭한 다음 **[!UICONTROL API 자격 증명 만들기]**.

   ![](assets/sms_6.png)

1. 을(를) 선택합니다 **[!UICONTROL SMS 공급업체]**:

   * [!DNL Sinch] 질문에 답합니다. 을(를) 찾으려면 **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]**, Sinch 계정에서 SMS > API 메뉴에 액세스합니다.
   * [!DNL Twilio] 질문에 답합니다. 을(를) 찾으려면 **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]**&#x200B;콘솔 대시보드 페이지의 계정 정보 창에 액세스합니다.

1. 을(를) 입력합니다. **[!UICONTROL 이름]** API 자격 증명의 경우.

1. 을(를) 입력합니다. **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]**.

   ![](assets/sms_7.png)

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료했을 때.

API 자격 증명을 만들고 구성한 후 이제 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

## SMS 메시지의 채널 표면 만들기 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="SMS 카테고리를 정의합니다"
>abstract="이 서피스를 사용할 때 전송할 SMS 메시지 유형을 선택합니다. 사용자 동의가 필요한 프로모션 SMS 메시지 마케팅 또는 비상업적 SMS 메시지를 위한 트랜잭션용으로 특정 컨텍스트에서 가입 해지된 프로필에도 보낼 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="마케팅 SMS 메시지의 옵트아웃"

SMS 채널이 구성되면 SMS 메시지를 보낼 수 있는 채널 표면을 만들어야 합니다 **[!DNL Journey Optimizer]**.

채널 서피스를 생성하려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL 채널]** > **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 서피스]** 메뉴를 클릭한 다음 **[!UICONTROL 채널 서피스 생성]**.

   ![](assets/preset-create.png)

1. 서피스의 이름과 설명(선택 사항)을 입력한 다음 SMS 채널을 선택합니다.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 구성 **SMS** 설정.

   ![](assets/preset-sms.png)

   * 을(를) 선택합니다 **[!UICONTROL SMS 유형]** 서피스와 함께 전송됩니다. **[!UICONTROL 트랜잭션]** 또는 **[!UICONTROL 마케팅]**.

   * 을(를) 선택합니다 **[!UICONTROL SMS 구성]** 서피스와 연관되도록 합니다.

      SMS 메시지를 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](#create-api).

   * 을(를) 입력합니다. **[!UICONTROL 발신자 번호]** 커뮤니케이션에 &#x200B; 사용하려고 합니다.

   * 을(를) 선택합니다 **[!UICONTROL SMS 실행 필드]** 을(를) 선택하려면 **[!UICONTROL 프로필 속성]** 프로필의 전화 번호와 연관됩니다.

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인합니다. 채널 서피스를 구안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](assets/sms_preset_2.png)

1. 채널 서피스가 생성되면 목록에 과 함께 표시됩니다. **[!UICONTROL 처리 중]** 상태.

   >[!NOTE]
   >
   >검사가 실패하면 의 가능한 실패 이유에 대해 자세히 알아보십시오 [이 섹션](#monitor-channel-surfaces).

1. 확인이 성공하면 채널 서피스가 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

이제 Journey Optimizer에서 SMS 메시지를 보낼 준비가 되었습니다.

**관련 항목**

* [SMS 메시지 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
