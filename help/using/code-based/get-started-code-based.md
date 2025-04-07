---
title: 코드 기반 경험 시작
description: Journey Optimizer의 코드 기반 경험에 대해 알아보기
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 98%

---

# 코드 기반 채널 시작 {#get-sarted-code-based}

[!DNL Journey Optimizer]을(를) 사용하면 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV 연결 장치, 스마트 TV, 키오스크, ATM, 음성 지원, IoT 장치 등과 같은 모든 터치포인트에서 고객에게 제공할 경험을 개인화하고 테스트할 수 있습니다.

**코드 기반 경험** 기능을 사용하면 간단하고 직관적인 비시각적 편집기를 사용하여 인바운드 경험을 정의할 수 있습니다. 전체 콘텐츠에 수정 사항을 적용하는 대신 사용 중인 애플리케이션 유형에 관계없이 앱이나 웹 페이지의 개별적이고 더 세분화된 위치에 특정 요소를 삽입하고 편집할 수 있습니다.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>코드 기반 경험에 대한 특정 권장 사항은 [이 페이지](code-based-prerequisites.md)에 자세히 설명되어 있습니다.


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="리드" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>작동 방식</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="유효성 검사" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>가드레일 및 사전 지식</strong></a>
</div>
<p>
</td>
<td>
<a href="code-based-configuration.md">
<img alt="유효성 검사" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>코드 기반 채널 구성</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="드물게" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>코드 기반 경험 만들기</strong></a>
</div>
<p></td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ 콘텐츠 실험을 사용하여 의사 결정을 코드 기반 경험 채널과 비교하는 방법을 보여주는 엔드투엔드 사용 사례가 [이 섹션](../experience-decisioning/experience-decisioning-uc.md)에 나와 있습니다.

## 코드 기반 채널과 기타 채널을 사용할 경우 비교 {#code-based-vs-other-channels}

### 코드 기반 채널과 기타 채널 비교

기타 [!DNL Journey Optimizer] 채널 대신 코드 기반 채널을 언제 사용합니까?

* 웹 브라우저나 모바일 앱을 통해 디지털 속성에 액세스하지 않는 경우 언제든지 코드 기반 경험 사용을 고려할 수 있습니다. 이 경우 [!DNL Journey Optimizer] [웹 채널](../web/get-started-web.md){target="_blank"}또는 [!DNL Journey Optimizer] [인앱 메시징](../in-app/get-started-in-app.md){target="_blank"} 채널을 사용하는 것이 더 좋을 수 있습니다.

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* API 기반, 헤드리스 또는 서버측 구현이 있는 경우 [!DNL Journey Optimizer] 웹 또는 인앱 채널 대신 코드 기반 채널을 사용할 수 있습니다.

* 모달, 팝업 또는 오버레이를 표시하지 않고 기본 앱 내의 콘텐츠를 수정하려는 경우 기본 모바일 애플리케이션의 코드 기반 채널을 인앱 채널 대신 활용할 수도 있습니다.

### 코드 기반 채널과 웹 채널 비교 {#code-based-vs-web}

웹 사용 사례를 실행하기 위해 웹 채널이나 코드 기반 경험을 사용할 수 있지만, 상황에 따라 하나가 다른 것보다 더 적합할 수 있습니다. 언제 무엇을 사용할지 결정하는 데 필요한 정보를 확인할 수 있도록 주요 차이점이 아래에 나열되어 있습니다.

**웹**

* [웹 디자이너](../web/web-visual-editor.md){target="_blank"} 시각적 편집기 또는 웹 [비시각적 편집기](../web/web-non-visual-editor.md)를 사용하여 콘텐츠를 편집합니다.
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}(클라이언트측 구현)가 필요합니다.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* 웹 채널에서는 페이지의 모든 내용을 수정할 수 있으며 변경할 수 있는 사전 정의된 작업 목록이 있습니다. [자세히 알아보기](../web/web-visual-editor.md){target="_blank"}
* 쉽게 설정하고 빠르게 진행할 수 있습니다.
* 마케팅 담당자 중심입니다.

**코드 기반 경험**

* [개인화 편집기](create-code-based.md#edit-code)를 사용하여 콘텐츠를 편집합니다.
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}(클라이언트측 구현) 또는 [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=ko-KR){target="_blank"}(서버측 구현)가 필요합니다.
* 코드 기반 경험에서는 구현에 대해 기존 개발 작업이 필요합니다. 이는 애플리케이션이 [!DNL Journey Optimizer]에서 해당 위치에 대해 Edge로 게시된 콘텐츠를 해석 및 게재할 수 있게 하기 위해서입니다. [자세히 알아보기](code-based-surface.md)
* 더 많은 계획이 필요하고 개발자가 지정하는 사항만 변경할 수 있습니다. 따라서 개인화 또는 테스트를 위해 수정해야 하는 애플리케이션의 구성 요소(홈 배너, 히어로 이미지, 메뉴 표시줄 등)를 식별하고 개발 팀과 협력하여 이러한 변경 사항을 처리하는 데 필요한 구현을 구축하는 것이 중요합니다.
* JSON 코드 콘텐츠를 사용할 수 있습니다.
* 개발자에 초점을 맞춥니다.

## 작동 방식 {#how-it-works}

>[!CAUTION]
>
>이 기능은 개발자 및/또는 숙련된 사용자를 위한 것입니다. 개발 팀에서 채널 구성과 초기 설정을 처리하면 약간의 코드 작성 기술을 갖춘 마케팅 담당자가 이 기능을 사용할 수 있습니다.

[!DNL Journey Optimizer] 코드 기반 경험 기능을 사용하여 콘텐츠를 편집하려면 페이지 또는 앱을 계측해야 합니다. 이렇게 하려면 콘텐츠를 삽입하거나 바꾸려는 특정 개별 위치(&quot;[표면](code-based-surface.md)&quot;이라고 함)를 미리 선언해야 합니다.

>[!NOTE]
>
>현재 구성과 연결된 콘텐츠는 HTML 또는 JSON으로만 설정할 수 있습니다. 

코드 기반 경험을 만들고 게재하는 주요 단계는 다음과 같습니다.

1. 채널별 사전 요구 사항을 준수해야 합니다. [자세히 알아보기](code-based-prerequisites.md)

1. 애플리케이션 구현에서 [표면](code-based-surface.md#surface-definition)을 정의합니다. 표면이란 환경을 추가할 위치입니다.

1. 해당 위치를 참조하는 코드 기반 채널 구성을 만듭니다. [방법 알아보기](code-based-configuration.md#create-code-based-configuration)

1. [!DNL Journey Optimizer]에서 이 구성을 사용하여 여정 또는 캠페인을 만듭니다. [방법 알아보기](create-code-based.md#create-code-based-campaign)

1. [!DNL Journey Optimizer] 개인화 편집기로 선택한 구성에 대한 콘텐츠를 지정하여 경험을 만듭니다. [방법 알아보기](create-code-based.md#edit-code)

1. 코드 기반 경험을 테스트합니다. [방법 알아보기](test-code-based.md)

1. 게시합니다. [방법 알아보기](publish-code-based.md)

1. 코드 기반 경험 여정 또는 캠페인이 시작된 후 콘텐츠를 검색하고 표시하려면 표면에 표시할 콘텐츠를 요청하는 앱 또는 페이지 구현이 있어야 합니다.

   >[!INFO]
   >
   >이를 위해 앱 구현 팀은 “배너 텍스트” 또는 “권장 사항 트레이 1”과 같이 코드 기반 구성에서 정의된 표면에 사용할 콘텐츠나, “검색 알고리즘 매개변수”와 같이 애플리케이션의 UI 관련이 아닌 결정 지점에 사용할 콘텐츠를 가져오기 위해 명시적 API 또는 SDK 호출을 수행합니다. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [자세히 알아보기](code-based-implementation-samples.md)

