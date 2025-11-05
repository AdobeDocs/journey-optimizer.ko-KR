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
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# inAudience 함수 {#inAudience}

`inAudience` 함수는 여정의 개인이 특정 대상에 속하는지 여부를 확인할 수 있는 Adobe Experience Platform 함수입니다. 이 강력한 기능을 사용하면 대상자 멤버십을 기반으로 개인화된 여정 경로를 만들 수 있으므로 고객 경험 내에서 정교한 세분화 및 타겟팅을 가능하게 합니다.

다음을 수행해야 하는 경우 `inAudience` 함수를 사용합니다.

* 대상자 멤버십을 기반으로 여정 경로를 분기합니다. [자세히 알아보기](../condition-activity.md#using-a-segment)
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

| 매개변수 | 설명 | 유형 |
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

+++예

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

## 관련 항목

Adobe Journey Optimizer에서 대상 사용에 대해 자세히 알아보기:

* **[대상 정보](../../audience/about-audiences.md)** - 대상을 만들고 관리하는 방법을 포함하여 Adobe Experience Platform 및 Journey Optimizer에서 대상이 작동하는 방식을 이해합니다.
* **[대상 활동 읽기](../read-audience.md)** - 대상을 사용하여 여정 항목을 트리거하고 모든 대상 구성원이 여정을 입력하도록 할 수 있습니다.
* **[대상 자격 이벤트](../audience-qualification-events.md)** - 대상의 프로필 시작 및 종료를 수신하여 실시간으로 여정 작업을 트리거합니다.
* **[조건에서 대상 사용](../condition-activity.md#using-a-segment)** - 조건 활동을 사용하여 대상 멤버십을 기반으로 조건부 여정 경로를 만듭니다.
* **[여정 속성 - 병합 정책](../journey-properties.md)** - inAudience 함수와 함께 여러 대상을 사용할 때 병합 정책이 작동하는 방식을 이해합니다.

