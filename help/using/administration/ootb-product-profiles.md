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
source-git-commit: 2a5db6950ac82fd18deb2e4009c9a43247444d6a
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 7%

---

# 기본 제공 역할 {#ootb-product-profiles}

기본 제공 역할은 사용자가 인터페이스의 특정 기능이나 개체에 액세스할 수 있도록 하는 통합된 권한 세트입니다. 역할을 만드는 데 사용할 수 있는 사용 권한 목록은 [이 페이지](ootb-permissions.md)를 참조하세요.


## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]** 역할을 통해 관리 메뉴를 사용하여 캠페인 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li> </ul> |
| 캠페인 | <ul><li> **[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul> <li>**[!DNL Export suppression list]**: 비표시 목록을 CSV 파일로 내보내기에 액세스할 수 있습니다.</li> <li>**[!DNL Manage alerts]**: 캠페인, 메시지 및 권한에 대한 경고를 활성화/비활성화합니다.</li> <li>**[!DNL Manage IP pools]**: ip 풀을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage landing page settings]**: 랜딩 페이지 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages presets]**: 콘텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li> <li>**[!DNL Manage SMS settings]**: SMS 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 만들기, 편집 및 삭제</li> <li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View suppression list]**: 로컬 비표시 목록을 읽고 내보냅니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 결정을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

**[!DNL Campaign Approver]** 역할을 통해 사용자는 게재를 승인하고 게시할 수 있습니다. 나중에 **[!DNL Campaigns]** 보고서를 통해 게재 성공 여부를 확인할 수 있습니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

**[!DNL Campaign Manager]** 역할을 통해 사용자는 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 캠페인]**&#x200B;에 연결된 모든 기능을 만들고 편집할 수 있지만 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

**[!DNL Campaign Viewer]** 역할을 통해 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 의사 결정 관리]** 기능에 대한 읽기 전용 액세스를 허용합니다.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL View campaigns]**: 캠페인에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 결정 엔터티에 대한 읽기 전용 액세스 권한입니다.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]** 역할에서는 **[!UICONTROL 콘텐츠 템플릿]** 메뉴에만 액세스할 수 있습니다. 이 역할에 할당된 사용자는 여정 또는 캠페인에 액세스하지 않고 템플릿 라이브러리에 액세스하여 콘텐츠를 만들 수만 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Journey Optimizer 라이브러리 | <ul><li>**[!DNL Manage library items]**: 콘텐츠 템플릿 및 조각을 포함한 Journey Optimizer 라이브러리 항목을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage simulate content]**: 미리 보기 및 증명을 위해 **[!UICONTROL 콘텐츠 시뮬레이션]** 옵션에 액세스</li><li>**[!DNL Publish Fragment]**: 콘텐츠 조각을 게시합니다.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]** 역할에서는 **[!UICONTROL 의사 결정 관리]** 메뉴에만 액세스할 수 있습니다. 이 역할에 할당된 사용자는 결정을 관리, 보기 및 게시만 할 수 있습니다.

이 권한에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li><li>**[!DNL View decisions]**: 의사 결정 엔터티에 대한 읽기 전용 액세스입니다.</li><li>**[!DNL Publish decisions]**: 의사 결정 활동을 활성화하거나 비활성화합니다.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

**[!DNL Journey Administrator]** 역할을 사용하면 관리 메뉴에서 여정 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li> </ul> |
| 채널 구성 | <ul> <li>**[!DNL Manage alerts]**: 여정 및 자격에 대한 경고를 활성화/비활성화합니다.</li> <li>**[!DNL Manage IP pools]**: ip 풀을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage Landing page settings]**: 랜딩 페이지 하위 도메인 및 랜딩 페이지 사전 설정을 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages presets]**: 콘텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li> <li>**[!DNL Manage SMS settings]**: SMS 채널을 사용하도록 설정하는 데 필요한 API 자격 증명 및 SMS 채널 구성을 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 만들기, 편집 및 삭제</li> <li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View suppression list]**: 로컬 비표시 목록을 읽고 내보냅니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL Manage data usage policies]**: 데이터 사용 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage usage label]**: 사용 레이블을 읽고 만들고 삭제합니다.</li> <li>**[!DNL View data usage policies]**: 데이터 사용 정책에 대한 읽기 전용 액세스입니다.</li> <li>**[!DNL View user activity log]**: Experience Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스 권한..</li> </ul> |
| 의사 결정 관리 | <ul> <li>**[!DNL Manage decisions]**: 결정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 여정 | <ul> <li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집, 일시 중지, 중지 및 삭제</li> <li>**[!DNL Manage journeys events, data sources and actions]**: 이벤트, 소스 또는 작업을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Publish journeys]**: 여정 게시.</li> <li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li> </ul> |
| Journey Optimizer 라이브러리 | <ul> <li>**[!DNL Manage Library Items]**: [!DNL Journey Optimizer] 라이브러리에 저장된 식을 추가하고 삭제합니다.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]** 역할을 통해 사용자는 게재를 승인하고 게시할 수 있습니다. 나중에 **[!DNL Journey]** 보고서를 통해 게재 성공 여부를 확인할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel configurations]**: 채널 구성에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집, 일시 중지, 중지 및 삭제</li><li>**[!DNL Publish journey]**: 여정 게시.</li><li>**[!DNL View journeys events, data sources and actions]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]** 역할을 통해 사용자는 **[!UICONTROL 여정]** 및 **[!UICONTROL 여정]**&#x200B;에 연결된 모든 기능을 만들고 편집할 수 있지만 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel configurations]**: 채널 구성에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL View journeys events]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

**[!DNL Journey viewer]** 역할에서는 **[!UICONTROL 여정]** 및 **[!UICONTROL 의사 결정 관리]** 기능에 대한 읽기 전용 액세스를 허용합니다.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 결정 엔터티에 대한 읽기 전용 액세스 권한입니다.</li></ul> |
| 여정 | <ul><li>**[!DNL View journeys]**: 여정에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys event, data sources, actions]**: 여정 이벤트 및 데이터 원본에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

**[!DNL Orchestrated Campaign Administrator]** 역할을 통해 관리 메뉴를 사용하여 오케스트레이션된 캠페인을 관리하고 게시할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**: AI 기반 캠페인 및 대상자 기능을 활성화하거나 액세스합니다.</li> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li> <li>**[!DNL View operational insights]**: 시스템 수준 인사이트 및 모니터링 대시보드에 대한 읽기 전용 액세스</li></ul> |
| 채널 구성 | <ul><li>**[!DNL Export suppression list]**: 비표시 목록을 CSV 파일로 내보내기에 액세스할 수 있습니다.</li> <li>**[!DNL Manage alerts]**: 캠페인, 메시지 및 권한에 대한 경고를 활성화/비활성화합니다.</li> <li>**[!DNL Manage custom dashboards]**: 사용자 지정 대시보드를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage IP pools]**: ip 풀을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage landing page settings]**: 랜딩 페이지 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage messages presets]**: 콘텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li> <li>**[!DNL Manage SMS settings]**: SMS 설정을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 만들기, 편집 및 삭제</li> <li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View suppression list]**: 로컬 비표시 목록을 읽고 내보냅니다.</li> </ul> |
| 대시보드 | <ul> <li>**[!DNL Manage standard dashboard]**: 위젯 라이브러리를 통해 사용자 정의 위젯 및 위젯 스키마를 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL View user activity log]**: Experience Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스입니다. </li> </ul> |
| 데이터 수집 | <ul> <li>**[!DNL Manage sources]**: 소스를 읽고 만들고 편집하고 사용하지 않도록 설정합니다.</li> </ul> |
| 데이터 관리 | <ul> <li>**[!DNL Manage datasets]**: 데이터 세트를 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 데이터 모델링 | <ul> <li>**[!DNL Manage schemas]**: 스키마 및 관련 리소스를 읽고 만들고 편집하고 삭제합니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 결정을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul> |
| Journey Optimizer 규칙 | <ul> <li>**[!DNL View frequency rules]**: 빈도 규칙에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage frequency rules]**: 빈도 규칙을 읽거나, 만들거나, 편집하거나, 삭제합니다.</li> </ul> |
| 메시지 | <ul><li> **[!DNL Manage Messages]**: 메시지를 읽고 만들고 편집하고 삭제합니다. </li> **[!DNL Manage Messages Preview and Test]**: 정책이 적용될 때 메시지를 승인하고 게시합니다.</li><li>**[!DNL Publish Messages]**: 메시지 게시. </li><li>**[!DNL View Messages Report]**: 메시지 보고서를 읽고 편집합니다. <li></ul> |
| 오케스트레이션된 캠페인 | <ul><li> **[!DNL Manage orchestrated campaigns]**: 오케스트레이션된 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: Adobe Experience Platform 프로필과 관계형 저장소 엔터티 간의 링크 및 조정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish orchestrated campaigns]**: 오케스트레이션된 캠페인을 게시합니다.</li><li>**[!DNL View orchestrated campaigns report]**: 오케스트레이션된 캠페인 보고서를 읽고 편집합니다.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

**[!DNL Orchestrated Campaign Approver]** 역할을 통해 사용자가 오케스트레이션된 캠페인을 게시할 수 있습니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li> <li>**[!DNL Enable AI Assistant]**: AI 기반 캠페인 및 대상자 기능을 활성화하거나 액세스합니다.</li>  <li>**[!DNL View operational insights]**: 시스템 수준 인사이트 및 모니터링 대시보드에 대한 읽기 전용 액세스</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li> <li>**[!DNL Manage custom dashboards]**: 사용자 지정 대시보드를 만들고, 편집하고, 삭제합니다.</li></ul> |
| 대시보드 | <ul> <li>**[!DNL Manage standard dashboard]**: 위젯 라이브러리를 통해 사용자 정의 위젯 및 위젯 스키마를 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL View user activity log]**: Experience Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스입니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Journey Optimizer 규칙 | <ul> <li>**[!DNL View frequency rules]**: 빈도 규칙에 대한 읽기 전용 액세스 권한.</li></ul> |
| 메시지 | <ul><li> **[!DNL Manage Messages]**: 메시지를 읽고 만들고 편집하고 삭제합니다. </li> **[!DNL Manage Messages Preview and Test]**: 정책이 적용될 때 메시지를 승인하고 게시합니다.</li><li>**[!DNL Publish Messages]**: 메시지 게시. </li><li>**[!DNL View Messages Report]**: 메시지 보고서를 읽고 편집합니다. <li></ul> |
| 오케스트레이션된 캠페인 | <ul><li>**[!DNL Manage orchestrated campaigns]**: 오케스트레이션된 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Publish orchestrated campaigns]**: 오케스트레이션된 캠페인을 게시합니다.</li><li>**[!DNL View orchestrated campaigns admin]**: Adobe Experience Platform 프로필과 관계형 저장소 엔터티 간의 링크 및 조정에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View orchestrated campaigns report]**: 오케스트레이션된 캠페인 보고서를 읽고 편집합니다.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

**[!DNL Orchestrated Campaign Manager]** 역할을 통해 사용자는 **[!UICONTROL 오케스트레이션된 캠페인]** 및 **[!UICONTROL 오케스트레이션된 캠페인]**&#x200B;에 연결된 모든 기능을 만들고 편집할 수 있지만 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: AI 기반 캠페인 및 대상자 기능을 활성화하거나 액세스합니다.</li> <li>**[!DNL Manage merge policies]**: 병합 정책을 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필을 읽고 만들고 편집하고 삭제합니다.</li><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL View datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li>  <li>**[!DNL View operational insights]**: 시스템 수준 인사이트 및 모니터링 대시보드에 대한 읽기 전용 액세스</li><li>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL Manage custom dashboards]**: 사용자 지정 대시보드를 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |
| 대시보드 | <ul> <li>**[!DNL Manage standard dashboard]**: 위젯 라이브러리를 통해 사용자 정의 위젯 및 위젯 스키마를 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL View user activity log]**: Experience Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스입니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔터티를 읽고 만들고 편집하고 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Journey Optimizer 규칙 | <ul> <li>**[!DNL View frequency rules]**: 빈도 규칙에 대한 읽기 전용 액세스 권한. </li></ul> |
| 메시지 | <ul><li> **[!DNL Manage Messages]**: 메시지를 읽고 만들고 편집하고 삭제합니다. </li> **[!DNL Manage Messages Preview and Test]**: 정책이 적용될 때 메시지를 승인하고 게시합니다.</li><li>**[!DNL View Messages Report]**: 메시지 보고서를 읽고 편집합니다. </li></ul> |
| 오케스트레이션된 캠페인 | <ul><li>**[!DNL Manage orchestrated campaigns]**: 오케스트레이션된 캠페인을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View orchestrated campaigns report]**: 오케스트레이션된 캠페인을 읽고 편집합니다.</li><li>**[!DNL View orchestrated campaigns admin]**: Adobe Experience Platform 프로필과 관계형 저장소 엔터티 간의 링크 및 조정에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

**[!DNL Campaign Viewer]** 역할을 통해 **[!UICONTROL 오케스트레이션된 캠페인]** 기능에 대한 읽기 전용 액세스를 허용합니다.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: AI 기반 캠페인 및 대상자 기능을 활성화하거나 액세스합니다.</li> <li>**[!DNL View operational insights]**: 시스템 수준 인사이트 및 모니터링 대시보드에 대한 읽기 전용 액세스</li></ul> |
| 채널 구성 | <ul><li>**[!DNL Manage custom dashboards]**: 사용자 지정 대시보드를 만들고, 편집하고, 삭제합니다.</li></ul> |
| 대시보드 | <ul> <li>**[!DNL Manage standard dashboard]**: 위젯 라이브러리를 통해 사용자 정의 위젯 및 위젯 스키마를 읽고, 만들고, 편집하고, 삭제합니다.</li> </ul> |
| 데이터 거버넌스 | <ul> <li>**[!DNL View user activity log]**: Experience Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스입니다.</li> </ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 결정 엔터티에 대한 읽기 전용 액세스 권한입니다.</li></ul> |
| Journey Optimizer 규칙 | <ul> <li>**[!DNL View frequency rules]**: 빈도 규칙에 대한 읽기 전용 액세스 권한.</li></ul> |
| 오케스트레이션된 캠페인 | <ul><li>**[!DNL View orchestrated campaigns]**: 오케스트레이션된 캠페인에 대한 읽기 전용 액세스</li><li>**[!DNL View orchestrated campaigns report]**: 오케스트레이션된 캠페인 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |




