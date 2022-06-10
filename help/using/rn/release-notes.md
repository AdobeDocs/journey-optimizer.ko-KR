---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 06eb2ebec284f807de7ddca5d26e13fc08194642
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 90%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.

## 2022년 5월 릴리스 {#may-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>메시지 빈도 규칙</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외하는 채널  비즈니스 규칙을 설정할 수 있습니다.</p>
<img src="assets/frequency-rn.gif"/>
<p>자세한 내용은 <a href="../configuration/frequency-rules.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>의사 결정 관리 - AI 등급 자동 최적화 모델</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 의사 결정 관리에서 련된 모델 시스템을 사용할 수 있습니다. 이 새 기능은 주어진 프로필에 대해 표시할 오퍼에 등급을 지정합니다.</p>
<img src="assets/optimization.gif"/>
<p>자세한 내용은 <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 감사 로그</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer 리소스에서 사용자가 수행한 작업을 모니터링할 수 있습니다.</p>
<img src="assets/audit-rn.gif"/>
<p>자세한 내용은 <a href="../reports/audit-logs.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**개인화**

* **문자 숨김을 위한 새 도우미 함수** - `mask` 도우미 함수를 사용하면 문자열의 일부를 &quot;X&quot; 문자로 바꿀 수 있습니다. [자세히 보기](../personalization/functions/string.md#mask)

**랜딩 페이지**

* **양식이 없는 랜딩 페이지** - 이제 양식을 포함하지 않고 방문자의 작업이 필요 없는 랜딩 페이지를 만들어 게시할 수 있습니다.
* **랜딩 페이지 템플릿** - 이제 랜딩 페이지를 템플릿으로 저장하고 다른 랜딩 페이지를 만들 때 다시 사용할 수 있습니다. [자세히 보기](../landing-pages/lp-templates.md)
* **기본 페이지로 돌아가기** - 이제 동일한 랜딩 페이지 내의 하위 페이지에서 기본 페이지에 링크를 추가할 수 있습니다.
* **사용자 지정 JavaScript 지원** - 이제 사용자 지정 JavaScript를 랜딩 페이지 콘텐츠에 추가하여 고급 스타일을 수행하거나 사용자 지정 동작을 랜딩 페이지에 추가할 수 있습니다.	[자세히 보기](../landing-pages/lp-custom-js.md)

**여정**

* **세그먼트 읽기** - 이제 일회성 읽기 세그먼트 여정이 여정 실행 후 30일 후에 완료됨 상태로 이동합니다. 예약된 읽기 세그먼트의 경우 마지막 항목이 실행된 후 30일이 경과한 시점입니다. [자세히 보기](../building-journeys/read-segment.md)
* **표현식 편집기** - 목록의 항목 수를 제한할 수 있도록 [limit](../building-journeys/functions/functionlimit.md) 함수가 추가되었습니다. 이제 [sort](../building-journeys/functions/functionsort.md) 함수를 사용하여 목록 개체를 정렬할 수 있습니다. 또한 [disctinct](../building-journeys/functions/functiondistinct.md) 및 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 함수에 listObject에 대한 지원도 추가되었습니다.

**관리**

* **라이선스 사용 대시보드 업데이트** - 사용 가능한 라이센스 사용량 대시보드 [!DNL Adobe Journey Optimizer] 이제 사용자 인터페이스에 의 정확한 값이 반영됩니다 **라이센스** 평균 프로필 품질. 이 지표 표시에 감소가 표시되는데, 이것은 이제 라이선스 제한이 올바로 보고됨을 의미합니다. [자세히 보기](../segment/licence-usage.md)
