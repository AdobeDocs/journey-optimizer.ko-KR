---
title: 템플릿 Personalization의 예
description: Journey Optimizer Personalization 예
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: f1d6c293fb8b22085911ab45c18f944a63b9655b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# 의료 서비스 플랜 처방 전자 메일 {#plan-prescription}

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
      <strong>처방 ID:</strong> pres4<br>
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
