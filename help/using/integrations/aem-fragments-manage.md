---
solution: Journey Optimizer
product: journey optimizer
title: AEM 컨텐츠 조각
description: AEM 콘텐츠 조각 관리 방법 알아보기
topic: Content Management
role: User
level: Beginner
source-git-commit: ce34eb885d85c6c0f81b477e155cb81547d53e03
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Adobe Experience Manager 컨텐츠 조각 관리 {#aem-fragments}

>[!BEGINSHADEBOX]

**이 페이지에서:** 상태 및 메타데이터를 모니터링하기 위해 콘텐츠 관리 조각 목록에서 AEM 콘텐츠 조각을 관리합니다. 조각이 여정 및 캠페인에서 사용되는 위치를 확인하고, Experience Manager에서 게시된 업데이트를 동기화하며, Journey Optimizer에서 나가지 않고 편집할 조각을 엽니다.

>[!ENDSHADEBOX]

Adobe Experience Manager as a Cloud Service 또는 Managed Services을 Adobe Journey Optimizer과 통합하면 콘텐츠에서 AEM 콘텐츠 조각을 사용할 수 있으며 Journey Optimizer에서 나가지 않고 조각 상태를 확인할 수 있습니다.

여정 또는 캠페인에 이미 사용된 조각을 다시 게시하면 Adobe Experience Manager에서 조각이 **게시**&#x200B;된 후 동기화 타이머가 시작됩니다. 업데이트된 콘텐츠는 일반적으로 단일 여정 및 캠페인에 대해 약 **5분** 이내에 Journey Optimizer에서 사용할 수 있으며, 일괄 게재의 경우 변경 사항이 **다음 처리 일괄 처리**&#x200B;에 표시됩니다. [Adobe Experience Manager 콘텐츠 조각을 사용하여 작업](aem-fragments.md)을 참조하세요. 지연이 발생하는 경우 Journey Optimizer에서 해당 조각을 수동으로 동기화하여 게시된 최신 버전을 가져올 수 있습니다.

## AEM 컨텐츠 조각 액세스 {#access-aem-fragments}

1. **[!UICONTROL 콘텐츠 관리]** 메뉴에서 **[!UICONTROL 조각]**&#x200B;을 선택합니다.

1. **[!UICONTROL AEM 조각]** 탭을 열어 Adobe Experience Manager에서 사용할 수 있는 콘텐츠 조각을 봅니다.

1. 조각 목록에서 ![고급 메뉴](assets/do-not-localize/Smock_FolderSearch_18_N.svg)를 클릭하여 **[!UICONTROL 참조 살펴보기]**&#x200B;를 수행합니다.

   ![](assets/fragment-list-1.png)

1. 조각을 선택하여 상태 및 사용 가능한 작업을 검토합니다.

   * **[!UICONTROL 참조 탐색]**: 여정, 캠페인, 오케스트레이션된 캠페인 및 해당 조각을 사용하는 템플릿을 참조하십시오.
   * **[!UICONTROL AEM에서 열기]**: Adobe Experience Manager에서 조각을 열어 편집하거나 다시 게시합니다.
   * **[!UICONTROL 동기화]**: Adobe Experience Manager에서 Journey Optimizer으로 게시된 최신 버전을 가져옵니다. 예를 들어 다시 게시된 콘텐츠가 일반적인 동기화 기간 후에 표시되지 않는 경우입니다. 제어가 비활성화되면 조각은 이미 Experience Manager의 게시된 버전과 일치합니다.

     ![](assets/fragment-list-2.png)

1. **[!UICONTROL 세부 정보]** 메뉴를 사용하면 메타데이터를 검토하고 동기화된 페이로드를 미리 볼 수 있습니다.

   * **[!UICONTROL 이름]**: Adobe Experience Manager에서 가져온 콘텐츠 조각의 제목입니다.
   * **[!UICONTROL 설명]**: Adobe Experience Manager에서 가져온 설명입니다.
   * **[!UICONTROL 변형]**: 이 조각에 대해 현재 표시된 게시된 변형입니다.
   * **[!UICONTROL 저장소 ID]**: Adobe Experience Manager의 조각에 대한 저장소 식별자입니다.
   * **[!UICONTROL AEM 조각 ID]**: Adobe Experience Manager의 고유한 콘텐츠 조각 식별자.
   * **[!UICONTROL 태그]**: Adobe Experience Manager에 할당된 태그(조직 및 샌드박스의 선택기에 조각이 표시되는지 여부를 결정하는 Journey Optimizer 지원 태그 포함). [태그를 만들고 할당하는 방법을 알아보세요](aem-fragments.md#create-tag)
   * **[!UICONTROL JSON 미리 보기]**: Journey Optimizer에서 사용하는 조각 콘텐츠의 읽기 전용 JSON 구조입니다.

1. **[!UICONTROL 참조 탐색]**&#x200B;에서 탭을 사용하여 여정, 캠페인, 조정된 캠페인 및 조각을 참조하는 템플릿을 확인하세요.

   ![](assets/fragment-list-3.png)

➡️ [콘텐츠 조각에 대해 자세히 알아보기](aem-fragments.md)


