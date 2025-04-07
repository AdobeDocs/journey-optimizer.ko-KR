---
solution: Journey Optimizer
product: journey optimizer
title: 권한 수준
description: 사용자가 다양한 기능에 액세스할 수 있는 높은 수준 및 낮은 수준의 권한에 대해 알아봅니다.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: 권한, 높은 수준, 낮은 수준, 프로필, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# 권한 수준 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

각 역할은 사용자가 다양한 기능에 액세스할 수 있는 권한으로 구성됩니다.
두 가지 유형으로 나눌 수 있습니다.

* **높은 수준의 권한**: **[!DNL Publish journeys]** 및 **[!DNL Manage subdomains delegation]**&#x200B;과(와) 같이 **[!UICONTROL 역할]**&#x200B;에 할당할 수 있는 다양한 권한을 나타냅니다. 높은 수준의 권한은 낮은 수준의 권한을 포함합니다. 높은 수준의 사용 권한이 [이 페이지](ootb-permissions.md)에 자세히 설명되어 있습니다.

* **낮은 수준의 사용 권한**: 높은 수준의 사용 권한에서 가져온 다양한 사용 권한을 나타냅니다.

예를 들어 **[!DNL Journey administrator]** 역할에는 **[!DNL Manage journeys]** 권한이 할당됩니다. 이 권한으로 인해 여정 관리자가 여정을 작성, 읽기 및 삭제할 수 있는 낮은 수준의 권한이 생깁니다.

## 여정 리소스 {#journey-capability}

* **[!DNL Manage journeys]** 높은 수준의 권한을 통해 사용자는 새 여정을 만들고 기존 여정을 편집/삭제할 수 있을 뿐만 아니라 여정 흐름을 만들기 위해 캔버스에 사용되는 개체에 액세스할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:

      * journeys.read
      * journeys.write
      * journeys.delete
      * messages.read

   * Adobe Experience Platform 관련:

      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read

+++

* **[!DNL Publish journeys]**&#x200B;개의 높은 수준의 권한으로 사용자가 여정을 게시할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** 높은 수준의 사용 권한을 통해 여정을 검색하고 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * journeys.read

   * Adobe Experience Platform 관련:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** 높은 수준의 권한을 통해 사용자가 이벤트 및 데이터 구성을 구성할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * 여정_events.read
      * 여정_events.write
      * 여정_events.delete
      * 여정_data_sources.read
      * 여정_data_sources.write
      * 여정_data_sources.delete
      * 여정_actions.read
      * 여정_actions.write
      * 여정_actions.delete

   * Adobe Experience Platform 관련:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys events, data sources and actions]** 높은 수준의 권한을 통해 사용자는 여정 흐름에서 이벤트와 데이터를 사용할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * 여정_events.read
      * 여정_data_sources.read
      * 여정_actions.read

   * Adobe Experience Platform 관련:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** 높은 수준의 권한으로 사용자가 읽기 전용 여정 보고서를 사용할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * 여정_report.read
      * messages_report.read

   * Adobe Experience Platform 관련:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Journey Optimizer 규칙 리소스 {#journey-rules-capability}

* **[!DNL Manage frequency rules]** 높은 수준의 사용 권한을 통해 사용자가 빈도 규칙을 읽고, 만들고, 편집하고, 삭제하고, 활성화/비활성화할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** 높은 수준의 사용 권한을 통해 사용자가 빈도 규칙을 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * frequency_rules.read

+++

## 캠페인 리소스 {#campaign-capability}

* **[!DNL Export suppression list]** 높은 수준의 권한을 통해 사용자가 비표시 목록을 CSV 파일로 다운로드할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * suppression_list.export

   * Adobe Experience Platform 관련:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]** 높은 수준의 권한을 통해 사용자가 캠페인을 새로 만들고 편집/삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** 높은 수준의 권한으로 사용자가 캠페인을 게시할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:

      * 캠페인 읽기
      * campaign-게시
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** 높은 수준의 권한으로 사용자가 캠페인 보고서를 읽고 편집할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## 의사 결정 관리 리소스 {#decisions-permissions}

* **[!DNL Manage decisions]** 높은 수준의 권한을 통해 사용자는 새로운 항목을 만들고 기존 **[!DNL Activity entities]**&#x200B;을(를) 편집/삭제할 수 있을 뿐만 아니라 해당 활동에 사용된 개체를 관리하여 결정을 내릴 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

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

   * Adobe Experience Platform 관련:
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]** 높은 수준의 권한을 통해 사용자는 기존 활동 및 관련 비즈니스 개체를 사용하여 결정을 내릴 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * 의사 결정 관리 특정:
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Adobe Experience Platform 관련:
      * schemas.read
      * segment.read
      * datasets.read

+++

* **[!DNL Manage offers]** 높은 수준의 권한을 통해 사용자는 모든 오퍼, 구성 요소를 만들고 편집하고 삭제할 수 있으며, 의사 결정 및 컬렉션을 읽을 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * 의사 결정 관리 특정:
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Adobe Experience Platform 관련:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** 높은 수준의 권한을 통해 사용자가 순위 전략을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * 의사 결정 관리 특정:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## 채널 구성 리소스 {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ It includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* **[!DNL Manage file routing]** 높은 수준의 사용 권한을 통해 사용자가 파일 라우팅 구성을 만들고 편집하고 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* **[!DNL Manage IP pools]** 높은 수준의 권한을 통해 사용자는 선호도 정의를 만들고 편집하고 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]** 높은 수준의 권한을 통해 사용자가 랜딩 페이지 하위 도메인 및 사전 설정 설정을 읽고, 만들고, 편집할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]** 높은 수준의 권한을 통해 사용자는 샌드박스 수준에서 전역 설정을 만들고 편집하고 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Adobe Experience Platform 관련:
      * schemas.read

+++

* **[!DNL Manage messages presets]** 높은 수준의 권한을 통해 사용자는 샌드박스 수준의 채널 전체에서 채널 구성을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * 데이터 수집별:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]** 높은 수준의 권한을 통해 사용자는 하위 도메인을 기반으로 구성된 PTR 레코드를 읽고 편집할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]** 높은 수준의 사용 권한을 통해 사용자가 Seedlist를 읽고 만들고 편집하고 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]** 고급 권한으로 사용자는 SMS 하위 도메인을 읽고, 만들고, 편집하고, 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegations]** 높은 수준의 권한을 통해 사용자는 하위 도메인 위임(IP 풀 포함)을 만들고 편집하고 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]** 높은 수준의 사용 권한을 사용하면 비표시 목록에 이메일 주소를 추가하기 전에 반송 수를 정의하고 비표시 목록에 항목을 추가 및 삭제할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]** 높은 수준의 사용 권한을 통해 사용자가 파일 라우팅 구성을 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:

      * file_routing.read

+++

* **[!DNL View messages general settings]** 높은 수준의 사용 권한을 통해 사용자는 실행 주소와 같은 일반 설정 메시지를 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * messages_general_settings.read

   * Adobe Experience Platform 관련:
      * schemas.read

+++

* **[!DNL View messages presets]**&#x200B;개의 높은 수준 권한으로 사용자는 메시지 사전 설정을 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * 데이터 수집별:
      * Mobile_setting.read

+++

* **[!DNL View PTR records]** 높은 수준의 권한을 통해 사용자는 하위 도메인을 기반으로 구성된 PTR 레코드를 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.
   * Journey Optimizer 관련:

      * PTR_records.read
      * subdomains_delegation.read

+++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]** 높은 수준의 사용 권한을 통해 사용자가 제외 목록 콘텐츠 및 설정을 볼 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준의 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * suppression_list.view

   * Adobe Experience Platform 관련:
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

## AI 지원 리소스 {#ai-permissions}

* **[!DNL Generate content]**&#x200B;개의 높은 수준의 권한을 통해 사용자가 Journey Optimizer의 AI Assistant에 액세스할 수 있습니다.

+++ 여기에는 다음과 같은 낮은 수준 권한이 포함됩니다.

   * Journey Optimizer 관련:
      * ai-assistant-generated-content.generate

+++
