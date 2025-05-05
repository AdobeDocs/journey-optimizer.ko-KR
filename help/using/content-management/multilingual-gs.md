---
solution: Journey Optimizer
product: journey optimizer
title: 다국어 콘텐츠 시작
description: Journey Optimizer 다국어 콘텐츠에 대해 자세히 알아보기
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: 시작하기, 시작, 콘텐츠, 실험
exl-id: b57683b4-6dcc-4f6c-a8b2-4ba371d78d21
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 32%

---

# 다국어 콘텐츠 시작 {#multilingual-gs}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_homepage"
>title="번역"
>abstract="다국어 기능을 사용하면 단일 캠페인 또는 여정 내에 여러 언어로 된 콘텐츠를 손쉽게 만들 수 있습니다. 번역 페이지를 통해 프로젝트를 설정하거나 번역 제공자를 선택하거나 로케일별 사전을 관리할 수 있습니다."

다국어 기능을 사용하면 단일 캠페인 또는 여정 내에서 손쉽게 여러 언어로 콘텐츠를 만들 수 있습니다. 이 기능을 사용하면 캠페인을 편집할 때 언어 간에 전환할 수 있으므로 전체 편집 프로세스를 간소화하고 다국어 콘텐츠를 효율적으로 관리할 수 있습니다.

Journey Optimizer을 사용하면 두 가지 서로 다른 방법을 통해 다국어 콘텐츠를 만들 수 있습니다.

* **수동 번역**: 이메일 Designer에서 직접 콘텐츠를 번역하거나 기존 다국어 콘텐츠를 가져옵니다. [자세히 알아보기](multilingual-manual.md)

* **자동 번역**: 자동 번역을 위해 선호하는 언어 공급자에게 콘텐츠를 보냅니다. [자세히 알아보기](multilingual-automated.md)

</br>

![](assets/translation_schema.png)

## 전제 조건 {#prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_error"
>title="번역 오류"
>abstract="번역 페이지에 액세스할 수 없다면 번역 기능이 활성화되어 있지 않기 때문일 수 있습니다. 이 문제를 해결하려면 조직 및 샌드박스 관리자가 번역 기능을 활성화했는지 확인해야 합니다."

Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 독립적으로 서드파티 번역 서비스(기계 번역 또는 사람 번역)를 제공하는 번역 공급업체와 통합됩니다.

선택한 번역 공급업체를 추가하기 전에 해당 공급업체에 계정을 만들어야 합니다.

번역 공급업체의 번역 서비스를 사용하는 경우 해당 공급업체의 추가 약관이 적용됩니다.  타사 솔루션인 번역 서비스는 통합을 통해 Adobe Journey Optimizer 사용자에게 제공됩니다.  Adobe은 타사 제품을 제어하지 않으며 책임도 지지 않습니다.

번역과 관련된 문제 또는 지원 요청은 해당 번역 공급업체에 문의하십시오.

다국어 콘텐츠의 경우 다음 설정을 정의해야 합니다.

* Journey Optimizer에서 번역 기능을 사용하려면 해당 역할에 API를 할당해야 합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/platform-apis/api-authentication#assign-api-to-a-role)

* 다국어 콘텐츠 만들기를 시작하려면 사용자에게 **[!UICONTROL 언어 설정 관리]** 권한이 부여되어야 합니다. 자동 흐름의 경우 사용자는 **[!UICONTROL 번역 서비스]** 기능과 관련된 권한도 필요합니다. [권한에 대해 자세히 알아보기](../administration/permissions.md)

+++ 다국어 관련 권한을 할당하는 방법 알아보기

   1. **권한** 제품에서 **역할** 탭으로 이동하여 원하는 **역할**&#x200B;을 선택하십시오.

   1. 권한을 수정하려면 **편집**&#x200B;을 클릭하십시오.

   1. **번역 서비스** 리소스를 추가한 다음 드롭다운 메뉴에서 적절한 다국어 권한을 선택합니다.

      ![](assets/multilingual-permission.png){zoomable="yes"}

   1. 변경 내용을 적용하려면 **저장**&#x200B;을 클릭하십시오.

      이 역할에 이미 할당된 모든 사용자의 권한은 자동으로 업데이트됩니다.

   1. 새 사용자에게 이 역할을 할당하려면 **역할** 대시보드의 **사용자** 탭으로 이동하여 **사용자 추가**&#x200B;를 클릭하십시오.

   1. 사용자 이름, 이메일 주소를 입력하거나 목록에서 선택한 다음 **저장**&#x200B;을 클릭합니다.

   1. 이전에 사용자를 생성하지 않은 경우 [이 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/abac/permissions-ui/users)를 참조하십시오.

+++

* 번역 페이지에 액세스할 수 없는 경우 번역 기능을 활성화하고 **[!UICONTROL 번역 서비스]** 관련 권한을 부여해야 합니다. [자세히 알아보기](../administration/ootb-permissions.md)

+++ 번역 기능 활성화 방법 알아보기

   1. 다음 오류 페이지가 표시되면 **[!UICONTROL 번역]** 기능이 아직 활성화되지 않았음을 나타냅니다. 액세스를 요청하려면 조직 및 샌드박스 관리자에게 문의하십시오.

  ![](assets/multi-troubleshoot.png)

   1. 관리자가 왼쪽 사이드바의 **[!UICONTROL 번역]** 메뉴로 이동해야 합니다.

      번역 기능이 자동으로 활성화됩니다.

   1. 기능을 활성화하면 **[!UICONTROL 프로젝트]**, **[!UICONTROL 공급자]** 및 **[!UICONTROL 로케일]** 탭과 함께 **[!UICONTROL 번역]** 페이지에 액세스할 수 있습니다.

   1. 이 절차가 실패해도 동일한 오류 페이지가 표시됩니다. 이 경우 추가 지원이 필요한 경우 Adobe 담당자에게 문의하십시오.

+++

## 사용 방법 비디오 {#video}

단일 캠페인 또는 여정 내에서 여러 언어로 콘텐츠를 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3430921/)
