---
solution: Journey Optimizer
product: journey optimizer
title: Twilio 공급자 구성
description: Twilio를 사용하여 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 1%

---

# Twilio 공급자 구성 {#sms-configuration-twilio}

Journey Optimizer으로 Twilio를 구성하려면 Twilio에 사용되는 새 API 자격 증명을 만들어야 합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]**: 액세스 **계정 정보** 자격 증명을 찾을 수 있는 Twilio 콘솔 대시보드 페이지의 창입니다.

   * **[!UICONTROL 메시지 SID]**: Twilio의 API에서 만든 모든 메시지에 할당된 고유 식별자를 입력합니다. 다음에서 자세히 알아보기 [Twilio 설명서](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

