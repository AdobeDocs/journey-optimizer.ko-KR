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
source-git-commit: fd8835b1f9bffd887758e4015171074c5dfc16c0
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 6%

---

# 기본 역할 {#ootb-product-profiles}

기본 제공 역할은 사용자가 인터페이스의 특정 기능이나 개체에 액세스할 수 있도록 하는 통합된 권한 세트입니다. 을(를) 참조하십시오 [이 페이지](ootb-permissions.md) 역할 빌드에 사용 가능한 권한 목록입니다.

## [!DNL Campaign Administrator] {#campaign-administrator}

다음 **[!DNL Campaign Administrator]** 역할 을 사용하면 관리 메뉴에서 캠페인 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li> **[!DNL Manage campaigns]**: 캠페인 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage IP pools]**: ip 풀 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li><li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스</li><li> **[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage messages presets]**: 컨텐츠 브랜딩 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 생성, 편집 및 삭제</li><li>**[!DNL Export suppression list]**: 비표시 목록을 CSV 파일로 내보낼 수 있는 액세스 권한.</li><li>**[!DNL View suppression list]**: 로컬 제외 목록을 읽고 내보냅니다.</li><li>**[!DNL Manage alerts]**: 캠페인, 메시지 및 권한에 대한 경고를 활성화/비활성화합니다.</li><li>**[!DNL Manage landing page settings]**: 랜딩 페이지 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage SMS settings]**: SMS 설정 읽기, 만들기, 편집 및 삭제</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

다음 **[!DNL Campaign Approver]** 사용자는 역할을 통해 게재를 승인하고 게시할 수 있습니다. 나중에 를 사용하여 게재의 성공을 확인할 수 있습니다. **[!DNL Campaigns]** 보고서.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View Campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

다음 **[!DNL Campaign Manager]** 사용자는 역할을 통해 을 만들고 편집할 수 있습니다. **[!UICONTROL 캠페인]** 및 연결된 모든 기능 **[!UICONTROL 캠페인]** 그러나 은(는) 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL Manage campaigns]**: 캠페인 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL View campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

다음 **[!DNL Campaign Viewer]** 역할에 대해 읽기 전용 액세스 권한 허용 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 의사 결정 관리]** 기능.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 캠페인 | <ul><li>**[!DNL View campaigns]**: 캠페인에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서에 대한 읽기 전용 액세스 권한</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 의사 결정 엔티티에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

다음 **[!DNL Journey Administrator]** 역할 을 사용하면 관리 메뉴에서 여정 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li> **[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Publish journeys]**: 여정 게시.</li><li>**[!DNL Manage journeys events, data sources and actions]**: 이벤트, 소스 또는 작업을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage IP pools]**: ip 풀 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li><li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스</li><li>**[!DNL Manage messages presets]**: 컨텐츠 브랜딩 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage Landing page settings]**: 랜딩 페이지 하위 도메인 및 랜딩 페이지 사전 설정을 만들고, 편집하고, 삭제합니다.</li><li> **[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage SMS settings]**: SMS 채널을 활성화하는 데 필요한 API 자격 증명 및 SMS 채널 표면을 생성, 편집 및 삭제합니다.</li><li>**[!DNL Manage suppression rules]**: 비표시 규칙에 액세스, 생성, 편집 및 삭제</li><li>**[!DNL View suppression list]**: 로컬 제외 목록을 읽고 내보냅니다.</li><li>**[!DNL Manage alerts]**: 여정 및 권한에 대한 경고를 활성화/비활성화합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 등급 전략을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| Journey Optimizer 라이브러리 | <ul><li>**[!DNL Manage Library Items]**: 저장된 표현식을 추가하고 삭제합니다. [!DNL Journey Optimizer] 라이브러리.</li></ul> |
| 데이터 거버넌스 | <ul><li>**[!DNL Manage usage label]**: 사용량 레이블 읽기, 만들기 및 삭제</li><li>**[!DNL Manage data usage policies]**: 데이터 사용 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View data usage policies]**: 데이터 사용 정책에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View user activity log]**: 감사 로그를 읽고 내보냅니다.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

다음 **[!DNL Journey Approver]** 사용자는 역할을 통해 게재를 승인하고 게시할 수 있습니다. 나중에 를 사용하여 게재의 성공을 확인할 수 있습니다. **[!DNL Journey]** 보고서.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Publish journey]**: 여정 게시.</li><li>**[!DNL View journeys events, data sources and actions]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel surfaces]**: 채널 표면에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

다음 **[!DNL Journey Manager]** 사용자는 역할을 통해 을 만들고 편집할 수 있습니다. **[!UICONTROL 여정]** 및 연결된 모든 기능 **[!UICONTROL 여정]** 그러나 은(는) 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL View journeys events]**: 여정 이벤트, 여정 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |
| 채널 구성 | <ul><li>**[!DNL View channel surfaces]**: 채널 표면에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

다음 **[!DNL Journey viewer]** 역할에 대해 읽기 전용 액세스 권한 허용 **[!UICONTROL 여정]** 및 **[!UICONTROL 의사 결정 관리]** 기능.

이 역할에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 역할에는 다음 권한이 포함됩니다.

| 리소스 | 권한 |
|-|-|
| 여정 | <ul><li>**[!DNL View journeys]**: 여정에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys event, data sources, actions]**: 여정 이벤트 및 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서에 대한 읽기 전용 액세스 권한.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL View decisions]**: 의사 결정 엔티티에 대한 읽기 전용 액세스 권한.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

다음 **[!DNL Decisioning manager]** 역할은 다음에 대한 액세스만 허용합니다 **[!UICONTROL 의사 결정 관리]** 메뉴 아래의 제품에서 사용할 수 있습니다. 이 역할에 할당된 사용자는 결정을 관리, 보기 및 게시만 할 수 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL View decisions]**: 의사 결정 엔티티에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li><li>**[!DNL Publish decisions]**: 의사 결정 활동을 활성화하거나 비활성화합니다.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Experience decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

다음 **[!DNL Content Library Manager]** 역할은 다음에 대한 액세스만 허용합니다 **[!UICONTROL 콘텐츠 템플릿]** 메뉴 아래의 제품에서 사용할 수 있습니다. 이 역할에 할당된 사용자는 여정 또는 캠페인에 액세스하지 않고 템플릿 라이브러리에 액세스하여 콘텐츠를 만들 수만 있습니다.

이 역할에는 다음 권한이 포함됩니다.

| 기능 | 권한 |
|-|-|
| Journey Optimizer 라이브러리 | <ul><li>**[!DNL Manage library items]**: 콘텐츠 템플릿 및 조각을 포함한 Journey Optimizer 라이브러리 항목을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage simulate content]**: 액세스 권한 **[!UICONTROL 콘텐츠 시뮬레이션]** 미리보기 및 증명 옵션</li><li>**[!DNL Publish Fragment]**: 콘텐츠 조각을 게시합니다.</li></ul> |
| 의사 결정 관리 | <ul><li>**[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: 세그먼트 정의를 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</li></ul> |