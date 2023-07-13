---
title: 오퍼 게재 API 시작
description: 개인화된 오퍼를 제공하는 데 사용할 수 있는 API에 대해 자세히 알아보십시오.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 6%

---

# 오퍼 게재 API 시작 {#about-decisioning-apis}

다음 중 하나를 사용하여 오퍼를 게재할 수 있습니다. **의사 결정** 또는 **Edge Decisioning** API. 또한 **일괄 의사 결정** API를 사용하면 한 번의 호출로 주어진 대상의 모든 프로필에 오퍼를 게재할 수 있습니다. 대상의 각 프로필에 대한 오퍼 콘텐츠는 사용자 지정 일괄 처리 워크플로우에 사용할 수 있는 Adobe Experience Platform 데이터 세트에 배치됩니다.

이 페이지에서는 사용 가능한 특정 기능에 대한 정보를 확인할 수 있습니다. **의사 결정** 및 **Edge Decisioning** API. 둘 다 고객에게 오퍼를 게재할 수 있지만 **Edge Decisioning** 인바운드 사용 사례와 플랫폼에서 더 나은 지연 시간 및 처리량을 보장하기 위해 가능한 한 항상 API입니다.

|  | 요청/초 | 지연 |
|---|---|---|
| Decisioning API | 2000 | &lt;500ms |
| Edge Decisioning API | 5000 | &lt;250ms |

API 작업 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

## Edge Decisioning API 기능 {#edge}

**경험 이벤트 및 의사 결정 요청에 대한 고유 요청**

Edge Decisioning API를 사용하면 두 개의 서로 다른 요청이 없는 대신, 하나의 단일 요청에서 Decisioning 요청과 함께 경험 이벤트 자체를 보낼 수 있습니다.

예를 들어 고객이 웹 사이트를 방문하는 경우 요청에는 경험 이벤트(고객의 페이지 방문)가 포함되고, 오퍼를 다시 가져와서 방문한 페이지를 채웁니다.

**Adobe Experience Platform에 컨텍스트 데이터 스토리지**

컨텍스트 데이터는 오퍼를 반환하려는 시점에만 알고 있는 데이터를 나타냅니다. 예를 들어 구입한 문서의 색상, 구입 시 날씨 등이 여기에 해당합니다.

Edge Decisioning API 요청을 사용하여 컨텍스트 데이터를 전달할 때 데이터가 Adobe Experience Platform 프로필에 저장되므로 나중에 다시 사용할 수 있습니다.

>[!NOTE]
>
>컨텍스트 데이터를 저장하려면 전용 XDM 스키마가 구성되어 있어야 합니다.

## API 기능 결정 {#decisioning}

아래 나열된 기능은 Decisioning API를 통해서만 사용할 수 있습니다. 이들 중 하나를 활용하여 요구 사항을 충족해야 하는 경우 Decisioning API를 사용하십시오. 그렇지 않으면 Edge Decisioning API를 사용하는 것이 좋습니다.

* **경험 이벤트**: 경험 이벤트를 활용하여 의사 결정 규칙을 만듭니다.
* **오퍼 콘텐츠 및 특성**: 전용 옵션을 사용하여 오퍼의 콘텐츠 및 특성을 반환하지 않도록 선택할 수 있습니다.
* **오퍼 메타데이터**: 오퍼의 메타데이터를 반환하는 옵션을 활성화합니다.
* **병합 정책**: 샌드박스에 연결된 정책과 다른 병합 정책을 요청에 사용합니다.
* **이벤트 및 빈도 결정**: 발생하는 빈도 캡핑에 의해 이벤트 계산이 차단됩니다.
* **중복 제안**: 제안에 대한 중복 제거를 수행하지 않는 옵션을 활성화합니다.
