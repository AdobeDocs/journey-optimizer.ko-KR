---
title: 권한 수준
description: 높은 권한 및 낮은 수준에 대해 알아보기
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: ad24f1ed5b3480385cb8cab471f638e289bf5094
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 0%

---

# 권한 수준 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

각 제품 프로필은 사용자가 다른 기능에 액세스할 수 있는 권한으로 구성되어 있습니다.
두 가지 유형으로 나눌 수 있습니다.

* **높은 수준의 권한**: 에는 지정할 수 있는 다양한 권한을 나타냅니다 **[!UICONTROL Product profile]** 에서 [!DNL Admin console], 예 **[!DNL Publish journeys]** 및 **[!DNL Manage subdomains delegation]**. 높은 수준의 권한은 낮은 수준의 권한을 포함합니다.

* **낮은 수준 권한**: 는 높은 수준 권한이 있는 다른 권한을 나타냅니다.

예: **[!DNL Journey administrator]** 제품 프로필이 할당됨 **[!DNL Manage journeys]** 권한. 이 사용 권한을 통해 여정 관리자가 여정을 작성, 읽기 및 삭제할 수 있는 낮은 수준의 권한이 만들어집니다.

## 여정 기능 {#journey-capability}

### [!DNL Manage journeys] 권한 {#manage-journeys}

다음 **[!DNL Manage journeys]** 높은 수준의 권한을 통해 사용자는 여정 흐름을 작성하기 위해 여정 캔버스에서 사용되는 개체에 액세스할 수 있을 뿐만 아니라, 기존 여정을 새로 만들고 편집/삭제할 수 있습니다.

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

### [!DNL Publish journeys] 권한 {#publish-journeys}

다음 **[!DNL Publish journeys]** 높은 수준의 권한을 통해 사용자가 여정을 게시할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 권한 {#view-journeys}

다음 **[!DNL View journeys]** 높은 수준의 권한을 통해 사용자가 여정을 탐색하고 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * journeys.read

* Adobe Experience Platform 특정:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 권한 {#manage-journeys-events}

다음 **[!DNL Manage journeys events, data sources and actions]** 높은 수준의 권한을 통해 사용자는 이벤트 및 데이터 구성을 구성할 수 있습니다.

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

### [!DNL View journeys events, data sources and actions] 권한 {#view-journeys-event}

다음 **[!DNL View journeys events, data sources and actions]** 높은 수준의 권한을 사용하면 여정 흐름에서 이벤트와 데이터를 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * 여정_events.read
   * 여정_data_sources.read
   * 여정_actions.read

* Adobe Experience Platform 특정:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] 권한 {#view-journeys-report}

다음 **[!DNL View journeys report]** 높은 수준의 권한을 통해 사용자는 읽기 전용 여정 보고서를 볼 수 있습니다.

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

### [!DNL Manage messages] 권한 {#manage-messages}

다음 **[!DNL Manage messages]** 높은 수준의 권한을 통해 사용자는 메시지를 만들고 편집/삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform 특정:
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] 권한 {#mange-messages-preview}

다음 **[!DNL Manage messages preview and test]** 높은 수준의 권한을 통해 사용자는 개인화된 메시지를 미리 볼 수 있습니다.

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

### [!DNL Publish messages] 권한 {#publish-messages}

다음 **[!DNL Publish messages]** 높은 수준의 권한을 통해 사용자가 메시지를 게시할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.publish

* Adobe Experience Platform 특정:
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] 권한 {#view-messages}

다음 **[!DNL View messages]** 높은 수준의 권한을 통해 사용자는 메시지만 읽을 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform 특정:
   * schemas.read
   * segments.read

### [!DNL View messages report] 권한 {#view-message-reports}

다음 **[!DNL View messages report]** 높은 수준의 권한을 통해 사용자는 읽기 전용 전자 메일 및 푸시 보고서를 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 의사 결정 관리 기능 {#decisions-permissions}

### [!DNL Manage decisions] 권한 {#manage-decisioning}

다음 **[!DNL Manage decisions]** 높은 수준의 권한을 통해 사용자는 기존 사용자를 새로 만들고 편집/삭제할 수 있습니다 **[!DNL Activity entities]**&#x200B;뿐만 아니라 이러한 활동에서 결정을 내리는 데 사용되는 개체를 관리합니다.

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

### [!DNL View decisions] 권한 {#view-decisions}

다음 **[!DNL View decisions]** 높은 수준의 권한을 통해 사용자는 기존 활동 및 관련 비즈니스 개체를 사용하여 결정을 내릴 수 있습니다.

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

### [!DNL Publish offers decisioning] 권한 {#publish-decisions}

다음 **[!DNL Publish offers decisioning]** 높은 수준의 권한을 통해 사용자는 오퍼 활동을 승인/승인하지 않을 수 있습니다.

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

### [!DNL Manage ranking strategies] 권한 {#manage-decisions}

다음 **[!DNL Manage ranking strategies]** 높은 수준의 권한을 통해 사용자는 사용자 지정 메시지 보고서를 읽고, 만들고, 편집하고, 삭제할 수 있으며 작업 기능을 사용할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* 의사 결정 관리 특정:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 관리 기능 {#administration-permissions}

### [!DNL Manage subdomains delegation] 권한 {#manage-subdomain}

다음 **[!DNL Manage subdomains delegation]** 높은 수준의 권한을 통해 사용자는 하위 도메인 위임(IP 풀 포함)을 생성, 편집 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] 권한 {#manage-ptr}

다음 **[!DNL Manage PTR records]** 높은 수준의 권한을 통해 사용자는 하위 도메인을 기반으로 구성된 PTR 레코드를 읽고 편집할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] 권한 {#view-ptr}

다음 **[!DNL View PTR records]** 높은 수준의 권한을 통해 사용자는 하위 도메인을 기반으로 구성된 PTR 레코드를 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] 권한 {#manage-ip-pools}

다음 **[!DNL Manage IP pools]** 높은 수준 권한을 사용하면 친화성 정의를 생성, 편집 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] 권한 {#manage-message-settings}

다음 **[!DNL Manage messages general settings]** 높은 수준의 권한을 통해 사용자는 샌드박스 수준에서 전역 설정을 만들고, 편집하고, 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform 특정:
   * schemas.read

### [!DNL View messages general settings] 권한 {#view-message-settings}

다음 **[!DNL View messages general settings]** 높은 수준의 권한을 통해 사용자는 실행 주소와 같은 메시지 일반 설정을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_general_settings.read
* Adobe Experience Platform 특정:
   * schemas.read

### [!DNL Manage messages presets] 권한 {#manage-message-presets}

다음 **[!DNL Manage messages presets]** 높은 수준의 권한을 사용하면 샌드박스 수준에서 채널 간에 메시지 사전 설정을 만들고, 편집하고, 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (Adobe Experience Platform Launch에서)

### [!DNL View messages presets] 권한 {#view-message-presets}

다음 **[!DNL View messages presets]** 높은 수준의 권한을 사용하면 메시지를 만들 때 사용할 메시지 사전 설정을 알기 위해 메시지 사전 설정을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (Adobe Experience Platform 데이터 수집에서)

### [!DNL Manage suppression] 권한 {#manage-suppression}

다음 **[!DNL Manage suppression]** 높은 수준의 권한을 통해 사용자는 전자 메일 주소가 제외 목록에 추가되기 전에 바운스 수를 정의하고 제외 목록에 항목을 추가 및 삭제할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] 권한 {#view-suppression-list}

다음 **[!DNL View suppression list]** 높은 수준의 권한을 통해 사용자는 억제 목록 콘텐츠 및 설정을 볼 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * suppression_list.view

* Adobe Experience Platform 특정:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 권한 {#export-suppression-list}

다음 **[!DNL Export suppression list]** 높은 수준의 권한을 통해 사용자는 억제 목록을 CSV 파일로 다운로드할 수 있습니다.

여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

* Journey Optimizer 특정:
   * suppression_list.export

* Adobe Experience Platform 특정:
   * profiles.read
   * datasets.read
