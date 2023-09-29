---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 및 역할 관리
description: 사용자 및 역할 관리 방법 알아보기
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: 제품, 프로필, 샌드박스
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 6%

---

# 사용자 및 역할 관리 {#manage-permissions}

>[!IMPORTANT]
>
> 아래에 자세히 설명된 각 절차는 다음에서만 수행할 수 있습니다. **[!UICONTROL 제품]** 또는 **[!UICONTROL 시스템]** 관리자.

**[!UICONTROL 역할]** 동일한 권한 및 샌드박스를 공유하는 사용자 컬렉션을 참조하십시오. 이러한 역할을 사용하면 조직 내의 다양한 사용자 그룹에 대한 액세스 및 권한을 쉽게 관리할 수 있습니다.

포함 [!DNL Journey Optimizer] product, you have to choose선택 from a range범위 of existing기존 **[!UICONTROL 역할]**&#x200B;을 조정할 때 반드시 필요합니다. 사용 가능한 항목에 대한 자세한 정보 **[!UICONTROL 역할]**, 다음을 참조하십시오. [페이지](ootb-product-profiles.md).

사용자가 다음에 속할 때 **[!UICONTROL 역할]**, 제품 내에 포함된 Adobe 앱 및 서비스에 대한 액세스 권한이 부여됩니다.

기존 역할이 조직의 특정 요구 사항을 충족하지 않는 경우 사용자 지정을 만들 수도 있습니다 **[!UICONTROL 역할]** 를 사용하여 인터페이스의 특정 기능이나 개체에 대한 액세스를 미세 조정할 수 있습니다. 이렇게 하면 각 사용자가 작업을 효율적으로 수행하는 데 필요한 리소스 및 도구에만 액세스할 수 있습니다.

## 역할 할당 {#assigning-role}

기본 제공 또는 사용자 지정을 지정하도록 선택할 수 있습니다. **[!UICONTROL 역할]** (으)로 가져왔습니다.

권한이 할당된 모든 기본 역할 목록은 [기본 제공 역할](ootb-product-profiles.md) 섹션.

를 할당하려면 **[!UICONTROL 역할]**:

1. 에서 사용자에게 역할을 할당하려면 다음을 수행하십시오. [!DNL Permissions] product에서 **[!UICONTROL 역할]** 을(를) 탭하고 원하는 역할을 선택합니다.

   ![](assets/do-not-localize/access_control_2.png)

1. 다음에서 **[!UICONTROL 사용자]** 탭을 클릭하고 **[!UICONTROL 사용자 추가]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 사용자 이름 또는 이메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**.

   사용자가에서 이전에 생성된 적이 없는 경우 [!DNL Admin Console]을(를) 참조하십시오. [사용자 설명서 추가](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html).

   ![](assets/do-not-localize/access_control_4.png)

그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

사용자 관리에 대한 자세한 내용은 [액세스 제어 설명서](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=ko).

인스턴스에 액세스하면에 할당된 권한에 따라 사용자에게 특정 보기가 표시됩니다 **[!UICONTROL 역할]**. 사용자에게 기능에 대한 올바른 액세스 권한이 없는 경우 다음 메시지가 표시됩니다.

`You don't have permission to access this feature. Permission needed: XX.`

## 기존 역할 편집 {#edit-product-profile}

기본 제공 또는 사용자 정의 **[!UICONTROL 역할]**, 언제든지 권한을 추가하거나 삭제할지 결정할 수 있습니다.

이 예제에서는 를 추가합니다 **[!UICONTROL 권한]** 관련 항목: **[!UICONTROL 여정]** 여정 뷰어에 할당된 사용자용 리소스 **[!UICONTROL 역할]**. 그러면 사용자는 여정을 게시할 수 있습니다.

기본 제공 또는 사용자 지정을 수정하는 경우 **[!UICONTROL 역할]**, 이는 이에 할당된 모든 사용자에게 영향을 줍니다. **[!UICONTROL 역할]**.

1. 에서 사용자에게 역할을 할당하려면 다음을 수행하십시오. [!DNL Permissions] product에서 **[!UICONTROL 역할]** 여정 뷰어에서 원하는 역할을 탭하고 선택합니다. **[!UICONTROL 역할]**.
   ![](assets/do-not-localize/access_control_5.png)

1. 출처: **[!UICONTROL 역할]** 대시보드, 클릭 **[!UICONTROL 편집]**.

   ![](assets/do-not-localize/access_control_6.png)

1. 다음 **[!UICONTROL 리소스]** 메뉴에 적용되는 리소스 목록이 표시됩니다 **[!UICONTROL Experience Cloud - 플랫폼 기반 애플리케이션]** 제품. 리소스를 드래그 앤 드롭하여 권한을 할당합니다.

   다음에서 **[!UICONTROL 여정]** 리소스 드롭다운에서 게시 여정을 선택합니다. **[!UICONTROL 권한]**.

   ![](assets/do-not-localize/access_control_14.png)

1. 필요한 경우 **[!UICONTROL 포함된 권한 항목]**&#x200B;에 있는 X 아이콘을 클릭하여 역할에 대한 권한 또는 리소스를 제거합니다.

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

필요한 경우 특정 권한을 사용하여 새 역할을 만들 수도 있습니다. 자세한 내용은 다음을 참조하십시오. [새 역할 만들기](#create-product-profile).

## 새 역할 만들기 {#create-product-profile}

[!DNL Journey Optimizer] 을(를) 통해 나만의 고유한 **[!UICONTROL 역할]** 및 에서는 사용 권한 집합 및 샌드박스를 사용자에게 할당합니다. 포함 **[!UICONTROL 역할]**, 인터페이스에서 특정 기능 또는 개체에 대한 액세스를 승인하거나 거부할 수 있습니다.

샌드박스를 만들고 관리하는 방법에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=ko-KR){target="_blank"}.

이 예제에서는 다음과 같은 역할을 생성하겠습니다. **여정 읽기 전용** 여기서 여정 기능에 읽기 전용 권한을 부여합니다. 사용자는 여정에 액세스하고 볼 수만 있고 와 같은 다른 기능에 액세스할 수 없습니다. **[!DNL  Decision management]** 위치: [!DNL Journey Optimizer].

을(를) 만들려면 **여정 읽기 전용** **[!UICONTROL 역할]**:

1. 에서 사용자에게 역할을 할당하려면 다음을 수행하십시오. [!DNL Permissions] product에서 **[!UICONTROL 역할]** tab 키를 누른 다음 클릭 **[!UICONTROL 역할 만들기]**.

   ![](assets/do-not-localize/access_control_9.png)

1. 추가 **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]** 새 항목 **[!UICONTROL 역할]**. 그런 다음 을 클릭합니다. **[!UICONTROL 확인]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 다음에서 **[!UICONTROL 샌드박스]** 리소스 드롭다운에서 원하는 샌드박스를 **[!UICONTROL 역할]**. [샌드박스에 대한 자세한 내용을 살펴보십시오](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. 다음과 같은 여러 리소스 중에서 선택합니다. **[!DNL Journeys]**, **[!DNL Segments]** 또는 **[!DNL Decision management]** 다음에서 사용 가능 [!DNL Journey Optimizer] 왼쪽 메뉴에 나열됩니다.

   여기에서 **[!UICONTROL 여정]** 리소스.

   ![](assets/do-not-localize/access_control_11.png)

1. 다음에서 **[!UICONTROL 여정]** 드롭다운에서 다음에 할당할 권한을 선택합니다. **[!UICONTROL 역할]**.

   여기 선택 **[!DNL View journeys]**, **[!DNL View journeys report]**  및 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

사용자 **[!UICONTROL 역할]** 이제 이(가) 생성되고 구성되었습니다. 이제 사용자에게 할당합니다.

역할 생성 및 관리에 대한 자세한 내용은 [Admin Console 설명서](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html).
