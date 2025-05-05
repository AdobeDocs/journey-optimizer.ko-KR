---
title: 배치 만들기
description: 오퍼에 대한 배치를 만드는 방법을 알아봅니다
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 88e7140183700da0283fa00d89f6fff2c71c138f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 31%

---

# 배치 만들기 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="배치"
>abstract="배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다. 올바른 오퍼 콘텐츠가 메시지 내의 적합한 위치에 표시되도록 할 수 있습니다. 배치는 “구성 요소” 메뉴에서 생성됩니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_request"
>title="요청 설정"
>abstract="**[!UICONTROL 배치 간 중복 허용]** 옵션을 활성화하여 시스템이 여러 배치에 대해 동일한 오퍼를 고려하도록 합니다. **[!UICONTROL 오퍼 요청]** 필드를 사용하여 반환되는 오퍼의 수를 조정합니다. 예를 들어 2를 선택하면 선택한 결정 범위에 대해 최상의 오퍼 2개가 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_response"
>title="응답 형식"
>abstract="**[!UICONTROL 콘텐츠 포함]** 및 **[!UICONTROL 메타데이터 포함]** 옵션을 사용하면 오퍼의 콘텐츠와 메타데이터를 API 응답에 반환해야 하는지 여부를 지정할 수 있습니다. 모든 메타데이터 또는 특정 필드만 포함할 수 있습니다. 기본적으로 메타데이터 포함 값은 true로 설정됩니다."

배치는 올바른 오퍼 콘텐츠가 메시지 내의 올바른 위치에 표시되도록 하는 데 도움이 됩니다. 오퍼에 컨텐츠를 추가할 때 해당 컨텐츠가 표시될 수 있는 배치를 선택하라는 메시지가 표시됩니다.

➡️[이 비디오에서 배치를 만드는 방법을 알아봅니다](#video)

아래 예에는 세 개의 배치가 있으며, 서로 다른 유형의 콘텐츠(이미지, 텍스트, HTML)에 해당합니다.

![](../assets/offers_placement_schema.png)

배치 목록은 **[!UICONTROL 구성 요소]** 메뉴에서 액세스할 수 있습니다. 필터를 사용하여 특정 채널 또는 콘텐츠에 따라 배치를 검색할 수 있습니다.

![](../assets/placements_filter.png)

배치를 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 배치 만들기]**&#x200B;를 클릭합니다.

   ![](../assets/offers_placement_creation.png)

1. 배치의 특성을 정의합니다.

   * **[!UICONTROL 이름]**: 배치 이름입니다. 의미 있는 이름을 정의하여 보다 쉽게 검색할 수 있도록 해야 합니다.
   * **[!UICONTROL 채널 형식]**: 배치를 사용할 채널입니다.
   * **[!UICONTROL 콘텐츠 형식]**: 배치에서 표시할 수 있는 콘텐츠 형식(텍스트, HTML, 이미지 링크 또는 JSON)입니다.
   * **[!UICONTROL 설명]**: 배치에 대한 설명입니다(선택 사항).

   ![](../assets/offers_placement_creation_properties.png)

1. **[!UICONTROL 요청 설정]** 및 **[!UICONTROL 응답 형식]** 섹션에서 추가 매개 변수를 제공합니다.

   * **[!UICONTROL 배치 간 중복 허용]**: 다른 배치에서 동일한 오퍼를 여러 번 제안할 수 있는지 여부를 제어합니다. 활성화되면 시스템은 여러 배치에 대해 동일한 오퍼를 고려합니다. 기본적으로 매개 변수는 false로 설정됩니다.

     Decisioning 요청의 모든 배치에 대해 이 옵션이 false로 설정되면 요청의 모든 배치가 &quot;false&quot; 설정을 상속합니다.

   * **[!UICONTROL 오퍼 요청]**: 기본적으로 각 프로필에 대해 결정 범위의 오퍼 하나가 반환됩니다. 이 옵션을 사용하여 반환된 오퍼의 수를 조정할 수 있습니다. 예를 들어 2를 선택하면 선택한 결정 범위에 대해 최상의 오퍼 2개가 표시됩니다.

   * **[!UICONTROL 콘텐츠 포함]** / **[!UICONTROL 메타데이터 포함]**: 오퍼의 콘텐츠 및 메타데이터를 API 응답에서 반환할지 여부를 지정합니다. 모든 메타데이터 또는 특정 필드만 포함할 수 있습니다. 기본적으로 메타데이터 포함 값은 true로 설정됩니다.

   이러한 매개 변수는 [Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html?lang=ko)을(를) 사용하여 작업하는 경우 API 요청에 직접 설정할 수도 있습니다. 그러나 사용자 인터페이스에서 이를 구성하면 각 API 요청에서 전달할 필요가 없으므로 시간을 절약할 수 있습니다. 사용자 인터페이스와 API 요청 모두에서 매개 변수를 구성하는 경우 API 요청의 값이 인터페이스의 값보다 우선합니다.

   >[!NOTE]
   >
   >[Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?lang=ko&)로 작업하는 경우 이러한 매개 변수를 요청에 설정할 수 없습니다. 이 화면에서 정의해야 합니다.
   >
   >[Batch Decisioning API](../api-reference/offer-delivery-api/batch-decisioning-api.md)로 작업하는 경우 이 화면 또는 API 요청에서 이러한 매개 변수를 설정할 수 있습니다. 화면과 APi 요청 사이에 매개 변수 값이 일치하지 않으면 요청 값이 사용됩니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭하여 확인합니다.

1. 배치가 생성되면 배치 목록에 표시됩니다. 속성을 표시하고 편집할 수 있습니다.

   ![](../assets/placement_created.png)

## 방법 비디오{#video}

의사 결정 관리에서 배치를 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

