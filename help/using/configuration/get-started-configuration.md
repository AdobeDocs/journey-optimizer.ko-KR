---
solution: Journey Optimizer
product: journey optimizer
title: 시작하기 [!DNL Journey Optimizer] 구성
description: 추가 정보 [!DNL Journey Optimizer] 구성
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# 시작하기 [!DNL Journey Optimizer] 구성 {#start-optimizer-configuration}

[!DNL Journey Optimizer]에 처음 액세스하면 프로덕션 샌드박스가 프로비저닝되고 계약에 따라 특정 수의 IP가 할당됩니다.

여정을 만들고 메시지를 보내려면 아래 구성 단계를 수행해야 합니다.

## 메시지 및 채널 구성

채널 서피스를 정의하고 메시지를 조정하고 사용자 정의합니다.

* [하위 Adobe에 위임](about-subdomain-delegation.md) 전자 메일 및 [IP 풀 만들기](ip-pools.md) 그룹에 제공된 IP 주소를 함께 그룹화합니다.

* 금지 목록에 이메일 주소를 보내기 전에 재시도를 하는 기간(일)을 관리합니다. [자세히 알아보기](manage-suppression-list.md)

* [!DNL Adobe Experience Platform] 및 [!DNL Adobe Experience Platform Launch] 모두에서 푸시 알림 설정을 정의합니다. [자세히 알아보기](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* SMS를 전송하도록 인스턴스를 구성합니다(현재 조직 세트에만 사용 가능 - 제한된 가용성). [자세히 알아보기](../sms/sms-configuration.md)

* 채널 서피스를 만들어 메시지를 전달하는 데 필요한 모든 기술 매개 변수를 구성합니다. [자세히 알아보기](channel-surfaces.md)

* Adobe Experience Platform에서 여러 주소/번호를 사용할 수 있는 경우 수신자의 우선 순위에 사용할 이메일 주소 및/또는 전화 번호를 결정합니다. [자세히 알아보기](primary-email-addresses.md)

## 여정 구성

여정을 빌드하려면 다음을 구성해야 합니다 **[!UICONTROL 데이터 소스]**, **[!UICONTROL 이벤트]** 및 **[!UICONTROL 작업]**. [자세히 알아보기](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* 다음 **데이터 소스** 구성을 사용하면 시스템에 대한 연결을 정의하여 여정에서 사용할 추가 정보를 검색할 수 있습니다. [자세히 알아보기](../datasource/about-data-sources.md)

* **이벤트**&#x200B;를 사용하면 여정을 통합적으로 트리거하여 여정에 참여하는 개인에게 실시간으로 메시지를 보낼 수 있습니다. 이벤트 구성에서 여정에서 예상되는 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. [자세히 알아보기](../event/about-events.md)

* [!DNL Journey Optimizer] 에는 콘텐츠를 디자인하고 전송할 수 있는 기본 제공 메시지 기능이 포함되어 있습니다. 서드파티 시스템을 사용하여 메시지를 전송하는 경우 **사용자 지정 작업**. [자세히 알아보기](../action/action.md)