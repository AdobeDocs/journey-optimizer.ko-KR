---
solution: Journey Optimizer
product: journey optimizer
title: AEM 컨텐츠 조각
description: AEM 콘텐츠 조각 액세스 및 관리 방법 알아보기
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 92690f1b3f73c75d9b81746b49836a24ebf7c457
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 4%

---

# Adobe Experience Manager 콘텐츠 조각 {#aem-fragments}

이제 Adobe Experience Manager as a Cloud Service를 Adobe Journey Optimizer와 통합하여 AEM 콘텐츠 조각을 Journey Optimizer 콘텐츠에 원활하게 통합할 수 있습니다. 이렇게 간소화된 연결을 통해 AEM 콘텐츠에 액세스하고 활용하는 프로세스가 간단해져 개인화되고 동적인 캠페인 및 여정을 만들 수 있게 됩니다.

AEM 콘텐츠 조각에 대한 자세한 내용은 Experience Manager 설명서에서 [콘텐츠 조각을 사용하여 작업](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}을 참조하세요.

## 시작하기 전 {#start}

>[!AVAILABILITY]
>
>의료 고객의 경우 Journey Optimizer Healthcare Shield 및 Adobe Experience Manager Enhanced Security 추가 기능 서비스의 라이선스가 있을 때만 통합이 활성화됩니다.

### 제한 사항 {#limitations}

Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 사용하여 작업할 때 다음 제한 사항을 참고하십시오.

* **콘텐츠 조각 유형**: 간단한 콘텐츠 조각 및 중첩된 콘텐츠 조각이 지원됩니다. 콘텐츠 조각 변형은 현재 지원되지 않습니다.

* **다국어 콘텐츠**: 수동 흐름만 지원됩니다. 각 언어 변형은 Adobe Experience Manager에서 독립적으로 작성, 태그 지정, 게시 및 Journey Optimizer에서 수동으로 선택해야 합니다. 자동 언어 확인 또는 대체 메커니즘이 없습니다.

* **저장소 액세스**: Journey Optimizer은 인증되지 않은 공개 끝점을 통해 콘텐츠 조각을 사용할 수 있는 Adobe Experience Manager 게시 계층과 배타적으로 통합됩니다. 작성자 저장소는 저장소 선택기에 표시될 수 있지만, 게시 계층에 게시된 콘텐츠 조각만 Journey Optimizer에서 사용할 수 있습니다.

* **콘텐츠 조각 상태**: Journey Optimizer은 **게시됨** 및 **수정됨** 상태의 콘텐츠 조각을 표시합니다. 모든 경우에 게시된 최신 버전만 사용됩니다. 게시 후 조각이 수정되면 해당 변경 사항은 콘텐츠 조각이 Journey Optimizer에서 다시 게시될 때까지 Adobe Experience Manager에 반영되지 않습니다. Adobe Experience Manager과 Journey Optimizer 간에는 자동 버전 조정이 없습니다.

* **Personalization**: 프로필 특성, 컨텍스트 특성, 정적 문자열 및 사전 선언된 변수만 지원됩니다. 파생 또는 계산된 속성은 지원되지 않습니다.

* **업데이트 및 버전 관리**: 콘텐츠 조각 업데이트는 Adobe Experience Manager에서 수동으로 다시 게시해야 합니다. Adobe Experience Manager과 Journey Optimizer 간에는 자동 버전 조정이 없습니다. 컨텐츠 조각이 Adobe Experience Manager에 게시되면 Journey Optimizer은 이벤트를 수신하고 Journey Optimizer 측에서 업데이트합니다. 성공하면 단일 여정의 경우 5분 후, 배치 사용 사례의 경우 다음 배치에서 업데이트를 사용할 수 있습니다.

* **캐싱 및 증명**: 콘텐츠 조각은 Adobe Experience Manager 게시 계층에서 실시간으로 검색됩니다. 사전 렌더링 또는 스냅샷 캐싱이 없습니다. 캠페인 및 여정에 대한 증명은 항상 가장 최근에 게시된 콘텐츠 조각 버전을 반영하며 기록 버전은 증명을 위해 잠글 수 없습니다.

* **사용자 액세스**: 실수로 인한 오류 위험을 줄이기 위해 콘텐츠 조각을 게시할 수 있는 액세스 권한을 가진 사용자 수를 제한하는 것이 좋습니다.

### 콘텐츠 동기화 흐름 {#content-sync-flow}

Adobe Experience Manager과 Journey Optimizer 간의 통합은 다음 데이터 흐름을 따릅니다.

1. **[만들기 및 작성자](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: 콘텐츠가 Adobe Experience Manager에서 콘텐츠 조각으로 만들어지고 구성됩니다.

1. **[태그 지정](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: 콘텐츠 조각은 Journey Optimizer 관련 태그(`ajo-enabled:{OrgId}/{SandboxName}`)로 태그 지정되어야 합니다.

1. **[게시](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: 콘텐츠 조각이 Adobe Experience Manager에 게시되어 Journey Optimizer에서 사용할 수 있습니다.

1. **[액세스](#aem-add)**: Journey Optimizer은 Adobe Experience Manager 게시 인스턴스에서 사용 가능한 콘텐츠 조각을 실시간으로 가져와서 표시합니다.

1. **[통합](#aem-add)**: 콘텐츠 조각을 선택하여 캠페인 또는 여정에 통합합니다.

컨텐츠 조각이 Adobe Experience Manager에 게시되면 Journey Optimizer 측의 컨텐츠를 업데이트하는 이벤트가 전송됩니다. 업데이트에 성공하면 단일 여정의 경우 약 5분 내에 콘텐츠 조각을 사용할 수 있고 일괄 처리 사례의 경우 다음 처리 배치에서 사용할 수 있습니다. Journey Optimizer에서 업데이트를 사용할 수 있게 되면 해당되는 모든 캠페인 및 여정에 걸쳐 게시된 최신 콘텐츠가 사용됩니다.

### 콘텐츠 조각 라이프사이클

![](assets/do-not-localize/AEM_CF.png)

콘텐츠 조각은 존재하는 Adobe Experience Manager 계층에 따라 다른 라이프사이클 단계를 따릅니다. [Adobe Experience Manager 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

콘텐츠는 **작성자 계층**&#x200B;에서 만들어지고 관리되며, 조각에는 새로 만들기, 초안, 게시됨, 수정됨 또는 게시 취소됨 등의 상태가 있을 수 있습니다. 이러한 상태는 **작성자 계층**&#x200B;에만 적용되며 콘텐츠 만들기 및 검토를 지원합니다.

콘텐츠 조각이 게시되면 복사본이 **게시 계층**&#x200B;에 만들어지고 인증되지 않은 공개 끝점을 통해 노출됩니다. Journey Optimizer은 이 **게시 계층**&#x200B;과(와) 독점적으로 통합됩니다.

따라서 Journey Optimizer은 게시된 콘텐츠 조각 또는 수정된 콘텐츠 조각만 표시하고 항상 게시된 최신 버전을 사용합니다. 게시 후 수행된 모든 변경 사항은 컨텐츠 조각이 다시 게시될 때까지 Journey Optimizer에 반영되지 않습니다.

## Experience Manager에서 태그 만들기 및 할당

Journey Optimizer에서 컨텐츠 조각을 사용하기 전에 Journey Optimizer에 특별히 태그를 만들어야 합니다.

1. **Experience Manager** 환경에 액세스합니다.

1. **도구** 메뉴에서 **태그 지정**&#x200B;을 선택합니다.

   ![](assets/do-not-localize/aem_tag_1.png)

1. **태그 만들기**&#x200B;를 클릭합니다.

1. ID가 `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}` 구문을 준수하는지 확인하십시오.

1. **만들기**&#x200B;를 클릭합니다.

1. [Experience Manager 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"}에 자세히 설명된 대로 콘텐츠 조각 모델을 정의하고 새로 만든 Journey Optimizer 태그를 할당하십시오.

이러한 실시간 연결은 콘텐츠가 항상 최신 상태임을 보장하지만 게시된 조각에 대한 모든 변경 사항이 활성 캠페인 및 여정에 즉시 영향을 준다는 것을 의미합니다.

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
테스트를 수행하고 콘텐츠의 유효성을 검사하면 대상자에게 [캠페인을 전송](../campaigns/review-activate-campaign.md)하거나 [여정을 게시](../building-journeys/publish-journey.md)할 수 있습니다.

Adobe Experience Manager을 사용하면 컨텐츠 조각이 사용되는 Journey Optimizer 캠페인 또는 여정을 식별할 수 있습니다. 자세한 내용은 [Adobe Experience Manager 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references)를 참조하세요.

## 문제 해결 {#troubleshooting}

Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 사용하여 작업할 때 문제가 발생하는 경우 다음의 일반적인 문제 및 해결 방법을 참조하십시오.

| 문제 | 원인 | 해결 방법 |
|-|-|-|
| **태그를 찾을 수 없음** 또는 **콘텐츠 조각이 선택기에 표시되지 않음** | Adobe Experience Manager 태그 구문이 필수 형식 `ajo-enabled:{OrgId}/{SandboxName}`과(와) 일치하지 않습니다. | 태그 ID가 올바른 **조직 ID** 및 **샌드박스 이름**&#x200B;을 사용하는지 확인하십시오. 공백이나 잘못된 구분 기호가 없는지 확인합니다. 태그를 수정한 후 콘텐츠 조각을 다시 게시합니다. |
| **콘텐츠 조각이 목록에 표시되지 않음** | 콘텐츠 조각이 초안 상태이거나 승인되지 않음 | 승인되고 게시된 콘텐츠 조각만 Journey Optimizer 선택기에 표시됩니다. Adobe Experience Manager에서 콘텐츠 조각을 게시하고 이 조각이 승인됨 상태인지 확인합니다. |
| **정의되지 않은 변수 오류** | Personalization 자리 표시자가 조각 도우미 태그에 선언되지 않음 | 조각 도우미 태그에 모든 필수 매개 변수를 추가합니다. 콘텐츠 조각에 사용된 각 자리 표시자는 해당 매핑으로 명시적으로 선언해야 합니다. |
| **증명이 예기치 않은 콘텐츠를 표시함** | 증명은 Adobe Experience Manager의 최신 게시 버전을 사용합니다. | 증명은 항상 Adobe Experience Manager에서 콘텐츠 조각의 가장 최근 게시를 반영합니다. Adobe Experience Manager에서 최근 변경 작업을 수행한 경우 조각을 다시 게시하고 증명을 새로 고칩니다. |
| **CPES(액세스 거부) 오류** | 사용자 역할이 특정 속성에 액세스할 수 있는 권한이 없음 | 시스템 관리자에게 문의하여 개인화에 사용된 프로필 또는 컨텍스트 속성에 대해 역할에 적절한 권한이 있는지 확인하십시오. |
| **조각이 비어 있거나 누락된 콘텐츠를 표시합니다** | 필수 개인화 매개 변수 또는 대체 값 누락 | 모든 필수 매개 변수가 제공되었는지 확인하고 선택적 속성에 대한 대체 값을 추가하는 것이 좋습니다. |

문제가 지속되면 컨텐츠 조각 ID, 캠페인 또는 여정 ID에 대한 세부 정보와 표시되는 오류 메시지를 Adobe 담당자에게 문의하십시오.
