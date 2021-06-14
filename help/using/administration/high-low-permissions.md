---
title: 권한 수준
description: 높은 권한 및 낮은 수준에 대해 알아보기
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: 컨트롤 그룹
topic: 관리
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# 권한 수준 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

각 제품 프로필은 사용자가 다른 기능에 액세스할 수 있는 권한으로 구성되어 있습니다.
두 가지 유형으로 나눌 수 있습니다.

* **높은 수준의 권한**:는  **[!UICONTROL Product profile]** 및  [!DNL Admin console]처럼  **[!UICONTROL Publish journeys]** 에서 지정할 수 있는  **[!UICONTROL Manage subdomains delegation]**&#x200B;다양한 권한을 나타냅니다. 높은 수준의 권한은 낮은 수준의 권한을 포함합니다.

* **낮은 수준 권한**:는 높은 수준 권한이 있는 다른 권한을 나타냅니다.

예를 들어 **[!UICONTROL Journey administrator]** 제품 프로필에 **[!UICONTROL Manage journeys]** 권한이 할당됩니다. 이 사용 권한을 통해 여정 관리자가 여정을 작성, 읽기 및 삭제할 수 있는 낮은 수준의 권한이 제공됩니다.

## 여정 기능 {#journey-capability}

### 여정 관리 권한 {#manage-journeys}

**[!UICONTROL Manage journeys]** 높은 수준의 권한을 사용하면 여정 흐름을 작성하기 위해 여정 캔버스에서 사용되는 개체에 액세스할 수 있을 뿐만 아니라, 기존 여정을 새로 만들고 편집/삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform 특정:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### 여정 게시 권한 {#publish-journeys}

**[!UICONTROL Publish journeys]** 높은 수준의 권한을 사용하여 여정을 게시할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * journeys.publish
   * journeys.read

### 여정 보기 권한 {#view-journeys}

**[!UICONTROL View journeys]** 높은 수준의 권한을 통해 사용자가 여정을 탐색하고 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * journeys.read

* Adobe Experience Platform 특정:
   * segments.read
   * profiles.read

### 여정 이벤트, 데이터 소스 및 작업 관리 권한 {#manage-journeys-events}

**[!UICONTROL Manage journeys events, data sources and actions]** 높은 수준의 권한을 사용하여 이벤트 및 데이터 구성을 구성할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * 여정_events.read
   * 여정_events.write
   * 여정_events.delete
   * 여정_data_sources.read
   * 여정_data_sources.write
   * 여정_data_sources.delete
   * 여정_actions.read
   * 여정_actions.write
   * 여정_actions.delete
* Adobe Experience Platform 특정:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### 여정 이벤트, 데이터 소스 및 작업 보기 권한 {#view-journeys-event}

**[!UICONTROL View journeys events, data sources and actions]** 높은 수준의 권한을 사용하면 여정 흐름에서 이벤트와 데이터를 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * 여정_events.read
   * 여정_data_sources.read
   * 여정_actions.read

* Adobe Experience Platform 특정:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### 여정 보고서 보기 권한 {#view-journeys-report}

**[!UICONTROL View journeys report]** 높은 수준의 권한을 통해 사용자는 읽기 전용 여정 보고서를 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * 여정_report.read
   * messages_report.read

* Adobe Experience Platform 특정:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 메시지 기능 {#message-capability}

### 메시지 관리 권한 {#manage-messages}

**[!UICONTROL Manage messages]** 높은 수준의 권한을 사용하여 메시지를 만들고 편집/삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform 특정:
   * segments.read
   * schemas.read

### 메시지 미리 보기 및 테스트 권한 관리 {#mange-messages-preview}

**[!UICONTROL Manage messages preview and test]** 높은 수준의 권한을 통해 사용자는 개인화된 메시지를 미리 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform 특정:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### 메시지 게시 권한 {#publish-messages}

**[!UICONTROL Publish messages]** 높은 수준의 권한을 통해 사용자가 메시지를 게시할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.publish

* Adobe Experience Platform 특정:
   * profiles.read
   * schemas.read
   * datasets.read

### 메시지 보기 권한 {#view-messages}

**[!UICONTROL View messages]** 높은 수준의 권한을 통해 사용자는 메시지만 읽을 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform 특정:
   * schemas.read
   * segments.read

### 메시지 보고서 권한 보기 {#view-message-reports}

**[!UICONTROL View messages report]** 높은 수준의 권한을 통해 사용자는 읽기 전용 전자 메일 및 푸시 보고서를 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 의사 결정 관리 기능 {#decisions-permissions}

### 의사 결정 권한 관리 {#manage-decisioning}

**[!UICONTROL Manage decisions]** 높은 수준의 권한을 통해 사용자는 기존 **[!UICONTROL Activity entities]**&#x200B;을 새로 만들고 편집/삭제하고, 결정을 내리기 위해 해당 활동에 사용되는 개체를 관리할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* 의사 결정 관리 특정:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform 특정:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### 의사 결정 권한 보기 {#view-decisions}

**[!UICONTROL View decisions]** 높은 수준의 권한을 통해 사용자는 기존 활동 및 관련 비즈니스 개체를 사용하여 결정을 내릴 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* 의사 결정 관리 특정:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform 특정:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Offers 의사 결정 권한 게시 {#publish-decisions}

**[!UICONTROL Publish offers decisioning]** 높은 수준의 권한을 통해 사용자는 오퍼 활동을 승인/승인하지 않을 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* 의사 결정 관리 특정:
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform 특정:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### 등급 전략 관리 권한 {#manage-decisions}

**[!UICONTROL Manage ranking strategies]** 높은 수준의 권한을 통해 사용자는 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제할 수 있으며 작업 기능을 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* 의사 결정 관리 특정:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 관리 기능 {#administration-permissions}

### 하위 도메인 위임 권한 관리 {#manage-subdomain}

**[!UICONTROL Manage subdomains delegation]** 높은 수준의 권한을 통해 사용자는 하위 도메인 위임(IP 풀 포함)을 생성, 편집 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### PTR 레코드 보기 권한 {#view-ptr}

**[!UICONTROL View PTR records]** 높은 수준의 권한을 사용하면 하위 도메인을 기반으로 구성되고 다음과 같은 낮은 수준의 권한을 포함하는 PTR 레코드를 볼 수 있습니다.

* PTR_records.read
* subdomains_delegation.read

### IP 풀 관리 권한 {#manage-ip-pools}

**[!UICONTROL Manage IP pools]** 높은 수준의 권한을 사용하면 선호도 정의를 생성, 편집 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### 메시지 일반 설정 권한 관리 {#manage-message-settings}

**[!UICONTROL Manage messages general settings]** 고급 권한을 사용하면 샌드박스 수준에서 전역 설정을 만들고, 편집하고, 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Adobe Experience Platform 특정:
   * schemas.read

### 메시지 일반 설정 권한 보기 {#view-message-settings}

**[!UICONTROL View messages general settings]** 높은 수준의 권한을 통해 사용자는 억제 규칙 또는 실행 주소와 같은 일반 설정을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_general_settings.read
* Adobe Experience Platform 특정:
   * schemas.read

### 메시지 사전 설정 관리 권한 {#manage-message-presets}

**[!UICONTROL Manage messages presets]** 고급 권한을 사용하면 샌드박스 수준의 채널에서 메시지 사전 설정을 생성, 편집 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (Adobe Experience Platform Launch에서)

### 메시지 사전 설정 보기 권한 {#view-message-presets}

**[!UICONTROL View messages presets]** 고급 권한을 사용하면 메시지를 만들 때 사용할 메시지 사전 설정을 알 수 있도록 메시지 사전 설정을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (Adobe Experience Platform Launch에서)

### 제외 규칙 권한 관리 {#manage-suppression-rules}

**[!UICONTROL Manage suppression rules]** 높은 수준의 권한을 사용하면 사용자의 이메일 주소가 제외 목록에 추가되기 전에 바운스 수를 정의할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete

### 제외 목록 보기 권한 {#view-suppresion-list}

**[!UICONTROL View suppression list]** 고급 권한을 사용하면 메시지 사전 설정 및 일반 메시지 설정을 포함한 메시지 구성을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * suppression_list.view
* Adobe Experience Platform 특정:
   * profiles.read
   * datasets.read

### 내보내기 억제 목록 권한 {#export-suppression-list}

**[!UICONTROL Export suppression list]** 고급 권한을 사용하면 메시지 사전 설정 및 일반 메시지 설정을 포함한 메시지 구성을 구성할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Adobe Experience Platform 특정:
   * profiles.read
   * datasets.read
