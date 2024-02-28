---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 90%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 2월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 2월 21~22일

### 새로운 기능{#e-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.


<table>
<thead>
<tr>
<th><strong>웹 인앱 메시지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 웹 인앱 메시지 기능을 사용하면 모달 오버레이 메시지를 통해 웹 사이트에 직접 개인화된 콘텐츠를 표시할 수 있습니다. 이 기능을 사용하면 웹 방문자와 효과적으로 상호 작용하여 사용자 상호 작용, 보존 및 전환율을 향상할 수 있습니다.<br/><br/></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>SMS 및 DM 빈도 규칙</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 SMS 및 DM 채널에 대한 빈도 규칙을 만들 수 있습니다. 빈도 규칙은 빈도 상한에 도달하면 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외합니다. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상자**

* **시드 목록** - 이제 **시드 목록**&#x200B;을 사용할 때 변형이 지원됩니다. 타겟팅된 대상자의 각 프로필과 마찬가지로, 시드 주소는 동일한 메시지의 모든 변형(예: 콘텐츠 실험의 다양한 처리) 사본을 받습니다.

이전에 Beta로 제공되었던 향상된 기능은 이제 모든 사용자가 사용할 수 있습니다.

* 이제 **대상자 구성을 통해 생성된** 대상자를 타겟팅하고 여정에서 데이터 보강 속성을 활용할 수 있습니다. [자세히 알아보기](../building-journeys/read-audience.md)

* 이제 여정과 캠페인에 **CSV 파일에서 업로드된 대상자**&#x200B;를 타겟팅할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 대상자 구성 및 사용자 정의 업로드(CSV 파일)의 대상자 및 속성은 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다.
  >* CSV 파일 개선 사항의 대상자 업로드는 초기 릴리스 이후 며칠 동안 점진적으로 롤아웃됩니다. 일부 사용자는 즉시 액세스할 수 있지만 다른 사용자는 자신의 계정에서 사용할 수 있게 되기까지 지연이 발생할 수 있습니다.

**여정**

* **여정 필터링** - 이제 기존의 사전 정의된 날짜 필터 외에도 **사용자 정의 날짜를 사용하여 여정** 인벤토리를 필터링할 수 있습니다. 이렇게 하면 특정 날짜, 특정 달 내, 전체 연도 또는 지정된 시간 범위 내에서 만들거나 게시한 여정을 표시하여 목록을 개선할 수 있습니다.
* **사용자 지정 작업** - 이제 다음을 업데이트할 수 있습니다. **content-type** 머리글입니다. 이 새로운 항목 **content-type** 는 JSON 콘텐츠를 참조해야 합니다.
* **구성** - stepEvents의 identityMap 속성이 이제 미리 채워져 있습니다. 기본 신원은 “primary = true”로 정의됩니다.
* **사용자 인터페이스** - 여정 화면의 상단 표시줄이 향상된 경험을 위해 재구성되었습니다. 여러 업데이트 중 여정 속성에 액세스할 수 있는 “연필” 아이콘이 이제 여정 이름 옆의 상단 표시줄 왼쪽에 표시됩니다.

**SMS 채널**

* **옵트인/옵트아웃 키워드** - 이제 SMS 채널을 구성할 때 원하는 대로 **옵트인 및 옵트아웃 키워드**&#x200B;를 사용자 정의할 수 있습니다. Journey Optimizer는 지정된 이러한 키워드를 기반으로 응답을 트리거합니다.

**캠페인**

* **API 트리거 캠페인** - API 트리거 캠페인을 활성화한 후 생성된 cURL 코드가 향상되었습니다. 이제 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다.

**의사 결정 관리**

* **상한 규칙** - 이제 하나의 오퍼에 **여러 상한 규칙**&#x200B;을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 높일 수 있습니다.

**콘텐츠 템플릿**

* **썸네일** - **썸네일 보기** 는 이제 개선된 시각적 액세스를 위해 콘텐츠 템플릿 및 조각에 사용할 수 있습니다.

  >[!AVAILABILITY]
  >
  >이 기능은 소규모 고객을 위해 LA(Limited Availability)에서 출시됩니다.

* **다중 채널 템플릿** - 이제 웹을 제외한 **모든 채널**&#x200B;에서 콘텐츠 템플릿을 사용할 수 있습니다. 이제 이메일의 경우 유형(HTML 또는 컨텐츠)을 선택할 수 있습니다.
