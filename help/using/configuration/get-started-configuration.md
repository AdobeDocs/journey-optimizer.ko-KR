---
title: 시작하기 [!DNL Journey Optimizer] 구성
description: 추가 정보 [!DNL Journey Optimizer] 구성
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 7c9f04b8d3faa171444bfa0adc537b5faabde37e
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 9%

---


# 시작하기 [!DNL Journey Optimizer] 구성 {#start-optimizer-configuration}

액세스 시 [!DNL Journey Optimizer] 처음으로 프로덕션 샌드박스를 프로비저닝하고 계약에 따라 특정 수의 IP를 할당하게 됩니다.

여정을 만들고 메시지를 보내려면 다음 구성 단계를 수행해야 합니다.

1. **메시지 및 채널 구성**: 사전 설정 정의, 이메일 및 푸시 메시지 조정 및 사용자 정의

   * 두 위치에서 푸시 알림 설정 정의 [!DNL Adobe Experience Platform] 및 [!DNL Adobe Experience Platform Launch]. [자세히 알아보기](../messages/push-gs.md)

   * 이메일 및 푸시 알림 메시지에 필요한 모든 기술 매개 변수를 구성하려면 메시지 사전 설정을 만듭니다. [자세히 알아보기](message-presets.md)

   * Adobe Experience Platform에서 여러 주소를 사용할 수 있는 경우 수신자의 우선 순위에 사용할 이메일 주소를 결정합니다. [자세히 알아보기](primary-email-addresses.md)

   * 전자 메일 주소를 제외 목록으로 보내기 전에 다시 시도를 수행하는 일 수를 관리합니다. [자세히 알아보기](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../messages/push-gs.md)
    -->

1. **하위 도메인 위임**: Journey Optimizer에서 사용할 새 하위 도메인의 경우 첫 번째 단계는 하위 도메인을 위임하는 것입니다. [자세히 알아보기](about-subdomain-delegation.md)

   ![](assets/subdomain.png)

1. **IP 풀 만들기**: 인스턴스로 제공된 IP 주소를 그룹화하여 이메일 게재 능력과 평판을 향상시킵니다. [자세히 알아보기](ip-pools.md)

   ![](assets/ip-pool.png)

1. **여정 구성**: 여정을 빌드하려면 다음을 구성해야 합니다 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 및 **[!UICONTROL Actions]**. [자세히 알아보기](about-data-sources-events-actions.md)

   ![](assets/admin-menu.png)

   * 다음 **데이터 소스** 구성을 사용하면 시스템에 대한 연결을 정의하여 여정에서 사용할 추가 정보를 검색할 수 있습니다. 데이터 소스에 대해 자세히 알아보십시오 [섹션](../datasource/about-data-sources.md)

   * **이벤트** 여정으로 유입되는 개인에게 실시간으로 메시지를 보낼 때까지 여정을 트리거할 수 있습니다. 이벤트 구성에서는 여정에 필요한 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. 이 비디오에서 이벤트에 대해 자세히 알아보기 [섹션](../event/about-events.md)

   * [!DNL Journey Optimizer] 에는 메시지 기능이 내장되어 있습니다. 콘텐츠를 디자인하고 메시지를 게시할 수 있습니다. 서드파티 시스템을 사용하여 메시지를 전송하는 경우 **사용자 지정 작업**. 이 단원의 작업에 대해 자세히 알아보기 [섹션](../action/action.md)