---
solution: Journey Optimizer
product: journey optimizer
title: 다크 모드로 전환
description: 이메일 Designer에서 다크 모드를 사용하는 방법에 대해 알아봅니다.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 다크 모드, 이메일, 색상, 편집기
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: b6f0174b31b4ef317c18644a93a4ae38a712fb36
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 10%

---

# 다크 모드 콘텐츠 관리 {#dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode"
>title="다크 모드로 전환"
>abstract="다크 모드로 전환하면 어떻게 렌더링되는지 미리 보고 특정 사용자 정의 설정을 정의할 수 있습니다. <br>최종 렌더링은 수신자의 이메일 클라이언트에 따라 다릅니다. 모든 이메일 클라이언트가 사용자 정의 다크 모드를 지원하지 않음에 유의하여 주십시오."

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_preview"
>title="다크 모드로 전환"
>abstract="다크 모드로 전환하여 지원되는 이메일 클라이언트에서 어떻게 렌더링되는지 미리 확인합니다. <br>최종 렌더링은 수신자의 이메일 클라이언트에 따라 다릅니다. 모든 이메일 클라이언트가 다크 모드를 지원하지 않음에 유의하여 주십시오."

전자 메일을 디자인할 때 [!DNL Journey Optimizer] [전자 메일 Designer](get-started-email-design.md)을(를) 사용하면 **[!UICONTROL 어두운 모드]** 보기로 전환할 수 있습니다.

이 <!--Email Designer -->다크 모드 보기에서는 다크 모드가 켜져 있을 때 지원 전자 메일 클라이언트가 표시할 특정 사용자 지정 설정을 정의할 수도 있습니다.

<!--When designing your emails, the Journey Optimizer Email Designer allows you to switch to Dark mode where you can define specific custom settings. When dark mode is on, the supporting email clients will display the settings that you defined for this mode.-->

## 다크 모드란? {#what-is-dark-mode}

다양한 이메일 클라이언트에서 다크 모드가 렌더링되는 방식은 복잡합니다. 먼저 어두운 모드를 정의하겠습니다.

다크 모드를 사용하면 지원되는 이메일 클라이언트 및 앱에서 텍스트, 버튼 및 기타 UI 요소에 대해 배경이 어둡고 색상이 밝은 이메일을 표시할 수 있습니다. 눈의 피로를 줄이고, 배터리 수명을 절약하며, 저조도 환경에서 가독성을 향상시켜 보다 편안한 시청 환경을 제공합니다.

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

주요 운영 체제 및 앱<!-- (Apple Mail, Gmail, Outlook, Twitter, Slack)-->에서 증가하는 추세로, 콘텐츠를 읽기 쉽고 시각적으로 모든 사용자에게 어필할 수 있도록 하는 것이 최신 이메일 디자인에서 중요한 고려 사항이 되었습니다.

## 가드레일 {#guardrails}

다크모드 렌더링 측면에서의 기대는 다양한 이메일 클라이언트에서 적용하는 방식이 많이 달라질 수 있어 신중하게 고려해야 한다.

<!--The dark mode final rendering depends on the recipient's email client. It is not possible to guarantee that your email will look the same in dark mode across all devices.-->

[!DNL Journey Optimizer] 전자 메일 Designer에서 다크 모드를 사용하기 전에 기본 전자 메일 클라이언트가 이를 처리하는 방법을 이해하는 것이 중요합니다. 구별해야 할 세 가지 경우가 있습니다.

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

### 클라이언트가 다크 모드를 지원하지 않음 {#not-supporting}

일부 이메일 클라이언트는 다음과 같이 이 기능을 전혀 지원하지 않습니다.

* Yahoo!Mail
* AOL

이메일 Designer에서 다크 모드 사용자 지정 설정을 정의하는지 여부에 관계없이 이러한 이메일 클라이언트에는 다크 모드 렌더링이 표시되지 않습니다. <!--Regardless of whether the interface is in light or dark mode, your email will render the same.-->

### 자체 다크 모드를 적용하는 클라이언트 {#default-support}

일부 이메일 클라이언트는 수신되는 모든 이메일에 대해 자체 기본 다크 모드를 체계적으로 적용합니다. 색상, 배경, 이미지 등 은 이메일 클라이언트별 다크 모드 설정에 따라 자동으로 조정되며, 이는 외부 수정이 불가능함을 의미합니다.

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->

이러한 클라이언트의 예는 다음과 같습니다.

* Gmail(데스크탑 웹 메일, iOS, Android, 모바일 웹 메일)
* 창 보기
* Outlook Windows 메일

이 경우 이메일 Designer에서 사용자 정의 다크 모드 설정을 정의하는 경우 해당 설정은 이메일 클라이언트 설정으로 재정의됩니다.

이러한 이메일 클라이언트가 다크 모드를 처리하지만 특정 다크 모드 디자인은 렌더링되지 않는다는 것을 이해하는 것이 중요합니다.

<!--In this case, the custom settings that you defined in the Email Designer cannot be rendered.-->

<!--Some visual changes may also be caused by the email app or device overriding the original design.-->

### 사용자 정의 다크 모드를 지원하는 클라이언트 {#custom-support}

다른 이메일 클라이언트는 `@media (prefers-color-scheme: dark)` 이메일 Designer에서 사용하는 메서드인 [!DNL Journey Optimizer] 쿼리를 사용하여 사용자 지정 다크 모드를 렌더링하는 옵션을 제공합니다.

다음은 이 옵션을 처리하는 주 클라이언트 목록입니다.

* Apple 메일 macOS
* Apple 메일 iOS
* macOS 보기
* Outlook.com
* iOS 보기
* Android 보기

이 경우 이메일 Designer에서 정의하는 특정 설정이 표시됩니다.

>[!NOTE]
>
>[이 섹션](#define-custom-dark-mode)에서 전자 메일 Designer을 사용하여 사용자 지정 다크 모드 설정을 정의하는 방법을 알아봅니다.

단, 각 이메일 클라이언트에 따라 일부 제한 사항이 적용될 수 있습니다. 예를 들어 Apple Mail 16(macOs 13)과 같은 일부 클라이언트는 이미지가 이메일 콘텐츠에 있는 경우 다크 모드를 생성하지 않습니다.

최적의 결과를 얻으려면 타겟팅하는 이메일 클라이언트로 콘텐츠를 테스트합니다. 각 클라이언트의 최종 결과에 최대한 근접한 시뮬레이션을 보려면 이메일 Designer에서 [이메일 렌더링](../content-management/rendering.md) 옵션을 사용하십시오.

## 이메일 디자이너의 다크 모드 {#dark-mode-email-designer}

이메일 Designer의 다크 모드와 관련하여 두 가지 측면을 고려해야 합니다.

* 대부분의 지원 이메일 클라이언트에서 기본 다크 모드가 어떻게 렌더링될지 미리 볼 수 있습니다. [자세히 알아보기](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* 지원되는 이메일 클라이언트에 대한 기본 설정을 재정의하려면 편집 중인 이메일에 적용되는 사용자 정의 다크 모드 설정을 정의할 수 있습니다. [자세히 알아보기](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### 기본 다크 모드 미리 보기 {#preview-dark-mode}

이메일 Designer에서 다크 모드에 액세스하여 기본 다크 모드 설정을 미리 보려면 아래 단계를 따르십시오.

1. 이메일 Designer 홈 페이지에서 **[!UICONTROL 처음부터 디자인]** 옵션을 선택합니다. [자세히 알아보기](content-from-scratch.md)

<!--Should work with templates and themes, NOT for LP and fragments - but TBC with eng.
    >[!NOTE]
    >
    >Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. 콘텐츠에 [구조체](content-from-scratch.md) 및 [콘텐츠 구성 요소](content-components.md)를 추가하십시오.

1. 중앙 캔버스의 오른쪽 상단에서 전환을 **[!UICONTROL 어두운 모드]**(으)로 전환합니다.

   ![](assets/light-mode-toggle.png)

1. 기본 어두운 모드 미리보기가 표시됩니다.

   ![](assets/dark-mode-default.png)

기본적으로 이메일 Designer 어두운 모드 미리 보기는 이미지와 아이콘을 제외한 모든 요소에 &#39;전체 색상 반전&#39; 색상 스키마를 적용합니다.

밝고 어두운 요소를 가진 영역을 탐지하고 반전시켜 밝은 배경은 어둡게, 어두운 텍스트는 밝게, 어두운 배경은 밝게, 밝은 텍스트는 어두워지게 하는 것을 의미한다.

>[!CAUTION]
>
>최종 렌더링은 수신자의 이메일 클라이언트에 따라 달라질 수 있습니다. 각 전자 메일 클라이언트에 대한 최종 결과에 최대한 가까운 시뮬레이션을 보려면 [전자 메일 렌더링](../content-management/rendering.md) 옵션을 사용하십시오.

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### 사용자 정의 다크 모드 정의 {#define-custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_image"
>title="다크 모드용 특정 이미지 사용"
>abstract="다크 모드가 켜져 있을 때 표시될 다른 이미지를 선택할 수 있습니다. <br>다크 모드용 특정 이미지를 추가해도 모든 이메일 클라이언트에서의 올바른 렌더링을 보장하지는 않습니다. 모든 이메일 클라이언트가 사용자 정의 다크 모드를 지원하지 않음에 유의하여 주십시오."

**[!UICONTROL 어두운 모드]**(으)로 전환한 후에는 받는 사람의 전자 메일 클라이언트에서 어두운 모드가 활성화된 경우에만 표시되는 콘텐츠의 특정 스타일 요소를 편집할 수 있습니다(해당 기능이 지원되는 경우).

>[!WARNING]
>
>다크 모드 최종 렌더링은 각 이메일 클라이언트에 따라 다르므로 결과가 서로 다를 수 있습니다. [자세히 알아보기](#guardrails)

<!--
>[!WARNING]
>
>Not all email clients support dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.-->

이메일 Designer 사용자 지정 다크 모드 스타일을 활용하기 위해 Journey Optimizer에서는 <!-- `@media (prefers-color-scheme: dark)` method-->을(를) 사용합니다. `@media (prefers-color-scheme: dark)` CSS 쿼리로, 사용자의 전자 메일 클라이언트가 어두운 모드로 설정되어 있는지 검색하고 전자 메일에 정의된 어두운 테마 디자인을 적용합니다.

사용자 지정 어두운 모드 설정을 정의하려면 아래 단계를 따르십시오.

1. 이메일 Designer에서 **[!UICONTROL 어두운 모드]** 미리 보기로 전환하세요. [방법 알아보기](#preview-dark-mode)

1. 텍스트, 배경, 단추 등의 모든 스타일 색상 속성을 편집합니다.

1. 이미지와 아이콘의 색상을 변경할 수 없지만 어두운 모드에 대해서만 특정 에셋을 정의할 수 있습니다. 이렇게 하려면 이미지를 선택합니다. **[!UICONTROL 설정]** 창에서 전용 토글을 사용하여 **[!UICONTROL 어두운 모드]**(으)로 전환하고 다른 에셋을 선택하세요.

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. 언제든지 **[!UICONTROL 실시간 보기로 전환]**&#x200B;하여 다양한 장치 크기에서 콘텐츠가 어떻게 렌더링되는지 확인할 수 있습니다. 이 보기에서 화면 상단의 어두운 모드 토글을 선택하여 다른 장치에서 콘텐츠의 어두운 모드 버전을 미리 봅니다.

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >라이브 보기는 다양한 장치 크기에서 렌더링이 어떻게 표시될 수 있는지 비교하도록 설계된 일반 미리 보기입니다. 최종 렌더링은 수신자의 이메일 클라이언트에 따라 달라질 수 있습니다.

1. 다크 모드 변경 사항에 만족하면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하세요.

   ![](assets/dark-mode-simulate.png)

1. **[!UICONTROL 전자 메일 렌더링]**&#x200B;을 선택하고 Litmus 계정에 연결합니다. 다양한 이메일 클라이언트에 대한 최종 다크 모드 렌더링을 볼 수 있습니다. [전자 메일 렌더링](../content-management/rendering.md)에 대해 자세히 알아보세요.

   >[!WARNING]
   >
   >시뮬레이션은 이메일이 다크 모드로 표시되는 방식과 거의 유사하지만 실제 렌더링은 이메일 서비스 공급자 또는 장치 수준 설정의 변경으로 인해 달라질 수 있습니다.

## 모범 사례 {#best-practices}

주요 이메일 클라이언트에서 다크 모드 채택이 증가함에 따라 [사용자 지정 다크 모드](#define-custom-dark-mode)를 사용하는지 여부에 관계없이 밝은 환경과 어두운 환경 모두에서 이메일이 렌더링되는 방식을 고려해야 합니다.

어두운 모드는 색상, 배경 및 이미지를 변경할 수 있으며 디자인 선택 사항을 오버라이드할 수도 있습니다. 시각적 일관성, 접근성 및 브랜드 무결성을 보장하려면 아래 나열된 모범 사례를 따르십시오.

**이미지 및 로고 최적화**

* 어두운 모드에서 흰색 상자가 보이지 않도록 로고와 아이콘을 투명 배경이 있는 PNG로 저장합니다.

* 흰색 또는 밝은 배경이 하드코딩된 이미지를 사용하지 마십시오.

* 투명도가 옵션이 아닌 경우 디자인에서 단색 배경에 이미지를 배치하여 어색한 색상 반전을 방지합니다.

**배경 보기**

* 밝은 모드와 어두운 모드 모두에서 가독성을 위해 텍스트와 배경색 간의 충분한 대비를 보장합니다.

* 중요한 콘텐츠에 배경색에만 의존하지 마십시오. 일부 클라이언트는 어두운 모드에서 배경색을 재정의하므로 키 정보가 계속 표시되는지 확인합니다.

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

**어두운 모드에서 액세스 가능한 콘텐츠 디자인**

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

* 색맹이 있는 사람들을 구별하기 쉬운 색상 조합을 사용하십시오.

* 중간 색조 팔레트를 사용하여 밝은 배경과 어두운 배경의 대비를 보장합니다.

* 높은 대비로 액세스 가능한 색상 조합을 사용하여 가독성을 향상시키고 WCAG(Web Content Accessibility Guidelines) 표준을 충족합니다. WebAIM의 대비 검사기와 같은 도구를 사용하여 색상 대비를 확인합니다.

* 가독성에 영향을 줄 수 있으므로 가는 글꼴을 사용하지 마십시오. 브랜드에 얇은 글꼴이 필요한 경우 어두운 모드에서 굵게 표시합니다.

* 눈의 피로를 유발할 수 있고 일부 이메일 클라이언트가 자동으로 반전시킬 수 있으므로 순수한 검정에서 순수한 흰색을 건너뜁니다.

* 다크 모드가 지원되지 않는 경우 액세스 가능한 대체 스타일을 제공합니다.

**어두운 모드 환경에서 전자 메일 테스트**

* 반전된 색상 구성표를 사용하여 문제를 조기에 발견하는 이메일 Designer의 [어두운 모드 미리 보기](#preview-dark-mode)를 사용하십시오.

* Litmus를 활용하는 [전자 메일 렌더링](../content-management/rendering.md) 옵션을 사용하여 주요 전자 메일 클라이언트(Apple Mail, Gmail, Outlook)의 디자인을 시뮬레이션하고 어두운 모드에서 색상과 이미지가 어떻게 작동하는지 확인합니다.

<!--

## Email clients supporting dark mode {#supporting-email-clients}

Below is a list of the main email clients supporting dark mode using the with the `@media (prefers-color-scheme: dark)` query.

>[!NOTE]
>
>Some versions of these email clients do not support dark mode, so they are also presented in this table for the sake of clarity.

| Email clients supporting custom dark mode| Compatible versions | *Unsupported versions* |
|---------|----------|---------|
| Apple Mail macOS| 12.4, 16.0 | *10.3* |
| Apple Mail iOS | 13.0, 16.1 | *12.2* |
| Outloook macOS | 2019, 16.70, 16.80 | NA |
| Outlook.com | 2019-07, 2022-12 | NA |
| Outloook iOS | 2020-01, 2022-12 | NA |
| Outloook Android | 2023-03 | *2020-01, 2022-12* |

| Other email clients supporting custom dark mode| Compatible versions | *Unsupported versions* |
|---------|----------|---------|
| Samsung Email (Android) | 6.1 | *6.0* |
| Mozilla Thunderbird (macOS) | 68.4 | *60.8, 78.5, 91.13* |
| Fastmail (Desktop Webmail)| 2022-12 | *2021-07* |
| HEY (Desktop Webmail)| 2020-06 | *2022-12* |
| Orange Desktop Webmail| 2019-08, 2021-03, 2022-12, 2024-04 | NA |
| Orange iOS | 2022-12, 2024-04 | *2020-01* |
| Orange Android | 2024-04 | *2020-01, 2022-12* |
| LaPoste.net | 2021-08, 2022-12 | NA |
| SFR  Desktop Webmail | 2019-08, 2022-12 | NA |
| GMX (iOs and Android) | 2022-06 | NA |
| 1&1 (Desktop Webmail and Android) | 2022-06 | NA |
| WEB.DE (iOs and Android) | 2022-06 | NA |
| Free.fr | 2022-12 | NA |

>[!WARNING]
>
>The dark mode final rendering depends on each email client, so results can vary from one to another.

## Email clients not supporting dark mode {#non-supporting-email-clients}

Some email clients allow users to switch their interface to dark mode, but this setting does not affect how HTML emails are displayed.  Here is a list of those clients:

| Main email clients with their own dark mode| 
|---------|
| Gmail (Desktop Webmail, iOS, Android, Mobile Webmail) | 
| Outloook Windows |
| Outlook Windows Mail |

Other email clients do not support dark mode at all:

| Main email clients not supporting dark mode| 
|---------|
| Yahoo!Mail | 
| AOL | 

| Other mail clients not supporting dark mode| 
|---------|
| ProtonMail |
| SFR iOS |
| SFR Android | 
| GMX Desktop Webmail | 
| Mail.ru | 
| WEB.DE Desktop Webmail | 
| T-online.de |

-->