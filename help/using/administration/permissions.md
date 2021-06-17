---
title: 사용자 및 제품 프로필 관리
description: 권한을 관리하는 방법 알아보기
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: 컨트롤 그룹
topic: 관리
role: Administrator
level: Intermediate
source-git-commit: f2c280ba3d2148a62eebff421ef6c8c3c0352936
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 16%

---

# 사용자 및 제품 프로필 관리 {#manage-permissions}

>[!IMPORTANT]
>
> 아래 설명된 각 절차는 **[!UICONTROL Product]** 또는 **[!UICONTROL System]** 관리자만 수행할 수 있습니다. 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html)를 참조하십시오.

**[!UICONTROL Product profiles]** 는 조직 내에서 동일한 권한과 샌드박스를 공유하는 사용자 집합입니다.

[!DNL Journey Optimizer] 제품을 사용하면 사용자에게 할당할 권한이 있는 다른 기본 **[!UICONTROL Product profiles]** 중에서 선택할 수 있습니다. 사용 가능한 **[!UICONTROL Product profiles]**&#x200B;에 대한 자세한 내용은 이 [page](ootb-product-profiles.md)를 참조하십시오.

**[!UICONTROL Product profiles]**&#x200B;에 속한 각 사용자에게는 제품에 포함된 Adobe 앱과 서비스가 부여됩니다.

인터페이스에서 특정 기능 또는 개체에 대한 사용자의 액세스를 세밀하게 조정하려면 고유한 **[!UICONTROL Product profiles]** 을(를) 만들 수도 있습니다.

## 제품 프로필 할당 {#assigning-product-profile}

기본 제공 또는 사용자 지정 **[!UICONTROL Product profile]**&#x200B;을 사용자에게 할당하도록 선택할 수 있습니다.

권한이 할당된 모든 기본 제품 프로필의 목록은 [기본 제공 제품 프로필](ootb-product-profiles.md) 섹션에 있습니다.

**[!UICONTROL Product profile]**&#x200B;을 할당하려면

1. [!DNL Admin Console]의 **[!UICONTROL Products]** 탭에서 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품을 선택합니다.

1. **[!UICONTROL Product profile]**&#x200B;을(를) 선택합니다. 

   ![](../assets/access_control_2.png)

1. **[!UICONTROL Users]** 탭에서 **[!UICONTROL Add user]**&#x200B;을 클릭합니다.

   ![](../assets/access_control_3.png)

1. 사용자 이름이나 이메일 주소를 입력하고 사용자를 선택합니다.

   사용자가 이전에 [!DNL Admin Console]에서 만들어지지 않았다면 [사용자 추가 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)를 참조하십시오.

   ![](../assets/access_control_4.png)

1. 위와 동일한 단계를 수행하여 다른 사용자를 **[!UICONTROL Product profile]**&#x200B;에 추가합니다. 그런 다음 **[!UICONTROL Save]** 을 클릭합니다.

그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

사용자 관리에 대한 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html)를 참조하십시오.

인스턴스에 액세스할 때 사용자에게 **[!UICONTROL Product profile]**&#x200B;에 지정된 권한에 따라 특정 보기가 표시됩니다. 사용자에게 기능에 대한 액세스 권한이 없는 경우 다음 화면이 나타납니다.

![](../assets/access_control_1.png)

## 기존 제품 프로필 편집 {#edit-product-profile}

기본 제공 또는 사용자 지정 **[!UICONTROL Product profiles]**&#x200B;의 경우 언제든지 권한을 추가하거나 삭제할 수 있습니다.

이 예제에서는 여정 뷰어 **[!UICONTROL Product profile]**&#x200B;에 할당된 사용자에 대해 **[!UICONTROL Message]** 기능과 관련된 **[!UICONTROL Permissions]**&#x200B;을 추가하려고 합니다. 그러면 사용자가 메시지를 게시할 수 있습니다.

기본 제공 또는 사용자 지정 **[!UICONTROL Product profile]**&#x200B;을 수정하는 경우 이 **[!UICONTROL Product profile]**&#x200B;에 지정된 모든 사용자에게 영향을 줍니다.

1. [!DNL Admin Console]의 **[!UICONTROL Products]** 탭에서 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품을 선택합니다.

1. 여정 뷰어 **[!UICONTROL Product profile]**&#x200B;를 선택합니다.

1. **[!UICONTROL Permissions]** 탭을 선택합니다. 

   **[!UICONTROL Permissions]** 탭에는 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품에 적용되는 기능 목록이 표시됩니다.

   ![](../assets/access_control_5.png)

1. **[!UICONTROL Messages]** 기능을 선택합니다.

   ![](../assets/access_control_6.png)

1. **[!UICONTROL Available Permission Items]** 목록에서 더하기(+) 아이콘을 클릭하여 **[!UICONTROL Product profile]**&#x200B;에 할당할 권한을 선택합니다.

   여기서는 **[!UICONTROL Publish messages]** 권한을 추가합니다.

   ![](../assets/access_control_7.png)

1. 필요한 경우 **[!UICONTROL Included Permission Items]** 아래에서 옆에 있는 X 아이콘을 클릭하여 제품 프로필에서 권한을 제거합니다.

1. 완료되었으면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](../assets/access_control_8.png)

필요한 경우 특정 권한이 있는 새 제품 프로필을 만들 수도 있습니다. 자세한 내용은 [제품 프로필 만들기](#create-product-profile)를 참조하십시오.

## 제품 프로필 만들기 {#create-product-profile}

[!DNL Journey Optimizer] 에서는 직접 만들고 권한 집합 **[!UICONTROL Product profiles]** 과 샌드박스를 사용자에게 할당할 수 있습니다. **[!UICONTROL Product profiles]**&#x200B;을 사용하면 인터페이스에서 특정 기능 또는 개체에 대한 액세스를 승인하거나 거부할 수 있습니다.

샌드박스를 만들고 관리하는 방법에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=ko)를 참조하십시오.

이 예에서는 **여정 읽기 전용**&#x200B;이라는 제품 프로필을 만듭니다. 여기서 여정 기능에 읽기 전용 권한을 부여합니다. 사용자는 여정에 액세스하고 볼 수만 있으며, [!DNL Journey Optimizer]에서 **[!UICONTROL Decision management]** 또는 **[!UICONTROL Messages]** 등의 다른 기능에 액세스할 수 없습니다.

**여정을 만들려면** **[!UICONTROL product profiles]**:

1. [!DNL Admin Console]에 액세스합니다.

1. **[!UICONTROL Products]** 탭에서 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품을 선택합니다.

1. **[!UICONTROL New Profile]**&#x200B;을(를) 클릭합니다.

   ![](../assets/access_control_9.png)

1. 새 **[!UICONTROL product profiles]**&#x200B;에 대해 **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** 및 **[!UICONTROL Description]**&#x200B;를 추가합니다.

   ![](../assets/access_control_10.png)

1. 이 제품 프로필에 추가되거나 제거될 때 사용자에게 이메일로 알릴 것인지 여부를 **[!UICONTROL Notifications]** 카테고리에서 선택합니다.

1. 완료되면 **[!UICONTROL Save]** 을 클릭하고 새로 만든 **[!UICONTROL product profiles]** 을 선택합니다.

1. 사용자가 다른 기능에 액세스할 수 있는 권한을 추가하려면 **[!UICONTROL Permissions]** 탭을 선택합니다.

1. 왼쪽 메뉴에 나열된 [!DNL Journey Optimizer]에서 사용할 수 있는 **[!UICONTROL Messages]**, **[!UICONTROL Segments]** 또는 **[!UICONTROL Decision management]** 등의 다양한 기능 중에서 선택합니다.

   여기서는 **[!UICONTROL Journeys]** 기능을 선택합니다.

   ![](../assets/access_control_11.png)

1. **[!UICONTROL Available Permission Items]** 목록에서 더하기(+) 아이콘을 클릭하여 **[!UICONTROL Product profile]**&#x200B;에 할당할 권한을 선택합니다.

   여기에서는 **[!UICONTROL View journeys]** 및 **[!UICONTROL View journeys event, data sources, actions]**&#x200B;을 선택합니다.

   ![](../assets/access_control_12.png)

1. **[!UICONTROL Sandbox access]** 기능을 선택하여 **[!UICONTROL Product profile]**&#x200B;에 할당할 샌드박스를 선택합니다.

   ![](../assets/access_control_13.png)

1. **[!UICONTROL Available Permissions Items]** 아래에서 더하기(+) 아이콘을 클릭하여 샌드박스를 프로필에 할당합니다. [샌드박스에 대한 자세한 내용을 살펴보십시오](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ko).

1. 완료되었으면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

이제 **[!UICONTROL Product profile]**&#x200B;이(가) 생성되어 구성되었습니다. 이제 사용자에게 할당해야 합니다.

제품 프로필 만들기 및 관리에 대한 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html)를 참조하십시오.
