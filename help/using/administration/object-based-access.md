---
solution: Journey Optimizer
product: journey optimizer
title: 객체 수준 액세스 제어
description: 개체 수준 액세스 제어에 대해 알아보기
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 객체 수준 액세스 제어 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="객체 수준 액세스 제어"
>abstract="액세스할 수 없는 레이블을 적용하면 이 객체에 대한 액세스가 취소됩니다."

>[!IMPORTANT]
>
>객체 수준 액세스 제어 사용은 현재 선택한 고객에게만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.

OLAC(객체 수준 액세스 제어)를 사용하면 다양한 객체에 대한 데이터 액세스를 관리할 권한을 정의할 수 있습니다.

* 여정
* 캠페인
* 랜딩 페이지
* 오퍼
* 오퍼 컬렉션
* Offer Decisioning

이 소프트웨어의 목적은 개인 데이터를 추가로 보호할 수 있도록 권한이 없는 사용자로부터 중요한 디지털 자산을 보호하는 것입니다.

Adobe Journey Optimizer에서 OLAC를 사용하여 데이터를 보호하고 특정 객체에 대한 특정 액세스 권한을 부여할 수 있습니다.

## 레이블 만들기 {#create-assign-labels}

>[!IMPORTANT]
>
>레이블을 만들려면 **[!UICONTROL Manage usage labels]** 권한.

**[!UICONTROL Labels]** 을(를) 사용하면 해당 데이터에 적용되는 사용 정책에 따라 데이터 세트 및 필드를 분류할 수 있습니다. **[!UICONTROL Labels]** 언제든지 적용할 수 있으므로 데이터를 유연하게 관리할 수 있습니다.

에서 레이블을 만들 수 있습니다 [!DNL Permissions] 제품. 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Labels]** 또한 Journey Optimizer에서 직접 만들 수도 있습니다.

1. Adobe Journey Optimizer 개체에서 새로 만든 항목이 있습니다 **[!UICONTROL Campaign]**&#x200B;를 클릭하고 **[!UICONTROL Manage access]** 버튼을 클릭합니다.

   ![](assets/olac_1.png)

1. 에서 **[!UICONTROL Manage access]** 창 **[!UICONTROL Create label]**.

   ![](assets/olac_2.png)

1. 레이블을 구성하려면 다음을 지정해야 합니다.
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. 클릭 **[!UICONTROL Create]** 저장 **[!UICONTROL Label]**.

새로 만든 사용자 **[!UICONTROL Label]** 이제 목록에서 을 사용할 수 있습니다. 필요한 경우, [!DNL Permissions] 제품.

## 레이블 지정 {#assign-labels}

>[!IMPORTANT]
>
>레이블을 할당하려면 관리 권한이 있는 역할의 일부여야 합니다(예: [!DNL Manage journeys], [!DNL Manage Campaigns] 또는 [!DNL Manage decisions]. 이 권한이 없으면 **[!UICONTROL Manage access]** 버튼이 회색으로 표시됩니다.

사용자 지정 또는 코어 데이터 사용 레이블을 Journey Optimizer 개체에 할당하려면 다음을 수행합니다.

1. Adobe Journey Optimizer 개체에서 새로 만든 항목이 있습니다 **[!UICONTROL Campaign]**&#x200B;를 클릭하고 **[!UICONTROL Manage access]** 버튼을 클릭합니다.

   ![](assets/olac_1.png)

1. 에서 **[!UICONTROL Manage access]** 창에서 사용자 지정 또는 핵심 데이터 사용 레이블을 선택하여 이 객체에 대한 액세스를 관리합니다.

   코어 데이터 사용 레이블에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. 클릭 **[!UICONTROL Save]** 레이블 제한을 적용하려면

이 객체에 액세스하려면 사용자가 **[!UICONTROL Label]** 포함됨 **[!UICONTROL Roles]**.
예를 들어 C1 레이블이 있는 사용자는 C1에 대해 레이블이 지정되거나 레이블이 지정되지 않은 객체에만 액세스할 수 있습니다.

할당 방법에 대한 자세한 내용 **[!UICONTROL Label]** 변환 후 **[!UICONTROL Role]**&#x200B;를 참조하려면 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
