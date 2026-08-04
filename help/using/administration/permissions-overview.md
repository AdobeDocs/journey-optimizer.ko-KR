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
TQID: https://experienceleague.adobe.com/VRUXM-o41h44PxMAKyafwqSHKmduyt48j4sr11Gh-EQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 873
ht-degree: 5%

---

# 액세스 제어 시작 {#permissions-overview}

>[!BEGINSHADEBOX]

**이 페이지에서:** 역할, 권한, 샌드박스, 개체 및 특성 기반 액세스 제어 등 Journey Optimizer의 핵심 액세스 제어 개념을 이해하면 사용자에게 올바른 액세스 권한을 부여하는 방법을 계획할 수 있습니다.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer]을(를) 사용하면 다른 사용자에게 할당된 권한을 정의하고 관리할 수 있습니다. 권한은 제품 내 기능 및 기능에 대한 액세스를 승인 또는 거부하는 권한 및 제한 세트입니다.

[!DNL Adobe CX Enterprise]의 **권한**&#x200B;을 통해 [!DNL Journey Optimizer]에 대한 액세스 제어를 제공합니다. 이 기능은 권한 및 샌드박스를 사용자와 연결하는 역할 및 정책을 활용합니다.

Journey Optimizer에 대한 액세스 제어를 구성하려면 조직에 대한 시스템 또는 제품 관리자 권한이 있어야 합니다. 권한을 부여하거나 철회할 수 있는 최소 역할은 제품 관리자입니다. 권한을 관리할 수 있는 다른 관리자 역할은 시스템 관리자(제한 없음)입니다. 자세한 내용은 관리자 역할에 대한 [Adobe 도움말 센터 문서](https://helpx.adobe.com/enterprise/using/admin-roles.html){target="_blank"}를 참조하십시오.

<!--
 A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.
-->


[!DNL Journey Optimizer]의 사용자 관리는 다음 주요 개념을 기반으로 합니다.

* **[!UICONTROL 역할]**: 역할은 동일한 권한과 샌드박스를 공유하는 사용자 컬렉션을 참조합니다. 이러한 역할을 사용하면 조직 내의 다양한 사용자 그룹에 대한 액세스 및 권한을 쉽게 관리할 수 있습니다. 역할에는 사용자가 인터페이스의 특정 기능이나 개체에 액세스할 수 있도록 하는 통합된 권한(권한) 세트가 포함되어 있습니다.
[!DNL Journey Optimizer]을(를) 사용하면 다양한 수준의 권한을 가진 기존 **[!UICONTROL 역할]** 범위 중에서 선택하여 사용자에게 할당할 수 있습니다. [이 페이지](ootb-product-profiles.md)에서 사용 가능한 **기본 제공 역할**&#x200B;에 대해 자세히 알아보세요.

* **[!UICONTROL 권한]**: 권한은 **[!UICONTROL 역할]**&#x200B;에 할당된 권한을 정의할 수 있는 단일 권한입니다. 각 권한은 [!DNL Journey Optimizer]의 다양한 기능 또는 개체를 나타내는 리소스(예: 여정 또는 오퍼)에 수집됩니다. 자세한 내용은 [권한 수준](high-low-permissions.md) 섹션을 참조하십시오.

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL 샌드박스]**: 가상 샌드박스가 인스턴스를 별도의 격리된 가상 환경으로 분할합니다. 샌드박스는 권한에서 역할을 통해 할당됩니다. [샌드박스 사용](sandboxes.md)에 대해 자세히 알아보세요.

* **개체 기반 액세스 제어**: 개체에 대한 액세스를 제한하는 레이블입니다. 이 접근 방식은 민감한 디지털 자산을 무단 사용자로부터 보호하고 개인 데이터에 대한 보안을 강화합니다. [개체 기반 액세스 관리](object-based-access.md)에 대해 자세히 알아보세요.

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

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** Journey Optimizer의 액세스 제어는 세분화된 데이터 보호를 위해 개체 기반 액세스 제어(OLAC) 및 특성 기반 액세스 제어(ABAC)의 추가 레이어를 사용하여 Adobe CX 엔터프라이즈 권한을 통해 관리되는 역할, 권한 및 샌드박스를 기반으로 합니다.

**의도:**

* 역할, 권한, 샌드박스, 개체 기반 액세스 제어 및 속성 기반 액세스 제어의 5가지 핵심 액세스 제어 개념을 이해합니다
* 액세스 제어를 구성할 수 있는 사용자를 파악합니다(시스템 또는 제품 관리자)
* 각 액세스 제어 주제에 대한 올바른 설명서 섹션으로 이동합니다
* 조직에 대한 액세스 제어 전략 계획

**용어집:**

* **역할**: 동일한 권한과 샌드박스를 공유하는 사용자 컬렉션입니다. 기존 기본 제공 역할을 사용할 수 있으며 사용자 지정 역할을 만들 수 있습니다. *(제품별)*
* **권한**: 여정 또는 오퍼 *(제품별)와 같은 리소스 아래에 그룹화된 역할에 할당된 권한을 정의하는 단일 권한*
* **샌드박스**: Journey Optimizer 인스턴스를 별도의 격리된 가상 작업 공간으로 분할하는 가상 환경, 권한 *(제품별)의 역할을 통해 할당됨*
* **개체 기반 액세스 제어**: 권한이 있는 사용자에 대한 액세스를 제한하기 위해 특정 Journey Optimizer 개체(여정, 캠페인, 오퍼)에 적용되는 레이블 *(제품별)*
* **특성 기반 액세스 제어**: 스키마 필드 또는 세그먼트에 추가된 레이블과 같은 특성을 기반으로 개체 또는 기능에 대한 액세스를 제어하는 정책 *(제품별)*

**보호 기능:**

* 액세스 제어를 구성하려면 시스템 또는 제품 관리자 권한(사전 요구 사항)이 필요합니다
* 권한을 부여하거나 철회할 수 있는 최소 역할은 제품 관리자입니다(페이지에 설명된 대로)

**용어:**

* 정식 이름: 속성 기반 액세스 제어 — 약어: ABAC — 변형: 속성 기반 액세스 관리
* 정식 이름: 객체 기반 액세스 제어 — 약어: OLAC — 변형: 객체 수준 액세스 제어, 객체 기반 액세스 관리
* 혼동하지 마십시오. &quot;개체 기반 액세스 제어&quot;(레이블을 사용하여 여정, 캠페인 및 오퍼와 같은 특정 AJO 개체에 대한 액세스 제한) ≠ &quot;속성 기반 액세스 제어&quot;(레이블 정책을 기반으로 스키마 필드 및 세그먼트와 같은 데이터 속성에 대한 액세스 제한)
* 혼동하지 마십시오. &quot;역할&quot;(공유 권한 및 샌드박스를 가진 사용자 컬렉션)≠ &quot;권한&quot;(역할에 할당된 리소스 아래에 그룹화된 단일 권한)

**FAQ:**

* **Q: Journey Optimizer에서 액세스 제어를 구성할 수 있는 사람은 누구입니까?** — 시스템 관리자 또는 제품 관리자 권한이 있는 사용자
* **Q: 권한을 부여하거나 철회하는 데 필요한 최소 관리자 수준은 무엇입니까?** — 제품 관리자
* **Q: 샌드박스를 역할과 독립적으로 관리합니까?** — 아니요. 샌드박스는 권한 제품에서 역할을 통해 할당됩니다.
* **Q: Journey Optimizer에 대한 액세스 제어는 어디에 있습니까?** — 역할과 정책을 통해 사용자와 권한 및 샌드박스를 연결하는 Adobe CX Enterprise의 권한을 통해.

+++
<!-- ai-accordion-version: 1 | source-hash: 14be1dc6 -->