---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 구성
description: Journey Optimizer에서 푸시 알림을 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 15%

---

# 푸시 알림 만들기 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="푸시 메시지 생성"
>abstract="푸시 메시지를 추가하고 표현식 편집기로 개인화를 시작합니다."

## 여정 또는 캠페인에서 푸시 알림 만들기 {#create}

푸시 알림을 만들려면 아래 단계를 수행하십시오.

>[!BEGINTABS]

>[!TAB 여정에 푸시 추가]

1. 여정을 열고 팔레트의 작업 섹션에서 푸시 활동을 끌어다 놓습니다.

   ![](assets/push_create_1.png)

1. 메시지(레이블, 설명, 카테고리)에 대한 기본 정보를 제공한 다음 사용할 메시지 면을 선택합니다. 다음 **[!UICONTROL 서피스]** 필드는 기본적으로 사용자가 해당 채널에 사용하는 마지막 면과 함께 미리 채워져 있습니다.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >여정에서 푸시 알림을 전송하는 경우 Adobe Journey Optimizer의 전송 시간 최적화 기능을 활용하여 내역 열기 및 클릭률을 기반으로 참여를 극대화하기 위해 메시지를 보내는 최적의 시간을 예측할 수 있습니다. [전송 시간 최적화를 사용하는 방법을 알아봅니다](../building-journeys/journeys-message.md#send-time-optimization)

   여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)

1. 여정 구성 화면에서 **[!UICONTROL 컨텐츠 편집]** 푸시 컨텐츠를 구성하는 버튼을 클릭합니다. [푸시 알림 디자인](design-push.md)

1. 메시지가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다.

1. 푸시가 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 전송하기 위해

   푸시 열기 및/또는 상호 작용을 통해 수신자의 동작을 추적하려면 추적 섹션의 전용 옵션이 [이메일 활동](../building-journeys/journeys-message.md).

>[!TAB 캠페인에 푸시 추가]

1. 예약되었거나 API가 트리거된 새 캠페인을 만들어 다음을 선택합니다. **[!UICONTROL 푸시 알림]** 를 원하는 대로 선택하고 **[!UICONTROL 앱 표면]** 를 사용하십시오. [푸시 구성에 대해 자세히 알아보기](push-configuration.md).

   ![](assets/push_create_3.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

   ![](assets/push_create_4.png)

1. 을(를) 클릭합니다. **[!UICONTROL 대상 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 단추입니다. [자세히 알아보기](../segment/about-segments.md).

1. 에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. 캠페인은 특정 날짜 또는 반복 빈도에 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

1. 에서 **[!UICONTROL 작업 트리거]** 메뉴에서 **[!UICONTROL 빈도]** 푸시 알림:

   * 한 번
   * 일별
   * 주별
   * 월별

1. 캠페인 구성 화면에서 **[!UICONTROL 컨텐츠 편집]** 푸시 컨텐츠를 구성하는 버튼을 클릭합니다. [푸시 알림 디자인](design-push.md)

1. 메시지가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다.

1. 푸시가 준비되면 구성을 완료하십시오 [campaign](../campaigns/create-campaign.md) 전송하기 위해

   푸시 열기 및/또는 상호 작용을 통해 수신자의 동작을 추적하려면 추적 섹션의 전용 옵션이 [campaign](../campaigns/create-campaign.md).

>[!ENDTABS]

**관련 항목**

* [푸시 채널 구성](push-gs.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)

## 빠른 전송 모드 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="빠른 전송 모드"
>abstract="빠른 전송 모드를 사용하여 푸시 채널에서 고속 메시지를 30M 미만의 대상자 크기에 전송할 수 있습니다."

이전에 여정에서 버스트 모드라고 했던 빠른 전달 모드는 [!DNL Journey Optimizer] 캠페인을 통해 대용량 볼륨으로 푸시 메시지를 매우 빠르게 전송할 수 있는 추가 기능입니다.

신속한 게재는 휴대폰에 긴급 푸시 경고를 전송하려는 경우, 메시지 게재 지연이 비즈니스 크리티컬 상태일 때 사용됩니다. 예를 들어 뉴스 채널 앱을 설치한 사용자에게 최신 뉴스를 보냅니다.

빠른 전달 모드를 사용할 때의 성능에 대한 자세한 내용은 [Adobe Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html).

### 사전 요구 사항 {#prerequisites}

신속한 전송 메시징에는 다음과 같은 요구 사항이 포함됩니다.

* 빠른 배송이 가능한 시기 **[!UICONTROL 예약됨]** 캠페인만 사용할 수 있고 API로 트리거되는 캠페인에 사용할 수 없습니다.
* 푸시 메시지에 개인화가 허용되지 않습니다.
* 대상 대상에는 30M 미만의 프로필이 포함되어야 하며,
* 빠른 배달 모드를 사용하여 최대 5개의 캠페인을 동시에 실행할 수 있습니다.

### 빠른 전달 모드 활성화

1. 푸시 알림 캠페인을 만들고 **[!UICONTROL 신속한 전달]** 선택 사항입니다.

![](assets/create-campaign-burst.png)

1. 메시지 콘텐츠를 구성하고 타겟팅할 대상을 선택합니다. [캠페인을 만드는 방법을 알아봅니다](#create)

   >[!IMPORTANT]
   >
   >메시지 콘텐츠에 개인화가 포함되지 않으며 대상자에 30M 미만의 프로필이 포함되어 있는지 확인합니다.

1. 평소대로 캠페인을 검토하고 활성화합니다. 테스트 모드에서는 메시지가 빠른 게재 모드를 통해 전송되지 않습니다.