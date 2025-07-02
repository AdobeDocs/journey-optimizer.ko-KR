---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 데이터 소스
description: Adobe Experience Platform 데이터 소스를 구성하는 방법 알아보기
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 내장, 소스, 데이터, 플랫폼, 통합
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 8e020f79e0f44e6fc804fcceb149146f9644c777
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 27%

---

# Adobe Experience Platform 데이터 소스 {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform 데이터 소스"
>abstract="Adobe Experience Platform 데이터 소스는 Adobe 실시간 고객 프로필에 대한 연결을 정의합니다. 이 기본 제공 데이터 소스는 미리 구성되어 삭제할 수 없습니다. 실시간 고객 프로필 서비스에서 데이터를 검색하고 사용하도록 디자인되었습니다(예: 여정에 진입한 개인이 여성인지 확인)."

Adobe Experience Platform 데이터 소스는 Adobe 실시간 고객 프로필에 대한 연결을 정의합니다. 이 기본 제공 데이터 소스는 미리 구성되어 삭제할 수 없습니다. 이 데이터 소스는 실시간 고객 프로필 서비스에서 데이터를 검색하고 사용하도록 설계되었습니다(예: 여정에 입력한 사람이 여성인지 확인). Adobe 실시간 고객 프로필에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}를 참조하세요.

실시간 고객 프로필 서비스에 연결할 수 있도록 하려면 키를 사용하여 사용자를 식별하고 키를 컨텍스트화하는 네임스페이스를 사용해야 합니다. 따라서 여정이 키와 네임스페이스가 포함된 이벤트로 시작하는 경우에만 이 데이터 소스를 사용할 수 있습니다. [자세히 알아보기](../building-journeys/journey.md).

&quot;ProfileFieldGroup&quot;이라는 사전 구성된 필드 그룹을 편집하고, 새 필드 그룹을 추가하고, 초안 또는 라이브 여정에서 사용되지 않는 필드 그룹을 제거할 수 있습니다. [자세히 알아보기](../datasource/configure-data-sources.md#define-field-groups).


>[!CAUTION]
>
>여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 대체 방법을 고려하십시오. [자세히 알아보기](../building-journeys/exp-event-lookup.md)


기본 제공 데이터 소스에 필드 그룹을 추가하는 주요 단계는 아래에 자세히 설명되어 있습니다.

1. 데이터 원본 목록에서 기본 제공 **Adobe Experience Platform** 데이터 원본을 선택합니다.

   화면 오른쪽에 데이터 소스 구성 창이 열립니다.

   ![](assets/journey23.png)

1. **[!UICONTROL 새 필드 그룹 추가]**&#x200B;를 선택하여 검색할 [새 일련의 필드를 정의](../datasource/configure-data-sources.md#define-field-groups)합니다.

   ![](assets/journey24.png)

1. **[!UICONTROL 스키마]** 드롭다운에서 스키마를 선택합니다. 스키마 생성은 Adobe Experience Platform에서 수행되고, Adobe Journey Optimizer에서는 수행되지 않습니다.
1. 사용할 필드를 선택하고 변경 사항을 저장합니다.


>[!TIP]
>
>필드 그룹 이름 위로 마우스를 가져가면 오른쪽에 두 개의 아이콘이 표시됩니다. 필드 그룹을 **복제**&#x200B;하거나 **삭제**&#x200B;하려면 사용하세요. **[!UICONTROL Delete]** 아이콘은 **Live**, **초안** 또는 **완료됨** 여정에서 필드 그룹을 사용하지 않는 경우에만 사용할 수 있습니다. **[!UICONTROL 다음에서 사용됨]** 필드를 참조하여 해당 여부를 확인하십시오.
