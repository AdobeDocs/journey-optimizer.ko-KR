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
source-git-commit: d3570e2c3d6340deaba8ca0f342161ab43ad1c43
workflow-type: tm+mt
source-wordcount: '315'
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

속도 제어를 설정하려면 **[!UICONTROL 배달 설정]** 섹션에서 **[!UICONTROL 배달 스로틀]** 옵션을 활성화하고 원하는 **[!UICONTROL 초당 배달 속도]**&#x200B;를 지정하십시오.

* 지원되는 최소 게재 속도: 초당 1개.
* 지원되는 최대 배달 속도: &quot;배달 스로틀&quot; 옵션이 활성화된 경우 초당 2000입니다.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>게재 속도를 설정할 때 캠페인 대상자가 실행할 수 있는 최대 기간은 12시간입니다. 게재 속도가 12시간 이내에 모든 대상자에게 메시지를 보낼 수 없는 값으로 설정된 경우 나머지 프로필은 캠페인에서 제외됩니다. 캠페인 보고서에서 제외된 이러한 프로필의 수를 볼 수 있습니다.

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 이를 검토하고 활성화할 수 있습니다. [자세히 알아보기](../campaigns/review-activate-api-triggered-campaign.md)
