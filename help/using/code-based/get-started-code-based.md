---
title: 코드 기반 경험 시작
description: Journey Optimizer의 코드 기반 경험에 대해 알아보기
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: d2ac4dfe40559f01db59e314e8838f51b39a8659
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 81%

---

# 코드 기반 채널 시작 {#get-sarted-code-based}

[!DNL Journey Optimizer]을(를) 사용하면 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV 연결 장치, 스마트 TV, 키오스크, ATM, 음성 지원, IoT 장치 등과 같은 모든 터치포인트에서 고객에게 제공할 경험을 개인화하고 테스트할 수 있습니다.

**코드 기반 경험** 기능을 사용하면 간단하고 직관적인 비시각적 편집기를 사용하여 인바운드 경험을 정의할 수 있습니다. 전체 콘텐츠에 수정 사항을 적용하는 대신 사용 중인 애플리케이션 유형에 관계없이 앱이나 웹 페이지의 개별적이고 더 세분화된 위치에 특정 요소를 삽입하고 편집할 수 있습니다.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!NOTE]
>
>* 코드 기반 경험을 처음 만드는 경우 다음에 설명된 전제 조건을 따라야 합니다 [이 섹션](code-based-prerequisites.md).
>
>* 현재 위치 [!DNL Journey Optimizer] 다음을 사용하여 코드 기반 경험만 만들 수 있습니다. **캠페인**.
>
>* 코드 기반 경험 채널은 **사용할 수 없음** Adobe을 구입한 조직의 경우 **헬스케어 실드** 및 **개인 정보 보호 및 보안 보호** 추가 기능 제공.

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
<a href="code-based-prerequisites.md"><strong>보호 기능 및 사전 요구 사항</strong></a>
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
<td>
<a href="code-based-implementation-samples.md">
<img alt="유효성 검사" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>구현 샘플</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## 코드 기반 채널과 기타 채널을 사용할 경우 비교 {#code-based-vs-other-channels}

### 코드 기반 채널과 기타 채널 비교

기타 [!DNL Journey Optimizer] 채널 대신 코드 기반 채널을 언제 사용합니까?

* 웹 브라우저나 모바일 앱을 통해 디지털 속성에 액세스하지 않는 경우 언제든지 코드 기반 경험 사용을 고려할 수 있습니다. 이 경우 [!DNL Journey Optimizer] [웹 채널](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} 채널을 사용하는 것이 더 좋을 수 있습니다. 

* 웹 채널의 시각적 작성을 지원하는 [웹 디자이너](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"}에 웹 사이트를 로드할 수 없는 경우 [!DNL Journey Optimizer] 웹 채널 대신 코드 기반 채널을 사용할 수 있습니다.

* API 기반, 헤드리스 또는 서버 측 구현이 있는 경우 [!DNL Journey Optimizer] 웹 또는 인앱 채널 대신 코드 기반 채널을 사용할 수도 있습니다.

### 코드 기반 채널과 웹 채널 비교

웹 사용 사례를 실행하기 위해 웹 채널이나 코드 기반 경험을 사용할 수 있지만, 상황에 따라 하나가 다른 것보다 더 적합할 수 있습니다. 주요 차이점은 아래에 나열되어 있으므로 언제 무엇을 사용할지에 대한 올바른 결정을 내릴 수 있습니다.

**웹**
* [웹 디자이너](../web/edit-web-content.md#work-with-web-designer){target="_blank"} 시각적 편집기를 사용하여 콘텐츠를 편집합니다.
* [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}가 필요합니다.
* 웹 채널에서는 페이지의 모든 내용을 수정할 수 있으며 변경할 수 있는 사전 정의된 작업 목록이 있습니다. [자세히 알아보기](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* 쉽게 설정하고 빠르게 진행할 수 있습니다.
* 마케팅 담당자 중심입니다.

**코드 기반 경험**
* [표현식 편집기](create-code-based.md#edit-code)를 사용하여 콘텐츠를 편집합니다.
* 코드 기반 경험에서는 표면이 이러한 표면에 대해 [!DNL Journey Optimizer]에 의해 에지에 게시된 콘텐츠를 해석하고 전달할 수 있는지 확인하기 위해 구현에 대한 이전 개발 작업이 필요합니다. [자세히 알아보기](#surface-definition)
* 더 많은 계획이 필요하고 개발자가 지정하는 사항만 변경할 수 있습니다. 따라서 개인화 또는 테스트를 위해 수정해야 하는 표면의 구성 요소(홈 배너, 히어로 이미지, 메뉴 표시줄 등)를 식별하고 개발 팀과 협력하여 이러한 변경 사항을 처리하는 데 필요한 구현을 구축하는 것이 중요합니다.
* JSON 코드 콘텐츠를 사용할 수 있습니다.
* 개발자에 초점을 맞춥니다.

## 작동 방식 {#how-it-works}

>[!CAUTION]
>
>이 기능은 개발자 및/또는 숙련된 사용자를 위한 것입니다. 개발 팀에서 표면 구현과 초기 설정을 처리하는 한 코드 작성 기술을 갖춘 마케팅 담당자가 사용할 수 있습니다.

[!DNL Journey Optimizer] 코드 기반 경험 기능을 사용하여 콘텐츠를 편집하려면 페이지 또는 앱을 계측해야 합니다. 이렇게 하려면 콘텐츠를 삽입하거나 바꾸려는 특정 개별 위치(“[표면](#surface-definition)”이라고 함)를 미리 선언해야 합니다<!--HOW??-->.

>[!NOTE]
>
>현재 표면과 연결된 콘텐츠는 HTML 또는 JSON일 수 있습니다. <!--WILL COME LATER: text, image or another format depending on the application-->

코드 기반 캠페인을 구현하는 주요 단계는 다음과 같습니다.

1. 기본적으로 코드 기반 경험을 추가하려는 위치인 [표면](#surface-definition)을 정의하고 이 표면을 사용하여 [!DNL Journey Optimizer]에서 캠페인을 만듭니다. [방법 알아보기](create-code-based.md#create-code-based-campaign)

1. [!DNL Journey Optimizer] 표현식 편집기를 사용하여 선택한 표면에 대한 콘텐츠를 지정하여 경험을 구성하십시오. [방법 알아보기](create-code-based.md#edit-code)

1. 앱 구현 팀은 “배너 텍스트” 또는 “권장 사항 트레이 1”과 같은 이름이 지정된 표면에 대한 콘텐츠나 “검색 알고리즘 매개변수”와 같은 애플리케이션의 비UI 관련 결정 지점에 대한 콘텐츠를 가져오기 위해 명시적 API 또는 SDK 호출을 수행합니다. 이 경우 구현 팀은 반환된 콘텐츠를 렌더링하거나 해석하고 그에 따라 조치를 취할 책임이 있습니다.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## 표면이란 무엇입니까? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="코드 기반 경험 표면 정의"
>abstract="코드 기반 표면은 사용자 또는 시스템 상호 작용을 위해 설계된 엔티티로 URI를 통해 고유하게 식별됩니다."

**코드 기반 경험 표면**&#x200B;은 **URI**&#x200B;로 고유하게 식별되는 사용자 또는 시스템 상호 작용<!--ask Robert to explain further-->을 위해 설계된 모든 엔티티입니다.

다시 말해, 표면은 존재하는 엔티티(터치포인트)가 있는 모든 계층 구조 수준의 컨테이너로 볼 수 있습니다.<!--good idea to illustrate how it can be seen, but to clarify-->

* 웹 페이지, 모바일 앱, 데스크탑 앱, 더 큰 엔티티 내의 특정 콘텐츠 위치(예: `div`) 또는 비표준 표시 패턴(예: 키오스크 또는 데스크탑 앱 배너)일 수 있습니다.<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 또한 비표시 또는 추상화된 표시 목적을 위해 특정 콘텐츠 컨테이너 조각으로 확장할 수도 있습니다(예: 서비스로 제공되는 JSON Blob).

* 또한 다양한 클라이언트 표면 정의와 일치하는 와일드카드 표면일 수도 있습니다. 예를 들어 웹 사이트의 모든 페이지에 있는 히어로 이미지 위치는 web://mydomain.com/*#hero_image 와 같은 표면 URI로 변환될 수 있습니다.

기본적으로 표면 URI는 여러 섹션으로 구성됩니다.
1. **유형**: 웹, 모바일 앱, atm, 키오스크, tvcd, 서비스 등
1. **속성**: 페이지 URL 또는 앱 번들
1. **컨테이너**: 페이지/앱 활동의 위치

아래 표에는 다양한 장치에 대한 일부 표면 URI 정의 예가 나와 있습니다.

**웹 및 모바일**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 웹 | web://domain.com/path/page.html#element | 특정 도메인의 특정 페이지 내에서 개별 요소를 나타냅니다. 여기서 요소는 다음 예와 같이 레이블이 될 수 있습니다. hero_banner, top_nav, menu, footer 등 |
| iOS 앱 | mobileapp://com.vendor.bundle/activity#element | 버튼 또는 기타 보기 요소와 같이 기본 앱 활동 내의 특정 요소를 나타냅니다. |
| Android 앱 | mobileapp://com.vendor.bundle#element | 기본 앱 내의 특정 요소를 나타냅니다. |

**기타 디바이스 유형**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 데스크탑 | desktop://com.vendor.bundle#element | 버튼, 메뉴, 히어로 배너 등과 같은 애플리케이션 내의 특정 요소를 나타냅니다. |
| TV 앱 | tvcd://com.vendor.bundle#element | 스마트 TV 또는 TV 연결 장치 앱 - 번들 ID 내의 특정 요소를 나타냅니다. |
| 서비스 | service://servicename#element | 서버측 프로세스 또는 기타 수동 엔티티를 나타냅니다. |
| 키오스크 | kiosk://location/screen#element | 쉽게 추가될 수 있는 잠재적인 추가 서피스 유형의 예. |
| ATM | atm://location/screen#element | 쉽게 추가될 수 있는 잠재적인 추가 서피스 유형의 예. |

**와일드카드 표면**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 와일드카드 웹 | 와일드카드:web://domain.com/`*`#element | 와일드카드 표면 - 특정 도메인 아래의 각 페이지에 있는 개별 요소를 나타냅니다. |
| 와일드카드 웹 | 와일드카드:web://`*`domain.com/`*`#element | 와일드카드 표면 - &quot;domain.com&quot;으로 끝나는 모든 도메인 아래의 각 페이지에서 개별 요소를 나타냅니다. |


