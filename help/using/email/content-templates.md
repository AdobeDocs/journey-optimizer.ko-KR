---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 템플릿 만들기
description: Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하기 위해 템플릿을 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# 콘텐츠 템플릿 만들기 {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="콘텐츠 템플릿 만들기"
>abstract="독립형 템플릿을 만들어 여정 및 캠페인에서 콘텐츠를 재결합합니다."

액세스 가능하고 향상된 디자인 프로세스를 위해 독립형 템플릿을 만들어 전체 사용자 지정 컨텐츠를 쉽게 재사용할 수 있습니다 [!DNL Journey Optimizer] 캠페인 및 여정.

이 기능을 사용하면 컨텐츠 중심 사용자가 캠페인 또는 여정 외부의 템플릿에서 작업할 수 있습니다. 그런 다음 마케팅 사용자는 고유한 여정 또는 캠페인 내에서 이러한 독립형 컨텐츠 템플릿을 재사용하고 조정할 수 있습니다.

>[!CAUTION]
>
>컨텐츠 템플릿을 작성, 편집 및 삭제하려면 **[!DNL Manage Library Items]** 에 포함된 권한 **[!DNL Content Library Manager]** 제품 프로필 . [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

예를 들어 회사 내의 사용자는 컨텐츠만 담당하므로 캠페인이나 여정에 액세스할 수 없습니다. 그러나 이 사용자는 조직의 마케터가 모든 이메일에서 시작점으로 사용할 수 있도록 선택할 수 있는 이메일 템플릿을 만들 수 있습니다.

>[!NOTE]
>
>* 컨텐츠 템플릿에 대한 변경 사항은 라이브든 초안이든 캠페인 또는 여정에 전파되지 않습니다.
>
>* 마찬가지로, 캠페인이나 여정에서 템플릿을 사용할 경우 캠페인 및 여정 콘텐츠를 편집한 내용은 이전에 사용한 컨텐츠 템플릿에 영향을 주지 않습니다.


➡️ [이 비디오에서 템플릿을 만들고 사용하는 방법을 알아봅니다](#video-templates)

컨텐츠 템플릿을 만들려면 아래 단계를 수행하십시오.

1. 컨텐츠 템플릿 목록에 액세스하려면 다음을 선택합니다 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 콘텐츠 템플릿]** 왼쪽 메뉴에서 를 클릭합니다.

   ![](assets/content-template-list.png)

1. 여정, 캠페인 또는 **[!UICONTROL 콘텐츠 템플릿]** 메뉴 - 표시됩니다.

   >[!NOTE]
   >
   >만들기 또는 수정 날짜별로 콘텐츠 템플릿을 정렬할 수 있습니다.

1. 선택 **[!UICONTROL 템플릿 만들기]**.

1. 템플릿 세부 사항을 입력합니다.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >현재 **이메일** channel 및 **HTML** 유형이 지원됩니다.

1. 템플릿에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다 **[!UICONTROL 액세스 관리]**. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보기](../administration/object-based-access.md).

1. 클릭 **[!UICONTROL 만들기]** 다음 옵션을 사용하여 전자 메일을 디자인할 방법을 선택합니다.

   * **[!UICONTROL 처음부터 디자인]**
   * **[!UICONTROL 직접 코드 작성]**
   * **[!UICONTROL 가져오기 HTML]**
   * **[!UICONTROL 디자인 템플릿 선택]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >템플릿을 선택하면 다음 중 하나를 선택할 수 있습니다 **[!UICONTROL 샘플 템플릿]**, 기본 이메일 템플릿 및 **[!UICONTROL 저장된 템플릿]**- 여정, 캠페인 또는 **[!UICONTROL 콘텐츠 템플릿]** 메뉴 아래의 제품에서 사용할 수 있습니다. [자세히 알아보기](email-templates.md#save-as-template)

1. 이메일 디자이너가 표시됩니다. 선택한 옵션에 따라 여정 또는 캠페인 내의 모든 이메일에 대해 수행하는 것과 동일한 방식으로 필요에 따라 컨텐츠를 편집합니다.

   * [이메일 디자인 기초](content-from-scratch.md) 디자이너의 인터페이스를 통해 [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [원시 HTML 코드 또는 복사-붙여넣기](code-content.md) 이메일 디자이너에 바로 연결할 수 있습니다.

   * [기존 HTML 콘텐츠 가져오기](existing-content.md) 파일 또는 .zip 폴더에서 사용할 수 있습니다.

   * [기존 콘텐츠 사용](email-templates.md) 기본 제공 또는 사용자 지정 템플릿 목록에서 을 선택합니다.

   ![](assets/content-template-designer.png)

1. 클릭 **[!UICONTROL 컨텐츠 시뮬레이션]** 전자 메일 렌더링을 확인합니다. 데스크탑 또는 모바일 보기를 선택할 수 있습니다. [자세히 알아보기](preview.md)

   >[!CAUTION]
   >
   >컨텐츠를 시뮬레이션하려면 **[!DNL Manage Simulate Content]** 에 포함된 권한 **[!DNL Content Library Manager]** 제품 프로필 . [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. 콘텐츠를 테스트하고 여정 또는 캠페인에서 사용하기 전에 일부 내부 사용자가 승인하도록 증명을 보낼 수 있습니다.

   * 이렇게 하려면 **[!UICONTROL 증명 보내기]** 버튼을 클릭하고 [이 섹션](preview.md#send-proofs).

   * 증명을 보내기 전에 [이메일 표면](../configuration/channel-surfaces.md) 콘텐츠를 테스트하는 데 사용됩니다.

      ![](assets/content-template-stimulate-proof-surface.png)

1. 템플릿을 준비하고 나면 **[!UICONTROL 저장]**.

1. 필요한 경우 템플릿 이름 옆에 있는 화살표를 클릭하여 로 돌아갑니다. **[!UICONTROL 세부 사항]** 템플릿을 화면 및 편집합니다.

   ![](assets/content-template-designer-back.png)

1. 이제 작성할 때 이 콘텐츠 템플릿을 사용할 수 있습니다 [이메일](get-started-email-design.md) within [!DNL Journey Optimizer]. 추가 정보 [저장된 템플릿 사용](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## 방법 비디오{#video-templates}

에서 콘텐츠 템플릿을 작성, 편집 및 사용하는 방법을 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)