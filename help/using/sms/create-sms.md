---
solution: Journey Optimizer
product: journey optimizer
title: SMS 메시지 만들기
description: Journey Optimizer에서 SMS 메시지를 만드는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 18%

---

# SMS 메시지 만들기 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS 메시지 만들기"
>abstract="SMS 메시지를 추가하고 표현식 편집기로 개인화를 시작합니다."

## SMS 메시지 추가 {#create-sms-journey-campaign}

아래 탭을 탐색하여 캠페인 또는 여정에 SMS 메시지를 추가하는 방법을 알아보십시오.

>[!BEGINTABS]

>[!TAB 여정에 SMS 메시지 추가]

1. 여정을 연 다음 **작업** 팔레트의 섹션입니다.

   ![](assets/sms_create_1.png)

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 입력한 다음 사용할 메시지 표면을 선택합니다.

   ![](assets/sms_create_2.png)

   여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)

   다음 **[!UICONTROL 표면]** 필드는 기본적으로 미리 채워져 있으며 사용자가 해당 채널에 대해 마지막으로 사용한 서페이스가 있습니다.

이제에서 SMS 메시지의 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [SMS 콘텐츠 정의](#sms-content)

>[!TAB Campaign에 SMS 메시지 추가]

1. 새 예약된 캠페인 또는 API에서 트리거된 캠페인을 만들고, 다음을 선택합니다. **[!UICONTROL SMS]** 을(를) 작업으로 선택하고 **[!UICONTROL 앱 표면]** 사용할 수 있습니다. [SMS 구성에 대해 자세히 알아보기](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 다음에서 **[!UICONTROL 속성]** 섹션, 캠페인의 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

   ![](assets/sms_create_4.png)

1. 다음을 클릭합니다. **[!UICONTROL 대상자 선택]** 사용 가능한 Adobe Experience Platform 대상 목록에서 타깃팅할 대상을 정의하는 단추입니다. [자세히 알아보기](../audience/about-audiences.md).

1. 다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. 클릭 **[!UICONTROL 실험 만들기]** 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 타겟 대상자에 대한 최상의 옵션을 식별합니다. [자세히 알아보기](../campaigns/content-experiment.md)

1. 다음에서 **[!UICONTROL 작업 추적]** 섹션에서 SMS 메시지의 링크 클릭을 추적할지 여부를 지정합니다.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 의 내 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

1. 다음에서 **[!UICONTROL 작업 트리거]** 메뉴에서 다음을 선택합니다. **[!UICONTROL 빈도]** SMS 메시지:

   * 한 번
   * 일별
   * 주별
   * 월

이제에서 SMS 메시지의 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [SMS 콘텐츠 디자인](#sms-content)

>[!ENDTABS]

## SMS 콘텐츠 정의{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="SMS 콘텐츠 정의"
>abstract="표현식 편집기를 사용하여 콘텐츠를 정의하고 동적 요소를 통합하여 SMS 메시지를 사용자 정의하고 개인화합니다."

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL 콘텐츠 편집]** SMS 콘텐츠를 구성하는 단추입니다.

1. 다음을 클릭합니다. **[!UICONTROL 메시지]** 표현식 편집기를 여는 필드입니다.

   ![](assets/sms-content.png)

1. 표현식 편집기를 사용하여 콘텐츠를 정의하고 다이내믹 콘텐츠를 추가합니다. 프로필 이름 또는 구/군/시 등의 모든 속성을 사용할 수 있습니다. 자세히 알아보기 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md) 를 입력합니다.

1. 콘텐츠를 정의한 후 추적 URL을 메시지에 추가할 수 있습니다. 이렇게 하려면 **[!UICONTROL 도우미 함수]** 메뉴 및 선택 **[!UICONTROL 도우미]**.

   URL 단축 기능을 사용하려면 먼저 표면에 연결될 하위 도메인을 구성해야 합니다. [자세히 알아보기](sms-subdomains.md)

   >[!CAUTION]
   >
   > SMS 하위 도메인에 액세스하고 편집하려면 **[!UICONTROL SMS 하위 도메인 관리]** 프로덕션 샌드박스에 대한 권한.

   ![](assets/sms_tracking_1.png)

1. 다음 범위 내 **[!UICONTROL 도우미 함수]** 메뉴, 클릭 **[!UICONTROL URL 함수]** 다음을 선택합니다. **[!UICONTROL URL 추가]**.

   ![](assets/sms_tracking_2.png)

1. 다음에서 `originalUrl` 필드에 단축할 URL을 붙여넣습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭하고 미리보기에서 메시지를 확인합니다. 다음을 사용할 수 있습니다. **[!UICONTROL 콘텐츠 시뮬레이션]** 축약된 URL 또는 개인화된 콘텐츠를 미리 볼 수 있습니다.

   ![](assets/sms-content-preview.png)

이제 SMS 메시지를 테스트하고 대상자에게 보낼 수 있습니다. [자세히 알아보기](send-sms.md)
전송되면 캠페인 또는 여정 보고서 내에서 SMS의 영향을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../reports/campaign-global-report.md#sms-tab)을 참조하십시오.

>[!NOTE]
>
>업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. [옵트아웃 관리 방법 알아보기](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**관련 항목**

* [SMS 메시지 미리 보기, 테스트 및 보내기](send-sms.md)
* [SMS 채널 구성](sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
* [캠페인에 메시지 추가](../campaigns/create-campaign.md)
