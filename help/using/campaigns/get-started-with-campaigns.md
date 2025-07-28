---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 시작
description: Journey Optimizer의 캠페인에 대해 자세히 알아보기
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 캠페인, 방법 , 시작, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 69%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="캠페인 일정"
>abstract="기본적으로 캠페인은 수동 활성화 시 시작되고 메시지가 전송된 후에 즉시 종료됩니다. 메시지를 보낼 특정 날짜와 시간을 유연하게 설정할 수 있습니다. 또한 반복 작업 캠페인의 종료 날짜를 지정할 수 있습니다. 액션 트리거에서 환경 설정에 맞게 메시지 전송 빈도를 구성할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="캠페인 시작"
>abstract="메시지를 전송해야 하는 날짜와 시간을 지정하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="캠페인 종료"
>abstract="반복 캠페인 실행을 중지해야 하는 시점을 지정하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="캠페인 액션 트리거"
>abstract="캠페인 메시지를 전송해야 하는 빈도를 정의하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="조절률 제어"
>abstract="조절률 제어"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="캠페인 만들기"
>abstract="**Adobe Journey Optimizer**&#x200B;로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="캠페인을 만들어 다양한 채널을 통해 특정 대상자에게 일회성 콘텐츠를 게재할 수 있습니다. 캠페인을 만들기 전에 채널 구성과 Adobe Experience Platform 대상자를 사용할 준비가 되었는지 확인하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="캠페인 유형"
>abstract="**예약된 캠페인**&#x200B;은 즉시 또는 지정된 날짜에 실행되며 마케팅 유형 메시지 전송을 의미합니다. **API 트리거** 캠페인은 API 호출을 사용하여 실행됩니다. 이는 마케팅 메시지(사용자 동의가 필요한 프로모션 메시지) 또는 트랜잭션 메시지(특정 상황에서 구독하지 않은 프로필에도 보낼 수 있는 비상업적 메시지)를 전송하는 것을 목표로 합니다."

Journey Optimizer 캠페인으로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다.

![](assets/gs-campaigns.png)

Journey Optimizer에서 다양한 유형의 캠페인을 만들 수 있습니다.

* **작업 캠페인**

  작업 캠페인(또는 예약된 캠페인)을 사용하면 프로모션 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 사용 사례에 대한 간단한 애드혹 일괄 커뮤니케이션을 수행할 수 있습니다.

* **API 트리거 캠페인**

  API 트리거 캠페인을 사용하면 마케팅 커뮤니케이션이 적시에 대상자에게 연락하거나, 암호 재설정과 같은 개인에 대한 트랜잭션/운영 메시지를 보낼 수 있습니다. 여기에서는 프로필 속성뿐만 아니라 REST API 페이로드인 트리거에서 실시간 컨텍스트 데이터를 사용하여 개인화가 필요할 수 있습니다.

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, Orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## 시작하기 전 {#campaign-prerequisites}

[!DNL Journey Optimizer]에서 첫 번째 캠페인 만들기를 시작하기 전에 다음 사전 요구 사항을 확인하십시오.

1. **적절한 권한이 필요합니다**. 캠페인은 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 및/또는 캠페인 뷰어와 같은 캠페인 관련 **[!UICONTROL 제품 프로필]**&#x200B;에 액세스할 수 있는 사용자만 사용할 수 있습니다. 캠페인에 액세스할 수 없는 경우 권한을 확장해야 합니다.

   +++캠페인 관련 역할 할당하는 방법 알아보기

   1. [!DNL Permissions] 제품에서 사용자에게 역할을 할당하려면 **[!UICONTROL 역할]** 탭으로 이동하여 기본 제공 캠페인 관련 **[!UICONTROL 역할]**, wmr 캠페인 관리자(administrator), 캠페인 승인자, 캠페인 관리자(manager) 또는 캠페인 뷰어 중 하나를 선택하십시오.

   1.  **[!UICONTROL 사용자]** 탭에서 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

   1. 사용자 이름 또는 이메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**&#x200B;합니다.

      이전에 사용자를 생성하지 않은 경우 [사용자 설명서 추가](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/ui/users)를 참조하십시오.

   그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

+++

1. **대상자가 필요합니다**. 캠페인을 만들기 전에 대상자를 사용할 수 있어야 합니다. [대상자 시작](../audience/about-audiences.md).

1. **채널 구성이 필요합니다**. 채널을 선택하려면 해당 채널 구성(즉, 사전 설정)을 만들고 사용할 수 있는 상태로 설정해야 합니다. [채널 구성을 설정하는 방법을 알아봅니다](../configuration/channel-surfaces.md).

## 더 자세히 알아보기

[!DNL Journey Optimizer]의 캠페인에 대해 이해했으므로 이 설명서 섹션을 자세히 살펴보고 첫 번째 캠페인을 만들어야 합니다.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="작업 캠페인" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">액션 캠페인</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">API 트리거 캠페인</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
