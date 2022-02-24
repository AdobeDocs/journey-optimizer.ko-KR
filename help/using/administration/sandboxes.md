---
title: 샌드박스 관리
description: 샌드박스를 관리하는 방법 알아보기
feature: Sandboxes
topic: Administration
role: Admin
level: Intermediate
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 7de0088c07c644c42f5def3657d2629ce5e7754e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 66%

---

# 샌드박스 관리 {#sandboxes}

## 샌드박스 사용 {#using-sandbox}

[!DNL Journey Optimizer]에서는 인스턴스를 샌드박스라는 분리된 가상 환경으로 분할할 수 있습니다.
샌드박스는 Admin Console에서 제품 프로필을 통해 할당됩니다. [샌드박스를 할당하는 방법을 알아봅니다](permissions.md#create-product-profile).

[!DNL Journey Optimizer] (은)는 해당 조직을 위해 만들어진 Adobe Experience Platform 샌드박스를 반영합니다.
Adobe Experience Platform 인스턴스에서 Adobe Experience Platform 샌드박스를 만들거나 재설정할 수 있습니다. [자세한 내용은 샌드박스 사용 안내서를 참조하십시오](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;}.

조직 이름 옆에 있는 화면의 오른쪽 상단에 샌드박스 전환기 컨트롤이 있습니다. 한 샌드박스에서 다른 샌드박스로 전환하려면 전환기에서 현재 활성 샌드박스를 클릭하고 드롭다운 목록에서 다른 샌드박스를 선택하십시오.

![](../assets/sandbox_5.png)

➡️ [비디오에서 이 기능 살펴보기](#video)

## 샌드박스 할당 {#assign-sandboxes}

>[!IMPORTANT]
>
> 샌드박스 관리는 **[!UICONTROL Product]** 또는 **[!UICONTROL System]** 관리자 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}.

기본 제공 또는 사용자 지정에 다른 샌드박스를 할당하도록 선택할 수 있습니다 **[!UICONTROL Product profiles]**.

샌드박스를 할당하려면

1. 에서 [!DNL Admin Console]: **[!UICONTROL Products]** 탭에서 을 선택합니다 **[!UICONTROL Adobe Experience Platform Apps]** 제품.

1. **[!UICONTROL Product profile]**&#x200B;을(를) 선택합니다. 

   ![](../assets/sandbox_1.png)

1. **[!UICONTROL Permissions]** 탭을 선택합니다. 

1. 을(를) 선택합니다 **[!UICONTROL Sandboxes]** 기능.

   ![](../assets/sandbox_2.png)

1. **[!UICONTROL Available Permissions Items]** 아래에서 더하기(+) 아이콘을 클릭하여 샌드박스를 프로필에 할당합니다. [샌드박스에 대해 자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ko){target=&quot;_blank&quot;}.

   ![](../assets/sandbox_3.png)

1. 필요한 경우 아래의 **[!UICONTROL Included Permission Items]**&#x200B;아래에 있는 샌드박스를 제거하려면 옆에 X 아이콘을 클릭하십시오 **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_4.png)

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 콘텐츠 액세스 {#content-access}

콘텐츠 액세스 가능성을 구성하려면 각 샌드박스에 콘텐츠 공유 폴더를 할당해야 합니다. 관리자용 [!DNL Admin Console]에 표시된 **[!UICONTROL Storage]** 탭에서 공유 폴더를 만들고 구성할 수 있습니다. 시스템 관리자로서 [!DNL Admin Console]에 액세스할 수 있는 경우 공유 폴더를 만들고 다른 액세스 수준의 위임자를 공유 폴더에 추가할 수 있습니다.

![](../assets/do-not-localize/content_access.png)

내용이 올바른 샌드박스와 동기화되도록 하려면 샌드박스와 동일한 구문을 따라야 합니다. 예를 들어 샌드박스가 개발이라고 하는 경우 공유 폴더의 이름이 같아야 합니다.

[공유 폴더를 관리하는 방법 알아보기](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}.

## 방법 비디오{#video}

샌드박스의 정의, 그리고 개발과 프로덕션 샌드박스를 구분하는 방법을 이해합니다. 샌드박스를 만들고, 재설정하고, 삭제하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
