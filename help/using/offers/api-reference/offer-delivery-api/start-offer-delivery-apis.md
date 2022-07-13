---
title: 오퍼 배달 API 시작
description: 개인화된 오퍼를 전달하는 데 사용할 수 있는 API에 대해 자세히 알아보십시오.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 4%

---

# 오퍼 배달 API 시작 {#about-decisioning-apis}

다음 중 하나를 사용하여 오퍼를 제공할 수 있습니다 **의사결정** 또는 **Edge Decisioning** API. 또한 **Batch Decisioning** API를 사용하면 한 번의 호출로 주어진 세그먼트의 모든 프로필에 오퍼를 전달할 수 있습니다. 세그먼트의 각 프로필에 대한 오퍼 콘텐츠는 사용자 지정 일괄 처리 워크플로우에 사용할 수 있는 Adobe Experience Platform 데이터 세트에 배치됩니다.

이 페이지에서는 와 함께 사용 가능한 특정 기능에 대한 정보를 확인할 수 있습니다 **의사결정** 및 **Edge Decisioning** API. 두 가지 모두 고객에게 오퍼를 제공할 수 있지만, **Edge Decisioning** 인바운드 사용 사례와 플랫폼에서 향상된 지연 및 처리량을 보장하기 위해 가능한 한 항상 API입니다.

|  | 요청 수/초 | 지연 |
|---|---|---|
| Decisioning API | 2000년 | &lt;500ms |
| Edge Decisioning API | 5000년 | &lt;250ms |

API 작업 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.
* [의사 결정 API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

## Edge Decisioning API 기능 {#edge}

**경험 이벤트 및 의사 결정 요청에 대한 고유 요청**

Edge Decisioning API를 사용하면 두 개의 서로 다른 요청이 아닌 하나의 요청으로 경험 이벤트 자체를 의사 결정 요청과 함께 보낼 수 있습니다.

예를 들어 고객이 웹 사이트를 방문하는 경우 이 요청에는 경험 이벤트(고객의 페이지 방문)가 포함되며 오퍼를 다시 가져와 방문 페이지를 채웁니다.

**Adobe Experience Platform에 컨텍스트 데이터 저장 공간**

컨텍스트 데이터는 오퍼를 다시 가져올 때만 알고 있는 데이터를 나타냅니다. 예를 들어 구매한 문서의 색상, 구매 시 날씨 등이 있습니다.

Edge Decisioning API 요청을 사용하여 컨텍스트 데이터를 전달할 때 데이터가 Adobe Experience Platform 프로필에 저장되므로 향후 재사용할 수 있습니다.

>[!NOTE]
>
>컨텍스트 데이터를 저장하려면 전용 XDM 스키마를 구성해야 합니다.

## Decisioning API 기능 {#decisioning}

아래 나열된 기능은 Decisioning API에서만 사용할 수 있습니다. 요구 사항을 충족하기 위해 이러한 중 하나를 활용해야 하는 경우 Decisioning API를 사용합니다. 그렇지 않으면 Edge Decisioning API를 사용하는 것이 좋습니다.

* **경험 이벤트**: 경험 이벤트를 활용하여 의사 결정 규칙을 만듭니다.
* **오퍼 콘텐츠 및 특성**: 전용 옵션을 사용하여 오퍼의 컨텐츠와 특성을 반환하지 않도록 선택할 수 있습니다.
* **오퍼 메타데이터**: 오퍼의 메타데이터를 반환하려면 옵션을 활성화합니다.
* **병합 정책**: 요청에서 샌드박스에 연결된 병합 정책과 다른 병합 정책을 사용합니다.
* **의사 결정 이벤트 및 빈도 제한**: 발생하는 빈도 캡핑에서 의사 결정 이벤트를 카운트하지 않습니다.
* **중복된 proposition**: proposition을 중복 제거하지 않는 옵션을 활성화합니다.
