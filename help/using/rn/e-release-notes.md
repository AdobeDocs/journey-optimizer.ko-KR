---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9eb0e37b0547a3eb00802711825ecff63ab5f4a6
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 20%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 2월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 2월 20~21일

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
<p>이제 새로운 웹 인앱 메시지 기능을 사용하여 양식 오버레이 메시지를 통해 웹 사이트에 직접 개인화된 콘텐츠를 표시할 수 있습니다. 이 기능을 사용하면 웹 방문자와 효과적으로 상호 작용하여 사용자 상호 작용, 보존 및 전환율을 향상시킬 수 있습니다.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>비즈니스 규칙(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 SMS 및 DM 채널에 적용되는 빈도 제한 규칙을 만들 수 있습니다. 또한 통신 유형별로 빈도 제한 규칙을 설정할 수 있습니다.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상자**

* 를 사용할 때 변형이 지원됩니다. **시드 목록**. 타겟팅된 대상의 각 프로필과 마찬가지로, 시드 주소는 동일한 메시지의 모든 변형(예: 콘텐츠 실험의 다양한 처리)의 사본을 받습니다.

이전에 Beta로 제공되었던 향상된 기능은 이제 모든 사용자가 사용할 수 있습니다.

* 이제 타겟팅할 수 있습니다. **csv 파일에서 업로드한 대상자** 를 여정 및 캠페인에 포함시킵니다. [자세히 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)
* 이제 타겟팅할 수 있습니다. **대상자 구성을 통해 생성된 대상자** 여정에서 데이터 보강 속성을 활용할 수 있습니다. [자세히 보기](../building-journeys/read-audience.md)

**여정**

* 이제 다음을 사용할 수 있습니다. **여정을 필터링할 사용자 정의 날짜** 기존 사전 정의된 날짜 필터 외에 인벤토리 이렇게 하면 특정 날짜, 특정 달 내, 전체 연도 또는 지정된 시간 범위에 게시된 여정을 표시하여 목록을 세분화할 수 있습니다.
* 이제에서 &quot;content-type&quot; 헤더를 업데이트할 수 있습니다. **사용자 지정 작업**.
* stepEvents의 identityMap 속성이 이제 미리 채워집니다. 기본 ID는 &quot;primary = true&quot;로 정의됩니다.
* 여정 화면의 상단 표시줄이 향상된 경험을 위해 재구성되었습니다. 여러 업데이트 중 여정 속성에 액세스할 수 있는 &quot;연필&quot; 아이콘이 이제 여정 이름 옆의 상단 표시줄 왼쪽에 표시됩니다.


**SMS 채널**

* 이제 SMS 채널을 구성할 때 **옵트인 및 옵트아웃 키워드** 기본 설정에 따라. Journey Optimizer은 지정된 이러한 키워드를 기반으로 응답을 트리거합니다.

**캠페인**

* 의 &quot;cURL 요청&quot; 섹션에 정보가 추가되었습니다. **API 트리거된 캠페인** 샘플 cURL 요청이 캠페인이 게시되고 실행된 후에만 표시되도록 지정하려면 &quot;초안&quot; 상태입니다.

**의사 결정 관리**

* 이제 를 추가할 수 있습니다. **다중 최대 가용량 규칙** 하나의 오퍼에 대해. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 높일 수 있습니다.

**콘텐츠 템플릿**

* A **썸네일 보기** 는 이제 개선된 시각적 액세스를 위해 콘텐츠 템플릿 및 조각에 사용할 수 있습니다.
* 이제 다음에 대해 콘텐츠 템플릿을 사용할 수 있습니다. **모든 채널**, 웹 제외