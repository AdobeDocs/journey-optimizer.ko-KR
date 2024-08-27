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
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: ht
source-wordcount: '325'
ht-degree: 100%

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
<th><strong>콘텐츠 조각의 변수</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 조각은 <a href="../personalization/use-expression-fragments.md">표현식 조각</a> 및 <a href="../email/use-visual-fragments.md">시각적 조각</a> 모두에서 입력 변수를 사용할 수 있습니다. 이러한 변수를 사용하여 캠페인 및 여정에서 메시지 콘텐츠 및 매개 변수를 개인화할 수 있습니다.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 준비 워크플로</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>사용 가능한 날짜: 2013년 8월</p>
<p>완전히 새로운 IP 주소로 이메일을 보내는 경우 이제 사용자 인터페이스에서 직접 IP 준비 워크플로를 쉽게 수행할 수 있습니다. Adobe Journey Optimizer는 최적의 전달성을 위한 모범 사례에 따라 IP 주소를 준비하는 표준화되고 효율적인 방법을 제공합니다.</p>
<p>자세한 내용은 <a href="../configuration/ip-warmup-gs.md">세부 설명서</a>를 참조하십시오.</p>
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

* 이제 **조건** 활동에서 시간 조건은 기본적으로 00:00부터 12:00까지 시간 단위로 설정됩니다. [자세히 보기](../building-journeys/condition-activity.md#time_condition)
* 이제 여정을 설정할 때 경고가 드롭다운 목록에 표시되어 캠페인 경고와 일치하고 일관된 사용자 경험을 제공합니다. [자세히 보기](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 여정 도구 모음의 확대/축소 옵션이 개선되었습니다. 이제 확대/축소 비율이 표시되며 확대/축소 값을 100%로 쉽게 재설정할 수 있습니다.

**대상자**

* 이제 사용자 정의 업로드(CSV 파일)에서 가져온 대상자를 Privacy 및 Security Shield에도 사용할 수 있습니다.
* 이제 사용자 지정 업로드(CSV 파일) 대상자를 타기팅할 때 캠페인 및 여정에 있는 파일의 속성을 사용할 수 있습니다. 이러한 속성은 개인화 편집기에서 메시지를 개인화하는 데 사용할 수 있으며 여정 고급 표현식 편집기에서 사용할 수 있습니다.


<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
