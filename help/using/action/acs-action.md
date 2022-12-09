---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign Standard와 통합
description: Adobe Campaign Standard와 통합하는 방법을 알아봅니다
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Adobe Campaign Standard와 통합 {#using_adobe_campaign_standard}

Adobe Campaign Standard의 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다.

Adobe Campaign Standard가 설치되어 있다면 Adobe Campaign Standard에 연결할 수 있는 기본 작업을 사용할 수 있습니다.

Campaign Standard 트랜잭션 메시지와 관련 이벤트를 Journey Optimizer에서 사용하려면 게시해야 합니다. 이벤트가 게시되었지만 메시지가 게시되지 않은 경우 Journey Optimizer 인터페이스에 표시되지 않습니다. 메시지가 게시되었지만 연결된 이벤트가 게시되지 않은 경우 Journey Optimizer 인터페이스에 표시되지만 사용할 수 없습니다.

## 중요 정보 {#important-notes}

* Adobe Campaign Standard 작업에 대해 5분당 4000호출의 최대 가용량 규칙이 자동으로 정의됩니다. 이는 Adobe Campaign Standard 트랜잭션 메시지의 공식 규모에 해당합니다. 의 트랜잭션 메시지 SLA에 대해 자세히 알아보십시오. [Adobe Campaign Standard 제품 설명](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard 통합은 작업 목록의 전용 기본 작업을 통해 설정됩니다. 각 샌드박스에 대해 구성해야 합니다.

* 세그먼트 자격 또는 세그먼트 읽기 활동과 함께 Campaign Standard 작업을 사용할 수 없습니다.

* 여정에서 메시지 및 Campaign Standard 작업을 모두 사용할 수 없습니다.

## 작업 구성 {#configure-action}

구성하는 단계는 다음과 같습니다.

1. 선택 **[!UICONTROL Configurations]** 를 클릭합니다. 에서  **[!UICONTROL Actions]** 섹션을 클릭합니다. **[!UICONTROL Manage]**. 작업 목록이 표시됩니다.

1. 기본 제공 선택 **[!UICONTROL AdobeCampaignStandard]** 작업. 화면 오른쪽에 작업 구성 창이 열립니다.

   ![](assets/actioncampaign.png)

1. Adobe Campaign Standard 인스턴스 URL을 복사하여 다음 위치에 붙여넣습니다 **[!UICONTROL URL]** 필드.

1. 을(를) 클릭합니다. **[!UICONTROL Test the instance URL]** 를 눌러 인스턴스의 유효성을 테스트합니다.

   >[!NOTE]
   >
   >이 테스트는 다음을 확인합니다.
   >
   >호스트는 &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; 또는 &quot;.adls.adobe.com&quot;입니다.
   >
   >URL은 https,
   >
   >이 Adobe Campaign Standard 인스턴스에 연결된 ORG는 Journey Optimizer의 ORG와 동일합니다.

여정을 디자인할 때에는 **[!UICONTROL Action]** 범주: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** 자세한 내용은 [Adobe Campaign 작업 사용](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

을(를) 사용할 수 있습니다 **반응** 이벤트는 동일한 여정 내에서 전송된 Campaign Standard 메시지와 관련된 추적 데이터에 응답합니다. 푸시 알림의 경우 클릭, 전송 또는 실패한 메시지에 대응할 수 있습니다. SMS 메시지의 경우 보낸 메시지나 실패한 메시지에 대응할 수 있습니다. 이메일의 경우 클릭, 전송, 열림 또는 실패한 메시지에 대응할 수 있습니다. 자세한 내용은 [반응 이벤트](../building-journeys/reaction-events.md).

서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 추가하고 구성해야 합니다. 자세한 내용은 [사용자 지정 작업 구성](../action/about-custom-action-configuration.md).
