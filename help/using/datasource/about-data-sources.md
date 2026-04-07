---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 소스 시작
description: 데이터 소스를 시작하는 방법 알아보기
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 데이터, 소스, 여정, 플랫폼
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 8521e59022c221c0ca4e5b69b5b3aefe6304b417
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 35%

---

# 데이터 소스 시작 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="데이터 소스 정보"
>abstract="데이터 소스는 항상 기술 사용자가 구성해야 합니다. 데이터 소스를 구성하면 여정에서 사용할 추가 정보 검색을 위해 시스템에 대한 연결을 정의할 수 있습니다. 이러한 추가 정보에는 조건 정의, 작업의 매개변수 및 개인화 데이터, 사용자 정의 대기 정의, 시간대 정의 등이 있습니다."

>[!TIP]
>Journey Optimizer에서 데이터 관리를 처음 사용하십니까? 데이터 소스를 구성하기 전에 스키마, 데이터 세트, ID 및 데이터 흐름 방법을 이해하려면 [데이터 관리 시작하기](../data/gs-data.md) 개요로 시작하십시오.

데이터 소스를 구성하면 여정에서 사용할 추가 정보 검색을 위해 시스템에 대한 연결을 정의할 수 있습니다. 이러한 추가 정보에는 다음과 같은 항목이 포함됩니다.

* [조건 정의](../building-journeys/conditions.md)
* [작업](../action/action.md)의 매개 변수 및 개인화 데이터
* [사용자 지정 대기 정의](../building-journeys/wait-activity.md#custom)
* [시간대 정의](../building-journeys/timezone-management.md)

➡️ [비디오에서 이 기능 살펴보기](#video)

여정이 이벤트 페이로드에서 전송되는 로컬 데이터만 활용하는 경우에는 이 구성을 수행하지 않아도 됩니다. 예를 들어 여정이 이벤트, 그리고 이벤트의 데이터만 사용하는 채널 작업 활동으로 구성된 경우 데이터 소스를 구성할 필요가 없습니다.

데이터 소스에는 다음의 두 가지 유형이 있습니다.

* 실시간 고객 프로필 서비스에 대한 연결을 정의하는 **사전 구성된** Adobe Experience Platform 데이터 원본입니다. 데이터 소스(기본 제공 데이터 소스). [이 페이지](../datasource/adobe-experience-platform-data-source.md)를 참조하십시오.
* 외부 시스템에 대한 연결을 정의할 수 있는 **external** 데이터 원본입니다. 이러한 소스는 직접 만들 수 있습니다. [이 페이지](../datasource/external-data-sources.md)를 참조하십시오.

>[!NOTE]
>
>이제 응답이 지원되므로 외부 데이터 소스 사용 사례에서 데이터 소스 대신 사용자 지정 작업을 사용해야 합니다. 응답에 대한 자세한 내용은 이 [섹션](../action/action-response.md)을 참조하세요.

각 데이터 소스에서는 필드 그룹을 사용하여 검색할 정보를 정의합니다. 필드 그룹은 데이터 소스에서 검색할 수 있는 필드 세트입니다. [이 페이지](../datasource/configure-data-sources.md#define-field-groups)를 참조하십시오.

>[!NOTE]
>
>데이터 소스에 대해서는 스키마 관계가 지원되지 않습니다.

## 데이터 액세스 전략 선택 {#data-access-strategy}

데이터 소스를 구성하기 전에 사용 사례에 가장 적합한 접근 방식을 고려하십시오. 세 가지 옵션을 사용할 수 있으며, 각 옵션은 지속성, 프로필 보강 및 재사용 가능성 측면에서 서로 다른 장단점을 갖습니다. 이러한 옵션에 대한 자세한 내용은 [Journey Optimizer의 고급 여정 모범 사례](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}를 참조하십시오.

**옵션 1 — 사용자 지정 작업으로 외부 데이터에 액세스(데이터 레이크 없음)**

Experience Platform 데이터 레이크의 데이터를 유지하지 않고 여정 런타임 시 외부 API에 직접 연결합니다. 다음과 같은 경우에 가장 적합합니다.

* 이 데이터는 여정 컨텍스트 내에서만 유용하며 다른 곳에서는 필요하지 않습니다.
* 필요한 속성을 반환하는 API 끝점을 통해 외부 시스템에 액세스할 수 있습니다.

[사용자 지정 작업](../action/action.md) 및 [사용자 지정 작업 응답](../action/action-response.md)에 대해 자세히 알아보세요.

**옵션 2 — 데이터 레이크의 데이터 세트가 프로필에 대해 활성화되지 않음**

실시간 고객 프로필에 기여하지 않고 컨텍스트 기반 이벤트 데이터를 기반으로 여정을 트리거하고 개인화하기 위해 데이터 세트에 데이터를 수집합니다. 다음과 같은 경우에 가장 적합합니다.

* 레코드에는 Experience Platform에 이미 저장된 프로필에 액세스하는 데 사용할 수 있는 ID 필드가 포함되어 있습니다.
* Journey Optimizer 외부의 대상 만들기 또는 ID 결합에 데이터가 필요하지 않습니다.

**옵션 3 — 데이터 레이크의 프로필 사용 데이터 세트**

데이터를 [프로필이 활성화된 데이터 세트](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}에 수집하여 대상자를 만들고, ID 그래프를 보강하며, 여러 여정 및 RT-CDP 대상에서 데이터를 활용합니다. 다음과 같은 경우에 가장 적합합니다.

* 이 데이터는 Journey Optimizer 이외의 채널에 사용된 대상 정의에 유용합니다.
* 데이터에는 더욱 풍부하고 결합된 프로필 조각에 기여하는 여러 ID가 포함되어 있습니다.

| | 데이터 레이크에서 지속되는 데이터 | 프로필에 대해 데이터 세트 활성화됨 |
| --- | --- | --- |
| **옵션 1** — 사용자 지정 작업을 통한 외부 데이터 | 아니요 | 아니요 |
| **옵션 2** — 프로필에 대해 데이터 세트가 활성화되지 않음 | 예 | 아니요 |
| **옵션 3** — 프로필 사용 데이터 세트 | 예 | 예 |

Adobe Experience Platform 데이터 소스 및 외부 데이터 소스를 구성하는 방법, 그리고 여정에서 데이터를 찾아서 사용하는 방법과 관련된 자세한 내용을 확인하려면 이 [자습서 비디오](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}를 시청하십시오.

## 사용 방법 비디오 {#video}

데이터 소스의 정의를 이해하고 Experience Platform 및 외부 데이터 소스를 구성하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

