---
solution: Journey Optimizer
product: journey optimizer
title: SMS/MMS 메시지 만들기
description: Journey Optimizer에서 SMS/MMS 메시지를 만드는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 3d4b4fce529db70c53daea3d15d4af9a14b57424
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 8%

---

# SMS/MMS/RCS 메시지 만들기 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="텍스트 메시지 만들기"
>abstract="문자 메시지(SMS/MMS/RCS)를 만들려면 여정이나 캠페인에 SMS 액션을 추가하고 개인화 편집기로 개인화를 시작합니다."

Adobe Journey Optimizer에서 텍스트(SMS), 풍부한 커뮤니케이션(RCS) 및 멀티미디어(MMS) 메시지를 디자인하고 보낼 수 있습니다. 먼저 여정 또는 캠페인에 SMS 작업을 추가한 다음 아래에 설명된 대로 텍스트 메시지의 콘텐츠를 정의해야 합니다. Adobe Journey Optimizer은 전송 전에 텍스트 메시지를 테스트하여 렌더링, 개인화 속성 및 기타 모든 설정을 확인할 수 있는 기능도 제공합니다.

>[!NOTE]
>
>업계 표준 및 규정에 따라 모든 SMS/MMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. [옵트아웃 관리 방법 알아보기](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)


## 문자 메시지 추가 {#create-sms-journey-campaign}

아래 탭을 탐색하여 캠페인 또는 여정에 문자 메시지(SMS/MMS/RCS)를 추가하는 방법을 알아봅니다.

>[!BEGINTABS]

>[!TAB 여정에 문자 메시지 추가]

1. 여정을 열고 팔레트의 **작업** 섹션에서 SMS 활동을 끌어서 놓습니다.

   ![](assets/sms_create_1.png)

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 입력한 다음 사용할 메시지 구성을 선택합니다.

   ![](assets/sms_create_2.png)

   여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

   **[!UICONTROL 구성]** 필드는 기본적으로 미리 채워져 있으며 사용자가 해당 채널에 대해 마지막으로 사용한 구성입니다.

이제 **[!UICONTROL 콘텐츠 편집]** 단추에서 SMS 메시지의 콘텐츠 디자인을 시작할 수 있습니다. 자세한 내용은 다음과 같습니다.

>[!TAB 캠페인에 문자 메시지 추가]

1. **[!UICONTROL 캠페인]** 메뉴에 액세스한 다음 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

1. 실행할 캠페인 유형 선택

   * **예약됨 - 마케팅**: 캠페인을 즉시 또는 지정한 날짜에 실행합니다. 예약된 캠페인은 마케팅 메시지 전송을 목적으로 합니다. 사용자 인터페이스에서 구성 및 실행됩니다.

   * **API 트리거됨 - 마케팅/트랜잭션**: API 호출을 사용하여 캠페인을 실행하십시오. API 트리거 캠페인은 마케팅 또는 트랜잭션 메시지(예: 암호 재설정, 장바구니 구매 등 개인이 수행한 작업에 따라 전송된 메시지)를 보내는 것을 목표로 합니다.

1. **[!UICONTROL 속성]** 섹션에서 Campaign의 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**&#x200B;을(를) 편집합니다.

1. 사용 가능한 Adobe Experience Platform 대상 목록에서 타깃팅할 대상을 정의하려면 **[!UICONTROL 대상 선택]** 단추를 클릭하십시오. [자세히 알아보기](../audience/about-audiences.md).

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL SMS]**&#x200B;을(를) 선택하고 새 구성을 선택하거나 만드세요.

   [이 페이지](sms-configuration.md)에서 SMS 구성에 대해 자세히 알아보세요.

   ![](assets/sms_create_3.png)

1. 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 대상 대상에 가장 적합한 옵션을 식별하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하십시오. [자세히 알아보기](../content-management/content-experiment.md)

1. **[!UICONTROL 작업 추적]** 섹션에서 SMS 메시지의 링크 클릭을 추적할지 여부를 지정합니다.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. **[!UICONTROL 이 섹션]**&#x200B;에서 캠페인의 [일정](../campaigns/create-campaign.md#schedule)을 구성하는 방법을 알아보세요.

1. **[!UICONTROL 작업 트리거]** 메뉴에서 SMS 메시지의 **[!UICONTROL 빈도]**&#x200B;를 선택합니다.

   * 한 번
   * 일별
   * 매주
   * Month

이제 아래 자세히 설명된 대로 **[!UICONTROL 콘텐츠 편집]** 단추에서 문자 메시지의 콘텐츠 디자인을 시작할 수 있습니다.

>[!ENDTABS]

## SMS/RCS 콘텐츠 정의{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="SMS 콘텐츠 정의"
>abstract="개인화 편집기를 사용하여 콘텐츠를 정의하고 동적 요소를 통합하여 문자 메시지(SMS/MMS/RCS)를 사용자 정의하고 개인화합니다."

>[!AVAILABILITY]
>
>RCS Upscale은 HIPAA 준비 서비스가 아니며, 조직에서 Journey Optimizer에서 처리하는 것이 허용될 수 있는 허용된 상태 데이터(예: 개인 건강 정보 또는 PHI)를 포함하여 민감한 개인 데이터를 수집, 저장 또는 처리하는 데 사용되어서는 안 됩니다.

메시지 콘텐츠를 구성하려면 아래 단계를 따르십시오. MMS 설정에 대한 자세한 내용은 [이 섹션](#mms-content)을 참조하세요.

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하여 텍스트 메시지 콘텐츠를 구성합니다.

1. 개인화 편집기를 열려면 **[!UICONTROL 메시지]** 필드를 클릭하십시오.

   Infobip, Twilio 또는 기타 타사 공급자가 있는 RCS 메시지의 경우 필요한 JSON 페이로드를 [사용자 지정 SMS 구성](sms-configuration-custom.md#api-credential)에 붙여 넣으십시오.

   ![](assets/sms-content.png)

1. 개인화 편집기를 사용하여 콘텐츠를 정의하고 개인화 및 다이내믹 콘텐츠를 추가합니다. 프로필 이름 또는 도시 등의 모든 속성을 사용할 수 있습니다. 조건부 규칙을 정의할 수도 있습니다. 개인화 편집기에서 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md)에 대해 자세히 알아보려면 다음 페이지로 이동하십시오.

1. 콘텐츠를 정의한 후 추적된 URL을 메시지에 추가할 수 있습니다. 이렇게 하려면 **[!UICONTROL 도우미 함수]** 메뉴에 액세스하고 **[!UICONTROL 도우미]**&#x200B;를 선택하세요.

   URL 단축 기능을 사용하려면 먼저 구성에 연결될 하위 도메인을 구성해야 합니다. [자세히 알아보기](sms-subdomains.md)

   >[!NOTE]
   >
   > SMS 하위 도메인에 액세스하고 편집하려면 프로덕션 샌드박스에 대해 **[!UICONTROL SMS 하위 도메인 관리]** 권한이 있어야 합니다. [이 섹션](../administration/high-low-permissions.md)에서 권한에 대해 자세히 알아보십시오.

   ![](assets/sms_tracking_1.png)

1. **[!UICONTROL 도우미 함수]** 메뉴에서 **[!UICONTROL URL 함수]**&#x200B;을 클릭한 다음 **[!UICONTROL URL 추가]**&#x200B;를 선택하십시오.

   ![](assets/sms_tracking_2.png)

   <!--The URL shortening function cannot be used within a fragment. TBC-->

1. `originalUrl` 필드에 단축할 URL을 붙여 넣고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!CAUTION]
   >
   > 짧은 URL의 수명은 30일로 설정됩니다. 이 기간이 지나면 이러한 짧은 URL에 더 이상 액세스할 수 없으며 `404 short-code not found` 메시지를 표시합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭하고 미리 보기에서 메시지를 확인합니다. 이제 [이 섹션](#sms-mms-test)에 자세히 설명된 대로 메시지 콘텐츠를 테스트하고 확인할 수 있습니다.

## MMS 콘텐츠 정의{#mms-content}

MMS(멀티미디어 메시지 서비스) 메시지를 전송하여 비디오, 사진, 오디오 클립 및 GIF 등의 미디어를 공유할 수 있도록 함으로써 커뮤니케이션을 향상시킬 수 있습니다. 또한 MMS를 통해 메시지에 최대 1600자의 텍스트를 입력할 수 있습니다.

>[!NOTE]
>
> MMS 채널에는 [이 페이지](../start/guardrails.md#sms-guardrails)에 나열된 몇 가지 제한 사항이 있습니다.

MMS 콘텐츠를 만들려면 다음 단계를 수행합니다.

1. [이 섹션](#create-sms-journey-campaign)에 설명된 대로 SMS를 만드십시오.

1. [이 섹션](#sms-content)에 자세히 설명된 대로 SMS 콘텐츠를 편집합니다.

1. SMS 콘텐츠에 미디어를 추가하려면 MMS 옵션을 활성화합니다.

   ![](assets/sms_create_6.png)

1. 미디어에 **[!UICONTROL 제목]**&#x200B;을 추가합니다.

1. **[!UICONTROL 미디어]** 필드에 미디어의 URL을 입력하십시오.

   ![](assets/sms_create_7.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭하고 미리 보기에서 메시지를 확인합니다. 이제 아래에 자세히 설명된 대로 메시지 콘텐츠를 테스트하고 확인할 수 있습니다.

## 메시지 테스트 및 보내기 {#sms-mms-test}

**[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 사용하여 문자 메시지 콘텐츠, 단축된 URL 및 개인화된 콘텐츠를 미리 볼 수 있습니다.

![](assets/sms-content-preview.png)

테스트를 수행하고 콘텐츠의 유효성을 검사하면 대상자에게 문자 메시지를 보낼 수 있습니다. 이러한 단계는 [이 페이지](send-sms.md)에 자세히 설명되어 있습니다

전송되면 캠페인 또는 여정 보고서 내에서 SMS의 영향을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../reports/campaign-global-report-cja-sms.md)을 참조하십시오.

**관련 항목**

* [문자 메시지 미리 보기, 테스트 및 보내기](send-sms.md)
* [SMS 채널 구성](sms-configuration.md)
* [SMS/MMS 보고서](../reports/journey-global-report-cja-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
* [캠페인에 메시지 추가](../campaigns/create-campaign.md)
