---
title: 코드 기반 표면
description: 코드 기반 경험 표면이 무엇인지 알아봅니다
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: f247ef3c3cd7d1d270893ae6bf88fadf3932d05e
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 53%

---

# 코드 기반 경험 표면 {#code-based-surface}

## 표면이란 무엇입니까? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="구성 요소에 대한 표면 URI 추가"
>abstract="구현이 웹, iOS 또는 Android용이 아니거나 특정 URI를 타기팅해야 하는 경우, 경험을 게재하려는 엔티티를 가리키는 고유 식별자인 표면 URI를 입력하십시오. 자체 구현에 사용된 것과 일치하는 표면 URI를 입력해야 합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="다른 플랫폼을 위한 코드 기반 경험 구성 만들기"

코드 기반 경험 **surface**&#x200B;은(는) 사용자 또는 시스템 상호 작용을 위해 디자인된 모든 엔터티이며 [URI](#surface-uri)로 고유하게 식별됩니다. 표면은 [응용 프로그램 구현](code-based-prerequisites.md#implementation-prerequisites)에 지정되어 있으며 [코드 기반 경험 채널 구성](code-based-configuration.md)에서 참조된 표면과 일치해야 합니다.

표면은 존재하는 엔티티(터치포인트)가 있는 모든 계층 구조 수준에서 컨테이너로 볼 수 있습니다.

* 웹 페이지, 모바일 앱, 데스크탑 앱, 더 큰 엔티티 내의 특정 콘텐츠 위치(예: `div`) 또는 비표준 표시 패턴(예: 키오스크 또는 데스크탑 앱 배너)일 수 있습니다.<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 또한 비표시 또는 추상화된 표시 목적을 위해 특정 콘텐츠 컨테이너 조각으로 확장할 수도 있습니다(예: 서비스로 제공되는 JSON Blob).

* 또한 다양한 클라이언트 표면 정의와 일치하는 와일드카드 표면일 수도 있습니다. 예를 들어 웹 사이트의 모든 페이지에 있는 히어로 이미지 위치는 web://mydomain.com/*#hero_image 와 같은 표면 URI로 변환될 수 있습니다.

## 표면 식별자 {#surface-uri}

**표면 URI**&#x200B;은(는) 응용 프로그램 내의 개별 사용자 인터페이스 요소 또는 구성 요소로 이동하는 정확한 식별자 역할을 합니다. 기본적으로 서피스 URI는 여러 섹션으로 구성됩니다.

1. **유형**: 웹, 모바일 앱, atm, 키오스크, tvcd, 서비스 등
1. **속성**: 페이지 URL 또는 앱 번들
1. **컨테이너**: 페이지/앱 활동의 위치

아래 표에는 다양한 디바이스의 표면 URI 정의 예시가 일부 나와 있습니다.

**웹 및 모바일**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 웹 | `web://domain.com/path/page.html#element` | 특정 도메인의 특정 페이지 내 개별 요소를 나타냅니다. 여기서 요소는 hero_banner, top_nav, menu, footer 등의 예시와 같은 레이블이 될 수 있습니다. |
| iOS 앱 | `mobileapp://com.vendor.bundle/activity#element` | 기본 앱 활동 내의 특정 요소(예: 버튼 또는 기타 보기 요소)를 나타냅니다. |
| Android 앱 | `mobileapp://com.vendor.bundle/#element` | 기본 앱 내의 특정 요소를 나타냅니다. |

**기타 디바이스 유형**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 데스크탑 | `desktop://com.vendor.bundle/#element` | 버튼, 메뉴, 히어로 배너 등과 같은 애플리케이션 내의 특정 요소를 나타냅니다. |
| TV 앱 | `tvcd://com.vendor.bundle/#element` | 스마트 TV 또는 TV 연결 디바이스 앱 내 특정 요소, 번들 ID를 나타냅니다. |
| 서비스 | `service://servicename/#element` | 서버측 프로세스 또는 기타 수동 엔티티를 나타냅니다. |
| 키오스크 | `kiosk://location/screen#element` | 쉽게 추가할 수 있는 잠재적인 추가 표면 유형의 예. |
| ATM | `atm://location/screen#element` | 쉽게 추가할 수 있는 잠재적인 추가 표면 유형의 예. |

**와일드카드 표면**

| 유형 | URI | 설명 |
| --------- | ----------- | ------- | 
| 와일드카드 웹 | `wildcard:web://domain.com/*#element` | 와일드카드 표면 - 특정 도메인 아래의 각 페이지에 있는 개별 요소를 나타냅니다. |
| 와일드카드 웹 | `wildcard:web://*domain.com/*#element` | 와일드카드 표면 - &quot;domain.com&quot;으로 끝나는 모든 도메인 아래의 각 페이지에 있는 개별 요소를 나타냅니다. |

## URI 구성 {#uri-composition}

[!DNL Journey Optimizer]에서 코드 기반 경험 채널은 두 가지 유형의 고객 구현을 지원합니다.

* 웹 사이트용 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"} 또는 모바일 앱용 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}를 기반으로 합니다.
* [AEP Edge Network 서버 API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=ko-KR){target="_blank"}를 사용하는 서버측 또는 하이브리드.

>[!NOTE]
>
>[이 섹션](code-based-prerequisites.md#implementation-prerequisites)에서 구현 필수 구성 요소에 대해 자세히 알아보세요.

코드 기반 경험을 사용하면 [표면 URI](#surface-uri)을(를) 사용하여 [!DNL Journey Optimizer]에 의해 고유하게 식별되는 세분화된 위치 <!--(such as a specific location on a page, or inside a mobile native app)-->의 콘텐츠를 수정할 수 있습니다.

이러한 표면 URI는 구현 방법에 따라 구성되고 처리됩니다.

* **웹/모바일 SDK**: 웹/모바일 SDK는 현재 URL/앱 ID와 위치 문자열을 기반으로 표면 URI를 자동으로 구성할 수 있으므로 웹/모바일 개발자는 이러한 세분화된 위치를 간단한 문자열로 정의해야 합니다.

* **Edge Network API**: 이 유형의 구현에는 전체 URI가 필요하므로 앱/페이지 개발자는 콘텐츠를 사용할 전체 경로와 위치를 포함하는 전체 표면 URI를 정의해야 합니다.

[코드 기반 경험 채널 구성](code-based-configuration.md)을 만들 때 선택한 플랫폼에 따라 표면을 지정하는 두 가지 방법이 있는 이유입니다.

* **[!UICONTROL Web]**, **[!UICONTROL iOS]** 및 **[!UICONTROL Android]** 플랫폼의 경우 **URL/앱 ID**&#x200B;와 **위치 또는 경로**&#x200B;를 입력하여 표면을 구성해야 합니다. [web](code-based-configuration.md#web) 및 [mobile](code-based-configuration.md#mobile) 플랫폼에 대한 코드 기반 경험 구성에 대해 자세히 알아보세요.

* 플랫폼이 **[!UICONTROL 기타]**&#x200B;인 경우 [위](#surface-uri)의 예처럼 전체 **표면 URI**&#x200B;을 입력해야 합니다. [other](code-based-configuration.md#other) 플랫폼에 대한 코드 기반 경험 구성에 대해 자세히 알아보세요.
