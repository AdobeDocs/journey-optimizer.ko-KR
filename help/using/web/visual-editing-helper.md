---
title: Visual Editing Helper 확장 기능
description: Journey Optimizer에서 웹 페이지를 작성하고 미리 볼 수 있는 Visual Editing Helper Chrome 확장 기능을 살펴보십시오
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
badge: label="Beta" type="정보"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 18%

---

# Visual Editing Helper 확장 기능 {#visual-editing-helper}

>[!BEGINSHADEBOX]

이 설명서에서 찾을 수 있는 내용:

* [웹 채널 시작하기](get-started-web.md)
* [웹 경험 만들기 ](create-web.md)
* [웹 페이지 작성 ](author-web.md)
* **[Visual Editing Helper 확장 기능](visual-editing-helper.md)**
* [웹 보고 ](web-report.md)

>[!ENDSHADEBOX]

웹 경험을 빠르게 작성하고 미리 보기 위해 Google Chrome용 Adobe Experience Cloud Visual Editing Helper 브라우저 확장 기능을 사용하면 Adobe 내에서 웹 사이트를 안정적으로 로드할 수 있습니다 [!DNL Journey Optimizer] 웹 디자이너.

## Visual Editing Helper 확장 기능 설치 {#install-visual-editing-helper}

Visual Editing Helper 브라우저 확장 기능을 가져와 설치하려면 아래 단계를 따르십시오.

1. Google Chrome 웹 스토어에서 [Adobe Experience Cloud Visual Edit Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 브라우저 확장.

1. **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 기능 추가]**&#x200B;를 클릭합니다.

1. 에서 웹 채널 캠페인 만들기 [!DNL Journey Optimizer]. [방법 알아보기](author-web.md#create-web-campaign)

1. 를 엽니다. [!DNL Journey Optimizer] 웹 디자이너를 사용하십시오. [자세히 알아보기](author-web.md)

1. Chrome 브라우저의 도구 모음에서 해당 아이콘을 클릭하여 Visual Editing Helper 브라우저 확장 기능이 활성화되어 있는지 확인합니다.

   ![](assets/web-visual-editing-extension.png)

이제 웹 사이트에서 웹 사이트를 열 때 Adobe Experience Cloud Visual Editing Helper가 자동으로 활성화됩니다. [!DNL Journey Optimizer] 작성 기능을 제공하는 웹 디자이너입니다.

확장 기능에는 조건부 설정이 없으며 SameSite 쿠키 설정을 포함하여 모든 설정을 자동으로 처리합니다.

>[!NOTE]
>
>일부 웹 사이트는 [!DNL Journey Optimizer] 다음 이유 중 하나로 인한 웹 디자이너:
>
> * 웹 사이트에 엄격한 보안 정책이 있습니다.
> * 웹 사이트가 iframe으로 되어 있습니다.
> * 고객의 QA 또는 스테이지 사이트는 외부에서 사용할 수 없습니다(사이트는 내부 사이트임).


## 문제 해결

Adobe 사용 시 [!DNL Journey Optimizer] 웹 디자이너 로드에 실패한 웹 사이트를 로드하려고 하면 다음을 설치하라는 메시지가 표시됩니다. [Visual Editing Helper 브라우저 확장 기능](#install-visual-editing-helper).

웹 사이트에서 Adobe Experience Platform Web SDK가 아직 구현되지 않은 경우 Visual Editing Helper 브라우저 확장 기능을 설치하고 을 구현하라는 메시지가 웹 디자이너에 표시됩니다. [웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}.

사이트가 로드되지 않거나 예기치 않게 작동하는 경우 Adobe에서 로드하기 전에 브라우저에서 웹 사이트에 있는 쿠키를 수락하는 것이 잠재적 해결책입니다 [!DNL Journey Optimizer].

인증 중인 페이지의 경우 로그인 페이지가 로드되지 않거나 로그인하려고 시도한 후에도 여전히 로그인되지 않은 경우 먼저 브라우저의 다른 탭에 로그인한 다음 Adobe에 웹 사이트를 로드해 보십시오 [!DNL Journey Optimizer] 웹 디자이너.
