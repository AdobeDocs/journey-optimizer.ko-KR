---
title: 오퍼에 표현 추가
description: 오퍼에 표현을 추가하는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 오퍼에 표현 추가 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="표현"
>abstract="표현을 추가하여 오퍼가 메시지에 표시되는 위치를 정의합니다. 오퍼가 더 많은 표현을 보유하게 되면 더 많은 기회가 다른 배치 컨텍스트에서 오퍼를 사용할 수 있습니다."

오퍼는 메시지의 다른 위치에 표시할 수 있습니다. 위쪽 배너에 이미지, 단락 텍스트, HTML 블록 등으로 표시 오퍼가 더 많은 표현을 보유하게 되면 더 많은 기회가 다른 배치 컨텍스트에서 오퍼를 사용할 수 있습니다.

## 오퍼의 표현 구성 {#representations}

오퍼에 하나 이상의 표현을 추가하고 구성하려면 아래 단계를 수행하십시오.

1. 첫 번째 표현에 대해 다음을 선택하여 시작합니다 **[!UICONTROL 채널]** 사용됩니다.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >선택한 채널에 대해 사용 가능한 배치만 **[!UICONTROL 배치]** 드롭다운 목록.

1. 목록에서 배치를 선택합니다.

   또한 **[!UICONTROL 배치]** 모든 배치를 탐색하는 드롭다운 목록입니다.

   ![](../assets/browse-button-placements.png)

   거기에서 여전히 채널 및/또는 컨텐츠 유형에 따라 배치를 필터링할 수 있습니다. 배치를 선택하고 를 클릭합니다 **[!UICONTROL 선택]**.

   ![](../assets/browse-placements.png)

1. 표시에 컨텐츠를 추가합니다. 방법 알아보기 [이 섹션](#content).

1. 이미지나 URL과 같은 컨텐츠를 추가할 때 **[!UICONTROL 대상 링크]**: 오퍼를 클릭하는 사용자가 해당 페이지로 이동됩니다.

   ![](../assets/offer-destination-link.png)

1. 마지막으로, 사용자에게 표시할 언어를 식별하고 관리하는 데 도움이 되도록 원하는 언어를 선택합니다.

1. 다른 표현을 추가하려면 **[!UICONTROL 표현 추가]** 버튼을 클릭하고 필요한 만큼 표현을 추가합니다.

   ![](../assets/offer-add-representation.png)

1. 모든 표현을 추가한 후 **[!UICONTROL 다음]**.

## 표현 내용 정의 {#content}

표현에는 다른 유형의 컨텐츠를 추가할 수 있습니다.

>[!NOTE]
>
>배치의 컨텐츠 유형에 해당하는 컨텐츠만 사용할 수 있습니다.

### 이미지 추가 {#images}

선택한 배치가 이미지 유형인 경우 **Adobe Experience Cloud 자산** 라이브러리, 에서 제공하는 자산의 중앙 저장소 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 을 사용하여 작업하려면 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. 을(를) 선택합니다 **[!UICONTROL 자산 라이브러리]** 선택 사항입니다.

1. 선택 **[!UICONTROL 찾아보기]**.

   ![](../assets/offer-browse-asset-library.png)

1. 자산을 탐색하여 선택한 이미지를 선택합니다

1. **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   ![](../assets/offer-select-asset.png)

### HTML 또는 JSON 파일 추가 {#html-json}

선택한 배치가 HTML 유형인 경우, [Adobe Experience Cloud 자산 라이브러리](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

예를 들어에서 HTML 이메일 템플릿을 만들었습니다 [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 오퍼 컨텐츠에 해당 파일을 사용하려는 경우 새 파일을 만드는 대신 템플릿을 **자산 라이브러리** 을 재사용할 수 있도록 하는 것입니다.

표현에서 컨텐츠를 재사용하려면 **자산 라이브러리** 에 설명된 대로 [이 섹션](#images) 원하는 HTML 또는 JSON 파일을 선택합니다.

![](../assets/offer-browse-asset-library-json.png)

### URL 추가 {#urls}

외부 공용 위치에서 콘텐츠를 추가하려면 **[!UICONTROL URL]**&#x200B;을 입력한 다음 추가할 컨텐츠의 URL 주소를 입력합니다.

표현식 편집기를 사용하여 URL을 개인화할 수 있습니다. 추가 정보 [개인화](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

예를 들어 오퍼로 표시되는 이미지를 개인화하려고 합니다. 뉴욕시의 스카이라인을 선호하는 사용자와 비치 휴가를 선호하는 사용자들이 하와이 노쇼어를 보기 바란다.

표현식 편집기를 사용하여 결합 스키마를 사용하여 Adobe Experience Platform에 저장된 프로필 속성을 검색합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

를 지정하는 경우 **[!UICONTROL 대상 링크]**&#x200B;를 설정하는 경우 오퍼를 클릭하는 사용자가 이동하게 되는 URL을 개인화할 수도 있습니다.

### 사용자 지정 텍스트 추가 {#custom-text}

호환 배치를 선택할 때 텍스트 유형 컨텐츠를 삽입할 수도 있습니다.

1. 을(를) 선택합니다 **[!UICONTROL 사용자 지정]** 옵션을 선택하고 **[!UICONTROL 컨텐츠 추가]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >이 옵션은 이미지 유형 배치에 사용할 수 없습니다.

1. 오퍼에 표시할 텍스트를 입력합니다.

   ![](../assets/offer-text-content.png)

   표현식 편집기를 사용하여 콘텐츠를 개인화할 수 있습니다. 추가 정보 [개인화](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >전용 **[!UICONTROL 프로필 속성]**, **[!UICONTROL 세그먼트 멤버십]** 및 **[!UICONTROL 도우미 함수]** 결정 관리에 소스를 사용할 수 있습니다.

