---
product: journey optimizer
title: inAudience 함수
description: Adobe Experience Platform inAudience 함수에 대해 알아봅니다
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, 함수, 표현식, 여정, 대상, 세그멘테이션
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 1%

---

# inAudience 함수 {#inAudience}

`inAudience` 함수는 여정의 개인이 특정 대상에 속하는지 여부를 확인할 수 있는 Adobe Experience Platform 함수입니다. 이 강력한 기능을 사용하면 대상자 멤버십을 기반으로 개인화된 여정 경로를 만들 수 있으므로 고객 경험 내에서 정교한 세분화 및 타겟팅을 가능하게 합니다.

다음을 수행해야 하는 경우 `inAudience` 함수를 사용합니다.

* 대상자 멤버십을 기반으로 여정 경로를 분기합니다. [자세히 알아보기](../conditions.md#using-a-segment)
* 프로필이 특정 세그먼트에 속하는지 여부에 따라 달라지는 조건부 논리 적용
* 개인화된 경험을 가진 특정 고객 그룹 타기팅
* 여정 조건 내에서 실시간 대상 참여 평가
* 여러 대상 검사를 결합하여 복잡한 타깃팅 규칙 만들기

이 함수는 실시간으로 대상 멤버십을 평가하고 부울 값을 반환하므로 의사 결정 노드 및 조건부 표현식에 이상적입니다. 대상은 [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"}에서 정의 및 관리되며(Journey Optimizer에서 [대상 작업](../../audience/about-audiences.md)에 대해 자세히 알아보기), 표현식 편집기에서 자동 완성 제안 사항을 제공하므로 정확하게 참조할 수 있습니다.

**대상 상태:**

대상에는 두 가지 참여 상태가 있을 수 있습니다.

* **실현됨**: 개인이 대상 정의에 적합하며 활성 멤버입니다.
* **종료됨**: 개인이 대상을 떠났으므로 더 이상 자격이 없습니다.

**실현됨** 상태의 개인만 활성 대상 구성원으로 간주됩니다. 함수가 `true`을(를) 반환하면 개인이 실현된 상태를 확인하고 `false`을(를) 반환하면 종료된 상태를 나타냅니다. 대상 평가에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=ko#interpret-segment-results){target="_blank"}를 참조하세요.

+++구문

`inAudience(<parameter>)`

+++

+++매개변수

| 매개 변수 | 설명 | 유형 |
|--- |--- |--- |
| 대상자 | 대상자 이름 | `<string>` |

**중요 제약 조건:**

* 대상 이름은 문자열 상수여야 합니다.
* 필드 참조 또는 식일 수 없습니다.
* 단일 여정에서 최대 100개의 대상을 검색할 수 있습니다

+++

+++서명 및 반환된 유형

`inAudience(<string>)`

부울 반환:
* `true`: 개인이 대상의 구성원입니다(실현된 상태).

* `false`: 개인이 대상의 구성원이 아닙니다(종료됨 상태).

+++

+++예시

`inAudience("men over 50")`

여정 인스턴스 내의 개인이 &quot;50세 이상 남성&quot;이라는 Adobe Experience Platform 대상에 속하면 **true**&#x200B;을 반환하고 그렇지 않으면 **false**&#x200B;을 반환합니다.

**실제 사용 사례:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## 가드레일 및 제한 사항 {#guardrails}

여정에서 `inAudience` 함수를 사용하는 경우 다음 보호 기능 및 제한 사항에 유의하십시오.

**대상 검색 제한:**
* 단일 여정 내에서 최대 100개의 대상을 검색할 수 있습니다
* 표현식 편집기는 사용 가능한 대상자의 자동 완성 목록을 제공하여 대상자를 올바르게 참조하는 데 도움을 줍니다

**매개 변수 제약 조건:**
* 대상 이름은 문자열 상수여야 합니다.
* 필드 참조 및 표현식은 매개 변수로 지원되지 않습니다.

**대상 이름 변경:**
* Adobe Experience Platform에서 기존 대상자의 이름을 변경해도 여정 표현식에서 해당 대상자에 대한 참조가 자동으로 업데이트되지 않습니다
* 조건 노드에서 `inAudience('oldAudienceName')`을(를) 사용하는 경우 새 이름을 사용하도록 식을 수동으로 편집해야 합니다
* 대상 이름을 업데이트하지 않으면 여정 조건이 중단되고 잘못된 여정 동작이 발생할 수 있습니다

**병합 정책 고려 사항:**
* `inAudience` 함수와 함께 여러 대상을 사용하는 경우 병합 정책과 일치하지 않으면 오류나 경고가 발생할 수 있습니다
* 병합 정책 동작에 대한 자세한 내용은 [여정 속성](../journey-properties.md)을 참조하세요.

**전파 시간:** {#propagation-timing}

조건 노드에서 `inAudience()`을(를) 사용할 때 여정 멤버십 평가 시간은 조건이 세그먼트에 나타나는 위치에 따라 달라집니다.

* **대상 읽기 여정에서 대기 활동 전:** Journey Optimizer이 프로필의 일괄 처리 프로젝션에서 읽습니다. 이 프로젝션의 데이터는 수집 후 **2시간** 내에 새로 고쳐집니다. 일 기반 또는 시간 기반 조건에 의존하는 대상자는 추가적인 지연을 경험할 수 있습니다. 여정 시작 시 짧은 [대기 활동](../wait-activity.md)을 추가하거나 버퍼 시간을 허용하여 최신 세그먼트 멤버십이 반영되도록 하십시오.
* **단일 이벤트 여정에서 또는 대기 활동 후에** 세그먼트 멤버십을 스트리밍(단일) 프로젝션에서 읽습니다. 데이터는 일반적으로 **15분** 내에 사용할 수 있습니다. 자세한 내용은 [Adobe Experience Platform 스트리밍 수집 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/ingestion/streaming/overview){target="_blank"}를 참조하세요.

## 관련 항목

Adobe Journey Optimizer에서 대상 사용에 대해 자세히 알아보기:

* **[대상 정보](../../audience/about-audiences.md)** - 대상을 만들고 관리하는 방법을 포함하여 Adobe Experience Platform 및 Journey Optimizer에서 대상이 작동하는 방식을 이해합니다.
* **[대상 활동 읽기](../read-audience.md)** - 대상을 사용하여 여정 항목을 트리거하고 모든 대상 구성원이 여정을 입력하도록 할 수 있습니다.
* **[대상 자격 이벤트](../audience-qualification-events.md)** - 대상의 프로필 시작 및 종료를 수신하여 실시간으로 여정 작업을 트리거합니다.
* **[조건에서 대상 사용](../conditions.md#using-a-segment)** - 최적화 활동을 사용하여 대상 멤버십을 기반으로 조건부 여정 경로를 만듭니다.
* **[여정 속성 - 병합 정책](../journey-properties.md)** - inAudience 함수와 함께 여러 대상을 사용할 때 병합 정책이 작동하는 방식을 이해합니다.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 `inAudience` 함수를 문서화합니다. 이 함수는 여정 프로필이 명명된 Adobe Experience Platform 대상에 속하는지 여부를 실시간으로 확인하고 여정 조건에 사용된 부울을 반환합니다.

**의도:**
* `inAudience`을(를) 사용하여 프로필이 특정 대상의 구성원인지 여부를 기준으로 여정 경로를 분기합니다.
* 여러 `inAudience` 검사를 AND/OR 논리와 결합하여 복잡한 타깃팅 조건을 만듭니다.
* 프로필이 부정 확인(`inAudience("...") == false`)을 사용하여 특정 대상자를 입력하지 않았는지 확인하십시오.
* 대상자 읽기 여정과 단일 이벤트 여정 간의 전달 타이밍 차이를 이해합니다
* Adobe Experience Platform의 대상 이름 변경으로 인해 손상된 대상 참조를 식별하고 수정합니다

**용어집:**
* **실현됨**: 개인이 현재 대상 정의에 적합하고 활성 구성원 *(제품별)임을 나타내는 대상 참가 상태입니다.*
* **종료됨**: 개인이 대상을 떠났으며 더 이상 *(제품별)을(를) 사용할 수 없음을 나타내는 대상 참여 상태*
* **병합 정책**: 대상 멤버십 *(제품별)을(를) 평가할 때 여러 데이터 세트의 프로필 데이터가 결합되는 방법을 결정하는 Adobe Experience Platform의 규칙입니다*
* **일괄 프로젝션**: 대상자 읽기 여정 *(제품별)에서 사용하는 일정에 따라(수집 후 2시간 이내) 프로필 데이터 저장소가 새로 고쳐졌습니다.*
* **스트리밍 프로젝션**: 단일 이벤트 여정 및 대기 활동 후에 사용되는 실시간 프로필 데이터 저장소(일반적으로 15분 이내에 사용 가능) *(제품별)*

**보호 기능:**
* 단일 여정은 최대 100개의 대상을 검색할 수 있습니다
* 대상 이름 매개 변수는 문자열 상수여야 합니다. 필드 참조 및 동적 표현식은 지원되지 않습니다.
* Adobe Experience Platform에서 대상의 이름을 바꾸면 여정 식에서 `inAudience` 참조가 자동으로 업데이트되지 않습니다. 수동 업데이트가 필요합니다.
* 동일한 여정에서 사용된 여러 대상 간에 일관성 없는 병합 정책으로 인해 오류 또는 경고가 발생할 수 있습니다

**용어:**
* 정식 이름: inAudience — 약어: none — 변형: inSegment(기존 이름)
* 동의어: &quot;inAudience&quot; = &quot;audience membership check function&quot;
* 혼동하지 마십시오. &quot;인식됨&quot;(활성 멤버) ≠ &quot;종료됨&quot;(더 이상 멤버 아님)
* 혼동하지 마십시오. &quot;inAudience&quot;(현재 함수) ≠ &quot;inSegment&quot;(더 이상 사용되지 않는 레거시 함수)

**FAQ:**
* **Q: 프로필이 대상자를 종료하면 `inAudience`에서 반환하는 것은 무엇입니까?** — `false`을(를) 반환합니다. &quot;실현됨&quot; 상태의 프로필만 활성 구성원으로 간주되어 `true`을(를) 반환합니다.
* **Q: 단일 여정에서 몇 명의 대상을 확인할 수 있습니까?** — 단일 여정 내에서 최대 100개의 대상을 검색할 수 있습니다.
* **Q: 여정에서 대상을 사용한 후 Adobe Experience Platform에서 대상의 이름을 변경하면 어떻게 됩니까?** — 여정 표현식이 자동으로 업데이트되지 않습니다. 새 대상 이름을 사용하려면 `inAudience` 호출을 수동으로 편집해야 합니다. 그렇지 않으면 조건이 중단됩니다.
* **Q: 대상자 읽기 여정에서 프로필을 업데이트한 후 대상자 멤버십을 얼마나 빨리 사용할 수 있습니까?** — 대기 활동 전 대상 읽기 여정에서 수집 후 2시간 이내에 새로 고친 배치 투영에서 데이터를 읽습니다.
* **Q: 프로필 특성을 대상 이름 매개 변수로 전달할 수 있습니까?** — 아니요. 대상 이름은 문자열 상수여야 합니다. 필드 참조 및 표현식은 지원되지 않습니다.

+++
