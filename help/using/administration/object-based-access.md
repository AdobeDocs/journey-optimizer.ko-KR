---
solution: Journey Optimizer
product: journey optimizer
title: 오브젝트 수준 액세스 제어
description: 다양한 객체에 대한 데이터 액세스를 관리하기 위한 권한을 정의할 수 있는 객체 수준 액세스 제어에 대해 알아봅니다
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 객체, 레벨, 액세스, 제어, 레이블, olac, 인증
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 6%

---

# 오브젝트 수준 액세스 제어 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="액세스 관리 레이블"
>abstract="액세스 레이블에 따라 이 캠페인에 대한 액세스를 제한할 수 있습니다. 액세스 제한을 추가하려면 이 페이지 상단의 **액세스 관리** 단추를 찾아보십시오. 사용 권한이 있는 레이블만 선택해야 합니다."

OLAC(객체 수준 액세스 제어) 기능을 사용하면 다양한 객체에 대한 데이터 액세스를 관리할 권한을 정의할 수 있습니다.

* 여정
* Campaign
* 템플릿
* 조각
* 랜딩 페이지
* 오퍼
* 정적 오퍼 컬렉션
* 오퍼 결정
* 채널 구성
* IP 준비 계획

그 목적은 개인 데이터를 더 이상 보호할 수 있도록 권한이 없는 사용자로부터 민감한 디지털 자산을 보호하는 것입니다.

## 전제 조건 {#prereq-labels}

[레이블을 만들기](#create-labels)하려면 **[!UICONTROL 사용 레이블 관리]** 권한이 있는 역할에 속해야 합니다.

[레이블을 할당](#assign-labels)하려면 **관리** 권한(예: [!DNL Manage journeys], [!DNL Manage Campaigns] 또는 [!DNL Manage decisions])이 있는 역할의 일부여야 합니다. 이 권한이 없으면 **[!UICONTROL 액세스 관리]** 단추가 회색으로 표시됩니다.

[이 섹션](../administration/permissions.md)에서 권한에 대해 자세히 알아보십시오.

## 레이블 만들기 {#create-labels}

**[!UICONTROL 레이블]**&#x200B;을 통해 해당 데이터에 적용되는 사용 정책에 따라 데이터 세트와 필드를 분류할 수 있습니다. 언제든지 **[!UICONTROL 레이블]**&#x200B;을 적용할 수 있으므로 데이터를 관리하는 방법을 유연하게 선택할 수 있습니다.

레이블을 사용하여 사용자에게 액세스 권한을 제공하고 데이터 거버넌스 및 동의 정책을 적용합니다. 이러한 거버넌스 레이블은 다운스트림 소비에 영향을 줄 수 있습니다.

[!DNL Permissions] 제품에서 레이블을 만들 수 있습니다. 자세한 정보는 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}를 참조하세요.

Journey Optimizer에서 직접 **[!UICONTROL 레이블]**&#x200B;을 만들 수도 있습니다. 레이블을 만들려면 다음 단계를 수행합니다.

1. 새로 만든 **[!UICONTROL Campaign]**&#x200B;인 Adobe Journey Optimizer 개체에서 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다.

   ![](assets/olac_1.png)

1. **[!UICONTROL 액세스 관리]** 창에서 **[!UICONTROL 레이블 만들기]**&#x200B;를 클릭합니다.

   ![](assets/olac_2.png)

1. 레이블을 구성합니다. 다음을 지정해야 합니다.
   * **[!UICONTROL 이름]**
   * **[!UICONTROL 친숙한 이름]**
   * **[!UICONTROL 설명]**

   ![](assets/olac_3.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하여 **[!UICONTROL 레이블]**&#x200B;을(를) 저장합니다.

새로 만든 **[!UICONTROL 레이블]**&#x200B;을(를) 이제 목록에서 사용할 수 있습니다. 필요한 경우 [!DNL Permissions] 제품에서 수정할 수 있습니다.

## 레이블 할당 {#assign-labels}

Journey Optimizer 개체에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 수행하십시오.

1. 새로 만든 **[!UICONTROL Campaign]**&#x200B;인 Adobe Journey Optimizer 개체에서 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다.

   ![](assets/olac_1.png)

1. **[!UICONTROL 액세스 관리]** 창에서 이 개체에 대한 액세스를 관리할 사용자 지정 또는 핵심 데이터 사용 레이블을 선택합니다.

   핵심 데이터 사용 레이블에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html){target="_blank"}를 참조하세요.

   ![](assets/olac_4.png)

1. 이 레이블 제한을 적용하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하십시오.

이 개체에 액세스하려면 사용자가 **[!UICONTROL 역할]**&#x200B;에 특정 **[!UICONTROL 레이블]**을(를) 포함해야 합니다.
예를 들어 C1 레이블이 있는 사용자는 레이블이 지정되거나 레이블이 지정되지 않은 C1에만 액세스할 수 있습니다.

**[!UICONTROL 역할]**&#x200B;에 **[!UICONTROL 레이블]**&#x200B;을(를) 할당하는 방법에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}를 참조하세요.