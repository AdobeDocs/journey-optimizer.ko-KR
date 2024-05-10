---
solution: Journey Optimizer
product: journey optimizer
title: SMS 표면 구성
description: Journey Optimizer에서 문자 메시지를 보내도록 SMS/MMS 표면을 구성하는 방법을 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 3a0e0bb7fd958441cf6b07f70a255a16c7692724
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 8%

---

# SMS/MMS 표면 만들기 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="메시지 범주 정의"
>abstract="이 표면을 사용하여 문자 메시지 유형 선택: 사용자 동의가 필요한 프로모션 메시지를 위한 마케팅 또는 암호 재설정과 같은 비상업적 메시지를 위한 트랜잭션."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=ko-KR#sms-opt-out-management" text="마케팅 문자 메시지 옵트아웃"

SMS/MMS 채널이 구성되면 SMS 및 MMS 메시지를 보낼 수 있는 채널 표면을 만들어야 합니다. **[!DNL Journey Optimizer]**.

채널 표면을 만들려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 표면]**. 다음을 클릭합니다. **[!UICONTROL 채널 표면 만들기]** 단추를 클릭합니다.

   ![](assets/preset-create.png)

1. 표면에 대한 이름과 설명(선택 사항)을 입력한 다음 SMS 채널을 선택합니다.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 다음을 정의합니다. **SMS 설정**.

   ![](assets/sms-surface-settings.png)

   다음을 선택하여 시작 **[!UICONTROL SMS 유형]** 이 데이터는 표면과 함께 전송됩니다. **[!UICONTROL 트랜잭션]** 또는 **[!UICONTROL 마케팅]**.

   * 선택 **마케팅** 프로모션 텍스트 메시지: 이러한 메시지에는 사용자의 동의가 필요합니다.
   * 선택 **트랜잭션** 예를 들어 주문 확인, 암호 재설정 알림 또는 게재 정보와 같은 비상업적인 메시지의 경우.

   SMS/MMS를 만들 때 메시지에 대해 선택한 범주와 일치하는 유효한 채널 표면을 선택해야 합니다.

   >[!CAUTION]
   >
   >**트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필에 메시지를 보낼 수 있습니다. 이러한 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

1. 다음 항목 선택 **[!UICONTROL SMS 구성]** 서피스와 연관시킬 수 있습니다.

   SMS 메시지를 보내도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](#create-api).

1. 다음을 입력합니다. **[!UICONTROL 발신자 번호]** 통신&#x200B;에 을 사용하려고 합니다.

1. 다음 항목 선택 **[!UICONTROL SMS 실행 필드]** 을(를) 선택하려면 **[!UICONTROL 프로필 속성]** 프로필의 전화 번호와 연결됩니다.

1. SMS 메시지에서 URL 단축 기능을 사용하려면 **[!UICONTROL 하위 도메인]** 목록을 표시합니다.

   >[!NOTE]
   >
   >하위 도메인을 선택하려면 최소 하나 이상의 SMS/MMS 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](sms-subdomains.md)

1. 다음을 입력합니다. **[!UICONTROL 옵트아웃 번호]** 이 서피스에 를 사용합니다. 프로필이 이 번호에서 옵트아웃해도 문자 메시지를 보낼 때 사용할 수 있는 다른 번호에서 메시지를 보낼 수 있습니다. [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >위치 [!DNL Journey Optimizer], 텍스트 메시지에 대한 옵트아웃은 더 이상 채널 수준에서 관리되지 않습니다. 이제 숫자에 따라 다릅니다.

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인할 수 있습니다. 채널 서피스를 구배로 저장하고 나중에 구성을 재개할 수도 있습니다.

   ![](assets/sms-submit-surface.png)

1. 채널 표면이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 처리 중]** 상태.

   >[!NOTE]
   >
   >검사가 실패한 경우 다음에서 가능한 실패 이유에 대해 자세히 알아보십시오. [이 섹션](#monitor-channel-surfaces).

1. 검사가 성공하면 채널 표면이 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

이제 Journey Optimizer에서 문자 메시지를 보낼 준비가 되었습니다.
