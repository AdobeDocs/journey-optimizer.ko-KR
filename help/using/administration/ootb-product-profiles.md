---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 기본 역할
description: 기본 제공 역할에 대해 알아보기
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: 권한, 작성, 메시지
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: e20db7c39e751bf720cd0ae75b4e8f031de18eef
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# 기본 제공 역할 {#ootb-product-profiles}

기본 제공 역할은 사용자가 인터페이스의 특정 기능이나 개체에 액세스할 수 있도록 하는 통합된 권한 세트입니다. 역할을 만드는 데 사용할 수 있는 사용 권한 목록은 [이 페이지](ootb-permissions.md)를 참조하세요.

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]** 역할에서는 **[!UICONTROL 콘텐츠 템플릿]** 메뉴에만 액세스할 수 있습니다. 이 역할에 할당된 사용자는 여정 또는 캠페인에 액세스하지 않고 템플릿 라이브러리에 액세스하여 콘텐츠를 만들 수만 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| Journey Optimizer 라이브러리 | <ul><li>**[!DNL Manage library items]**: 콘텐츠 템플릿 및 조각을 포함한 Journey Optimizer 라이브러리 항목을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage simulate content]**: 미리 보기 및 증명을 위해 **[!UICONTROL 콘텐츠 시뮬레이션]** 옵션에 액세스</li><li>**[!DNL Publish Fragment]**: 콘텐츠 조각을 게시합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]** 역할에서는 **[!UICONTROL 의사 결정 관리]** 메뉴에만 액세스할 수 있습니다. 이 역할에 할당된 사용자는 결정을 관리, 보기 및 게시만 할 수 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li><li>**[!DNL View decisions]**: 의사 결정 엔터티에 대한 읽기 전용 액세스입니다.</li><li>**[!DNL Publish decisions]**: 의사 결정 활동을 활성화하거나 비활성화합니다.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]** 역할을 통해 관리 메뉴를 사용하여 캠페인 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li> **[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul> <li>**[!DNL Export suppression list]**: 비표시 목록을 CSV 파일로 내보내기에 액세스할 수 있습니다.</li> <li>**[!DNL Manage alerts]**: 캠페인, 메시지 및 권한에 대한 경고를 활성화/비활성화합니다.</li> <li>**[!DNL Manage IP pools]**: ip 풀을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage landing page settings]**: 랜딩 페이지 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages presets]**: 콘텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li> <li>**[!DNL Manage SMS settings]**: SMS 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 만들기, 편집 및 삭제</li> <li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View suppression list]**: 로컬 비표시 목록을 읽고 내보냅니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 결정을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

**[!DNL Campaign Approver]** 역할을 통해 사용자는 게재를 승인하고 게시할 수 있습니다. 나중에 **[!DNL Campaigns]** 보고서를 통해 게재 성공 여부를 확인할 수 있습니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

**[!DNL Campaign Manager]** 역할을 통해 사용자는 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 캠페인]**&#x200B;에 연결된 모든 기능을 만들고 편집할 수 있지만 게시할 수 없습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

**[!DNL Campaign Viewer]** 역할을 통해 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 의사 결정 관리]** 기능에 대한 읽기 전용 액세스를 허용합니다.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL View campaigns]**: 캠페인에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 결정 엔터티에 대한 읽기 전용 액세스 권한입니다.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

**[!DNL Journey Administrator]** 역할을 사용하면 관리 메뉴에서 여정 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul> <li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li> <li>**[!DNL Manage journeys events, data sources and actions]**: 이벤트, 소스 또는 작업을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Publish journeys]**: 여정 게시.</li> <li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li> </ul> |
| 채널 구성 | <ul> <li>**[!DNL Manage alerts]**: 여정 및 자격에 대한 경고를 활성화/비활성화합니다.</li> <li>**[!DNL Manage IP pools]**: ip 풀을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage Landing page settings]**: 랜딩 페이지 하위 도메인 및 랜딩 페이지 사전 설정을 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages presets]**: 콘텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li> <li>**[!DNL Manage SMS settings]**: SMS 채널을 사용하도록 설정하는 데 필요한 API 자격 증명 및 SMS 채널 구성을 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 만들기, 편집 및 삭제</li> <li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View suppression list]**: 로컬 비표시 목록을 읽고 내보냅니다.</li> </ul> |
| 의사 결정 관리 | <ul> <li>**[!DNL Manage decisions]**: 결정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li> </ul> |
| Journey Optimizer 라이브러리 | <ul> <li>**[!DNL Manage Library Items]**: [!DNL Journey Optimizer] 라이브러리에 저장된 식을 추가하고 삭제합니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL Manage data usage policies]**: 데이터 사용 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage usage label]**: 사용 레이블을 읽고 만들고 삭제합니다.</li> <li>**[!DNL View data usage policies]**: 데이터 사용 정책에 대한 읽기 전용 액세스입니다.</li> <li>**[!DNL View user activity log]**: 감사 로그를 읽고 내보냅니다.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]** 역할을 통해 사용자는 게재를 승인하고 게시할 수 있습니다. 나중에 **[!DNL Journey]** 보고서를 통해 게재 성공 여부를 확인할 수 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Publish journey]**: 여정 게시.</li><li>**[!DNL View journeys events, data sources and actions]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel configurations]**: 채널 구성에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]** 역할을 통해 사용자는 **[!UICONTROL 여정]** 및 **[!UICONTROL 여정]**&#x200B;에 연결된 모든 기능을 만들고 편집할 수 있지만 게시할 수 없습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL View journeys events]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel configurations]**: 채널 구성에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

**[!DNL Journey viewer]** 역할에서는 **[!UICONTROL 여정]** 및 **[!UICONTROL 의사 결정 관리]** 기능에 대한 읽기 전용 액세스를 허용합니다.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 권한에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL View journeys]**: 여정에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys event, data sources, actions]**: 여정 이벤트 및 데이터 원본에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 결정 엔터티에 대한 읽기 전용 액세스 권한입니다.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Campaigns and Decision management. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: XX.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: XX.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL Read Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!DNL Campaigns]** reports. 

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit orchestrated campaign reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL View orchestrated campaigns admin]**: XX.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li> <li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li></ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Campaigns]** and every capability linked to **[!UICONTROL Campaigns]** but will not be able to publish them.

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit journey report.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Campaigns]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li></ul>|

-->