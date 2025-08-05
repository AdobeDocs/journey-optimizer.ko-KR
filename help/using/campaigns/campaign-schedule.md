---
solution: Journey Optimizer
product: journey optimizer
title: 작업 캠페인 예약
description: 작업 캠페인을 예약하는 방법을 알아봅니다.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 만들기, 최적화 도구, 캠페인, 표면, 메시지
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 16%

---

# 작업 캠페인 예약 {#action-campaign-schedule}

**[!UICONTROL 일정]** 탭을 사용하여 캠페인 일정을 정의합니다.

기본적으로 작업 캠페인은 수동으로 활성화되면 시작되고 메시지가 한 번 전송되는 즉시 종료됩니다. 활성화 직후 캠페인을 실행하지 않으려면 **[!UICONTROL 캠페인 시작]** 옵션을 사용하여 메시지를 보낼 날짜와 시간을 지정할 수 있습니다.

**[!UICONTROL 캠페인 끝]** 옵션을 사용하면 캠페인 실행을 중지해야 하는 시기를 지정할 수 있습니다. 지정한 날짜 외에는 캠페인이 실행되지 않습니다.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]에서 캠페인을 예약할 때는 시작 날짜/시간이 원하는 첫 번째 게재에 맞춰졌는지 확인합니다. 반복 캠페인의 경우 초기 예약 시간이 이미 경과했을 때는 캠페인이 반복 규칙에 따라 다음 사용 가능한 시간 슬롯으로 넘어갑니다.

캠페인 채널을 기반으로 추가 예약 옵션을 사용할 수 있습니다.

* **빈도**(전자 메일, SMS, 푸시 동작)

  캠페인 메시지를 전송해야 하는 빈도를 정의할 수 있습니다. 이렇게 하려면 캠페인 만들기 화면에서 **[!UICONTROL 작업 트리거]** 옵션을 사용하여 캠페인을 매일, 매주 또는 매월 실행할지 여부를 지정합니다.

* **IP 준비 계획 활성화**(전자 메일)

  이메일 캠페인의 경우 특정 IP 준비 계획 활성화 캠페인을 만들 수 있습니다. 캠페인 일정은 해당 일정과 연결될 IP 준비 계획에 의해 좌우되며, 이는 일정이 캠페인 자체에서 더 이상 정의되지 않음을 의미합니다. [IP 준비 캠페인을 만드는 방법을 알아보세요](../configuration/ip-warmup-campaign.md).

## 다음 단계 {#next}

캠페인 일정이 준비되면 캠페인을 검토하고 활성화할 수 있습니다. [자세히 알아보기](review-activate-campaign.md)
