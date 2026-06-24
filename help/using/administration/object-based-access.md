---
solution: Journey Optimizer
product: journey optimizer
title: 오브젝트 수준 액세스 제어
description: 다양한 객체에 대한 데이터 액세스를 관리하기 위한 권한을 정의할 수 있는 객체 수준 액세스 제어에 대해 알아봅니다
feature: Access Management
topic: Administration
role: Admin, Developer
level: Experienced
keywords: 객체, 레벨, 액세스, 제어, 레이블, olac, 인증
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
feature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: []
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1017
ht-degree: 10%

---

# 오브젝트 수준 액세스 제어 {#object-level-access}

>[!BEGINSHADEBOX]

**이 페이지에서:** 개체 수준 액세스 제어를 사용하여 액세스 레이블이 있는 여정, 캠페인 및 오퍼와 같은 개별 개체를 제한하면 중요한 콘텐츠와 개인 데이터를 인증된 사용자로 제한할 수 있습니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="액세스 관리 레이블"
>abstract="액세스 레이블에 따라 오브젝트에 대한 액세스를 제한할 수 있습니다. 이 접근 방식은 민감한 디지털 자산을 무단 사용자로부터 보호하고 개인 데이터에 대한 보안을 강화합니다. **반드시 권한이 부여된 레이블만 선택하십시오.**"

액세스 레이블에 따라 오브젝트에 대한 액세스를 제한할 수 있습니다. 이 접근 방식은 민감한 디지털 자산을 무단 사용자로부터 보호하고 개인 데이터에 대한 보안을 강화합니다.

OLAC(객체 수준 액세스 제어) 기능을 사용하면 객체 선택에 대한 데이터 액세스를 관리할 권한을 정의할 수 있습니다.

* 여정
* 캠페인
* 템플릿
* 조각
* 랜딩 페이지
* 오퍼
* 정적 오퍼 컬렉션
* 오퍼 결정
* 채널 구성
* IP 준비 계획


## 사전 요구 사항 {#prereq-labels}

[레이블을 만들기](#create-labels)하려면 **[!UICONTROL 사용 레이블 관리]** 권한이 있는 역할에 속해야 합니다.

[레이블을 할당](#assign-labels)하려면 **관리** 권한(예: [!DNL Manage journeys], [!DNL Manage Campaigns] 또는 [!DNL Manage decisions])이 있는 역할에 속해야 합니다. 이 권한이 없으면 **[!UICONTROL 액세스 관리]** 단추가 회색으로 표시됩니다.

[이 섹션](../administration/permissions.md)에서 권한에 대해 자세히 알아보십시오.

## 레이블 만들기 {#create-labels}

**[!UICONTROL 레이블]**&#x200B;을 통해 해당 데이터에 적용되는 사용 정책에 따라 데이터 세트와 필드를 분류할 수 있습니다. 언제든지 **[!UICONTROL 레이블]**&#x200B;을 적용할 수 있으므로 데이터 관리 방법을 유연하게 사용할 수 있습니다.

레이블을 사용하여 사용자에게 액세스 권한을 제공하고 데이터 거버넌스 및 동의 정책을 시행합니다. 이러한 거버넌스 레이블은 다운스트림 소비에 영향을 줄 수 있습니다.

[!DNL Permissions] 제품에서 레이블을 만들 수 있습니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}를 참조하세요.

Journey Optimizer에서 직접 **[!UICONTROL 레이블]**&#x200B;을 만들 수도 있습니다. 레이블을 만들려면 다음 단계를 수행합니다.

1. 새로 만든 **[!UICONTROL Campaign]**&#x200B;과(와) 같은 Adobe Journey Optimizer 개체에서 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다.

   ![Adobe Journey Optimizer의 액세스 관리 단추](assets/olac_1.png)

1. **[!UICONTROL 액세스 관리]** 창에서 **[!UICONTROL 레이블 만들기]**&#x200B;를 클릭합니다.

   ![](assets/olac_2.png)

1. 레이블을 구성합니다. 다음을 지정해야 합니다.

   * **[!UICONTROL 이름]**
   * **[!UICONTROL 친숙한 이름]**
   * **[!UICONTROL 설명]**

   ![레이블 구성 필드](assets/olac_3.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭하여 **[!UICONTROL 레이블]**&#x200B;을(를) 저장합니다.

새로 만든 **[!UICONTROL 레이블]**&#x200B;을(를) 이제 목록에서 사용할 수 있습니다. 필요한 경우 [!DNL Permissions] 제품에서 수정할 수 있습니다.

## 레이블 할당 {#assign-labels}

Journey Optimizer 개체에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 수행하십시오.

1. 새로 만든 **[!UICONTROL Campaign]**&#x200B;과(와) 같은 Adobe Journey Optimizer 개체에서 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다.

   ![Adobe Journey Optimizer의 액세스 관리 단추](assets/olac_1.png)

1. **[!UICONTROL 액세스 관리]** 창에서 이 개체에 대한 액세스를 관리할 사용자 지정 또는 핵심 데이터 사용 레이블을 선택합니다.

   핵심 데이터 사용 레이블에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html){target="_blank"}를 참조하세요.

   ![](assets/olac_4.png)

1. 이 레이블 제한을 적용하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하십시오.

이 개체에 액세스하려면 사용자의 **[!UICONTROL 역할]**&#x200B;에 특정 **[!UICONTROL 레이블]**&#x200B;이 포함되어 있어야 합니다. 예를 들어 C1 레이블이 있는 사용자는 C1 레이블이 있거나 레이블이 지정되지 않은 개체에만 액세스할 수 있습니다.

**[!UICONTROL 역할]**&#x200B;에 **[!UICONTROL 레이블]**&#x200B;을(를) 할당하는 방법에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}를 참조하세요.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 개체 수준 액세스 제어(OLAC)를 사용하면 여정, 캠페인, 오퍼와 같은 특정 Journey Optimizer 개체에 액세스 레이블을 적용할 수 있으므로 일치하는 레이블을 가진 사용자만 해당 개체를 보거나 상호 작용할 수 있습니다.

**의도:**

* Journey Optimizer에서 직접 또는 권한 제품을 통해 사용자 지정 액세스 레이블 만들기
* Journey Optimizer 개체(여정, 캠페인, 오퍼 등)에 액세스 레이블 지정
* 인증된 사용자만 중요 콘텐츠를 제한합니다.
* 레이블을 만들고 할당하는 데 필요한 권한 이해

**용어집:**

* **OLAC(개체 수준 액세스 제어)**: 특정 Journey Optimizer 개체 *(제품별) 선택에 대한 데이터 액세스를 관리할 권한을 정의하는 기능*
* **레이블**: 사용 정책별로 분류하고 역할 멤버십 *(제품별)에 따라 액세스를 제한하기 위해 개체에 적용되는 태그*
* **액세스 관리**: 액세스 레이블 *(제품별)을(를) 만들고 할당하기 위해 지원되는 Journey Optimizer 개체에서 사용할 수 있는 단추나 인터페이스*
* **핵심 데이터 사용 레이블**: 조직 *(제품별)에서 만든 사용자 지정 레이블이 아닌 Adobe Experience Platform에서 제공하는 사전 정의된 레이블입니다*

**보호 기능:**

* 레이블을 만들려면 **사용 레이블 관리** 권한(필수 구성 요소)이 필요합니다.
* 레이블을 할당하려면 개체 유형(예: 여정 관리, 캠페인 관리 또는 의사 결정 관리)에 대한 **관리** 권한이 필요합니다. 이 권한이 없으면 **액세스 관리** 단추가 회색으로 표시됩니다(필수 조건)
* OLAC 레이블에 대해 지원되는 개체: 여정, 캠페인, 템플릿, 조각, 랜딩 페이지, 오퍼, 정적 오퍼 컬렉션, 오퍼 결정, 채널 구성, IP 웜업 계획

**용어:**

* 정식 이름: 객체 수준 액세스 제어 — 약어: OLAC — 변형: 객체 기반 액세스 제어, 객체 기반 액세스 관리
* 혼동하지 마십시오: OLAC(레이블을 사용하여 여정 및 캠페인과 같은 특정 AJO 오브젝트에 대한 액세스 제한) ≠ ABAC(속성 기반, 플랫폼 수준에서 스키마 필드, 데이터 세트 및 대상에 레이블 정책을 적용)
* 혼동하지 마십시오. &quot;핵심 데이터 사용 레이블&quot;(Adobe Experience Platform에서 사전 빌드된 레이블) ≠ &quot;사용자 지정 레이블&quot;(조직에서 만든 레이블)

**FAQ:**

* **Q: 권한 제품으로 이동하지 않고 Journey Optimizer에서 직접 레이블을 만들 수 있습니까?** — 예. 지원되는 객체에 대해 액세스 관리 창을 사용하고 레이블 생성을 누릅니다.
* **Q: OLAC 레이블을 지원하는 개체 유형은 무엇입니까?** — 여정, 캠페인, 템플릿, 조각, 랜딩 페이지, 오퍼, 정적 오퍼 컬렉션, 오퍼 의사 결정, 채널 구성 및 IP 웜업 계획.
* **Q: 여정에 레이블을 할당하는 데 필요한 권한은 무엇입니까?** — 여정 관리 권한. 관리 권한이 없으면 액세스 관리 버튼이 회색으로 표시됩니다.
* **Q: 사용자의 역할에 C1 레이블만 있는 경우 액세스할 수 있는 개체는 무엇입니까?** — C1 레이블이 지정되거나 레이블이 지정되지 않은 객체만 해당됩니다.

+++
<!-- ai-accordion-version: 1 | source-hash: 4e9b2577 -->
