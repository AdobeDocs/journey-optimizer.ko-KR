---
solution: Journey Optimizer
product: journey optimizer
title: SMS 채널 구성
description: Journey Optimizer을 사용하여 모바일 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 42%

---

# 모바일 구성 시작하기 {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Journey Optimizer로 SMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 SMS 서비스 제공자를 통해 모바일 메시지를 보냅니다. 제공자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Journey Optimizer로 MMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 MMS 서비스 공급자를 통해 미디어 콘텐츠를 보냅니다. 제공자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Journey Optimizer로 SMS/RCS/MMS 제공자 구성"
>abstract="모바일 메시지(SMS/RCS/MMS)를 전송하기 전에 제공자 설정을 Journey Optimizer와 통합해야 합니다. 이 작업이 완료되면 SMS/RCS/MMS 구성을 만들어야 합니다. 이 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다."
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
   * [정보 피드](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [트빌리오](mobile-configuration-twilio.md)
   * [사용자 정의 공급자](mobile-configuration-custom.md)
1. [웹후크 만들기](mobile-webhook.md)
1. [모바일 구성 만들기](mobile-configuration-surface.md)

이 단계는 Adobe Journey Optimizer [시스템 관리자](../start/path/administrator.md)가 수행해야 합니다.

## 전제 조건{#sms-prerequisites}

Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 독립적으로 모바일 메시징 서비스를 제공하는 서드파티 공급자와 통합됩니다. 모바일 메시징 및 MMS에 대해 지원되는 공급자는 **Sinch**, **Twilio** 및 **Infobip**&#x200B;입니다. [사용자 지정 공급자 구성](mobile-configuration-custom.md)을 사용하여 추가 메시징 공급자를 구성할 수 있습니다.

모바일 채널을 구성하기 전에 이러한 공급자 중 하나로 계정을 만들어 **API 토큰** 및 **서비스 ID**&#x200B;를 받아야 합니다. 이 ID는 Adobe Journey Optimizer과 해당 공급자 간의 연결을 구성해야 합니다.

모바일 메시징 및 MMS 서비스 사용은 해당 공급자의 추가 약관을 따릅니다. 타사 솔루션인 Sinch, Twilio 및 Infobip은 통합을 통해 Adobe Journey Optimizer 사용자에게 제공됩니다. Adobe은 서드파티 제품을 제어하지 않으며 이에 대해 책임을 지지 않습니다. 모바일 메시징 서비스와 관련된 문제 또는 지원 요청은 공급자에게 문의하십시오.

>[!CAUTION]
>
>SMS 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대해 **[!UICONTROL SMS 하위 도메인 관리]** 권한이 있어야 합니다. [이 페이지](../administration/high-low-permissions.md#administration-permissions)의 사용 권한에 대해 자세히 알아보세요.
>

