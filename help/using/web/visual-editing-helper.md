---
title: Visual Editing Helper 확장 기능
description: Journey Optimizer에서 웹 페이지를 작성 및 미리 볼 수 있는 Visual Editing Helper Chrome 확장 프로그램을 살펴보십시오
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 01fc9bfba54e9cdbd356c1ed06ef2caeb3705a0a
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 14%

---

# Visual Editing Helper 확장 기능 {#visual-editing-helper}

웹 경험을 빠르게 작성 및 미리 보기 위해 Google Chrome용 Adobe Experience Cloud Visual Editing Helper 브라우저 확장 프로그램을 사용하면 Adobe에서 웹 사이트를 안정적으로 로드할 수 있습니다 [!DNL Journey Optimizer] 웹 디자이너

>[!NOTE]
>
>웹 채널 기능은 현재 베타로 사용되어 사용자만 선택할 수 있습니다.

## Visual Editing Helper 확장 프로그램 설치 {#install-visual-editing-helper}

Visual Editing Helper 브라우저 확장 프로그램을 가져와 설치하려면 아래 단계를 따르십시오.

1. Google Chrome 웹 스토어에서 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 브라우저 확장.

1. **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 기능 추가]**&#x200B;를 클릭합니다.

1. 에서 웹 채널 캠페인 만들기 [!DNL Journey Optimizer]. [방법 알아보기](author-web.md#create-web-campaign)

1. 를 엽니다. [!DNL Journey Optimizer] 웹 디자이너의 웹 경험 작성을 시작합니다. [자세히 알아보기](author-web.md)

1. 해당 아이콘을 클릭하여 Chrome 브라우저의 도구 모음에서 Visual Editing Helper 브라우저 확장 프로그램이 활성화되어 있는지 확인합니다.

   ![](assets/web-visual-editing-extension.png)

이제 웹 사이트가 [!DNL Journey Optimizer] 웹 디자이너의 강력한 저작 기능

확장에는 조건부 설정이 없으며 SameSite 쿠키 설정을 포함하여 모든 설정을 자동으로 처리합니다.

>[!NOTE]
>
>일부 웹 사이트는 [!DNL Journey Optimizer] 다음 이유 중 하나로 인해 웹 디자이너
>
> * 웹 사이트에 엄격한 보안 정책이 있습니다.
> * 웹 사이트가 iframe으로 되어 있습니다.
> * 고객의 QA 또는 스테이지 사이트는 외부에서 사용할 수 없습니다(사이트는 내부 사이트임).


## 문제 해결

Adobe 사용 시 [!DNL Journey Optimizer] 웹 디자이너에 로드하지 못하는 웹 사이트를 로드하려고 하면 설치 메시지가 표시됩니다 [시각적 편집 도우미 브라우저 확장](#install-visual-editing-helper).

웹 사이트에 Adobe Experience Platform Web SDK가 아직 구현되지 않은 경우 웹 디자이너에 Visual Editing Helper 브라우저 확장 프로그램을 설치하고 를 구현하라는 메시지가 표시됩니다 [웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}.

사이트가 로드되지 않거나 예기치 않게 동작하는 경우 Adobe에서 사이트를 로드하기 전에 브라우저에서 웹 사이트의 쿠키를 허용하는 것이 잠재적 수정 사항입니다 [!DNL Journey Optimizer].

인증 중인 페이지의 경우, 로그인 페이지가 로드되지 않거나 로그인 시도 후에도 아직 로그인하지 않은 경우 브라우저의 다른 탭에 먼저 로그인한 다음 Adobe에서 웹 사이트를 로드해 보십시오 [!DNL Journey Optimizer] 웹 디자이너
