---
solution: Journey Optimizer
product: journey optimizer
title: 샌드박스 사용 및 할당
description: 샌드박스를 관리하는 방법 알아보기
feature: Sandboxes
topic: Administration
role: Admin, Developer
level: Experienced
keywords: 샌드박스, 가상, 환경, 조직, 플랫폼
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
TQID: https://experienceleague.adobe.com/8vcaHkqHeyoP-TZltCkjpBhvZIifuiPbKy-Whoj74Z8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
subfeature_v2: []
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 919
ht-degree: 12%

---

# 샌드박스 사용 및 할당 {#sandboxes}

>[!BEGINSHADEBOX]

**이 페이지에서:** 샌드박스를 사용하여 Adobe Journey Optimizer 인스턴스를 격리된 환경으로 분할하면 다른 작업에 영향을 주지 않고 프로덕션에서 개발, 테스트 및 실행할 수 있습니다.

>[!ENDSHADEBOX]

**샌드박스**&#x200B;는 개발, 테스트 또는 프로덕션을 위해 Adobe Journey Optimizer 인스턴스를 별도의 격리된 작업 공간으로 분할하는 가상 환경입니다. **관리** > **채널** > **시스템 및 환경 연결**(또는 인터페이스 오른쪽 상단의 샌드박스 전환기를 통해)에서 샌드박스 관리를 찾을 수 있습니다. 샌드박스를 사용하면 안전하게 실험하고, 역할별로 다른 액세스 권한을 할당하고, 콘텐츠를 체계적으로 관리할 수 있습니다. 이 페이지에서는 샌드박스를 사용 및 할당하고, 콘텐츠 액세스를 구성하고, [다른 샌드박스로 개체 내보내기](../configuration/copy-objects-to-sandbox.md) 문서에서 샌드박스 간에 여정과 템플릿을 복사하는 방법을 다룹니다.

## 샌드박스 사용 {#using-sandbox}

[!DNL Journey Optimizer]에서는 인스턴스를 샌드박스라는 별도의 가상 환경으로 분할할 수 있습니다. 샌드박스는 권한에서 역할을 통해 할당됩니다. [샌드박스를 할당하는 방법을 알아봅니다](permissions.md#create-product-profile).

[!DNL Journey Optimizer]은(는) 해당 조직에 대해 만들어진 Adobe Experience Platform 샌드박스를 반영합니다. Adobe Experience Platform 인스턴스에서 Adobe Experience Platform 샌드박스를 만들거나 재설정할 수 있습니다. [자세한 내용은 샌드박스 사용 안내서를 참조하십시오](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=ko-KR){target="_blank"}.

화면 오른쪽 상단의 조직 이름 옆에 샌드박스 전환기 컨트롤이 있습니다. 한 샌드박스에서 다른 샌드박스로 전환하려면 전환기에서 현재 활성 샌드박스를 클릭하고 드롭다운 목록에서 다른 샌드박스를 선택하십시오.

![](assets/sandbox_5.png)

➡️ [이 비디오에서 샌드박스에 대해 자세히 알아보기](#video)

## 샌드박스 할당 {#assign-sandboxes}

>[!IMPORTANT]
>
> 샌드박스 관리는 **[!UICONTROL 제품]** 또는 **[!UICONTROL 시스템]** 관리자만 수행할 수 있습니다.

기본 제공 또는 사용자 지정 **[!UICONTROL 역할]**&#x200B;에 다른 샌드박스를 할당하도록 선택할 수 있습니다.

샌드박스를 할당하려면

1. [!DNL Permissions]의 **[!UICONTROL 역할]** 탭에서 **[!UICONTROL 역할]**&#x200B;을(를) 선택합니다.

   ![](assets/sandbox_1.png)

1. **[!UICONTROL 편집]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 샌드박스]** 리소스 드롭다운에서 역할에 할당할 샌드박스를 선택합니다.

   ![](assets/sandbox_3.png)

1. 필요한 경우 옆에 있는 X 아이콘을 클릭하여 **[!UICONTROL 역할]**&#x200B;에서 샌드박스 액세스를 제거합니다.

   ![](assets/sandbox_4.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 콘텐츠에 액세스 {#content-access}

컨텐츠 액세스 가능성을 구성하려면 각 샌드박스에 컨텐츠 공유 폴더를 할당합니다. 관리자용 [!DNL Admin Console]에 표시된 **[!UICONTROL 저장소]** 탭에서 공유 폴더를 만들고 구성할 수 있습니다. 시스템 관리자로서 [!DNL Admin Console]에 액세스할 수 있는 경우 공유 폴더를 만들고 다른 액세스 수준의 위임자를 공유 폴더에 추가할 수 있습니다.

![](assets/do-not-localize/content_access.png)

콘텐츠가 올바른 샌드박스와 동기화되려면 샌드박스와 동일한 구문을 따라야 합니다. 예를 들어 샌드박스를 &quot;개발&quot;이라고 하는 경우 공유 폴더의 이름은 동일해야 합니다.

[공유 폴더 관리 방법에 대해 알아봅니다](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## 사용 방법 비디오{#video}

샌드박스의 정의, 그리고 개발과 프로덕션 샌드박스를 구분하는 방법을 이해합니다. 샌드박스를 만들고, 재설정하고, 삭제하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3416656?captions=kor&quality=12)

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

- **TL;DR:** 샌드박스는 개발, 테스트 및 프로덕션을 위해 Journey Optimizer 인스턴스를 격리된 가상 작업 공간으로 분할합니다. 샌드박스는 권한 제품의 역할을 통해 사용자에게 할당되며 Admin Console의 공유 폴더를 통해 콘텐츠 액세스가 구성됩니다.

**의도:**

- 샌드박스 전환기를 사용하여 Journey Optimizer 인터페이스에서 샌드박스 간 전환
- 권한 제품의 역할에 하나 이상의 샌드박스 할당
- 역할에서 샌드박스 액세스 제거
- 샌드박스에 대한 콘텐츠 액세스(공유 폴더) 구성
- 샌드박스가 역할 및 권한과 어떤 관련이 있는지 이해할 수 있습니다.

**용어집:**

- **샌드박스**: Journey Optimizer 인스턴스를 개발, 테스트 또는 프로덕션을 위해 별도의 격리된 작업 공간으로 분할하는 가상 환경 *(제품별)*
- **샌드박스 전환기**: 조직 이름 옆의 Journey Optimizer 인터페이스 오른쪽 상단에 있는 컨트롤로 샌드박스 *(제품별) 간에 전환하는 데 사용됨*
- **공유 폴더**: Admin Console에서 콘텐츠 액세스를 허용하는 샌드박스에 대해 구성된 저장소 폴더입니다. 해당 이름은 콘텐츠가 올바르게 동기화되려면 샌드박스 이름과 일치해야 합니다. *(제품별)*

**보호 기능:**

- 샌드박스 관리는 제품 또는 시스템 관리자만 수행할 수 있습니다(페이지의 중요 참고 사항에 명시된 필수 구성 요소)
- 공유 폴더 이름은 콘텐츠에 대한 샌드박스 이름과 동일한 구문을 따라야 합니다(페이지에 설명된 대로)

**용어:**

- 혼동하지 마십시오. &quot;샌드박스 사용&quot;(샌드박스 전환기를 사용하여 UI에서 샌드박스로 전환) ≠ &quot;샌드박스 할당&quot;(권한 제품의 역할에 샌드박스 추가) ≠ &quot;샌드박스 만들기&quot;(Journey Optimizer이 아닌 Adobe Experience Platform에서 수행)
- 이 페이지의 컨텍스트에서 동의어: &quot;sandbox&quot; = &quot;virtual environment&quot;
- 혼동하지 마십시오. &quot;샌드박스 할당&quot;(권한의 역할에 샌드박스 추가) ≠ &quot;샌드박스 관리&quot;(샌드박스 만들기, 재설정 또는 삭제 — Adobe Experience Platform에서 완료)

**FAQ:**

- **Q: Journey Optimizer에서 샌드박스 간을 어떻게 전환합니까?** — 화면 오른쪽 상단의 조직 이름 옆에 있는 샌드박스 전환기를 사용합니다. 활성 샌드박스를 클릭하고 드롭다운 목록에서 다른 샌드박스를 선택합니다.
- **Q: 역할에 샌드박스를 할당할 수 있는 사용자는 누구입니까?** — 제품 또는 시스템 관리자만 사용할 수 있습니다.
- **Q: 사용자가 샌드박스를 어떻게 사용할 수 있습니까?** — 샌드박스는 권한 제품에서 역할을 통해 할당됩니다.
- **Q: 공유 폴더는 어떤 명명 규칙을 따라야 합니까?** — 공유 폴더의 이름이 연결된 샌드박스와 같아야 합니다(예: 샌드박스를 &quot;개발&quot;이라고 하는 경우 공유 폴더도 &quot;개발&quot;이라고 해야 함).

+++
<!-- ai-accordion-version: 1 | source-hash: 0a5ada9b -->