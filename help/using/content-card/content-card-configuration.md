---
title: 콘텐츠 카드 구성
description: 콘텐츠 카드 채널 구성
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="제한된 가용성" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 46%

---

# 콘텐츠 카드 구성 {#content-card-configuration}

>[!BEGINSHADEBOX]

**목차**

* [콘텐츠 카드 시작](get-started-content-card.md)
* [콘텐츠 카드 사전 요구 사항](content-card-configuration-prereq.md)
* **콘텐츠 카드 채널 구성**
* [콘텐츠 카드 만들기](create-content-card.md)
* [콘텐츠 카드 디자인](design-content-card.md)
* [컨텐츠 카드 보고서](content-card-report.md)

>[!ENDSHADEBOX]

## 구성이란 무엇입니까? {#surface-definition}

**콘텐츠 카드 경험 구성**&#x200B;은(는) 사용자 또는 시스템 상호 작용을 위해 디자인된 엔터티이며, **URI**&#x200B;에 의해 고유하게 식별됩니다.

다시 말해, 표면은 존재하는 엔티티(접점)를 가진 계층 구조의 모든 수준에서 컨테이너로 볼 수 있습니다.

* 웹 페이지, 모바일 앱, 데스크탑 앱, 더 큰 엔터티 내의 특정 콘텐츠 위치(예: `div`) 또는 비표준 표시 패턴(예: 키오스크 또는 데스크탑 앱 배너)일 수 있습니다.

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

## 콘텐츠 카드 구성 만들기 {#create-config}

1. **[!UICONTROL 채널]** > **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/content_card_config_1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-`자를 사용할 수도 있습니다.

1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. **[!UICONTROL 콘텐츠 카드]** 채널을 선택하십시오.

   ![](assets/content_card_config_2.png)

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

1. 콘텐츠 카드 경험을 적용할 플랫폼을 선택합니다.

   ![](assets/content_card_config_3.png)

1. 웹:

   * 변경 내용을 단일 페이지에만 적용하려면 **[!UICONTROL 페이지 URL]**&#x200B;을(를) 지정하십시오.

   * 또는 지정된 규칙과 일치하는 여러 URL을 대상으로 **[!UICONTROL 페이지 일치 규칙]**&#x200B;을(를) 만듭니다. 예를 들어 모든 페이지에서 히어로 배너를 업데이트하거나 모든 제품 페이지에 표시할 상단 이미지를 추가하는 등 웹 사이트에서 전체적으로 변경 사항을 적용하는 데 사용할 수 있습니다. [자세히 알아보기](../web/web-configuration.md)

1. iOS 및 Android의 경우

   * **[!UICONTROL 앱 ID]**, **[!UICONTROL 앱 내의 위치 또는 경로]** 및 **[!UICONTROL 미리 보기 URL]**&#x200B;을 입력하거나 선택합니다.

1. 변경 사항을 제출합니다.

이제 콘텐츠 카드 경험을 만들 때 구성을 선택할 수 있습니다.

