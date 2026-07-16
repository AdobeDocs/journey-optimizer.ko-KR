---
title: 템플릿 Personalization의 예
description: Journey Optimizer Personalization 예
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 1%

---

# 건강 계획 처방 이메일 {#plan-prescription}

>[!BEGINSHADEBOX]

**이 페이지에서:** 조건부 규칙을 사용하여 중첩된 프로필 배열을 반복하는 개인화 사용 사례를 따라 픽업 또는 회수할 준비가 된 상태 계획 전자 메일 목록 처방전을 작성하십시오.

>[!ENDSHADEBOX]

프로필에는 상태 플랜이 포함되어 있으며 각 플랜에는 처방이 포함됩니다. 처방에는 &quot;준비됨&quot;, &quot;회수&quot; 또는 &quot;수거&quot;와 같이 다양한 상태가 있습니다.

이 사용 사례에서는 수령하거나 회수할 준비가 된 모든 처방전을 포함하여 각 프로필에 하나의 이메일을 보내려고 합니다. 이 사용 사례를 구현하는 데 사용할 구문에 대한 자세한 내용을 보려면 아래의 각 탭을 클릭하십시오.

>[!BEGINTABS]

>[!TAB 렌더링된 메시지]

<p>안녕하세요, John Doe 님,</p>
<p>다음은 수령할 준비가 되었거나 회수된 처방전입니다.</p>

**상태 관리 계획 A**

<ul>

<li>
      <strong>처방전 ID:</strong> pres1<br>
      <strong>이름:</strong> 약물 A<br>
      <strong>상태:</strong> 준비
   </li>

<li>
      <strong>처방 ID:</strong> pres2<br>
      <strong>이름:</strong> 약물 B<br>
      <strong>상태:</strong> 회수
   </li>

</ul>

**상태 관리 계획 B**

<ul>

<li>
      <strong>처방전 ID:</strong> pres4<br>
      <strong>이름:</strong> 약물 D<br>
      <strong>상태:</strong> 준비
   </li>

</ul>

>[!TAB HTML 템플릿]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB 프로필 데이터]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]

## 빠른 참조 {#quick-reference}

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

>[!BEGINTABS]

>[!TAB 개요]

**TL;DR**

이 페이지에서는 완전한 개인화 사용 사례를 보여 줍니다. 조건부 필터링으로 중첩된 프로필 배열(처방전이 포함된 상태 계획)을 반복하여 이메일에 &quot;준비됨&quot; 또는 &quot;회수&quot; 상태의 처방만 표시합니다.

**의도**

* 개인화된 의료 서비스 이메일의 렌더링된 출력 예 보기
* 조건부 배열 반복에 대해 중첩된 `{{#each}}` 및 `{%#if%}` 블록을 사용하여 HTML 템플릿을 이해합니다.
* 필요한 프로필 데이터 구조 이해: 각 플랜에 `state` 필드가 있는 `prescriptions` 배열이 포함된 `plans` 배열

>[!TAB 용어집]

* **중첩 반복**: 다른 `{{#each}}` 루프 내에서 `{{#each}}` 루프를 사용하여 프로필 데이터(예: 플랜 → 처방)의 다중 수준 배열 구조를 이동합니다.
* **처방 상태**: 이 사용 사례에서 라이프사이클 상태를 나타내는 각 처방 개체의 필드입니다. 사용된 값은 &quot;준비&quot;, &quot;회수&quot; 및 &quot;선택됨&quot;입니다. *(사용 사례별)*
* **`{%#if%}`/`{%/if%}`**: 반복하는 동안 배열 항목을 필터링하기 위해 메시지 템플릿 내에서 사용되는 조건부 블록 구문(이중 곱슬 `{{#if}}` Handlebars 구문과 구별됨).

>[!TAB 용어]

* **정식 이름:** 중첩된 배열 반복 — 변형: 중첩된 루프, 중첩된 각 다중 레벨 반복
* **혼동하지 마십시오:** `{{#each}}` / `{{/each}}`(Handlebars 반복 구문, 이중 중괄호) ≠ `{%#if%}` / `{%/if%}`(조건부 구문, % 중괄호) — 둘 다 이 템플릿에서 함께 사용됩니다.
* **혼동하지 마십시오.** &quot;준비됨&quot;(처방 선택용) ≠ &quot;회수&quot;(처방이 회수됨) ≠ &quot;픽업됨&quot;(처방이 이미 수집됨, 조건부 필터에서 출력에서 제외됨)

>[!TAB FAQ]

**Q: 전자 메일 출력에는 어떤 처방 상태가 포함됩니까?**

상태가 &quot;준비&quot; 또는 &quot;회수&quot;인 처방만 표시됩니다. 상태가 &quot;선택됨&quot;인 처방은 `{%#if prescription.state = "ready" or prescription.state = "recall"%}` 조건부 필터에서 제외됩니다.

**Q: 이 사용 사례에 필요한 프로필 데이터 구조는 무엇입니까?**

각 계획 개체에 `prescriptions` 배열이 포함된 배열이 `plans`인 프로필입니다. 각 처방 개체에는 `prescription_id`, `name` 및 `state` 필드가 있어야 합니다.

**Q: 템플릿에서 계획과 처방은 어떻게 반복됩니까?**

외부 `{{#each profile.plans as |plan|}}` 루프가 각 상태 계획을 반복합니다. `{{#each plan.prescriptions as |prescription|}}`은(는) 각 플랜의 처방전을 반복하며 조건부 차단 필터는 &quot;준비&quot; 또는 &quot;회수&quot; 상태만 필터링합니다.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
