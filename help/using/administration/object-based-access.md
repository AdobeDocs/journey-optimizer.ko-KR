---
solution: Journey Optimizer
product: journey optimizer
title: 객체 수준 액세스 제어
description: 개체 선택에 대한 데이터 액세스를 관리할 권한을 정의할 수 있는 개체 수준 액세스 제어에 대해 알아봅니다
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 개체, 수준, 액세스, 제어, 레이블, 논리, 권한 부여
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 10%

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
* Campaign
* 랜딩 페이지
* 오퍼
* 오퍼 컬렉션
* Offer decisioning

이 소프트웨어의 목적은 개인 데이터를 추가로 보호할 수 있도록 권한이 없는 사용자로부터 중요한 디지털 자산을 보호하는 것입니다.

Adobe Journey Optimizer에서 OLAC를 사용하면 데이터를 보호하고 특정 객체에 대한 특정 액세스 권한을 부여할 수 있습니다.

## 레이블 만들기 {#create-assign-labels}

>[!IMPORTANT]
>
>레이블을 만들려면 **[!UICONTROL 사용 레이블 관리]** 권한.

**[!UICONTROL 레이블을 사용하면 해당 데이터에 적용되는 사용 정책에 따라 데이터 세트 및 필드를 분류할 수 있습니다.]** **[!UICONTROL 레이블]** 언제든지 적용할 수 있으므로 데이터를 유연하게 관리할 수 있습니다.

에서 레이블을 만들 수 있습니다 [!DNL Permissions] 제품. 자세한 정보는 이 [페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html)를 참조하십시오.

**[!UICONTROL 레이블]** Journey Optimizer에서 직접 만들 수도 있습니다.

1. Adobe Journey Optimizer 개체에서 새로 만든 항목이 있습니다 **[!UICONTROL 캠페인]**&#x200B;를 클릭하고 **[!UICONTROL 액세스 관리]** 버튼을 클릭합니다.

   ![](assets/olac_1.png)

1. 에서 **[!UICONTROL 액세스 관리]** 창 **[!UICONTROL 레이블 만들기]**.

   ![](assets/olac_2.png)

1. 레이블을 구성하려면 다음을 지정해야 합니다.
   * **[!UICONTROL 이름]**
   * **[!UICONTROL 친숙한 이름]**
   * **[!UICONTROL 설명]**

   ![](assets/olac_3.png)

1. 클릭 **[!UICONTROL 만들기]** 저장 **[!UICONTROL 레이블]**.

새로 만든 사용자 **[!UICONTROL 레이블]** 이제 목록에서 을 사용할 수 있습니다. 필요한 경우, [!DNL Permissions] 제품.

## 레이블 지정 {#assign-labels}

>[!IMPORTANT]
>
>레이블을 할당하려면 관리 권한이 있는 역할의 일부여야 합니다(예: [!DNL Manage journeys], [!DNL Manage Campaigns] 또는 [!DNL Manage decisions]. 이 권한이 없으면 **[!UICONTROL 액세스 관리]** 버튼이 회색으로 표시됩니다.

사용자 지정 또는 핵심 데이터 사용 레이블을 Journey Optimizer 개체에 지정하려면 다음을 수행하십시오.

1. Adobe Journey Optimizer 개체에서 새로 만든 항목이 있습니다 **[!UICONTROL 캠페인]**&#x200B;를 클릭하고 **[!UICONTROL 액세스 관리]** 버튼을 클릭합니다.

   ![](assets/olac_1.png)

1. 에서 **[!UICONTROL 액세스 관리]** 창에서 사용자 지정 또는 핵심 데이터 사용 레이블을 선택하여 이 객체에 대한 액세스를 관리합니다.

   코어 데이터 사용 레이블에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. 클릭 **[!UICONTROL 저장]** 레이블 제한을 적용하려면

이 객체에 액세스하려면 사용자가 **[!UICONTROL 레이블]** 포함됨 **[!UICONTROL 역할]**.
예를 들어 C1 레이블이 있는 사용자는 C1에 대해 레이블이 지정되거나 레이블이 지정되지 않은 객체에만 액세스할 수 있습니다.

할당 방법에 대한 자세한 내용 **[!UICONTROL 레이블]** 변환 후 **[!UICONTROL 역할]**&#x200B;를 참조하려면 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
