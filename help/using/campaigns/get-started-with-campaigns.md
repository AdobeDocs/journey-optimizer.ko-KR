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
source-git-commit: 4bd3e202935cfc971990faa7d1dd2f3d0d7cdc6d
workflow-type: ht
source-wordcount: '879'
ht-degree: 100%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="캠페인 일정"
>abstract="기본적으로 캠페인은 수동 활성화 시 시작되고 메시지가 전송된 후에 즉시 종료됩니다. 메시지를 보낼 특정 날짜와 시간을 유연하게 설정할 수 있습니다. 또한 반복적인 액션 캠페인의 종료 날짜를 지정할 수 있습니다. 액션 트리거에서 환경 설정에 맞게 메시지 전송 빈도를 구성할 수도 있습니다."

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
>title="속도 제어"
>abstract="원하는 속도 제한을 지정하여 캠페인에 대한 속도 제어를 설정합니다. 이 기능은 랜딩 페이지나 고객 지원 센터 플랫폼과 같은 다운스트림 시스템의 오버로드를 방지하는 데 특히 유용합니다."

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
>abstract="캠페인 유형을 선택합니다. 사용 가능한 채널은 선택한 유형에 따라 다릅니다. <br>**예약된 캠페인**(액션 캠페인) – 특정 시간에 실행되도록 예약할 수 있는 간단한 일회성 일괄 커뮤니케이션에 적합합니다.<br>**API 트리거 캠페인** – API 호출을 통해 활성화되어 외부 시스템에서 직접 자동화된 이벤트 기반 메시징을 사용할 수 있습니다.<br>**오케스트레이션된 캠페인** – 시각적으로 명확한 드래그 앤 드롭 캔버스를 제공하여 대상자 세분화부터 채널 전반의 개인화된 메시지 게재에 이르기까지 복잡하고 다단계적인 마케팅 워크플로를 설계하고 자동화합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="캠페인"
>abstract="세분화 플로우를 만들고 크로스 채널 메시지를 작성하고 캠페인을 기획합니다. 지원되는 채널: 이메일, SMS, 푸시 알림."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="캠페인"
>abstract="단일 또는 반복 아웃바운드 게재 또는 지속적인 인바운드 액션을 게재합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="캠페인"
>abstract="단일 또는 반복 아웃바운드 트랜잭션 액션을 게재합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="캠페인"
>abstract="타깃 대상자에게 개인화된 마케팅 커뮤니케이션을 게재합니다. 지원 채널: 이메일, SMS, 푸시 알림."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="캠페인"
>abstract="개별 프로필이나 프로필 그룹에 트랜잭션 커뮤니케이션을 보내 보세요. 지원 채널: 이메일, SMS, 푸시 알림."

Journey Optimizer 캠페인으로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다.

![](assets/gs-campaigns.png)

Journey Optimizer에서 다양한 유형의 캠페인을 만들 수 있습니다. 캠페인 유형에 따라 지원하는 채널 및 사용 사례가 달라집니다. 유형은 아래에 나와 있습니다.

* **액션 캠페인**

  액션 캠페인(또는 예약 캠페인)을 사용하면 프로모션 제안, 참여 캠페인, 공지, 법적 고지 또는 정책 업데이트와 같은 마케팅 사용 사례에 대한 간단한 임시 일괄 커뮤니케이션을 수행할 수 있습니다. [이 페이지에서](create-campaign.md) 액션 캠페인 기능, 사용 사례, 지원되는 채널에 대해 자세히 확인할 수 있습니다.

* **API 트리거 캠페인**

  API 트리거 캠페인을 사용하면 적시에 마케팅 커뮤니케이션을 대상자에게 보내거나 암호 재설정 등 개인에 대한 트랜잭션/운영 메시지를 보낼 수 있습니다. 이 경우 프로필 속성뿐만 아니라 실시간 상황 데이터, 즉 REST API 페이로드를 사용한 개인화가 필요할 수 있습니다. [이 페이지에서](api-triggered-campaigns.md) API 트리거 캠페인의 기능, 사용 사례, 지원 채널에 대해 자세히 알아볼 수 있습니다.

* **오케스트레이션된 캠페인**

  Adobe Journey Optimizer의 캠페인 오케스트레이션은 채널 전반에서 정교한 브랜드 주도 마케팅 캠페인을 강화하여 규모에 맞게 참여도, 매출, 고객 충성도를 높일 수 있습니다.

  크로스 채널 마케팅은 필수적이지만 오케스트레이션된 캠페인을 통해 원활하게 이루어집니다. 드래그하여 놓는 시각적 인터페이스를 통해 세그먼테이션에서 메시지 게재에 이르기까지 여러 채널에 걸쳐 복잡한 마케팅 워크플로를 디자인하고 자동화할 수 있습니다. 속도, 제어, 효율성을 위해 구축된 하나의 직관적인 환경에서 모든 작업이 수행됩니다. [이 페이지에서](../orchestrated/gs-orchestrated-campaigns.md) 오케스트레이션된 캠페인의 기능, 사용 사례, 지원 채널에 대해 자세히 확인할 수 있습니다.

## 전제 조건 {#prerequisites}

캠페인을 만들기 전에 아래의 사전 요구 사항을 검토했는지 확인하십시오.

### 권한

캠페인은 아래 나열된 적절한 권한이 있는 사용자만 사용할 수 있습니다. [Journey Optimizer 기본 제공 역할에 대해 자세히 알아보기](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB 액션 캠페인]

캠페인 관리자
캠페인 승인자
캠페인 관리자
캠페인 뷰어

>[!TAB API 트리거 캠페인]

캠페인 관리자
캠페인 승인자
캠페인 관리자
캠페인 뷰어

>[!TAB 오케스트레이션된 캠페인]

오케스트레이션된 캠페인 관리자
오케스트레이션된 캠페인 승인자
오케스트레이션된 캠페인 관리자
오케스트레이션된 캠페인 뷰어

>[!ENDTABS]

캠페인 기능에 액세스할 수 없는 경우 관리자에게 연락하여 필요한 권한을 요청하십시오.

+++캠페인 관련 역할 할당하는 방법 알아보기

1. [!DNL Permissions] 제품에서 사용자에게 역할을 할당하려면 **[!UICONTROL 역할]** 탭으로 이동하여 위에 설명된 기본 제공 캠페인 관련 **[!UICONTROL 역할]** 중 하나를 선택하십시오.

1.  **[!UICONTROL 사용자]** 탭에서 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

1. 사용자 이름 또는 이메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**&#x200B;합니다.

   이전에 사용자를 생성하지 않은 경우 [사용자 설명서 추가](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/ui/users)를 참조하십시오.

그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

+++

### 대상자

캠페인을 만들기 전에 대상자를 사용할 수 있어야 합니다. [대상자 시작하기](../audience/about-audiences.md).

### 채널 구성

채널을 선택하려면 해당 채널 구성(즉, 사전 설정)을 만들고 사용할 수 있는 상태로 설정해야 합니다. [채널 구성을 설정하는 방법을 알아봅니다](../configuration/channel-surfaces.md).

## 더 자세히 알아보기

[!DNL Journey Optimizer]의 캠페인에 대해 이해했다면 이 설명서 섹션을 자세히 살펴보고 첫 번째 캠페인을 만들 차례입니다.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="액션 캠페인" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">액션 캠페인</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 트리거 캠페인</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="푸시" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">오케스트레이션된 캠페인</a></td>
</tr></table>
