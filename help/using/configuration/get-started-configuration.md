---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Journey Optimizer]  구성 시작'
description: ' [!DNL Journey Optimizer]  구성에 대해 자세히 알아보기'
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: 구성, 구성하기, 메시지, 채널, 샌드박스, optimizer
source-git-commit: 970fef96b6fa04f2b5ce1a8d10f89802f513b373
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 97%

---


# [!DNL Journey Optimizer] 구성 시작 {#start-optimizer-configuration}

[!DNL Journey Optimizer]에 처음 액세스하면 프로덕션 샌드박스가 프로비저닝되고 계약에 따라 특정 수의 IP가 할당됩니다.

여정을 만들고 메시지를 보내려면 아래 단계에 따라 구성을 완료해야 합니다.

## 메시지 및 채널 구성

1. 메시지를 만들고 보내려면 채널에 따라 특정 구성을 수행해야 합니다.

   * **이메일** 채널의 경우 하위 도메인을 Adobe에 위임하고 IP 풀을 만들어 IP 주소를 함께 그룹화해야 합니다. [자세히 알아보기](../email/get-started-email-config.md)

   * **푸시** 채널에의 경우 [!DNL Adobe Experience Platform]과 [!DNL Adobe Experience Platform Launch] 양쪽에서 푸시 알림 설정을 정의해야 합니다. [자세히 알아보기](../push/push-configuration.md)

   * **SMS** 채널의 경우 공급자 설정을 [!DNL Journey Optimizer]에 통합하는 등 SMS를 보내는 인스턴스를 구성해야 합니다. [자세히 알아보기](../sms/sms-configuration.md)

1. 준비를 마친 다음에는 **채널 표면**&#x200B;을 만들어 메시지를 게재하는 데 필요한 기술 매개 변수를 모두 구성해야 합니다. [자세히 알아보기](channel-surfaces.md)

1. 다음 작업도 수행할 수 있습니다.

   * 금지 목록에 이메일 주소를 보내기 전에 재시도를 하는 기간(일)을 관리합니다. [자세히 알아보기](manage-suppression-list.md)

   * 개인 사용자에게 보내는 메시지의 사본을 보관하려면 **BBC 이메일 옵션**&#x200B;을 활성화합니다. [자세히 알아보기](archiving-support.md#enable-bcc)

   * 구성 **비즈니스 규칙** 받는 사람에게 과도한 요청을 보내는 것을 방지하기 위해. [자세히 알아보기](frequency-rules.md)

   * Adobe Experience Platform에서 수신자의 주소/전화번호를 여러 개 사용할 수 있는 경우 어느 주소/전화번호를 우선으로 사용할지 정합니다. [자세히 알아보기](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>이 단계는 [Adobe Journey Optimizer 시스템 관리자](../start/path/administrator.md)가 수행해야 합니다.

## 여정 구성

여정을 작성하려면 **[!UICONTROL 데이터 소스]**, **[!UICONTROL 이벤트]**, **[!UICONTROL 작업]**&#x200B;을 구성해야 합니다. [자세히 알아보기](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* **데이터 소스** 구성은 시스템에 대한 연결을 정의합니다. 이 연결을 통해 여정에 사용할 추가 정보를 검색할 수 있습니다. [자세히 알아보기](../datasource/about-data-sources.md)

* **이벤트**&#x200B;를 사용하면 여정을 통합적으로 트리거하여 여정에 참여하는 개인에게 실시간으로 메시지를 보낼 수 있습니다. 이벤트 구성에서 여정에서 예상되는 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. [자세히 알아보기](../event/about-events.md)

* [!DNL Journey Optimizer]는 콘텐츠를 디자인하고 보낼 수 있는 메시지 기능을 기본적으로 제공합니다. 서드파티 시스템을 사용하여 메시지를 보내는 경우 **사용자 정의 작업**&#x200B;을 만듭니다. [자세히 알아보기](../action/action.md)