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
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 49%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 8월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 8월 20~21일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>Marketo Engage 사용자 정의 작업</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer를 Adobe Marketo Engage와 통합하여 B2B 사용 사례를 작성할 수 있습니다. 여정에서 새로운 사용자 정의 작업을 통해 데이터를 Marketo로 수집할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>향상된 채널 구성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>현재 채널 표면 기능은 모든 채널에서 일관된 접근 방식을 위해 향상되었습니다. 이제 모든 채널에서 이러한 구성을 정의, 관리 및 재사용할 수 있습니다.</p>
<p><ul>
<li>이제 채널 표면 이름이 <strong>채널 구성</strong>(으)로 변경되었습니다.</li>
<li>이제 채널 구성 인벤토리에서 이제 웹, 인앱 메시징 또는 코드 기반 경험을 포함하여 모든 채널에 대해 재사용 가능한 채널 구성을 만들 수 있습니다</li>
<li>이제 각 채널 구성에 OLAC(개체 수준 액세스 제어)를 사용할 수 있으므로 특정 구성을 만들거나 사용할 수 있는 사용자를 결정할 수 있습니다</li>
<li>일부 채널의 경우 여러 플랫폼을 대상으로 하는 채널 구성을 만들 수 있습니다. 웹 페이지, iOS 앱 및 Android 앱을 타깃팅할 수 있는 인앱 메시지 채널 구성이 여기에 해당합니다.</li>
</ul></p>
<p>자세한 내용은 <a href="../configuration/ip-warmup-gs.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**여정**

* **조건** 활동에서 기본적으로 시간 조건은 00:00부터 12:00까지 시간 단위로 설정됩니다. [자세히 보기](../building-journeys/condition-activity.md#time_condition)

**대상자**

* 이제 사용자 정의 업로드(CSV 파일)에서 가져온 대상자를 Privacy 및 Security Shield에도 사용할 수 있습니다.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
