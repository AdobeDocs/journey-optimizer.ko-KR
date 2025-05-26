---
solution: Journey Optimizer
product: journey optimizer
title: AEM 컨텐츠 조각
description: AEM 콘텐츠 조각 액세스 및 관리 방법 알아보기
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 8538018f5c30b0c3c9c1df5726276c2e87e64149
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---

# Adobe Experience Manager Content 조각 {#aem-fragments}

이제 Adobe Experience Manager as a Cloud Service을 Adobe Journey Optimizer과 통합하여 AEM 콘텐츠 조각을 Journey Optimizer 콘텐츠에 원활하게 통합할 수 있습니다. 이렇게 간소화된 연결을 통해 AEM 콘텐츠에 액세스하고 활용하는 프로세스를 간소화하여 개인화되고 동적인 캠페인 및 여정을 만들 수 있습니다.

AEM 콘텐츠 조각에 대한 자세한 내용은 Experience Manager 설명서에서 [콘텐츠 조각을 사용하여 작업](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/overview){target="_blank"}을 참조하세요.

>[!AVAILABILITY]
>
>의료 고객의 경우 Journey Optimizer Healthcare Shield 및 Adobe Experience Manager Enhanced Security 추가 기능 서비스의 라이선스가 있을 때만 통합이 활성화됩니다.

## 제한 사항 {#limitations}

* 우발적 오류의 위험을 줄이기 위해 콘텐츠 조각을 게시할 수 있는 액세스 권한이 있는 사용자 수를 제한하는 것이 좋습니다.

* 다국어 콘텐츠의 경우 수동 흐름만 지원됩니다.

* 변형은 현재 지원되지 않습니다.

## Experience Manager에서 태그 만들기 및 할당

Journey Optimizer에서 컨텐츠 조각을 사용하기 전에 Journey Optimizer에 특별히 태그를 만들어야 합니다.

1. **Experience Manager** 환경에 액세스합니다.

1. **도구** 메뉴에서 **태그 지정**&#x200B;을 선택합니다.

   ![](assets/do-not-localize/aem_tag_1.png)

1. **태그 만들기**&#x200B;를 클릭합니다.

1. ID가 `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}` 구문을 준수하는지 확인하십시오.

1. **만들기**&#x200B;를 클릭합니다.

1. [Experience Manager 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"}에 자세히 설명된 대로 콘텐츠 조각 모델을 정의하고 새로 만든 Journey Optimizer 태그를 할당하십시오.

이제 Journey Optimizer에서 나중에 사용할 수 있도록 콘텐츠 조각을 만들고 구성할 수 있습니다. 자세한 내용은 [Experience Manager 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}를 참조하세요.

## Experience Manager 컨텐츠 조각 추가 {#aem-add}

이제 AEM 콘텐츠 조각을 만들고 개인화한 후 여정 최적화 도구 캠페인이나 여정으로 가져올 수 있습니다.

1. [캠페인](../campaigns/create-campaign.md) 또는 [여정](../building-journeys/journey-gs.md)을 만듭니다.

1. AEM 컨텐츠 조각에 액세스하려면 텍스트 필드 내에서 ![Personalization 아이콘](assets/do-not-localize/Smock_PersonalizationField_18_N.svg)을 클릭하거나 HTML 컨텐츠 구성 요소를 통해 소스 코드를 엽니다.

   ![](assets/aem_campaign_2.png)

1. 왼쪽 창의 **[!UICONTROL AEM 콘텐츠 조각]** 메뉴에서 **[!UICONTROL AEM CF 선택기 열기]**&#x200B;를 클릭합니다.

   ![](assets/aem_campaign_3.png)

1. 사용 가능한 목록에서 **[!UICONTROL 콘텐츠 조각]**&#x200B;을(를) 선택하여 Journey Optimizer 콘텐츠로 가져옵니다.

1. 콘텐츠 조각 목록을 미세 조정하려면 **[!UICONTROL 필터 표시]**&#x200B;를 클릭하십시오.

   기본적으로 콘텐츠 조각 필터는 승인된 콘텐츠만 표시하도록 사전 설정되어 있습니다.

   ![](assets/aem_campaign_4.png)

1. **[!UICONTROL 콘텐츠 조각]**&#x200B;을 선택한 후 **[!UICONTROL 선택]**&#x200B;을 클릭하여 엽니다.

   ![](assets/aem_campaign_5.png)

1. 조각 정보를 표시하려면 **[!UICONTROL 조각 보기]**&#x200B;를 클릭하세요. **[!UICONTROL 조각 정보]** 메뉴를 열면 편집기가 읽기 전용 모드로 전환됩니다.

   Adobe Experience Manager에서 조각을 보려면 오른쪽 메뉴에서 **[!UICONTROL 미리 보기]**&#x200B;를 선택하십시오.

   ![](assets/aem_campaign_7.png)

1. 조각의 고급 메뉴에 액세스하려면 ![추가 작업 아이콘](assets/do-not-localize/Smock_MoreSmallList_18_N.svg)을 클릭하세요.

   * **[!UICONTROL 조각 교체]**
   * **[!UICONTROL 참조 살펴보기]**
   * **[!UICONTROL AEM에서 열기]**

   ![](assets/aem_campaign_8.png)

1. **[!UICONTROL 조각]**&#x200B;에서 원하는 필드를 선택하여 콘텐츠에 추가하십시오.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. 실시간 개인화를 사용하려면 **[!UICONTROL 콘텐츠 조각]** 내에서 사용되는 모든 자리 표시자를 조각 도우미 태그의 매개 변수로 사용자가 명시적으로 선언해야 합니다. 다음 방법을 사용하여 이러한 자리 표시자를 프로필 속성, 컨텍스트 속성, 정적 문자열 또는 사전 정의된 변수에 매핑할 수 있습니다.

   1. **프로필 또는 컨텍스트 특성 매핑**: 자리 표시자를 프로필 또는 컨텍스트 특성(예: name = profile.person.name.firstName)에 할당합니다.

   1. **정적 문자열 매핑**: 큰 따옴표 안에 고정 문자열 값을 할당하십시오(예: name = &quot;John&quot;).

   1. **변수 매핑**: 같은 HTML 내에서 이전에 선언된 변수를 참조합니다(예: name = &#39;variableName&#39;).
이 경우 다음 구문을 사용하여 조각 ID를 추가하기 전에 **_variableName_**&#x200B;이(가) 선언되었는지 확인하십시오.

      ```html
      {% let variableName = attribute name %} 
      ```

   아래 예에서 **_name_** 자리 표시자는 조각 내의 **_profile.person.name.firstName_** 특성에 매핑됩니다.

   ![](assets/aem_campaign_9.png){zoomable="yes"}


1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 이제 [이 섹션](../content-management/preview.md)에 자세히 설명된 대로 메시지 콘텐츠를 테스트하고 확인할 수 있습니다.

테스트를 수행하고 콘텐츠의 유효성을 검사하면 대상자에게 [캠페인을 전송](../campaigns/review-activate-campaign.md)하거나 [여정을 게시](../building-journeys/publishing-the-journey.md)할 수 있습니다.

Adobe Experience Manager을 사용하면 컨텐츠 조각이 사용되는 Journey Optimizer 캠페인 또는 여정을 식별할 수 있습니다.
