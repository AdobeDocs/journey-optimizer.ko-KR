---
solution: Journey Optimizer
product: journey optimizer
title: AEM 저장소 설정 구성
description: 관리자가 Journey Optimizer에서 AEM 저장소, 사용자 지정 도메인, 인증된 게시 및 작성자 전용 콘텐츠 조각 액세스를 구성하는 방법에 대해 알아봅니다.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM, 콘텐츠 조각, 관리, 저장소, 인증, 작성자, 게시
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 0%

---

# Adobe Experience Manager 저장소 액세스 구성 {#aem-admin-settings}

Adobe Journey Optimizer은 **[!DNL Adobe Experience Manager as a Cloud Service]**&#x200B;과(와) 통합되므로 여정 및 캠페인에서 **콘텐츠 조각**&#x200B;을(를) 사용할 수 있습니다. **콘텐츠 조각**&#x200B;은(는) 기본적으로 Adobe Experience Manager 게시 리포지토리에서 읽혀집니다. 관리자는 **[!UICONTROL AEM 통합]** 메뉴에서 작성자 전용으로 전환하거나 게시 액세스를 조정할 수 있습니다.

➡️ 저장소가 구성되면 Journey Optimizer에서 작성 및 선택 작업을 위해 [Experience Manager 콘텐츠 조각을 사용하여 작업](../integrations/aem-fragments.md)을 계속합니다.

## 저장소 구성 {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL AEM 통합]**&#x200B;은(는) 저장소 설정을 **샌드박스당**&#x200B;에 저장합니다. 각 샌드박스는 자체 통합을 유지하며 샌드박스 간에 적용되지 않습니다.

Journey Optimizer은 조직, 샌드박스 및 Adobe Experience Manager 저장소당 하나의 통합을 저장합니다. 동일한 조합에 대해 새 통합을 저장하면 이전 설정이 대체되며 최신 구성만 유지됩니다.

저장소를 구성하려면 다음 작업을 수행하십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL AEM 통합]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 통합 만들기]**&#x200B;를 클릭합니다.

   ![](assets/aem-admin-settings-1.png)

1. **[!DNL Adobe Experience Manager Managed Services]**&#x200B;을(를) 사용하는 경우 **[!UICONTROL 사용자 지정 AMS 저장소 ID]** 필드에 `adobecqms.net`(으)로 끝나는 저장소 호스트 이름을 입력하십시오.

   ![](assets/aem-admin-settings-6.png)

1. 구성할 리포지토리를 선택하고 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

   또한 **[!UICONTROL 보기]**&#x200B;를 클릭하여 이 저장소에 액세스할 수 있습니다.

   >[!IMPORTANT]
   >
   >동일한 조직, 샌드박스 및 저장소에 대한 새 구성을 저장하면 **기본 구성, 즉**&#x200B;게시&#x200B;**저장소가 대체**&#x200B;됩니다.

   ![](assets/aem-admin-settings-2.png)

1. **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 설정 선택:

   +++ 작성자만 설정

   Journey Optimizer에서 Adobe Experience Manager **작성자** 환경에서만 콘텐츠 조각을 읽어야 하는 경우 **[!UICONTROL 작성자만 설정]**&#x200B;을 선택합니다. 작성자에서 게시 및 라이브 게시 업데이트로의 복제는 지원되지 않습니다.

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ 게시 인스턴스 설정

   1. 게시 인스턴스 설정을 켜려면 **[!UICONTROL 게시 인스턴스 설정]**&#x200B;을(를) 선택하십시오.

      ![](assets/aem-admin-settings-4.png)

   1. 필요한 경우 게시 인스턴스에 대한 요청에 서비스 자격 증명이 포함되도록 **[!UICONTROL 게시 인스턴스에 토큰 보내기]**&#x200B;를 사용하도록 설정하십시오.

   1. 인증을 위해 유효한 **[!UICONTROL 서비스 자격 증명 JSON]**&#x200B;을(를) 붙여 넣으십시오.

   1. 필요한 경우 조직에서 콘텐츠를 가져오기 위해 기본 AEM 게시 호스트(`publish-XX-XX.adobeaemcloud.com`)에 연결할 수 없는 경우 사용자 지정 도메인을 제공합니다.

      ![](assets/aem-admin-settings-5.png)

   +++

1. 인스턴스 설정을 완료한 후 콘텐츠 조각을 선택하여 통합이 작동하는지 확인합니다.

   ![](assets/aem-admin-settings-7.png)

1. **콘텐츠 관리자** 창에서 테스트할 조각을 선택한 다음 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 테스트 콘텐츠 조각을 선택한 상태로 저장하면 유효성 검사가 자동으로 실행됩니다. 유효성 검사가 실패하면 구성을 수정할 수 있도록 오류 목록이 표시됩니다.

   ![](assets/aem-admin-settings-8.png)

1. 이 리포지토리 통합을 편집하거나 비활성화하려면 **[!UICONTROL AEM 통합]** 메뉴에서 이전에 만든 구성에 액세스하십시오.

이 구성을 저장하면 Journey Optimizer이 현재 샌드박스의 해당 저장소에 대해 저장합니다. 그런 다음 **콘텐츠 관리자** 선택기에서 콘텐츠를 탐색하고 선택할 때 해당 리포지토리와 해당 설정을 사용할 수 있습니다.

