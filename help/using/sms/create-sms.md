---
solution: Journey Optimizer
product: journey optimizer
title: SMS 메시지 만들기
description: Journey Optimizer에서 SMS 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# SMS 메시지 만들기 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS 만들기"
>abstract="텍스트 메시지를 추가하고 표현식 편집기를 사용하여 개인화를 시작합니다."

>[!NOTE]
>
>업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. [옵트아웃을 관리하는 방법 알아보기](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## 여정 또는 캠페인에서 SMS 메시지 만들기 {#create-sms-journey-campaign}

SMS 메시지 개인화를 시작하려면 다음 단계를 수행합니다.

>[!BEGINTABS]

>[!TAB 여정에 SMS 메시지 추가]

1. 여정을 연 다음 팔레트의 작업 섹션에서 SMS 활동을 끌어서 놓습니다.

   ![](assets/sms_create_1.png)

1. 메시지(레이블, 설명, 카테고리)에 대한 기본 정보를 제공한 다음 사용할 메시지 면을 선택합니다.

   ![](assets/sms_create_2.png)

   여정을 구성하는 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)

이제 에서 SMS 메시지의 콘텐츠를 디자인할 수 있습니다 **[!UICONTROL Edit content]** 버튼을 클릭합니다. [SMS 콘텐츠 디자인](#sms-content)

>[!TAB Campaign에 SMS 메시지 추가]

1. 예약되었거나 API가 트리거된 새 캠페인을 만들어 다음을 선택합니다. **[!UICONTROL SMS]** 를 원하는 대로 선택하고 **[!UICONTROL App surface]** 를 사용하십시오. [SMS 구성에 대해 자세히 알아보기](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 클릭 **[!UICONTROL Create]**.

1. 에서 **[!UICONTROL Properties]** 섹션에서 캠페인 편집 **[!UICONTROL Title]** 및 **[!UICONTROL Description]**.

   ![](assets/sms_create_4.png)

1. 에서 **[!UICONTROL Actions tracking]** 섹션에서 SMS 메시지의 링크에 대한 클릭 수를 추적할지 지정합니다.

1. 을(를) 클릭합니다. **[!UICONTROL Select audience]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 단추입니다. [추가 정보](../segment/about-segments.md).

1. 에서 **[!UICONTROL Identity namespace]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [추가 정보](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. 캠페인은 특정 날짜 또는 반복 빈도에 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL Schedule]** 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

1. 에서 **[!UICONTROL Action triggers]** 메뉴에서 **[!UICONTROL Frequency]** SMS 메시지 개수:

   * 한 번
   * 일별
   * 주별
   * 월

이제 에서 SMS 메시지의 콘텐츠를 디자인할 수 있습니다 **[!UICONTROL Edit content]** 버튼을 클릭합니다. [SMS 콘텐츠 디자인](#sms-content)

>[!ENDTABS]

## SMS 콘텐츠 정의{#sms-content}

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL Edit content]** sms 콘텐츠를 구성하는 단추를 클릭합니다.

1. 을(를) 클릭합니다. **[!UICONTROL Message]** 필드 를 클릭하여 표현식 편집기를 엽니다.

   ![](assets/sms-content.png)

1. 표현식 편집기를 사용하여 컨텐츠를 정의하고 동적 컨텐츠를 추가합니다. 프로필 이름 또는 구/군/시 등의 속성을 사용할 수 있습니다. 추가 정보 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md) 를 입력합니다.

1. 클릭 **[!UICONTROL Save]** 미리 보기에서 메시지를 확인합니다. [추가 정보](send-sms.md)

   ![](assets/sms-content-preview.png)

**관련 항목**

* [SMS 채널 구성](sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [여정에서 메시지 추가](../building-journeys/journeys-message.md)
