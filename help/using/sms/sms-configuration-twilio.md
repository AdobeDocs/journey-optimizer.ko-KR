---
solution: Journey Optimizer
product: journey optimizer
title: Twilio 공급자 구성
description: Twilio를 사용하여 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# Twilio 공급자 구성 {#sms-configuration-twilio}

## SMS/MMS에 대한 API 자격 증명 구성

Journey Optimizer으로 Twilio를 구성하려면 Twilio에 대한 새 API 자격 증명을 만들어야 합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** `>` **[!UICONTROL SMS 설정]**&#x200B;으로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Twilio.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택하십시오.

   * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]**: Twilio 콘솔 대시보드 페이지의 **계정 정보** 창에 액세스하여 자격 증명을 찾습니다.

   * **[!UICONTROL 메시지 SID]**: Twilio의 API로 만든 모든 메시지에 할당된 고유 식별자를 입력하십시오. 자세한 내용은 [Twilio 설명서](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}를 참조하세요.

   * **[!UICONTROL 인바운드 번호]**: 고유한 인바운드 번호를 추가합니다. 이를 통해 서로 다른 샌드박스에서 동일한 API 자격 증명을 사용할 수 있으며, 각 샌드박스는 고유한 인바운드 번호를 가지고 있습니다.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

1. 기존 API 자격 증명에서 **[!UICONTROL SMS 연결 확인]**&#x200B;을 클릭하여 샘플 메시지를 지정된 장치로 보내 SMS API 자격 증명을 테스트하고 확인합니다.

1. **숫자** 및 **메시지** 필드를 입력하고 **[!UICONTROL 연결 확인]**&#x200B;을 클릭합니다.

   >[!IMPORTANT]
   >
   >공급자의 페이로드 형식에 맞게 메시지를 구조화해야 합니다.

   ![](assets/verify-connection.png)

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

## RCS에 대한 API 자격 증명 구성

RCS 메시지는 [사용자 지정 SMS 공급자](sms-configuration-custom.md) 기능을 사용하여 Twilio를 통해 Adobe Journey Optimizer에서 지원됩니다. 이를 통해 캐러셀, 버튼 및 멀티미디어 컨텐츠와 같은 요소를 통합하여 검증된 비즈니스 프로필을 통해 풍부한 대화형 메시지를 전달할 수 있습니다.

➡️ [Twilio가 Twilio 설명서에서 RCS를 지원하는 방법을 살펴봅니다](https://www.twilio.com/docs/rcs)

Twilio에서 RCS 메시지를 사용하려면 사용자 지정 SMS 공급자를 통해 새 API 자격 증명을 구성해야 합니다. RCS에는 고유한 페이로드 형식이 필요하므로 기존 Twilio SMS 자격 증명은 호환되지 않습니다.

Twilio로 RCS를 구성하려면:

1. **Twilio에서 RCS 메시지 등록**

   먼저 Twilio 플랫폼에서 RCS 등록 프로세스를 완료합니다. 여기에는 비즈니스 프로필 설정 및 계정에 대한 RCS 기능 활성화가 포함됩니다.

1. **SMS 웹후크 만들기**

   [수신 RCS 메시지 응답 또는 게재 업데이트를 받을 수 있는 SMS Webhook 구성](sms-configuration-custom.md#webhook). 양방향 통신을 위해서는 이 웹후크가 Twilio 설정에 제대로 연결되어 있어야 합니다.

1. **SMS 공급업체로 사용자 지정을 사용하여 API 자격 증명 만들기**

   Journey Optimizer에서 &quot;사용자 지정&quot;을 SMS 공급업체로 사용하는 RCS에 대해 [새 API 자격 증명을 정의](sms-configuration-custom.md#api-credential)합니다. 적절한 RCS 끝점 인증 방법, 기본 URL 및 헤더를 사용합니다.

API 자격 증명을 만들고 구성한 후에는 RCS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)







