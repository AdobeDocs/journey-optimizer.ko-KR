---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 채널 구성
description: Journey Optimizer에서 WhatsApp 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: 87931614150d6f764f565f683f83db4f63d88ee0
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 4%

---

# WhatsApp 구성 시작 {#whatsapp-config}

>[!BEGINSHADEBOX]

**목차**

* [WhatsApp 메시지 시작](get-started-whatsapp.md)
* **[WhatsApp 구성 시작](whatsapp-configuration.md)**
* [WhatsApp 메시지 만들기](create-whatsapp.md)
* [WhatsApp 메시지 확인 및 보내기](send-whatsapp.md)

>[!ENDSHADEBOX]

WhatsApp 메시지를 보내기 전에 Adobe Journey Optimizer 환경을 구성하고 WhatsApp 계정과 연결해야 합니다. 다음을 수행하십시오.

1. [WhatsApp API 자격 증명 만들기](#WhatsApp-credentials)
1. [WhatsApp 구성 만들기](#WhatsApp-configuration)

이 단계는 Adobe Journey Optimizer [시스템 관리자](../start/path/administrator.md)가 수행해야 합니다.

## WhatsApp API 자격 증명 만들기 {#whatsapp-credentials}

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택하십시오. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 API 자격 증명을 구성합니다.

   * **API 토큰**: API 토큰을 입력하십시오. [메타 설명서](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)에서 자세히 알아보기
   * **비즈니스 계정 ID**: 비즈니스 포트폴리오와 관련된 고유 번호를 입력하십시오. 자세한 내용은 [메타 설명서](https://www.facebook.com/business/help/1181250022022158?id=180505742745347)를 참조하세요.

   ![](assets/whatsapp-api.png)

1. **[!UICONTROL 계속을 클릭합니다]**.

1. WhatsApp API 자격 증명에 연결할 **비즈니스 계정**&#x200B;을(를) 선택하십시오.

   ![](assets/whatsapp-api-2.png)

1. Whatsapp 메시지를 보내는 데 사용되는 **전화 번호**&#x200B;을(를) 선택하십시오.

1. 전화 번호 설정이 자동으로 채워집니다.

   * **품질 평가**: 지난 24시간 동안 보낸 메시지에 대한 고객 피드백을 반영합니다.
      * 녹색: 고품질
      * 노란색: Medium 품질
      * 빨강: 낮은 품질

     [품질 평가](https://www.facebook.com/business/help/766346674749731#)에 대해 자세히 알아보기

   * **처리량**: 전화 번호에서 메시지를 보낼 수 있는 속도를 나타냅니다.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

API 자격 증명을 만들고 구성한 후에는 WhatsApp 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](#whatsapp-configuration)

## WhatsApp 구성 만들기 {#whatsapp-configuration}

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]**&#x200B;을 선택합니다. **[!UICONTROL 채널 구성 만들기]** 단추를 클릭합니다.

   ![](assets/whatsapp-config-1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력한 다음 WhatsApp 채널을 선택합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.`, 하이픈 `-`도 사용할 수 있습니다.

1. **[!DNL WhatsApp]**&#x200B;을(를) 채널로 선택합니다.

   ![](assets/whatsapp-config-2.png)

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하세요. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. 자세히 알아보기

1. 이전에 만든 **[!UICONTROL WhatsApp API 구성]**&#x200B;을(를) 선택하십시오.

   ![](assets/whatsapp-config-3.png)

1. 통신에 사용할 **[!UICONTROL 발신자 번호]**&#x200B;을(를) 입력하십시오.

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]**&#x200B;을 클릭하여 확인합니다. 채널 구성을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

1. 채널 구성이 만들어지면 목록에 **[!UICONTROL 처리 중]** 상태로 표시됩니다.

   >[!NOTE]
   >
   >검사에 실패한 경우 [이 섹션](../configuration/channel-surfaces.md)에서 가능한 실패 이유에 대해 자세히 알아보세요.

1. 검사가 성공하면 채널 구성이 **[!UICONTROL 활성]** 상태가 됩니다. 메시지를 전달하는 데 사용할 준비가 되었습니다.

이제 Journey Optimizer에서 WhatsApp 메시지를 보낼 준비가 되었습니다.
