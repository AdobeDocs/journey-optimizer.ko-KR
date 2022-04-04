---
title: 오퍼에 표현 추가
description: 오퍼에 표현을 추가하는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 0fa8ba1dc16062ea1553f9978752f3c018cec4c6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---

# 오퍼에 표현 추가 {#add-representations}

오퍼는 메시지의 다른 위치에 표시할 수 있습니다. 위쪽 배너에 이미지, 단락 텍스트, HTML 블록 등으로 표시 오퍼가 더 많은 표현을 보유하게 되면 더 많은 기회가 다른 배치 컨텍스트에서 오퍼를 사용할 수 있습니다.

## 오퍼의 표현 구성 {#representations}

오퍼에 하나 이상의 표현을 추가하고 구성하려면 아래 단계를 수행하십시오.

1. 첫 번째 표현에 대해 다음을 선택하여 시작합니다 **[!UICONTROL Channel]** 사용됩니다.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >선택한 채널에 대해 사용 가능한 배치만 **[!UICONTROL Placement]** 드롭다운 목록.

1. 목록에서 배치를 선택합니다.

   또한 **[!UICONTROL Placement]** 모든 배치를 탐색하는 드롭다운 목록입니다.

   ![](../assets/browse-button-placements.png)

   거기에서 여전히 채널 및/또는 컨텐츠 유형에 따라 배치를 필터링할 수 있습니다. 배치를 선택하고 를 클릭합니다 **[!UICONTROL Select]**.

   ![](../assets/browse-placements.png)

1. 표시에 컨텐츠를 추가합니다. 방법 알아보기 [이 섹션](#content).

1. 이미지나 URL과 같은 컨텐츠를 추가할 때 **[!UICONTROL Destination link]**: 오퍼를 클릭하는 사용자가 해당 페이지로 이동됩니다.

   ![](../assets/offer-destination-link.png)

1. 마지막으로, 사용자에게 표시할 언어를 식별하고 관리하는 데 도움이 되도록 원하는 언어를 선택합니다.

1. 다른 표현을 추가하려면 **[!UICONTROL Add representation]** 버튼을 클릭하고 필요한 만큼 표현을 추가합니다.

   ![](../assets/offer-add-representation.png)

1. 모든 표현을 추가한 후 **[!UICONTROL Next]**.

## 표현 내용 정의 {#content}

표현에는 다른 유형의 컨텐츠를 추가할 수 있습니다.

>[!NOTE]
>
>배치의 컨텐츠 유형에 해당하는 컨텐츠만 사용할 수 있습니다.

### 이미지 추가 {#images}

선택한 배치가 이미지 유형인 경우 **Adobe Experience Cloud 자산** 라이브러리, 에서 제공하는 자산의 중앙 저장소 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 을 사용하여 작업하려면 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, 배포해야 합니다. [!DNL Assets Essentials] 조직의 경우 사용자가 **Assets Essentials 소비자 사용자** 또는/and **Assets Essentials 사용자** 제품 프로필. 추가 정보 [이 페이지](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

1. **[!UICONTROL Asset library]** 옵션을 선택합니다.

1. **[!UICONTROL Browse]**&#x200B;를 선택합니다.

   ![](../assets/offer-browse-asset-library.png)

1. 자산을 탐색하여 선택한 이미지를 선택합니다

1. **[!UICONTROL Select]**&#x200B;을(를) 클릭합니다.

   ![](../assets/offer-select-asset.png)

### URL 추가 {#urls}

외부 공용 위치에서 콘텐츠를 추가하려면 **[!UICONTROL URL]**&#x200B;을 입력한 다음 추가할 컨텐츠의 URL 주소를 입력합니다.

![](../assets/offer-content-url.png)

### 사용자 지정 텍스트 추가 {#custom-text}

호환 배치를 선택할 때 텍스트 유형 컨텐츠를 삽입할 수도 있습니다.

1. 을(를) 선택합니다 **[!UICONTROL Custom]** 옵션을 선택하고 **[!UICONTROL Add content]**.

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
   >전용 **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** 및 **[!UICONTROL Helper functions]** 결정 관리에 소스를 사용할 수 있습니다.
