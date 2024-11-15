---
solution: Journey Optimizer
product: journey optimizer
title: 조각으로 시작
description: 컨텐츠 조각을 사용하여 Journey Optimizer 캠페인 및 여정에서 컨텐츠를 재사용하는 방법에 대해 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 2f5195f209c5e0e5665722b7c1e12e164acc587e
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 13%

---

# 조각으로 시작 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="나만의 조각 정의"
>abstract="여러 여정과 캠페인 전반에서 콘텐츠를 재사용할 수 있도록 독립 실행형 조각을 만들고 관리합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="조각 만들기"

조각은 [!DNL Journey Optimizer] 캠페인 및 여정에서 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다. 이 기능을 사용하면 마케팅 사용자가 향상된 디자인 프로세스에서 이메일 콘텐츠를 빠르게 조합하는 데 사용할 수 있는 여러 사용자 지정 콘텐츠 블록을 미리 빌드할 수 있습니다.

![](../rn/assets/do-not-localize/fragments.gif)

➡️[이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다](#video-fragments)

조각을 최대한 활용하려면 다음을 수행하십시오.

* **나만의 조각 만들기**: 처음부터 만들거나 콘텐츠를 조각으로 저장하여 시각적 또는 표현식 조각을 만듭니다. [조각을 만드는 방법을 알아보세요](#create-fragments). 또한 Journey Optimizer **콘텐츠 REST API**&#x200B;를 활용하여 콘텐츠 조각을 관리할 수 있습니다. 자세한 내용은 [Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}를 참조하세요.
* **조각 재사용:** 콘텐츠에 필요한 만큼 조각을 사용합니다. [시각적 조각 추가](../email/use-visual-fragments.md) 및 [식 조각 활용](../personalization/use-expression-fragments.md)을 참조하십시오.

## 시작하기 전 {#fragment-prerequisites}

조각을 만들고, 편집하고, 보관하고, 게시하려면 **[!DNL Content Library Manager]** 제품 프로필에 포함된 **[!DNL Manage library items]** 및 **[Publish 조각]** 권한이 필요합니다. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

이 버전에서는 다음 제한 사항이 적용됩니다.

* **시각적 조각**&#x200B;은(는) 전자 메일 채널에만 사용할 수 있습니다.
* 인앱 채널에는 **식 조각**&#x200B;을(를) 사용할 수 없습니다.

## 시각적 및 표현식 조각 {#visual-expression}

다음과 같은 두 가지 유형의 조각을 사용할 수 있습니다.

* **시각적 조각**&#x200B;은(는) [이메일 Designer](../email/get-started-email-design.md) 또는 [콘텐츠 템플릿](../email/use-email-templates.md)을(를) 사용하여 여러 이메일 게재에서 다시 사용할 수 있는 사전 정의된 시각적 블록입니다.
* **식 조각**&#x200B;은(는) [개인화 편집기](../personalization/personalization-build-expressions.md)의 전용 항목에서 사용할 수 있는 미리 정의된 식입니다.

만든 모든 조각은 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]** 왼쪽 메뉴에서 액세스할 수 있습니다. [조각 관리 방법 알아보기](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## 방법 비디오 {#video-fragments}

[!DNL Journey Optimizer]에서 **시각적 조각**&#x200B;을(를) 관리, 작성 및 사용하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

[!DNL Journey Optimizer]에서 **표현식 조각**&#x200B;을(를) 관리, 작성 및 사용하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
