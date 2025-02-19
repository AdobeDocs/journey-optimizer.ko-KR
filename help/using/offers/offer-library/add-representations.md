---
title: 오퍼에 표현 추가
description: 오퍼에 표시를 추가하는 방법을 알아봅니다
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 7%

---

# 오퍼에 표현 추가 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="표시"
>abstract="표현을 추가하여 메시지에 오퍼가 표시될 위치를 정의합니다. 오퍼에 표현이 많을수록 오퍼를 다양한 배치 컨텍스트에서 사용할 기회가 많아집니다."

오퍼는 메시지의 다른 위치에 표시될 수 있습니다. 이미지가 있는 상단 배너에서 단락 내 텍스트, HTML 블록 등으로 표시됩니다. 오퍼에 표현이 많을수록 오퍼를 다양한 배치 컨텍스트에서 사용할 기회가 많아집니다.

## 오퍼의 표시 구성 {#representations}

오퍼에 하나 이상의 표현을 추가하고 구성하려면 아래 단계를 따르십시오.

1. 첫 번째 표현의 경우 사용할 **[!UICONTROL 채널]**&#x200B;을(를) 선택하여 시작합니다.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >선택한 채널에 대해 사용 가능한 배치만 **[!UICONTROL 배치]** 드롭다운 목록에 표시됩니다.

1. 목록에서 배치를 선택합니다.

   **[!UICONTROL 배치]** 드롭다운 목록 옆에 있는 버튼을 사용하여 모든 배치를 찾아볼 수도 있습니다.

   ![](../assets/browse-button-placements.png)

   여기에서 채널 및/또는 콘텐츠 유형에 따라 배치를 필터링할 수 있습니다. 배치를 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   ![](../assets/browse-placements.png)

1. 표현에 콘텐츠를 추가합니다. [이 섹션](#content)에서 방법을 알아보세요.

1. 이미지 또는 URL과 같은 콘텐츠를 추가할 때 **[!UICONTROL 대상 링크]**&#x200B;를 지정할 수 있습니다. 오퍼를 클릭하는 사용자는 해당 페이지로 이동됩니다.

   ![](../assets/offer-destination-link.png)

1. 마지막으로, 원하는 언어를 선택하여 사용자에게 표시할 항목을 식별하고 관리합니다.

1. 다른 표현을 추가하려면 **[!UICONTROL 표현 추가]** 단추를 사용하고 필요한 만큼 표현을 추가하십시오.

   ![](../assets/offer-add-representation.png)

1. 표시를 모두 추가한 후에는 **[!UICONTROL 다음]**&#x200B;을(를) 선택하십시오.

## 표현에 사용할 콘텐츠 정의 {#content}

표현에 다양한 유형의 콘텐츠를 추가할 수 있습니다.

>[!NOTE]
>
>배치의 콘텐츠 유형에 해당하는 콘텐츠만 사용할 수 있습니다.

### 이미지 추가 {#images}

선택한 배치가 이미지 유형인 경우 [!DNL Adobe Experience Manager Assets]에서 제공하는 자산의 중앙 집중식 저장소인 **Adobe Experience Cloud 자산** 라이브러리에서 얻은 콘텐츠를 추가할 수 있습니다.

>[!NOTE]
>
> [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}을(를) 사용하여 작업하려면 조직에 대해 [!DNL Assets Essentials]을(를) 배포하고 사용자가 **Assets Essentials 소비자 사용자** 또는/및 **Assets Essentials 사용자** 제품 프로필에 속하는지 확인해야 합니다. [이 페이지](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}에 대해 자세히 알아보세요.

1. **[!UICONTROL 자산 라이브러리]** 옵션을 선택하십시오.

1. **[!UICONTROL 찾아보기]**&#x200B;를 선택하십시오.

   ![](../assets/offer-browse-asset-library.png)

1. 에셋을 탐색하여 선택한 이미지 선택

1. **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   ![](../assets/offer-select-asset.png)

### HTML 또는 JSON 파일 추가 {#html-json}

선택한 배치가 HTML 유형인 경우 [Adobe Experience Cloud 자산 라이브러리](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}에서 제공되는 HTML 또는 JSON 컨텐츠를 추가할 수도 있습니다.

예를 들어, [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"}에서 HTML 이메일 템플릿을 만들었고, 이 파일을 오퍼 콘텐츠에 사용하려고 합니다. 새 파일을 만드는 대신 템플릿을 **자산 라이브러리**&#x200B;에 업로드하여 오퍼의 표시에서 다시 사용할 수 있습니다.

표현에서 콘텐츠를 다시 사용하려면 [이 섹션](#images)에 설명된 대로 **자산 라이브러리**&#x200B;를 찾은 다음 선택한 HTML 또는 JSON 파일을 선택하십시오.

![](../assets/offer-browse-asset-library-json.png)

### URL 추가 {#urls}

외부 공개 위치에서 콘텐츠를 추가하려면 **[!UICONTROL URL]**&#x200B;을(를) 선택한 다음 추가할 콘텐츠의 URL 주소를 입력하십시오.

개인화 편집기를 사용하여 URL을 개인화할 수 있습니다. [개인화](../../personalization/personalize.md#use-expression-editor)에 대해 자세히 알아보세요.

![](../assets/offer-content-url.png)

예를 들어 오퍼로 표시되는 이미지를 개인화하려고 합니다. 뉴욕시의 스카이라인을 보기 위해 도시 휴가를 선호하는 이용자들과 하와이 북해안을 보기 위해 해변 휴가를 선호하는 이용자들을 원한다는 것이다.

개인화 편집기를 사용하여 유니온 스키마를 사용하여 Adobe Experience Platform에 저장된 프로필 속성을 검색합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

**[!UICONTROL 대상 링크]**&#x200B;를 지정하는 경우 오퍼를 클릭하는 사용자에게 표시할 URL을 개인화할 수도 있습니다.

### 사용자 정의 텍스트 추가 {#custom-text}

호환되는 배치를 선택할 때 텍스트 유형 컨텐트를 삽입할 수도 있습니다.

1. **[!UICONTROL 사용자 지정]** 옵션을 선택하고 **[!UICONTROL 콘텐츠 추가]**&#x200B;를 클릭합니다.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >이미지 유형 배치에는 이 옵션을 사용할 수 없습니다.

1. 오퍼에 표시할 텍스트를 입력합니다.

   ![](../assets/offer-text-content.png)

   개인화 편집기를 사용하여 콘텐츠를 개인화할 수 있습니다. [개인화](../../personalization/personalize.md#use-expression-editor)에 대해 자세히 알아보세요.

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >**[!UICONTROL 프로필 특성]**, **[!UICONTROL 대상]** 및 **[!UICONTROL 도우미 함수]** 원본만 의사 결정 관리에 사용할 수 있습니다.

## 컨텍스트 데이터를 기반으로 표현 개인화{#context-data}

컨텍스트 데이터가 [Edge decisioning](../api-reference/offer-delivery-api/edge-decisioning-api.md) 호출에서 전달되면 이러한 데이터를 활용하여 표현을 동적으로 개인화할 수 있습니다. 예를 들어 결정이 내려지는 시점의 현재 날씨 상태와 같은 실시간 요인을 기반으로 오퍼 표시를 조정할 수 있습니다.

오퍼 표현에 컨텍스트 데이터를 사용하려면 `profile.timeSeriesEvents.` 네임스페이스를 사용하여 컨텍스트 데이터 변수를 표현 컨텐츠 내에 직접 통합하십시오.

다음은 사용자의 운영 체제를 기반으로 오퍼의 표시를 개인화하는 데 사용되는 구문 예입니다.

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

컨텍스트 데이터를 포함하는 해당 Edge 의사 결정 요청은 다음과 같습니다.

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
