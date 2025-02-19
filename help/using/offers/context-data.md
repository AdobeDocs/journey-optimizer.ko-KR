---
product: experience platform
solution: Experience Platform
title: 컨텍스트 데이터 시작
description: 의사 결정 관리에 컨텍스트 데이터를 활용하는 방법을 알아봅니다.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# 컨텍스트 데이터 시작 {#context-data}

의사 결정 요청의 일부로 전송된 데이터는 컨텍스트 데이터로 간주됩니다. 예를 들어 의사 결정 엔진의 컨텍스트 데이터를 활용하여 의사 결정 요청이 수행될 때 현재 날씨가 ≥80도여야 하는 의사 결정 규칙을 디자인할 수 있습니다.

컨텍스트 데이터는 **Decisioning**&#x200B;과(와) **Edge Decisioning** API 요청 간에 다르게 정의됩니다. 두 유형의 요청 모두에 대해 컨텍스트 데이터는 자격 규칙 또는 등급 공식에 사용할 수 있지만, Edge Decisioning API 요청만 컨텍스트 데이터를 사용하여 콘텐츠를 개인화할 수 있습니다.

시작하기 전에 다음 보호 기능 및 제한 사항을 확인하십시오.

* Decisioning 호출과 Edge Decisioning 호출 간에 컨텍스트를 전달하는 방식이 다르기 때문에 컨텍스트 기반 자격 규칙 및 등급 공식은 Decisioning 호출과 Edge Decisioning 호출 간에 상호 교환되지 않습니다.
* Decisioning API에서만 `dryrun` 매개 변수로 테스트할 수 있습니다. Edge Decisioning API에서는 사용할 수 없습니다. Decisioning API를 사용하여 이 매개 변수를 `true`(으)로 설정하면 최대 용량 및 제안 수에 영향을 주지 않습니다.

각 API에서 컨텍스트 데이터를 사용하는 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [Edge Decisioning 요청에서 컨텍스트 데이터 사용](context-data-edge.md)
* [의사 결정 요청에서 컨텍스트 데이터 사용](context-data-decisioning.md)

