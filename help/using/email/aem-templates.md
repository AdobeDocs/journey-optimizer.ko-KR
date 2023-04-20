---
solution: Journey Optimizer
product: journey optimizer
title: AEM 템플릿으로 작업
description: AEM에서 템플릿을 만들어 Journey Optimizer으로 내보내는 방법을 알아봅니다
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Advertising"
exl-id: e4935129-c1cb-41b1-b84d-cd419053c303
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 2%

---

# Adobe Experience Manager 템플릿으로 작업 {#aem-templates}

>[!AVAILABILITY]
>
>Adobe Experience Manager과의 통합을 현재 베타로 사용하여 사용자만 선택할 수 있습니다.
> 베타 사용자는 [이 양식](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} 피드백을 공유하려면 다음을 수행하십시오.

Adobe Journey Optimizer을 사용하면 Adobe Experience Manager 사이트를 통해 맞춤형 메시지를 만들 수 있습니다. 먼저 Adobe Experience Manager의 콘텐츠 소스를 사용하여 템플릿을 디자인한 다음 Adobe Journey Optimizer으로 보냅니다. 공유되면 Adobe Journey Optimizer의 이메일 디자이너에서 이러한 템플릿에 액세스하여 원하는 대상에게 메시지를 만들고 보내는 프로세스를 단순화할 수 있습니다.

## 사전 요구 사항 {#prerequisites}

이 기능 사용을 시작하기 전에 다음 요구 사항을 충족하는지 확인하십시오.

* **Experience Manager 설정**

   이 기능은 [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   베타 프로그램의 일부로, Cloud Service 구성은 Adobe Experience Manager의 Adobe에서 Adobe Journey Optimizer에 연결하기 위해 수행됩니다.

* **권한**

   Adobe Journey Optimizer에서 컨텐츠 템플릿을 생성, 편집 및 삭제하려면 **[!DNL Manage Library Items]** 에 포함된 권한 **[!DNL Content Library Manager]** 제품 프로필 . [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

## 보호 및 제한 사항{#aem-templates-limitations}

Adobe Journey Optimizer으로 Adobe Experience Manager의 사용을 추가로 최적화하려면 다음과 같은 추가 보호 및 제한 사항을 알고 있어야 합니다.

* Experience Manager 템플릿의 개인화를 효과적으로 사용하려면 적절한 Journey Optimizer 구문이 필요합니다. [자세히 알아보기](../personalization/personalization-syntax.md)

* 벌크 템플릿 내보내기는 현재 지원되지 않으므로 개별적으로 내보내야 합니다.

* 현재 Experience Manager과 Journey Optimizer 간 동기화를 사용할 수 없습니다. Journey Optimizer으로 보낸 후 Experience Manager 템플릿이 변경되면 사용자는 템플릿을 다시 내보내고 Journey Optimizer으로 다시 보내야 합니다.

## Journey Optimizer으로 템플릿 보내기{#aem-templates-send}

Adobe Experience Manager 템플릿을 Adobe Journey Optimizer으로 내보내려면 아래 단계를 수행하십시오.

1. Adobe Experience Manager 홈페이지에서 **[!UICONTROL 아웃바운드 마케팅]**.

   ![](assets/aem-outbound-menu.png)

1. 콘텐츠 라이브러리에서 이전에 구성한 템플릿을 사용하거나 처음부터 만들 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. Journey Optimizer 개인화 구문을 템플릿에 포함함으로써 사용자 지정 기능을 향상시킬 수 있습니다. [자세히 알아보기](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. Journey Optimizer으로 내보낼 템플릿을 선택하고 을(를) 클릭합니다 **[!UICONTROL 보내기]** 고급 메뉴에서 을 클릭합니다.

   ![](assets/aem-advanced-menu.png)

1. 을(를) 입력합니다. **[!UICONTROL 이름]** 컨텐츠 템플릿 중에서 **[!UICONTROL 샌드박스]**.

   ![](assets/aem-send-template-settings.png)

1. 을(를) 클릭한 후 **[!UICONTROL 보내기]** 버튼을 누르면 내보내기 프로세스가 시작됩니다. 내보내기가 완료되면 사용자 인터페이스에 다음 메시지가 표시됩니다. &quot;템플릿 &quot;XX&quot;가 AJO로 성공적으로 전송되었습니다.&quot;

선택한 샌드박스의 Adobe Journey Optimizer 컨텐츠 템플릿에 템플릿이 추가됩니다.

## Adobe Experience Manager 템플릿 사용 및 개인화{#aem-templates-perso}

Experience Manager 템플릿을 Journey Optimizer에서 컨텐츠 템플릿으로 사용할 수 있게 되면 개인화를 포함하여 이메일에 필요한 컨텐츠를 식별하고 통합할 수 있습니다.

1. Journey Optimizer에서 **[!UICONTROL 컨텐츠 템플릿]** 메뉴에서 가져온 템플릿에 액세스합니다.

   ![](assets/aem_ajo_1.png)

1. 을 클릭하여 **[!UICONTROL 경고]** 버튼을 클릭하면 중요한 설정이 누락되었는지 신속하게 확인할 수 있습니다. 이렇게 하면 메시지가 제대로 구성되었는지 확인하고 잠재적인 오류나 문제를 방지할 수 있습니다.

   ![](assets/aem_ajo_2.png)

1. 에서 **[!UICONTROL 템플릿 속성]** 창에서 **[!UICONTROL 액세스 관리]** 사용자 지정 또는 코어 데이터 사용 레이블을 템플릿에 할당하는 단추. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보기](../administration/object-based-access.md)

1. Experience Manager 템플릿을 추가로 개인화하고 콘텐츠에 사용자 지정 개인화를 추가하려면 **[!UICONTROL 컨텐츠 편집]**. 이를 통해 손쉽게 변경하고 템플릿을 특정 요구에 맞게 조정할 수 있습니다. [자세히 알아보기](get-started-email-design.md)

   >[!NOTE]
   >
   > 템플릿을 편집하고 개인화하려면 호환성 모드만 사용할 수 있습니다.

1. 컨텐츠 템플릿이 준비되면 [테스트 및 유효성 검사](content-templates.md#test-template).

1. 컨텐츠가 정의되면, **[!UICONTROL 저장된 템플릿]** 컬렉션. 그런 다음 **[!UICONTROL 이 템플릿 사용]**.

   ![](assets/aem_ajo_3.png)

1. 이제 콘텐츠를 편집하고 개인화할 수 있습니다. 이메일 콘텐츠를 빌드하는 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. Experience Manager 템플릿에 개인화된 콘텐츠를 추가한 경우 **[!UICONTROL 컨텐츠 시뮬레이션]** 테스트 프로필을 사용하여 메시지에 표시되는 방법을 미리 봅니다.

[미리 보기 및 테스트 프로필에 대해 자세히 알아보기](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. 메시지 미리 보기를 볼 때 개인화된 모든 요소는 선택한 테스트 프로필의 해당 데이터로 자동 교체됩니다.

   필요한 경우 **[!UICONTROL 테스트 프로필 관리]** 버튼을 클릭합니다.

   ![](assets/aem_ajo_7.png)

이메일이 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md)를 활성화하여 메시지를 보냅니다.
