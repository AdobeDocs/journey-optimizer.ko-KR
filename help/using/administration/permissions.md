---
title: 사용자 및 제품 프로필 관리
description: 권한을 관리하는 방법 알아보기
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 7de0088c07c644c42f5def3657d2629ce5e7754e
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 14%

---

# 사용자 및 제품 프로필 관리 {#manage-permissions}

>[!IMPORTANT]
>
> 아래 설명된 각 절차는 **[!UICONTROL Product]** 또는 **[!UICONTROL System]** 관리자 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** 는 조직 내에서 동일한 권한과 샌드박스를 공유하는 사용자 집합입니다.

다음 [!DNL Journey Optimizer] 제품을 사용하면 다양한 기본 제공 중 선택할 수 있습니다 **[!UICONTROL Product profiles]** 사용자에게 할당할 수 있는 다양한 수준의 권한이 있습니다. 사용 가능한 항목에 대한 자세한 정보 **[!UICONTROL Product profiles]**, 다음을 참조하십시오 [페이지](ootb-product-profiles.md).

에 속하는 각 사용자 **[!UICONTROL Product profiles]** 는 제품에 포함된 Adobe 앱 및 서비스를 통해 권한을 받습니다.

직접 만들 수도 있습니다 **[!UICONTROL Product profiles]** 인터페이스에서 특정 기능 또는 개체에 대한 사용자의 액세스를 세밀하게 조정하려면

## 제품 프로필 할당 {#assigning-product-profile}

기본 제공 또는 사용자 지정을 선택할 수 있습니다 **[!UICONTROL Product profile]** 사용자에게 문의하십시오.

권한이 할당된 모든 기본 제품 프로필 목록은 [내장 제품 프로필](ootb-product-profiles.md) 섹션을 참조하십시오.

을(를) 할당하려면 **[!UICONTROL Product profile]**:

1. 에서 [!DNL Admin Console]: **[!UICONTROL Products]** 탭에서 을 선택합니다 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품.

1. **[!UICONTROL Product profile]**&#x200B;을(를) 선택합니다. 

   ![](../assets/do-not-localize/access_control_2.png)

1. **[!UICONTROL Users]** 탭에서 **[!UICONTROL Add user]**&#x200B;을 클릭합니다.

   ![](../assets/do-not-localize/access_control_3.png)

1. 사용자 이름이나 이메일 주소를 입력하고 사용자를 선택합니다.

   사용자가 이전에 [!DNL Admin Console]를 참조하려면 [사용자 추가 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/do-not-localize/access_control_4.png)

1. 위와 동일한 단계를 수행하여 다른 사용자를 **[!UICONTROL Product profile]**. 그런 다음 **[!UICONTROL Save]**.

그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

사용자 관리에 대한 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

인스턴스에 액세스할 때 사용자에게는 **[!UICONTROL Product profile]**. 사용자에게 기능에 대한 액세스 권한이 없는 경우 다음 화면이 나타납니다.

![](../assets/do-not-localize/access_control_1.png)

## 기존 제품 프로필 편집 {#edit-product-profile}

기본 제공 또는 사용자 지정 **[!UICONTROL Product profiles]**&#x200B;언제든지 권한을 추가하거나 삭제할 수 있습니다.

이 예제에서는 **[!UICONTROL Permissions]** 관련 **[!UICONTROL Message]** 여정 뷰어에 할당된 사용자를 위한 기능 **[!UICONTROL Product profile]**. 그러면 사용자가 메시지를 게시할 수 있습니다.

기본 제공 또는 사용자 지정을 수정하는 경우 **[!UICONTROL Product profile]**&#x200B;로 설정되면 지정된 모든 사용자에게 영향을 줍니다 **[!UICONTROL Product profile]**.

1. 에서 [!DNL Admin Console]: **[!UICONTROL Products]** 탭에서 을 선택합니다 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품.

1. 여정 뷰어 선택 **[!UICONTROL Product profile]**.

1. **[!UICONTROL Permissions]** 탭을 선택합니다. 

   다음 **[!UICONTROL Permissions]** 탭에는 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품.

   ![](../assets/do-not-localize/access_control_5.png)

1. 을(를) 선택합니다 **[!UICONTROL Messages]** 기능.

   ![](../assets/do-not-localize/access_control_6.png)

1. 에서 **[!UICONTROL Available Permission Items]** 목록에 지정할 권한을 선택합니다 **[!UICONTROL Product profile]** 더하기(+) 아이콘을 클릭합니다.

   여기에서는 **[!UICONTROL Publish messages]** 권한.

   ![](../assets/do-not-localize/access_control_7.png)

1. 필요한 경우 **[!UICONTROL Included Permission Items]** 아래에서 옆에 있는 X 아이콘을 클릭하여 제품 프로필에서 권한을 제거합니다.

1. 완료되었으면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](../assets/do-not-localize/access_control_8.png)

필요한 경우 특정 권한이 있는 새 제품 프로필을 만들 수도 있습니다. 자세한 내용은 [제품 프로필 만들기](#create-product-profile).

## 제품 프로필 만들기 {#create-product-profile}

[!DNL Journey Optimizer] 을(를) 통해 직접 **[!UICONTROL Product profiles]** 사용자에게 권한 집합 및 샌드박스를 할당합니다. 사용 **[!UICONTROL Product profiles]**&#x200B;로 설정하면 인터페이스에서 특정 기능 또는 개체에 대한 액세스를 승인하거나 거부할 수 있습니다.

샌드박스를 만들고 관리하는 방법에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;}.

이 예에서는 이름이 인 제품 프로필을 만듭니다 **여정 읽기 전용** 여기서 여정 기능에 읽기 전용 권한을 부여합니다. 사용자는 여정에 액세스하고 볼 수만 있으며, 와 같은 다른 기능에 액세스할 수 없습니다 **[!DNL  Decision management]** 또는 **[!DNL Messages]** in [!DNL Journey Optimizer].

Adobe의 **여정 읽기 전용** **[!UICONTROL product profiles]**:

1. 액세스 권한 [!DNL Admin Console].

1. 에서 **[!UICONTROL Products]** 탭에서 을 선택합니다 **[!UICONTROL Experience Cloud - Platform powered applications]** 제품.

1. **[!UICONTROL New Profile]**&#x200B;을(를) 클릭합니다.

   ![](../assets/do-not-localize/access_control_9.png)

1. 추가 **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** 및 **[!UICONTROL Description]** 새로운 **[!UICONTROL product profiles]**.

   ![](../assets/do-not-localize/access_control_10.png)

1. 이 제품 프로필에 추가되거나 제거될 때 사용자에게 이메일로 알릴 것인지 여부를 **[!UICONTROL Notifications]** 카테고리에서 선택합니다.

1. 완료되면 를 클릭합니다 **[!UICONTROL Save]** 새로 만든 **[!UICONTROL product profiles]**.

1. 사용자가 다른 기능에 액세스할 수 있는 권한을 추가하려면 **[!UICONTROL Permissions]** 탭.

1. 과 같은 다양한 기능 중에서 선택합니다. **[!DNL Messages]**, **[!DNL Segments]** 또는 **[!DNL Decision management]** 사용 가능 [!DNL Journey Optimizer] 왼쪽 메뉴에 나열됩니다.

   여기에서 을(를) 선택합니다 **[!UICONTROL Journeys]** 기능.

   ![](../assets/do-not-localize/access_control_11.png)

1. 에서 **[!UICONTROL Available Permission Items]** 목록에 지정할 권한을 선택합니다 **[!UICONTROL Product profile]** 더하기(+) 아이콘을 클릭합니다.

   여기에서 선택합니다 **[!DNL View journeys]** 및 **[!DNL View journeys event, data sources, actions]**.

   ![](../assets/do-not-localize/access_control_12.png)

1. 을(를) 선택합니다 **[!UICONTROL Sandbox access]** 사용자에게 지정할 샌드박스 선택 기능 **[!UICONTROL Product profile]**.

   ![](../assets/do-not-localize/access_control_13.png)

1. **[!UICONTROL Available Permissions Items]** 아래에서 더하기(+) 아이콘을 클릭하여 샌드박스를 프로필에 할당합니다. [샌드박스에 대한 자세한 내용을 살펴보십시오](sandboxes.md).

1. 완료되었으면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

사용자 **[!UICONTROL Product profile]** 이제 가 생성되어 구성되었습니다. 이제 사용자에게 할당해야 합니다.

제품 프로필 만들기 및 관리에 대한 자세한 내용은 [Admin Console 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
