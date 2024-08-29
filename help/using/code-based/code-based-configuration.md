---
title: 코드 기반 구성
description: 코드 기반 구성 만들기
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: 392fe9d87e1061a2ba40fbcae042cd1a0891a829
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 48%

---

# 코드 기반 경험 구성 {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="앱 ID"
>abstract="앱의 운영 환경 내에서 정확한 식별과 구성을 위해 앱 ID를 제공하여 원활한 통합과 기능을 보장합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="페이지에서의 위치"
>abstract="앱 필드 내의 위치 또는 경로는 사용자가 앱 내에서 액세스하기를 원하는 정확한 대상을 지정합니다. 이는 앱의 탐색 구조 내 특정 섹션이나 페이지일 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="표면 URI"
>abstract="표면 URI는 애플리케이션 내의 고유한 사용자 인터페이스 요소나 구성 요소를 가리키는 정확한 식별자 역할을 합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="기본 작성 및 미리보기 URL"
>abstract="이 필드는 규칙에 의해 생성되거나 규칙과 일치하는 페이지에 지정된 URL이 있는지 확인하는 데 필요한데, 이는 콘텐츠를 효과적으로 만들고 미리 보는 데 필수적입니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="기본 작성 및 미리보기 URL"
>abstract="이 필드는 규칙에 의해 생성되거나 규칙과 일치하는 페이지에 지정된 URL이 있는지 확인하는 데 필요한데, 이는 콘텐츠를 효과적으로 만들고 미리 보는 데 필수적입니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="미리보기 URL"
>abstract="이 필드는 애플리케이션 내에서 장치에서 직접 콘텐츠의 시뮬레이션 및 미리보기를 활성화하는 데 필수적입니다."

## 채널 구성 만들기 {#reatte-code-based-configuration}

채널 구성을 만들려면 다음 단계를 수행하십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/code_config_1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-`자를 사용할 수도 있습니다.

1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

1. **코드 기반 경험** 채널을 선택하십시오.

   ![](assets/code_config_2.png)

1. 코드 기반 경험을 적용할 플랫폼을 선택합니다.

1. 웹:

   * 변경 내용을 단일 페이지에만 적용하려면 **[!UICONTROL 페이지 URL]**&#x200B;을(를) 지정하십시오.

   * 또는 지정된 규칙과 일치하는 여러 URL을 대상으로 **[!UICONTROL 페이지 일치 규칙]**&#x200B;을(를) 만듭니다. 예를 들어 모든 페이지에서 히어로 배너를 업데이트하거나 모든 제품 페이지에 표시할 상단 이미지를 추가하는 등 웹 사이트에서 전체적으로 변경 사항을 적용하는 데 사용할 수 있습니다. [자세히 알아보기](../web/web-configuration.md)

1. iOS 및 Android의 경우

   * **[!UICONTROL 앱 ID]** 및 **[!UICONTROL 앱 내부의 위치 또는 경로]**&#x200B;를 입력하세요.

     ![](assets/code_config_3.png)

1. 구현이 웹, iOS 또는 Android용이 아니거나 특정 URI를 타깃팅해야 하는 경우 플랫폼으로 기타 를 선택합니다. 여러 플랫폼을 선택하거나 여러 URI를 추가하면 콘텐츠가 선택한 모든 페이지 또는 앱에 전달됩니다.

   * **[!UICONTROL 표면 URI]**&#x200B;를 입력하십시오.

   >[!CAUTION]
   >
   >코드 기반 캠페인에 사용된 표면 URI가 자체 구현에 사용된 표면 URI와 일치하는지 확인합니다. 그렇지 않으면 변경 사항이 전달되지 않습니다.

1. **[!UICONTROL 미리 보기 URL]** 필드를 입력하여 온디바이스 미리 보기를 사용하도록 설정합니다. 이 URL은 미리보기를 트리거할 때 사용할 특정 URL을 미리보기 서비스에 알립니다.

   * 웹:

      * 단일 페이지 URL을 입력하면 해당 URL이 미리보기에 사용됩니다.
      * 페이지 일치 규칙을 선택한 경우 브라우저에서 환경을 미리 보는 데 사용할 기본 미리 보기 URL을 입력해야 합니다.

   * 모바일 플랫폼(iOS / Android)의 경우:

      * 미리보기 URL은 앱 내의 앱 개발자가 구성한 딥링크입니다. 이렇게 하면 딥링크 체계와 일치하는 모든 URL이 모바일 웹 브라우저가 아닌 앱 내에서 열립니다. 앱에 대해 구성된 딥링크 체계를 얻으려면 앱 개발자에게 문의하십시오.

+++  다음 리소스는 앱 구현에 대한 딥링크를 구성하는 데 도움이 될 수 있습니다

      * Android의 경우

         * [앱 컨텍스트에 대한 딥 링크 만들기](https://developer.android.com/training/app-links/deep-linking)

      * iOS의 경우

         * [앱에 대한 사용자 정의 URL 체계 정의](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

         * [앱에서 범용 링크 지원](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >환경을 미리 보는 동안 문제가 발생하는 경우 [이 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link)를 참조하세요.

1. 특정 위치에 있는 응용 프로그램에서 예상하는 형식을 선택합니다. 이 템플릿은 캠페인 및 여정에서 코드 기반 경험을 작성할 때 사용됩니다.

1. 변경 사항을 제출합니다.

이제 코드 기반 경험을 만들 때 구성을 선택할 수 있습니다.


## 표면이란 무엇입니까? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="코드 기반 경험 구성 정의"
>abstract="코드 기반 구성은 콘텐츠가 게재되고 사용되는 애플리케이션 내부의 경로와 위치를 정의하며 애플리케이션 구현의 URI로 고유하게 식별됩니다."

**코드 기반 경험 표면**&#x200B;은(는) URI로 고유하게 식별되는 사용자 또는 시스템 상호 작용을 위해 디자인된 모든 엔터티입니다. 표면은 애플리케이션 구현에 지정되며, 코드 기반 경험 채널 구성에서 구성된 표면에 해당해야 합니다.

코드 기반 경험 채널 구성을 만들 때 - 웹, iOS 및 Android 플랫폼의 경우 표면을 구성할 경로와 위치를 입력해야 하며, 플랫폼이 기타인 경우 아래 예제와 같이 전체 URI를 입력해야 합니다.

다시 말해, 표면은 존재하는 엔티티(터치포인트)가 있는 모든 계층 구조 수준의 컨테이너로 볼 수 있습니다.<!--good idea to illustrate how it can be seen, but to clarify-->

* 웹 페이지, 모바일 앱, 데스크탑 앱, 더 큰 엔티티 내의 특정 콘텐츠 위치(예: `div`) 또는 비표준 표시 패턴(예: 키오스크 또는 데스크탑 앱 배너)일 수 있습니다.<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 또한 비표시 또는 추상화된 표시 목적을 위해 특정 콘텐츠 컨테이너 조각으로 확장할 수도 있습니다(예: 서비스로 제공되는 JSON Blob).

* 또한 다양한 클라이언트 표면 정의와 일치하는 와일드카드 표면일 수도 있습니다. 예를 들어 웹 사이트의 모든 페이지에 있는 히어로 이미지 위치는 web://mydomain.com/*#hero_image 와 같은 표면 URI로 변환될 수 있습니다.

기본적으로 표면 URI는 여러 섹션으로 구성됩니다.
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

