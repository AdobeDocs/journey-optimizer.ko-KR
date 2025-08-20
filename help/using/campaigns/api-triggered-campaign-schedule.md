---
solution: Journey Optimizer
product: journey optimizer
title: API 트리거 캠페인 예약
description: API 트리거 캠페인을 예약하는 방법을 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# API 트리거 캠페인 예약 {#api-schedule}

**[!UICONTROL 일정]** 탭을 사용하여 캠페인 일정을 정의합니다.

## 시작 및 종료 날짜 설정

기본적으로 API 트리거 캠페인은 트리거되면 시작되고, 메시지가 한 번 전송되는 즉시 종료됩니다. 캠페인이 트리거된 직후 실행하지 않으려면 **[!UICONTROL 캠페인 시작]** 옵션을 사용하여 메시지를 보낼 날짜와 시간을 지정할 수 있습니다.

**[!UICONTROL 캠페인 끝]** 옵션을 사용하면 캠페인 실행을 중지해야 하는 시기를 지정할 수 있습니다. 지정한 날짜 외에는 캠페인이 실행되지 않습니다.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]에서 캠페인을 예약할 때 시작 날짜/시간이 원하는 첫 번째 게재에 맞춰졌는지 확인하십시오.

## 속도 제어 설정

[!DNL Journey Optimizer]을(를) 통해 아웃바운드 동작(전자 메일, SMS, 푸시 알림)에 대한 속도 제어를 사용하도록 설정할 수 있습니다.

이 기능은 랜딩 페이지나 고객 지원 플랫폼과 같은 다운스트림 시스템의 오버로드를 방지하는 데 특히 유용합니다. 예를 들어, 속도가 초당 165개의 메시지로 제한하여 다운스트림 시스템을 압도하지 않고도 지속적인 전송을 보장할 수 있습니다.

속도 제어를 설정하려면 **[!UICONTROL 배달 설정]** 섹션에서 **[!UICONTROL 배달 조절]** 옵션을 활성화하고 원하는 **[!UICONTROL 배달 속도]**&#x200B;를 지정하십시오.

![](assets/throttling-rate-control.png)

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 이를 검토하고 활성화할 수 있습니다. [자세히 알아보기](review-activate-campaign.md)
