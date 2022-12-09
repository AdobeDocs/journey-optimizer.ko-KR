---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 만들기
description: Journey Optimizer에서 이메일을 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 이메일 만들기 {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="이메일 만들기"
>abstract="간단한 3단계로 이메일 매개 변수를 정의할 수 있습니다."

에서 이메일을 만들려면 [!DNL Journey Optimizer]를 채우기 위해 아래의 단계를 수행하십시오.

## 여정 또는 캠페인에서 이메일 만들기 {#create-email-journey-campaign}

추가 **[!UICONTROL Email]** 작업을 여정 또는 캠페인에 수행하고 해당 사례에 따라 아래 절차를 따르십시오.

>[!BEGINTABS]

>[!TAB 여정에 이메일 추가]

1. 여정을 연 다음 을(를) 끌어다 놓습니다 **[!UICONTROL Email]** 활동의 **[!UICONTROL Actions]** 섹션에 있는 마지막 항목이 될 필요가 없습니다.

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 제공합니다.

1. 을(를) 선택합니다 [이메일 표면](email-settings.md) 를 사용하십시오.

   ![](assets/email_journey.png)

>[!NOTE]
>
>여정에서 이메일을 보내는 경우 Adobe Journey Optimizer의 전송 시간 최적화 기능을 활용하여 메시지를 보내는 가장 적합한 시간을 예측하여 내역 공개 및 클릭 비율을 기반으로 참여를 극대화할 수 있습니다. [전송 시간 최적화를 사용하는 방법을 알아봅니다](../building-journeys/journeys-message.md#send-time-optimization)

여정을 구성하는 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md).

>[!TAB 캠페인에 이메일 추가]

1. 예약되었거나 API가 트리거된 새 캠페인을 만들고 를 선택합니다. **[!UICONTROL Email]** 를 작업에 사용할 수 있습니다.

1. 을(를) 선택합니다 [이메일 표면](email-settings.md) 를 사용하십시오.

   ![](assets/email_campaign.png)

1. 클릭 **[!UICONTROL Create]**.

1. 캠페인 속성과 같은 이메일 캠페인을 만드는 단계를 완료합니다. [대상자](../segment/about-segments.md), 및 [예약](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

캠페인 구성 방법에 대한 자세한 내용은 [이 페이지](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## 이메일 콘텐츠 정의 {#define-email-content}

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL Edit content]** 전자 메일 콘텐츠를 구성하는 단추입니다. [추가 정보](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. 에서 **[!UICONTROL Header]** 섹션 **[!UICONTROL Edit content]** 화면, **[!UICONTROL From name]**, **[!UICONTROL From email]** 및 **[!UICONTROL BCC]** 필드는 선택한 이메일 화면에서 가져옵니다. [추가 정보](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. 제목 줄을 추가할 수 있습니다. 일반 텍스트를 해당 필드에 직접 입력하거나 [표현식 편집기](../personalization/personalization-build-expressions.md) 제목 줄을 개인화합니다.

1. 을(를) 클릭합니다. **[!UICONTROL Edit email body]** 단추를 사용하여 콘텐츠 작성을 시작합니다. [!DNL Journey Optimizer] 이메일 디자이너. [추가 정보](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. 캠페인에 있는 경우, **[!UICONTROL Code Editor]** 표시되는 팝업 창을 사용하여 고유한 콘텐츠를 일반 HTML로 코딩하는 단추입니다.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >이메일 디자이너를 통해 이미 콘텐츠를 만들거나 가져온 경우에는 이 콘텐츠가 HTML로 표시됩니다.

## 경고 확인 {#check-email-alerts}

메시지를 디자인할 때 주요 설정이 누락되면 인터페이스(화면 오른쪽 상단)에 경고가 표시됩니다.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>이 단추가 표시되지 않으면 경고가 감지되지 않습니다.

시스템에서 선택한 설정 및 요소는 아래에 나와 있습니다. 또한 구성을 조정하여 해당 문제를 해결하는 방법에 대한 정보도 확인할 수 있습니다.

다음 두 가지 유형의 경고가 발생할 수 있습니다.

* **경고** 다음과 같은 권장 사항 및 우수 사례를 참조하십시오.

   * **[!UICONTROL The opt-out link is not present in the email body]**: 이메일 본문에 구독 취소 링크를 추가하는 것이 가장 좋습니다. 에서 구성하는 방법을 알아봅니다 [이 섹션](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >마케팅 유형 이메일 메시지에는 옵트아웃 링크가 포함되어야 하며, 이것은 트랜잭션 메시지에 필요하지 않습니다. 메시지 카테고리(**[!UICONTROL Marketing]** 또는 **[!UICONTROL Transactional]**)가에 정의되어 있습니다. [채널 표면](email-settings.md#email-type) 수준 및 시기 [메시지 만들기](#create-email-journey-campaign) 여정 또는 캠페인에서

   * **[!UICONTROL Text version of HTML is empty]**: HTML 콘텐츠를 표시할 수 없을 때 사용되므로 이메일 본문의 텍스트 버전을 정의하는 것을 잊지 마십시오. 에서 텍스트 버전을 만드는 방법을 알아봅니다. [이 섹션](text-version-email.md).

   * **[!UICONTROL Empty link is present in email body]**: 이메일의 모든 링크가 올바른지 확인합니다. 에서 콘텐츠 및 링크를 관리하는 방법 알아보기 [이 섹션](content-from-scratch.md).

   * **[!UICONTROL Email size has exceeded the limit of 100KB]**: 최적의 전달을 위해 이메일 크기가 100KB를 초과하지 않도록 하십시오. 에서 이메일 콘텐츠를 편집하는 방법 알아보기 [이 섹션](content-from-scratch.md).

* **오류** 다음과 같이 여정/캠페인이 해결되지 않는 한 테스트하거나 활성화할 수 없습니다.

   * **[!UICONTROL The subject line is missing]**: 이메일 제목란은 필수입니다. 에서 정의 및 개인화하는 방법을 알아봅니다 [이 섹션](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL The email version of the message is empty]**: 이 오류는 이메일 컨텐츠가 구성되지 않은 경우 표시됩니다. 에서 이메일 콘텐츠를 디자인하는 방법 알아보기 [이 섹션](get-started-email-design.md).

   * **[!UICONTROL Surface doesn't exist]**: 메시지 생성 후 선택한 서피스가 삭제되면 메시지를 사용할 수 없습니다. 이 오류가 발생하면 메시지에서 다른 서피스를 선택합니다 **[!UICONTROL Properties]**. 의 채널 표면에 대해 자세히 알아보기 [이 섹션](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>이메일을 사용하여 여정/캠페인을 테스트하거나 활성화하려면 모두 해결해야 합니다 **오류** 경고.

## 이메일 미리 보기 및 보내기

메시지 콘텐츠가 정의되면 미리 보기하여 전자 메일 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인할 수 있습니다. [추가 정보](preview.md)

![](assets/email_designer_edit_simulate.png)

이메일이 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md)를 활성화하여 메시지를 보냅니다.

>[!NOTE]
>
>전자 메일 열기 및/또는 상호 작용을 통해 수신자의 동작을 추적하려면 **[!UICONTROL Tracking]** 섹션이 여정의 [이메일 활동](../building-journeys/journeys-message.md) 또는 이메일에서 [campaign](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

