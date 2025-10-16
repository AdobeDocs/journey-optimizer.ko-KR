---
solution: Journey Optimizer
product: journey optimizer
title: SMS 채널 구성
description: Journey Optimizer에서 텍스트 메시지를 전송하도록 환경을 구성하는 방법 알아보기
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 41%

---

# SMS / MMS / RCS 구성 시작 {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Journey Optimizer로 SMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 SMS 서비스 제공자를 통해 문자 메시지를 보냅니다. 제공자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Journey Optimizer로 MMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 MMS 서비스 공급자를 통해 미디어 콘텐츠를 보냅니다. 제공자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Journey Optimizer로 SMS/MMS 제공자 구성"
>abstract="문자 메시지(SMS/MMS)를 전송하기 전에 공급자 설정을 Journey Optimizer와 통합해야 합니다. 이 작업이 완료되면 SMS/MMS 구성을 만들어야 합니다. 이 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="SMS 채널 구성 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="SMS 공급업체 구성 선택"
>abstract="SMS 공급업체에 맞게 구성된 API 자격 증명을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="퍼지 옵트아웃"
>abstract="활성화되면 퍼지 옵트아웃은 정의된 Opt-out 키워드(예: CANCIL)와 매우 유사한 인바운드 메시지를 감지하고 사용자의 구독 취소 의도를 확인하기 위해 자동으로 확인 응답을 보냅니다. 사용자가 정의된 프롬프트를 통해 확인하는 경우 해당 사용자의 구독을 취소합니다."

SMS, MMS 또는 RCS를 보내기 전에 Adobe Journey Optimizer 환경을 구성해야 합니다. 다음을 수행하십시오.

1. Journey Optimizer과 공급자 설정을 통합합니다.
단계는 SMS 공급자에 따라 다릅니다. 자세한 설명서에 액세스하려면 아래 링크를 찾아보십시오.
   * [정보 피드](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [트빌리오](sms-configuration-twilio.md)
   * [사용자 정의 공급자](sms-configuration-custom.md)
1. [SMS 구성 만들기](sms-configuration-surface.md)

이 단계는 Adobe Journey Optimizer [시스템 관리자](../start/path/administrator.md)가 수행해야 합니다.

## 전제 조건{#sms-prerequisites}

Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 독립적으로 텍스트 메시지 서비스를 제공하는 서드파티 공급자와 통합됩니다. 문자 메시지 및 MMS에 대해 지원되는 공급자는 **Sinch**, **Twilio** 및 **Infobip**&#x200B;입니다. [사용자 지정 공급자 구성](sms-configuration-custom.md)을 사용하여 추가 메시징 공급자를 구성할 수 있습니다.

SMS 채널을 구성하기 전에 이러한 공급자 중 하나로 계정을 만들어 **API 토큰** 및 **서비스 ID**&#x200B;를 받아야 합니다. 이 ID는 Adobe Journey Optimizer과 해당 공급자 간의 연결을 구성해야 합니다.

문자 메시지 및 MMS 서비스의 사용은 해당 공급자의 추가 약관을 따릅니다. 타사 솔루션인 Sinch, Twilio 및 Infobip은 통합을 통해 Adobe Journey Optimizer 사용자에게 제공됩니다. Adobe은 서드파티 제품을 제어하지 않으며 이에 대해 책임을 지지 않습니다. 문자 메시지 서비스(SMS/MMS)와 관련된 문제 또는 지원 요청은 공급자에게 문의하십시오.

>[!CAUTION]
>
>SMS 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대해 **[!UICONTROL SMS 하위 도메인 관리]** 권한이 있어야 합니다. [이 페이지](../administration/high-low-permissions.md#administration-permissions)의 사용 권한에 대해 자세히 알아보세요.
>

