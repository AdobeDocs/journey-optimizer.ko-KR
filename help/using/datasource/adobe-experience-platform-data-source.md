---
title: Adobe Experience Platform 데이터 소스
description: Adobe Experience Platform 데이터 소스를 구성하는 방법 알아보기
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 11%

---

# Adobe Experience Platform 데이터 소스 {#adobe-experience-platform-data-source}

Adobe Experience Platform 데이터 소스는 실시간 고객 프로필 서비스에 대한 연결을 정의합니다. 이 데이터 소스는 기본적으로 제공되며 사전 구성되어 있습니다. 삭제할 수 없습니다. 이 데이터 소스는 실시간 고객 프로필 서비스에서 데이터를 검색하고 사용하도록 설계되었습니다(예를 들어 여정을 입력한 사람이 여성인지 확인). 프로필 데이터 및 경험 이벤트 데이터를 사용할 수 있습니다. 실시간 고객 프로필 서비스에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target=&quot;_blank&quot;}.

>[!NOTE]
>
>1년 전에 만든 1,000개의 최신 경험 이벤트를 검색할 수 있습니다.

실시간 고객 프로필 서비스에 연결할 수 있도록 하려면 키를 사용하여 개인을 식별하고 키를 컨텍스트에 맞는 네임스페이스를 사용해야 합니다. 따라서 여정이 키 및 네임스페이스가 포함된 이벤트로 시작하는 경우에만 이 데이터 소스를 사용할 수 있습니다. [이 페이지](../building-journeys/journey.md)를 참조하십시오.

&quot;ProfileFieldGroup&quot;이라는 사전 구성된 필드 그룹을 편집하고, 새 필드 그룹을 추가하고, 초안 또는 라이브 여정에서 사용되지 않는 필드 그룹을 제거할 수 있습니다. [이 페이지](../datasource/configure-data-sources.md#define-field-groups)를 참조하십시오.

필드 그룹을 기본 데이터 소스에 추가하는 주요 단계는 다음과 같습니다.

1. 데이터 소스 목록에서 기본 제공 Adobe Experience Platform 데이터 소스를 선택합니다.

   화면 오른쪽에 데이터 소스 구성 창이 열립니다.

   ![](../assets/journey23.png)

1. 클릭 **[!UICONTROL Add a New Field Group]** 검색할 일련의 새 필드를 정의합니다. [이 페이지](../datasource/configure-data-sources.md#define-field-groups)를 참조하십시오.

   ![](../assets/journey24.png)

1. 에서 스키마 선택 **[!UICONTROL Schema]** 드롭다운. 이 필드에는 Adobe Experience Platform에서 사용할 수 있는 프로필 및 경험 이벤트 스키마가 나열됩니다. 스키마 만들기는 다음에서 수행되지 않습니다 [!DNL Journey Optimizer]. Adobe Experience Platform에서 공연되었습니다.
1. 사용할 필드를 선택합니다.
1. 클릭 **[!UICONTROL Save]**.

필드 그룹 이름에 커서를 놓으면 오른쪽에 두 개의 아이콘이 표시됩니다. 필드 그룹을 삭제하고 복제할 수 있습니다. 다음 사항에 유의하십시오. **[!UICONTROL Delete]** 아이콘 은 필드 그룹이 라이브 또는 초안 여정에서 사용되지 않는 경우에만 사용할 수 있습니다(정보에 표시) **[!UICONTROL Used in]** 필드)만 로드하는 것입니다.
