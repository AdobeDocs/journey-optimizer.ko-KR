---
solution: Journey Optimizer
product: journey optimizer
title: 내장 제품 프로필
description: 기본 제공 제품 프로필에 대해 알아보기
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 9%

---

# 내장 제품 프로필 {#ootb-product-profiles}


## 메시지와 관련된 권한 기본 정보{#message-permissions}

Adobe Journey Optimizer은 여정 또는 캠페인에서 직접 메시지를 만들고 작성할 수 있는 새로운 인라인 작성 기능을 릴리스했습니다.

이 기능은 다음과 같이 권한에 영향을 줍니다.

| 권한 이름 | 에 포함됩니다 |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**7월 25일 이후**, 관련 권한 **메시지** 은(는) 전환을 활성화하기 위해 여전히 메시지에 액세스할 수 있으며 템플릿으로 저장할 수 있으므로 계속 사용할 수 있습니다.

**9월 6일 기준**, 관련 권한 **메시지** 가 제거되고 더 이상 메시지에 액세스할 수 없습니다.

>[!WARNING]
>
>사용자에게 를 할당한 경우 **[!DNL Message Manager]** 제품 프로필 전용, **[!DNL Journey manager]** 제품 프로필에서는 컨텐츠를 계속 편집할 수 있도록 새 제품 프로필을 할당해야 합니다.


## [!DNL Campaign Administrator] {#campaign-administrator}

다음 **[!DNL Campaign Administrator]** 제품 프로필을 사용하면 관리 메뉴에서 캠페인 및 의사 결정 관리를 관리하고 게시할 수 있습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |캠페인| <ul><li> **[!DNL Manage campaigns]**: 캠페인을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다.</li></ul>|
|관리|<ul><li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage IP pools]**: ip 풀을 읽기, 생성, 편집 및 삭제합니다.</li><li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li><li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한입니다.</li><li> **[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage messages presets]**: 컨텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.</li><li>**[!DNL Manage suppression rules]**: 제어 규칙 읽기, 만들기, 편집 및 삭제에 액세스합니다.</li><li>**[!DNL Export suppression list]**: 제외 목록을 CSV 파일로 내보낼 수 있는 액세스 권한.</li><li>**[!DNL View suppression list]**: 로컬 제외 목록을 읽고 내보냅니다.</li><li>**[!DNL Manage alerts]**: 캠페인, 메시지 및 권한에 대한 경고를 활성화/비활성화합니다.</li><li>**[!DNL Manage landing page settings]**: 랜딩 페이지 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage SMS settings]**: SMS 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|
|의사 결정 관리|<ul><li>**[!DNL Manage decisions]**: 결정을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.</li><li>**[!DNL Manage ranking strategies]**: 순위 전략 읽기, 생성, 편집 및 삭제</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

다음 **[!DNL Campaign Approver]** 제품 프로필을 사용하면 사용자가 게재를 승인하고 게시할 수 있습니다. 나중에 를 통해 게재의 성공을 확인할 수 있습니다. **[!DNL Campaigns]** 보고서.

| 기능 | 권한| |-|-| |캠페인| <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Publish campaigns]**: 캠페인을 게시합니다.</li><li>**[!DNL View Campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL Manage decisions]**: 의사결정 엔티티를 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 정의 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용하십시오.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|
|관리| <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

다음 **[!DNL Campaign Manager]** 제품 프로필을 사용하면 사용자가 만들고 편집할 수 있습니다 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 캠페인]** 게시할 수 없습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |캠페인| <ul><li>**[!DNL Manage campaigns]**: 캠페인을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL View campaigns report]**: 여정 보고서를 읽고 편집합니다.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL Manage decisions]**: 의사결정 엔티티를 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 정의 메시지 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용하십시오.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|
|관리| <ul><li>**[!DNL View messages presets]**: 메시지 사전 설정에 대한 읽기 전용 액세스 권한.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

다음 **[!DNL Campaign Viewer]** 제품 프로필에서는 읽기 전용 액세스 권한을 갖습니다 **[!UICONTROL 캠페인]** 및 **[!UICONTROL 의사 결정 관리]** 기능.

이 제품 프로필에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |캠페인| <ul><li>**[!DNL View campaigns]**: 캠페인에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View campaigns report]**: 캠페인 보고서에 대한 읽기 전용 액세스 권한.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL View decisions]**: 의사 결정 엔터티에 대한 읽기 전용 액세스 권한.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

다음 **[!DNL Journey Administrator]** 제품 프로필을 사용하면 관리 메뉴에서 여정 및 의사 결정 관리를 관리 및 게시할 수 있습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |여정| <ul><li> **[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Publish journeys]**: 여정 게시.</li><li>**[!DNL Manage journeys events, data sources and actions]**: 이벤트, 소스 또는 작업을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul>|
|관리|<ul><li>**[!DNL Manage subdomains delegation]**: 하위 도메인 위임을 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage IP pools]**: ip 풀을 읽기, 생성, 편집 및 삭제합니다.</li><li>**[!DNL Manage PTR records]**: PTR 레코드를 읽고 편집합니다.</li><li>**[!DNL View PTR records]**: PTR 레코드에 대한 읽기 전용 액세스 권한입니다.</li><li>**[!DNL Manage channel surfaces]**: 컨텐츠 브랜딩을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.</li><li>**[!DNL Manage Landing page settings]**: 랜딩 페이지 하위 도메인 및 랜딩 페이지 사전 설정을 만들고, 편집하고, 삭제합니다.</li><li> **[!DNL Manage messages general settings]**: 메시지 일반 설정을 읽고, 만들고, 편집하고, 삭제합니다.</li><li>**[!DNL Manage SMS settings]**: sms 채널을 활성화하는 데 필요한 API 자격 증명 및 SMS 채널 서피스를 생성, 편집 및 삭제합니다.</li><li>**[!DNL Manage suppression rules]**: 제어 규칙 읽기, 만들기, 편집 및 삭제에 액세스합니다.</li><li>**[!DNL View suppression list]**: 로컬 제외 목록을 읽고 내보냅니다.</li><li>**[!DNL Manage alerts]**: 여정 및 권한에 대한 경고를 활성화/비활성화합니다.</li></ul>|
|의사 결정 관리|<ul><li>**[!DNL Manage decisions]**: 결정을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.</li><li>**[!DNL Manage ranking strategies]**: 순위 전략 읽기, 생성, 편집 및 삭제</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: 샌드박스에 대한 액세스 권한을 부여합니다.</li><li>**[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read Identity namespace]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>| |Journey Optimizer 라이브러리|<ul><li>**[!DNL Manage Library Items]**: 에서 저장된 표현식 추가 및 삭제 [!DNL Journey Optimizer] 라이브러리.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

다음 **[!DNL Journey Approver]** 제품 프로필을 사용하면 사용자가 게재를 승인하고 게시할 수 있습니다. 나중에 를 통해 게재의 성공을 확인할 수 있습니다. **[!DNL Journey]** 보고서.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |여정| <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Publish journey]**: 여정 게시.</li><li>**[!DNL View journeys events, data sources and actions]**: 여정 이벤트, 여정 사용자 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL Manage decisions]**: 의사결정 엔티티를 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽기, 만들기, 편집, 삭제하고 작업 기능을 사용합니다.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|
|관리| <ul><li>**[!DNL View channel surfaces]**: 채널 서피스에 대한 읽기 전용 액세스.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

다음 **[!DNL Journey Manager]** 제품 프로필을 사용하면 사용자가 만들고 편집할 수 있습니다 **[!UICONTROL 여정]** 및 **[!UICONTROL 여정]** 게시할 수 없습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |여정| <ul><li>**[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL View journeys events]**: 여정 이벤트, 여정 사용자 지정 작업 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL Manage decisions]**: 의사결정 엔티티를 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽기, 만들기, 편집, 삭제하고 작업 기능을 사용합니다.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: 세그먼트 읽기, 만들기, 편집 및 삭제</li><li>**[!DNL Manage profiles]**: 프로필 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL Read datasets]**: 데이터 세트에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Read schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage merge policies]**: 병합 정책을 읽고, 만들고, 편집하고, 삭제합니다.</li></ul>|
|관리| <ul><li>**[!DNL View channel surfaces]**: 채널 서피스에 대한 읽기 전용 액세스.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

다음 **[!DNL Journey viewer]** 제품 프로필에서는 읽기 전용 액세스 권한을 갖습니다 **[!UICONTROL 여정]** 및 **[!UICONTROL 의사 결정 관리]** 기능.

이 제품 프로필에 할당된 사용자는 편집하거나 게시할 수 없습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |여정| <ul><li>**[!DNL View journeys]**: 여정에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys event, data sources, actions]**: 여정 이벤트 및 데이터 소스에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL View journeys report]**: 여정 보고서에 대한 읽기 전용 액세스 권한.</li></ul>|
|의사 결정 관리| <ul><li>**[!DNL View decisions]**: 의사 결정 엔터티에 대한 읽기 전용 액세스 권한.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

다음 **[!DNL Decisioning manager]** 제품 프로필은 **[!UICONTROL 의사 결정 관리]** 메뉴 아래의 제품에서 사용할 수 있습니다. 이 제품 프로필에 할당된 사용자는 결정을 관리, 보기 및 게시할 수만 있습니다.

이 제품 프로필에는 다음과 같은 권한이 포함됩니다.

| 기능 | 권한| |-|-| |의사 결정 관리| <ul><li>**[!DNL Manage decisions]**: 의사결정 엔티티를 읽기, 만들기, 편집 및 삭제합니다.</li><li>**[!DNL View decisions]**: 의사 결정 엔터티에 대한 읽기 전용 액세스 권한.</li><li>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽기, 만들기, 편집, 삭제하고 작업 기능을 사용합니다.</li><li>**[!DNL Publish decisions]**: 의사결정 활동을 활성화 또는 비활성화합니다.</li></ul>|
