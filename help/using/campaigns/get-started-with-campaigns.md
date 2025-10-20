---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 시작
description: Journey Optimizer의 캠페인에 대해 자세히 알아보기
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 캠페인, 방법 , 시작, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="캠페인 예약"
>abstract="기본적으로 캠페인은 수동 활성화를 통해 시작되고 메시지가 한 번 발송되는 즉시 종료됩니다. 메시지를 전송할 특정 날짜와 시간을 유연하게 설정할 수 있습니다. 또한 반복적인 액션 캠페인의 종료 날짜를 지정할 수 있습니다. 액션 트리거에서는 환경 설정에 따라 메시지 전송 빈도를 구성할 수도 있습니다."

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

[!DNL Journey Optimizer] 캠페인을 사용하면 여러 채널에서 특정 대상자에게 일회성 콘텐츠를 게재할 수 있습니다. 작업을 단계별로 실행하는 여정과 달리 캠페인은 즉시 또는 정의된 일정에 따라 작업을 동시에 수행합니다.

![](assets/gs-campaigns.png)

## 캠페인 유형

[!DNL Journey Optimizer]에서는 세 가지 캠페인 유형을 지원합니다. 각 유형은 다양한 사용 사례에 적합하며 여러 채널을 지원합니다.

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB 오케스트레이션된 캠페인]

**오케스트레이션된 캠페인**&#x200B;은 다양한 채널에서 브랜드가 주도하는 정교한 마케팅 캠페인을 실시하여 대규모로 참여도, 수익, 고객 충성도를 촉진하는 데 도움이 됩니다.

크로스 채널 마케팅은 필수적이지만 오케스트레이션된 캠페인을 통해 원활하게 이루어집니다. 드래그하여 놓는 시각적 인터페이스를 통해 세그먼테이션에서 메시지 게재에 이르기까지 여러 채널에 걸쳐 복잡한 마케팅 워크플로를 디자인하고 자동화할 수 있습니다. 속도, 제어 및 효율성을 위해 구축된 하나의 직관적인 환경에서 모든 작업이 수행됩니다.

➡️ [오케스트레이션된 캠페인을 활용하는 방법 알아보기](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB 액션 캠페인(또는 예약된 캠페인)]

**액션 캠페인**&#x200B;은 예약된 캠페인이라고도 하며, 간단한 임시 일괄 처리 커뮤니케이션을 허용합니다.

* **예약됨 - 마케팅** - 프로모션 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 활용 사례에 사용됩니다. 수신자가 옵트인해야 합니다.
* **예약됨 - 트랜잭션** - 마케팅 캠페인과 달리 트랜잭션 캠페인에서는 수신자가 옵트인할 필요가 없습니다. 중단, 긴급 상황, 취소와 관련된 통신에 이 범주를 사용하십시오. 지원되는 채널: 이메일, SMS, 푸시 알림.

➡️ [액션 캠페인을 활용하는 방법 알아보기](create-campaign.md)

>[!TAB API 트리거 캠페인]

**API 트리거 캠페인**&#x200B;을 사용하면 API 호출을 사용하여 캠페인 실행을 트리거할 수 있습니다. 이러한 커뮤니케이션은 필요한 경우 암호 재설정과 같은 프로필 속성을 사용할 뿐만 아니라 REST API 페이로드인 트리거에서 실시간 컨텍스트 데이터를 사용할 수 있는 개인화가 포함될 수 있는 위치에 보낼 수 있습니다.

* **API가 트리거됨 - 마케팅** - 개인화된 마케팅 커뮤니케이션을 타깃팅된 대상자에게 보냅니다.
* **API 트리거됨 - 트랜잭션** - 암호 재설정 요청, 장바구니 구매 등과 같이 개인이 수행한 작업에 따라 메시지를 보냅니다.

➡️ [API 트리거 캠페인 작업 방법 알아보기](api-triggered-campaigns.md)


>[!ENDTABS]

## 캠페인 유형별 지원되는 채널 {#channels}

아래 표는 지원되는 위치를 나타내는 다양한 캠페인 유형에서 각 채널의 가용성을 보여줍니다.

| 채널 | 작업(마케팅) | 작업(트랜잭션) | API 트리거됨(마케팅) | API 트리거됨(트랜잭션) | 오케스트레이션됨 |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| 이메일 | ✅ | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ | ✅ |
| 푸시 알림 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 인앱 | ✅ | — | — | — | — |
| 다이렉트 메일 | ✅ | — | — | — | — |
| 웹 | ✅ | — | — | — | — |
| 코드 기반 표현식. | ✅ | — | — | — | — |
| 콘텐츠 카드 | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| 선 | ✅ | — | — | — | — |

## 전제 조건 {#prerequisites}

캠페인을 만들기 전에 아래의 사전 요구 사항을 검토했는지 확인하십시오.

* **대상자** 캠페인을 만들기 전에 대상자를 사용할 수 있어야 합니다. [대상자 시작하기](../audience/about-audiences.md).

* **채널 구성** - 채널을 선택하려면 해당 채널 구성(즉, 사전 설정)을 만들고 사용할 수 있는 상태로 설정해야 합니다. [채널 구성을 설정하는 방법을 알아봅니다](../configuration/channel-surfaces.md).

* **권한** - 캠페인은 아래 나열된 적절한 권한이 있는 사용자만 사용할 수 있습니다. 캠페인 기능에 액세스할 수 없는 경우 관리자에게 연락하여 필요한 권한을 요청하십시오. [Journey Optimizer 기본 제공 역할에 대해 자세히 알아보기](../administration/ootb-product-profiles.md)

  | 캠페인 유형 | 권한 |
  |----------------------------|----------------------------------------------------------------------------|
  | **액션 캠페인** | 캠페인 전체 관리자<br>캠페인 승인자<br>캠페인 관리자<br>캠페인 확인자 |
  | **API 트리거 캠페인** | 캠페인 전체 관리자<br>캠페인 승인자<br>캠페인 관리자<br>캠페인 확인자 |
  | **오케스트레이션된 캠페인** | 오케스트레이션된 캠페인 전체 관리자<br>오케스트레이션된 캠페인 승인자<br>오케스트레이션된 캠페인 관리자<br>오케스트레이션된 캠페인 확인자 |

  +++캠페인 관련 역할 할당하는 방법 알아보기

   1. [!DNL Permissions] 제품에서 사용자에게 역할을 할당하려면 **[!UICONTROL 역할]** 탭으로 이동하여 위에 설명된 기본 제공 캠페인 관련 **[!UICONTROL 역할]** 중 하나를 선택하십시오.

   1.  **[!UICONTROL 사용자]** 탭에서 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

   1. 사용자 이름 또는 전자 메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

      이전에 사용자를 생성하지 않은 경우 [사용자 설명서 추가](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/ui/users)를 참조하십시오.

  그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

  +++

## 더 자세히 알아보기

[!DNL Journey Optimizer]의 캠페인에 대해 이해했다면 이 설명서 섹션을 자세히 살펴보고 첫 번째 캠페인을 만들 차례입니다.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="액션 캠페인" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">액션 캠페인</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 트리거 캠페인</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="푸시" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">오케스트레이션된 캠페인</a></td>
</tr></table>
