---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 템플릿 만들기
description: 템플릿을 만들어 Journey Optimizer 캠페인 및 여정에서 콘텐츠를 재사용하는 방법에 대해 알아봅니다
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 14%

---


# 콘텐츠 템플릿 만들기 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="자신만의 콘텐츠 템플릿 정의"
>abstract="여러 여정과 캠페인 전반에서 콘텐츠를 재사용할 수 있도록 처음부터 독립형 사용자 정의 템플릿을 만듭니다."

다음 두 가지 방법으로 콘텐츠 템플릿을 만들 수 있습니다.

* 왼쪽 레일을 사용하여 처음부터 콘텐츠 템플릿 만들기 **[!UICONTROL 콘텐츠 템플릿]** 메뉴 아래의 제품에서 사용할 수 있습니다. [방법 알아보기](#create-template-from-scratch)

* 캠페인 또는 여정 내에서 콘텐츠를 디자인할 때 템플릿으로 저장합니다. [방법 알아보기](#save-as-template)

저장되면 콘텐츠 템플릿을 캠페인이나 여정에서 사용할 수 있습니다. 처음부터 만들거나 이전 콘텐츠에서 만들었든 이제 내에서 콘텐츠를 작성할 때 이 템플릿을 사용할 수 있습니다. [!DNL Journey Optimizer]. [방법 알아보기](#use-content-templates)

>[!NOTE]
>
>* 컨텐츠 템플릿에 대한 변경 사항은 라이브 또는 초안 여부에 관계없이 캠페인이나 여정에 전파되지 않습니다.
>
>* 마찬가지로 캠페인이나 여정에서 템플릿을 사용하는 경우 캠페인 및 여정 컨텐츠에 대한 편집 내용은 이전에 사용한 컨텐츠 템플릿에 영향을 주지 않습니다.

## 처음부터 템플릿 만들기 {#create-template-from-scratch}

처음부터 콘텐츠 템플릿을 만들려면 아래 단계를 수행하십시오.

1. 다음을 통해 콘텐츠 템플릿 목록에 액세스 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 콘텐츠 템플릿]** 왼쪽 메뉴.

1. 선택 **[!UICONTROL 템플릿 만들기]**.

1. 템플릿 세부 정보를 입력하고 원하는 채널을 선택합니다.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >현재 웹을 제외한 모든 채널을 사용할 수 있습니다.

1. 선택 **[!UICONTROL 유형]** 선택한 채널용입니다.

   ![](assets/content-template-type.png)

   * 대상 **[!UICONTROL 이메일]**&#x200B;을 선택하는 경우 **[!UICONTROL 콘텐츠]**, 다음을 정의할 수 있습니다. [제목 줄](../email/create-email.md#define-email-content) 을 템플릿의 일부로 사용하십시오. 다음을 선택하는 경우 **[!UICONTROL HTML]**, 이메일 본문의 콘텐츠만 정의할 수 있습니다.

   * 대상 **[!UICONTROL SMS]**, **[!UICONTROL 푸시]**, **[!UICONTROL 인앱]** 및 **[!UICONTROL 다이렉트 메일]**&#x200B;현재 채널에는 기본 유형만 사용할 수 있습니다. 그래도 선택해야 합니다.

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **[!UICONTROL 태그]** 검색을 개선하기 위해 템플릿을 분류하는 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 템플릿에 할당하려면 다음을 선택할 수 있습니다. **[!UICONTROL 액세스 관리]**. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md).

1. 클릭 **[!UICONTROL 만들기]** 선택한 채널에 따라 여정 또는 캠페인 내의 모든 콘텐츠에 대해 수행하는 것과 동일한 방식으로 콘텐츠를 디자인할 수 있습니다.

   ![](assets/content-template-edition.png)

   다음 섹션에서 다양한 채널에 대한 콘텐츠를 만드는 방법을 알아봅니다.
   * [이메일 콘텐츠 정의](../email/get-started-email-design.md)
   * [푸시 콘텐츠 정의](../push/design-push.md)
   * [SMS 콘텐츠 정의](../sms/create-sms.md#sms-content)
   * [DM 콘텐츠 정의](../direct-mail/create-direct-mail.md)
   * [인앱 콘텐츠 정의](../in-app/design-in-app.md)

1. 다음을 만드는 경우 **[!UICONTROL 이메일]** 이 있는 템플릿 **[!UICONTROL HTML]** 을 입력하면 콘텐츠를 테스트할 수 있습니다. [방법 알아보기](#test-template)

1. 템플릿이 준비되면 **[!UICONTROL 저장]**.

1. 템플릿 이름 옆에 있는 화살표를 클릭하여 로 돌아갑니다. **[!UICONTROL 세부 사항]** 화면.

   ![](assets/content-template-back.png)

이제 이 템플릿을 사용하여 내에서 콘텐츠를 작성할 수 있습니다. [!DNL Journey Optimizer]. [방법 알아보기](#use-content-templates)

## 콘텐츠를 콘텐츠 템플릿으로 저장 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="메시지를 마이그레이션하는 방법에 대해 알아보기"
>abstract="2022년 7월 25일 메시지 메뉴가 사라졌고 이제 여정에서 직접 메시지를 작성합니다. 여정에서 기존 메시지를 재사용하려면 템플릿으로 저장해야 합니다."

캠페인이나 여정에서 콘텐츠를 디자인할 때 나중에 다시 사용할 수 있도록 저장할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. 메시지에서 **[!UICONTROL 콘텐츠 편집]** 화면에서 **[!UICONTROL 콘텐츠 템플릿]** 단추를 클릭합니다.

1. 선택 **[!UICONTROL 콘텐츠 템플릿으로 저장]** 드롭다운 메뉴에서 을(를) 선택합니다.

   ![](assets/content-template-button-save.png)

   다음에 있는 경우 [이메일 Designer](../email/get-started-email-design.md)에서 이 옵션을 선택할 수도 있습니다. **[!UICONTROL 자세히]** 화면 오른쪽 위의 드롭다운 목록입니다.

   ![](assets/content-template-more-button-save.png)

1. 이 템플릿의 이름과 설명을 추가합니다.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >현재 채널 및 유형은 자동으로 채워지며 편집할 수 없습니다. 에서 만든 이메일 템플릿 [이메일 Designer](../email/get-started-email-design.md), **[!UICONTROL HTML]** 유형이 자동으로 선택됩니다.

1. 에서 Adobe Experience Platform 태그를 선택하거나 만듭니다. **태그** 템플릿을 분류할 필드입니다. [자세히 알아보기](../start/search-filter-categorize.md#tags)

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 템플릿에 할당하려면 다음을 선택할 수 있습니다. **[!UICONTROL 액세스 관리]**. [자세히 알아보기](../administration/object-based-access.md).

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 템플릿이 **[!UICONTROL 콘텐츠 템플릿]** 목록, 액세스 가능 [!DNL Journey Optimizer] 전용 메뉴. 이 템플릿은 목록에 있는 다른 항목으로 액세스, 편집 및 삭제할 수 있는 독립 실행형 콘텐츠 템플릿이 됩니다. [자세히 알아보기](#access-manage-templates)

이제 내에서 콘텐츠를 작성할 때 이 템플릿을 사용할 수 있습니다. [!DNL Journey Optimizer]. [방법 알아보기](#use-content-templates)

>[!NOTE]
>
>새 템플릿에 대한 변경 사항은 원래 콘텐츠에는 전파되지 않습니다. 마찬가지로 원본 컨텐츠가 해당 컨텐츠 내에서 편집되는 경우 새 템플릿은 수정되지 않습니다.
