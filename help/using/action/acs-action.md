---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign Standard 통합
description: Journey Optimizer을 Adobe Campaign Standard과 통합하는 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: 캠페인, 표준, 통합, 최대 가용량, 작업
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d92c280e40419d2e3ec62a7ba85cd492a0867fde
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 3%

---

# Adobe Campaign Standard 통합 {#using_adobe_campaign_standard}

Adobe Campaign Standard이 있는 경우 Adobe Campaign Standard에 연결할 수 있는 기본 제공 작업을 사용할 수 있습니다. Adobe Campaign Standard의 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다.

Journey Optimizer에서 사용하려면 Campaign Standard 트랜잭션 메시지와 관련 이벤트를 게시해야 합니다. 이벤트가 게시되었지만 메시지는 게시되지 않은 경우 Journey Optimizer 인터페이스에 표시되지 않습니다. 메시지가 게시되었지만 연결된 이벤트가 게시되지 않은 경우 Journey Optimizer 인터페이스에 표시되지만 사용할 수 없습니다.

## 가드레일 및 제한 사항 {#important-notes}

* Adobe Campaign Standard 작업에 대해 5분당 4,000회의 최대 가용량 규칙이 자동으로 정의됩니다. [Adobe Campaign Standard 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html){target="_blank"}에서 트랜잭션 메시지 SLA에 대해 자세히 알아보세요.

* Adobe Campaign Standard 통합은 작업 목록에서 전용 기본 제공 작업을 통해 설정됩니다. 각 샌드박스에 대해 구성해야 합니다.

* 대상 자격 또는 대상 읽기 활동과 함께 Campaign Standard 작업을 사용할 수 없습니다.

* 여정은 [기본 제공 채널 작업](../building-journeys/journeys-message.md)과 [Campaign Standard 작업](../building-journeys/using-adobe-campaign-standard.md)을 모두 사용할 수 없습니다.

## 작업 구성 {#configure-action}

Journey Optimizer에서는 트랜잭션 메시지당 하나의 작업을 구성해야 합니다.

Campaign Standard 작업을 구성하려면 다음 단계를 수행합니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL 구성]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 관리]**&#x200B;를 클릭합니다. 작업 목록이 표시됩니다.

1. 기본 제공 **[!UICONTROL AdobeCampaignStandard]** 액션을 선택하십시오. 작업 구성 창이 화면 오른쪽에 열립니다.

   ![](assets/actioncampaign.png)

1. Adobe Campaign Standard 인스턴스 URL을 복사하여 **[!UICONTROL URL]** 필드에 붙여넣습니다.

1. **[!UICONTROL 인스턴스 URL 테스트]**&#x200B;를 클릭하여 인스턴스의 유효성을 테스트합니다.

   >[!NOTE]
   >
   >이 테스트는 다음을 확인합니다.
   >
   >* 호스트는 &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; 또는 &quot;.adls.adobe.com&quot;입니다.
   >
   >* URL은 https로 시작합니다
   >
   >* 이 Adobe Campaign Standard 인스턴스와 연결된 조직은 Journey Optimizer 조직 RG와 동일합니다

이 구성이 완료되면 여정을 디자인할 때 **[!UICONTROL Action]** 범주에서 다음 세 가지 작업을 사용할 수 있습니다. **[!UICONTROL 이메일]**, **[!UICONTROL 푸시]**, **[!UICONTROL SMS]**. [사용 방법을 알아보세요](../building-journeys/using-adobe-campaign-standard.md).

![](assets/journey58.png)

**반응** 이벤트를 사용하여 동일한 여정 내에서 전송된 Campaign Standard 메시지와 관련된 추적 데이터에 반응합니다.

* 푸시 알림의 경우 여정은 클릭, 전송 또는 실패한 메시지에 반응할 수 있습니다.

* SMS 메시지의 경우, 여정은 보낸 메시지나 실패한 메시지에 반응할 수 있습니다.

* 이메일의 경우 여정은 클릭, 전송, 열림 또는 실패한 메시지에 반응할 수 있습니다. [반응 이벤트에 대해 자세히 알아보기](../building-journeys/reaction-events.md).

서드파티 시스템을 사용하여 메시지를 보낼 때 사용자 지정 작업을 추가하고 구성해야 합니다. [사용자 지정 작업 구성에 대해 자세히 알아보세요](../action/about-custom-action-configuration.md).