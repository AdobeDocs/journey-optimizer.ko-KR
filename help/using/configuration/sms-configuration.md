---
title: SMS 구성
description: Journey Optimizer을 사용하여 SMS 메시지를 보내도록 환경을 구성하는 방법을 알아봅니다
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 4%

---

# SMS 채널 구성 {#sms-configuration}

>[!CAUTION]
>
> 현재 SMS 채널을 사용하는 것은 초기 액세스 시 사용자만 선택할 수 있습니다. 이 기능을 활용하려면 Adobe 계정 담당자에게 문의하십시오.

[!DNL Journey Optimizer] 에서는 여정을 만들고 타겟팅된 대상자에게 메시지를 전송할 수 있습니다.

## 새 API 자격 증명 만들기 {#create-api}

Journey Optimizer을 사용하여 SMS 공급업체를 구성하려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** 메뉴를 클릭한 다음 **[!UICONTROL Create API credential]**.

   ![](../assets/sms_4.png)

1. Sinch를 로 선택합니다. **[!UICONTROL SMS vendor]**.

1. 을(를) 입력합니다. **[!UICONTROL Name]** API 자격 증명의 경우.

1. 을(를) 입력합니다. **[!UICONTROL Service ID]** 및 **[!UICONTROL API Token]**.

   >[!NOTE]
   >
   > Sinch에는 특별한 API 자격 증명이 필요합니다. 을(를) 찾으려면 **[!UICONTROL Service ID]** 및 **[!UICONTROL API Token]**, Sinch 계정에서 SMS > API 메뉴에 액세스,

   ![](../assets/sms_5.png)

1. 클릭 **[!UICONTROL Submit]** api 자격 증명 구성을 완료했을 때.

API 자격 증명을 만들고 구성한 후 이제 SMS 메시지에 대한 메시지 사전 설정을 만들어야 합니다.

## SMS 메시지에 대한 메시지 사전 설정 만들기 {#message-preset-sms}

SMS 채널이 구성되면 SMS 메시지를 보낼 수 있도록 메시지 사전 설정을 만들어야 합니다 **[!DNL Journey Optimizer]**.

메시지 사전 설정을 만들려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 메뉴를 클릭한 다음 **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. 사전 설정의 이름과 설명(선택 사항)을 입력한 다음 SMS 채널을 선택합니다.

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 구성 **SMS** 설정.

   ![](../assets/preset-sms.png)

   * 을(를) 선택합니다 **[!UICONTROL SMS Type]** 사전 설정으로 전송됩니다. **[!UICONTROL Transactional]** 또는 **[!UICONTROL Marketing]**.

   * 을(를) 선택합니다 **[!UICONTROL SMS configuration]** 사전 설정과 연결

      SMS 메시지를 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](sms-configuration.md).

   * 을(를) 입력합니다. **[!UICONTROL Sender number]** 커뮤니케이션에 &#x200B; 사용하려고 합니다.

1. 모든 매개 변수가 구성되면 **[!UICONTROL Submit]** 확인합니다. 메시지 사전 설정을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](../assets/sms_preset_2.png)

1. 메시지 사전 설정이 만들어지면 와 함께 목록에 표시됩니다 **[!UICONTROL Processing]** 상태.

   >[!NOTE]
   >
   >검사가 실패하면 의 가능한 실패 이유에 대해 자세히 알아보십시오 [이 섹션](#monitor-message-presets).

1. 확인이 성공하면 메시지 사전 설정이 **[!UICONTROL Active]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](../assets/preset-active.png)

이제 Journey Optimizer에서 SMS 메시지를 보낼 준비가 되었습니다.

**관련 항목**

* [SMS 메시지 만들기](../messages/create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
