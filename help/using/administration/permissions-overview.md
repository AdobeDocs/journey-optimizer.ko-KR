---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 관리 개요
description: 권한 정의 및 관리 방법 알아보기
feature: Access Management
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: 권한, 권한, 제한, 액세스, 샌드박스
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 8%

---

# 액세스 제어 시작 {#permissions-overview}

[!DNL Journey Optimizer]을(를) 사용하면 다른 사용자에게 할당된 권한을 정의하고 관리할 수 있습니다. 권한은 제품 내 기능 및 기능에 대한 액세스를 승인 또는 거부하는 권한 및 제한 세트입니다.

[!DNL Journey Optimizer]에 대한 액세스 제어는 Adobe Experience Cloud의 **권한**&#x200B;을 통해 제공됩니다. 이 기능은 권한 및 샌드박스를 사용자와 연결하는 역할 및 정책을 활용합니다.

Journey Optimizer에 대한 액세스 제어를 구성하려면 조직에 대한 시스템 또는 제품 관리자 권한이 있어야 합니다. 권한을 부여하거나 철회할 수 있는 최소 역할은 제품 관리자입니다. 권한을 관리할 수 있는 다른 관리자 역할은 시스템 관리자(제한 없음)입니다. 자세한 내용은 관리자 역할에 대한 [Adobe 도움말 센터 문서](https://helpx.adobe.com/enterprise/using/admin-roles.html){target="_blank"}를 참조하십시오.

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


[!DNL Journey Optimizer]의 사용자 관리는 다음 주요 개념을 기반으로 합니다.

* **[!UICONTROL 역할]**: 역할은 동일한 권한과 샌드박스를 공유하는 사용자 컬렉션을 참조합니다. 이러한 역할을 사용하면 조직 내의 다양한 사용자 그룹에 대한 액세스 및 권한을 쉽게 관리할 수 있습니다. 역할에는 사용자가 인터페이스의 특정 기능이나 개체에 액세스할 수 있도록 하는 통합된 권한(권한) 세트가 포함되어 있습니다.
[!DNL Journey Optimizer]을(를) 사용하면 다양한 수준의 권한을 가진 기존 **[!UICONTROL 역할]** 범위 중에서 선택하여 사용자에게 할당할 수 있습니다. **이 페이지**&#x200B;에서 사용 가능한 [기본 제공 역할](ootb-product-profiles.md)에 대해 자세히 알아보세요.

* **[!UICONTROL 권한]**: 권한은 **[!UICONTROL 역할]**&#x200B;에 할당된 권한을 정의할 수 있는 단일 권한입니다. 각 권한은 [!DNL Journey Optimizer]의 다양한 기능 또는 개체를 나타내는 리소스(예: 여정 또는 오퍼)에 수집됩니다. 자세한 내용은 [권한 수준](high-low-permissions.md) 섹션을 참조하십시오.

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL 샌드박스]**: 가상 샌드박스가 인스턴스를 별도의 격리된 가상 환경으로 분할합니다. 샌드박스는 권한에서 역할을 통해 할당됩니다. [샌드박스 사용](sandboxes.md)에 대해 자세히 알아보세요.

* **개체 기반 액세스 제어**: 개체에 대한 액세스를 제한하는 레이블입니다. 이 접근 방식은 민감한 디지털 자산을 무단 사용자로부터 보호하여 개인 데이터에 대한 보호 수준을 더욱 강화해 줍니다. [개체 기반 액세스 관리](object-based-access.md)에 대해 자세히 알아보세요.

* **특성 기반 액세스 제어**: 특정 팀이나 사용자 그룹의 데이터 액세스를 관리할 수 있는 권한. 속성 기반 액세스 제어를 통해 관리자는 속성에 따라 특정 객체 및/또는 기능에 대한 액세스를 제어할 수 있습니다. 속성은 스키마 필드 또는 세그먼트에 추가된 레이블과 같이 객체에 추가된 메타데이터일 수 있습니다. 관리자는 사용자 액세스 권한을 관리하기 위해 속성이 포함된 액세스 정책을 정의합니다. [특성 기반 액세스 관리](attribute-based-access.md)에 대해 자세히 알아보세요.


## 더 자세히 알아보기

**[!DNL Journey Optimizer]**&#x200B;의 액세스 제어 개념을 이해했으므로 이러한 문서 섹션을 자세히 살펴봄으로써 권한 구성을 시작할 수 있습니다.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="권한" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>액세스 권한 부여</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="기본 제공 권한" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>기본 제공 권한</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="샌드박스 관리" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>샌드박스 관리</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="속성 기반 액세스 제어" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>특성 기반 액세스 제어</strong></a>
</div>
<p>
</td>
</tr></table>