---
solution: Journey Optimizer
product: journey optimizer
title: 조각 시작
description: 컨텐츠 조각을 사용하여 Journey Optimizer 캠페인 및 여정에서 컨텐츠를 재사용하는 방법에 대해 알아봅니다
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: e7ff784d51da48c1970841e416c655c02cfafb7c
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%

---

# 조각 시작 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="나만의 조각 정의"
>abstract="독립형 조각을 만들고 관리하여 여러 여정 및 캠페인에서 콘텐츠를 재사용할 수 있도록 합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="조각 만들기"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="조각 업데이트 캠페인"
>abstract="조각 업데이트 캠페인"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="조각 업데이트 여정"
>abstract="조각 업데이트 여정"

조각은 의 하나 이상의 이메일에서 참조할 수 있는 재사용 가능한 구성 요소입니다 [!DNL Journey Optimizer] 캠페인 및 여정. 이 기능을 사용하면 마케팅 사용자가 향상된 디자인 프로세스에서 이메일 콘텐츠를 빠르게 조합하는 데 사용할 수 있는 여러 사용자 지정 콘텐츠 블록을 미리 빌드할 수 있습니다.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다](#video-fragments)

조각을 최대한 활용하려면 다음을 수행하십시오.

* **나만의 조각 만들기**: 처음부터 또는 콘텐츠를 조각으로 저장하여 시각적 또는 표현식 조각을 만듭니다. [조각을 만드는 방법 알아보기](#create-fragments). 또한 Journey Optimizer을 활용할 수 있습니다 **콘텐츠 REST API** 콘텐츠 조각을 관리합니다. 자세한 내용은 [Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **조각 재사용:** 콘텐츠에서 필요한 횟수만큼 사용하십시오. 다음을 참조하십시오 [시각적 조각 추가](../email/use-visual-fragments.md) 및 [표현식 조각 활용](../personalization/use-expression-fragments.md)

## 시작하기 전 {#fragment-prerequisites}

>[!NOTE]
>
>조각을 만들고, 편집하고, 보관하려면 **[!DNL Manage library items]** 에 포함된 권한 **[!DNL Content Library Manager]** 제품 프로필. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

이 버전에서는 다음 제한 사항이 적용됩니다.

* **시각적 조각** 은 이메일 채널에만 사용할 수 있습니다.
* **표현식 조각** 인앱 채널에는 사용할 수 없습니다.

## 시각적 및 표현식 조각 {#visual-expression}

두 가지 유형의 조각을 사용할 수 있습니다.

* **시각적 조각** 은 을 사용하여 여러 이메일 게재에서 재사용할 수 있는 사전 정의된 시각적 블록입니다. [이메일 디자이너](../email/get-started-email-design.md), 또는 [콘텐츠 템플릿](../email/use-email-templates.md).
* **표현식 조각** 는 의 전용 항목에서 사용할 수 있는 사전 정의된 표현식입니다. [개인화 편집기](../personalization/personalization-build-expressions.md).


모든 조각은 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]**  왼쪽 메뉴.

![](assets/fragment-list.png)

## 방법 비디오 {#video-fragments}

에서 시각적 조각을 관리, 작성 및 사용하는 방법에 대해 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

에서 표현식 조각을 관리, 작성 및 사용하는 방법에 대해 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
