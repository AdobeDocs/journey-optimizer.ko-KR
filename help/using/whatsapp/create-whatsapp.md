---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 메시지 만들기
description: Journey Optimizer에서 WhatsApp 메시지를 만드는 방법을 알아봅니다
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: cac6f675-59e0-431d-8c20-f24ef16d7bf2
source-git-commit: 6268989c14ccb0ae6fd5ac271a33efe4877dd903
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 3%

---

# WhatsApp 메시지 만들기 {#create-whatsapp}

>[!BEGINSHADEBOX]

**목차**

* [WhatsApp 메시지 시작](get-started-whatsapp.md)
* [WhatsApp 구성 시작](whatsapp-configuration.md)
* **[WhatsApp 메시지 만들기](create-whatsapp.md)**
* [WhatsApp 메시지 확인 및 보내기](send-whatsapp.md)

>[!ENDSHADEBOX]

Adobe Journey Optimizer을 사용하면 WhatsApp에서 매력적인 메시지를 디자인하고 보낼 수 있습니다. 여정 또는 캠페인에 WhatsApp 작업을 추가하고 아래에 자세히 설명된 대로 메시지 콘텐츠를 만들면 됩니다. 또한 Adobe Journey Optimizer을 사용하면 WhatsApp 메시지를 보내기 전에 테스트하여 완벽한 렌더링, 정확한 개인화 및 모든 설정의 적절한 구성을 보장할 수 있습니다.

Journey Optimizer에서는 아웃바운드 메시지 요소만 지원됩니다.

+++ 지원되는 메시지 요소 및 작업에 대한 호출에 대해 자세히 알아보기

WhatsApp에서는 다음 메시지 유형이 지원됩니다.

| 메시지 기능 | 설명 |
|-|-|
| 헤더 | 메시지 본문 위에 표시되는 선택적 텍스트입니다. |
| 텍스트 | 매개 변수를 통해 다이내믹 콘텐츠를 지원합니다. |
| 이미지(JPEG, PNG) | 8비트 RGB 또는 RGBA 형식이어야 하며 크기가 5MB 미만이어야 합니다. |
| 비디오 | 16MB 이하의 3GPP 또는 MP4여야 하며 URL을 통해 호스팅되어야 합니다. |
| 오디오 | 응답 메시지에만 사용할 수 있습니다. AAC, AMR, MP3, MP4 오디오 또는 OGG 형식이어야 하며 URL에서 호스팅되고 16MB 미만이어야 합니다. |
| 문서 | URL에서 호스팅되는 100MB 미만이어야 하며 .txt, .xls/.xlsx, .doc/.docx, .ppt/.pptx 또는 .pdf 형식 중 하나여야 합니다. |
| 본문 텍스트 | 매개 변수를 통해 다이내믹 콘텐츠를 지원합니다. |
| 바닥글 텍스트 | 매개 변수를 통해 다이내믹 콘텐츠를 지원합니다. |

WhatsApp 메시지에 다음과 같은 콜 투 액션 옵션을 사용할 수 있습니다.

| 콜 투 액션 | 설명 |
|-|-|
| 전화 번호 | 메시지 템플릿에서만 사용할 수 있습니다. 버튼 하나로 제한됩니다. |
| 사용자 정의 빠른 회신 단추 | 최대 3개의 버튼을 지원합니다. |
| 마케팅 옵트아웃 단추 | 구독 상태를 자동으로 업데이트하지 않습니다. |
| 쿠폰 코드 메시지 템플릿 | 메시지 템플릿에서만 사용할 수 있습니다. |
| CTA 응답 메시지 | 반응 메시지에 콜 투 액션 버튼을 포함할 수 있습니다. |

+++

## WhatsApp 메시지 추가 {#create-whatsapp-journey-campaign}

아래 탭을 탐색하여 캠페인 또는 여정에 WhatsApp 메시지를 추가하는 방법을 알아보십시오.

>[!BEGINTABS]

>[!TAB 여정에 WhatsApp 메시지 추가]

1. 여정을 열고 팔레트의 **작업** 섹션에서 **WhatsApp 활동**&#x200B;을(를) 끌어서 놓습니다.

   ![](assets/whatsapp-create-jo.png)

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 입력한 다음 사용할 메시지 구성을 선택합니다.

   여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

   **[!UICONTROL 구성]** 필드는 기본적으로 미리 채워져 있으며 사용자가 해당 채널에 대해 마지막으로 사용한 구성입니다.

이제 아래 자세히 설명된 대로 **[!UICONTROL 콘텐츠 편집]** 단추에서 WhatsApp 메시지의 콘텐츠 디자인을 시작할 수 있습니다.

>[!TAB Campaign에 WhatsApp 메시지 추가]

1. **[!UICONTROL 캠페인]** 메뉴에 액세스한 다음 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

1. **예약됨 - 마케팅** 캠페인 유형을 선택합니다.

1. **[!UICONTROL 속성]** 섹션에서 Campaign의 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**&#x200B;을(를) 편집합니다.

1. 사용 가능한 Adobe Experience Platform 대상 목록에서 타깃팅할 대상을 정의하려면 **[!UICONTROL 대상 선택]** 단추를 클릭하십시오. [자세히 알아보기](../audience/about-audiences.md).

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL WhatsApp]**&#x200B;을(를) 선택하고 새 구성을 선택하거나 만드십시오.

   [이 페이지](whatsapp-configuration.md)에서 WhatsApp 구성에 대해 자세히 알아보세요.

1. 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 대상 대상에 가장 적합한 옵션을 식별하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하십시오. [자세히 알아보기](../content-management/content-experiment.md)

1. **[!UICONTROL 작업 추적]** 섹션에서 WhatsApp 메시지의 링크 클릭을 추적할지 여부를 지정합니다.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. [이 섹션](../campaigns/create-campaign.md#schedule)에서 캠페인의 **[!UICONTROL 일정]**&#x200B;을 구성하는 방법을 알아보세요.

1. **[!UICONTROL 작업 트리거]** 메뉴에서 WhatsApp 메시지의 **[!UICONTROL 빈도]**&#x200B;를 선택합니다.

   * 한 번
   * 일별
   * 주간
   * 월

이제 아래 자세히 설명된 대로 **[!UICONTROL 콘텐츠 편집]** 단추에서 WhatsApp 메시지의 콘텐츠 디자인을 시작할 수 있습니다.

>[!ENDTABS]

## WhatsApp 콘텐츠 정의{#whatsapp-content}

>[!BEGINSHADEBOX]

Journey Optimizer에서 WhatsApp 메시지를 디자인하기 전에 먼저 메타에서 템플릿을 만들고 디자인해야 합니다. [자세히 알아보기](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343)

Journey Optimizer에서 WhatsApp 템플릿을 사용하기 전에 먼저 Meta에서 승인해야 합니다. 이 프로세스는 보통 몇 시간이 걸리지만 최대 24시간이 소요될 수 있습니다. [자세히 알아보기](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/#approval-process)

>[!ENDSHADEBOX]

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하여 WhatsApp 메시지 콘텐츠를 구성합니다.

<!--
1. Select **[!UICONTROL Template message]**.
-->

1. **템플릿 범주** 선택:

   * 마케팅
   * 유틸리티
   * 인증

   [템플릿 범주에 대해 자세히 알아보기](https://developers.facebook.com/docs/whatsapp/updates-to-pricing/new-template-guidelines/#template-category-guidelines)

1. **WhatsApp 템플릿** 드롭다운에서 메타로 이전에 만든 템플릿을 선택합니다.

   [Whatsapp 템플릿을 만드는 방법에 대해 자세히 알아보기](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343)

1. 개인화 편집기를 사용하여 템플릿에 개인화를 추가합니다. 프로필 이름 또는 도시 등의 모든 속성을 사용할 수 있습니다.

   [개인화](../personalization/personalize.md)에 대해 자세히 알아보려면 다음 페이지를 검색하십시오.

1. **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 사용하여 WhatsApp 메시지 콘텐츠, 단축된 URL 및 개인화된 콘텐츠를 미리 볼 수 있습니다. [자세히 알아보기](send-whatsapp.md)

테스트를 수행하고 콘텐츠의 유효성을 검사하면 WhatsApp 메시지를 대상자에게 보낼 수 있습니다. 이러한 단계는 [이 페이지](send-whatsapp.md)에 자세히 설명되어 있습니다


<!--
* **[!UICONTROL Template message]**: Predefined message imported from Meta into Journey Optimizer. These are intended for sending notifications, alerts, or updates to your customers.

* **[!UICONTROL Response message]**: Message created in Journey Optimizer and sent in reply to customer queries or interactions.

>[!BEGINTABS]

>[!TAB Template message]

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the WhatsApp message content.

1. Select **[!UICONTROL Template message]**.

1. Choose your Template category. [Learn more](https://developers.facebook.com/docs/WhatsApp/updates-to-pricing/new-template-guidelines/)

1. From the **WhatsApp template** drop-down, select your previously created template designed in Meta.

1. Use the personalization editor to define content, add personalization and dynamic content. You can use any attribute, such as the profile name or city for example. You can also define conditional rules. Browse to the following pages to learn more about [personalization](../personalization/personalize.md) and [dynamic content](../personalization/get-started-dynamic-content.md) in the personalization editor.

1. Use the **[!UICONTROL Simulate content]** button to preview your WhatsApp message content, shortened URLs, and personalized content. [Learn more](send-whatsapp.md)

Once you have performed your tests and validated the content, you can send your WhatsApp message to your audience. These steps are detailed in [this page](send-whatsapp.md)

>[!TAB Response message]

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the WhatsApp message content.

1. Select **[!UICONTROL Response message]**.

1. Enter your text in the **[!UICONTROL Body]** field.

1. Use the personalization editor to define content, add personalization and dynamic content. You can use any attribute, such as the profile name or city for example. You can also define conditional rules. Browse to the following pages to learn more about [personalization](../personalization/personalize.md) and [dynamic content](../personalization/get-started-dynamic-content.md) in the personalization editor.

1. Use the **[!UICONTROL Simulate content]** button to preview your WhatsApp message content, shortened URLs, and personalized content. [Learn more](send-whatsapp.md)

Once you have performed your tests and validated the content, you can send your WhatsApp message to your audience. These steps are detailed in [this page](send-whatsapp.md)

>[!ENDTABS]
-->
