---
solution: Journey Optimizer
product: journey optimizer
title: Twilio 공급자 구성
description: Twilio를 사용하여 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 4%

---

# Twilio 공급자 구성 {#sms-configuration-twilio}

Journey Optimizer으로 Twilio를 구성하려면 Twilio에 사용되는 새 API 자격 증명을 만들어야 합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Twilio.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택하십시오.

   * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]**: Twilio 콘솔 대시보드 페이지의 **계정 정보** 창에 액세스하여 자격 증명을 찾습니다.

   * **[!UICONTROL 메시지 SID]**: Twilio의 API로 만든 모든 메시지에 할당된 고유 식별자를 입력하십시오. 자세한 내용은 [Twilio 설명서](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}를 참조하세요.

   * **[!UICONTROL 인바운드 번호]**: 고유한 인바운드 번호를 추가합니다. 이를 통해 서로 다른 샌드박스에서 동일한 API 자격 증명을 사용할 수 있으며, 각 샌드박스는 고유한 인바운드 번호를 가지고 있습니다.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)
