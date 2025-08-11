---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '591'
ht-degree: 100%

---

# 사전 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.


## 2025년 8월 사전 릴리스 정보 {#25-7-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면 및 업데이트된 설명서는 릴리스 날짜에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 일자**: 2025년 8월 19일


### 새로운 기능 {#Aug-25-8-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>여정 일시 중단 및 다시 시작</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 일시 중단했다가 다시 시작할 수 있습니다. 이 기능을 사용하면 고객 경험을 중단하지 않고 라이브 여정을 일시적으로 중단할 수 있으므로 여정 실무자가 여정을 보다 자유롭게 제어하고 유연하게 조정할 수 있습니다. 일시 중단하면 커뮤니케이션이 전송되지 않으며 프로필은 여정이 다시 시작될 때까지 보류 상태로 유지됩니다.</p>
<p>하나의 여정만 일시 중단했다가 다시 시작하거나, 여정 그룹에 일괄 일시 중단 및 다시 시작 작업을 수행할 수 있습니다.</p>
<p>또한 일시 중단된 프로필에 전역 필터를 적용하여 속성에 따라 프로필을 제외할 수 있습니다.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>이전에는 제한된 고객 집합(제한된 가용성)에서 사용할 수 있었지만, 이제 모든 환경에서 이 기능을 사용할 수 있게 되었습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../building-journeys/journey-pause.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>캘린더 보기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 및 캠페인 목록에서 캘린더 보기를 사용할 수 있습니다. 이를 통해 각 목록에 있는 모든 여정 및 캠페인의 활성화를 시각화할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>날짜 내 탐색을 위한 디자인 개선 사항</li>
<li>시작 및 종료 날짜를 설정한 경우 초안 캠페인을 볼 수 있는 기능</li>
<li>오래 실행되는 일정 항목을 숨기고 표시하는 새로운 설정</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>자세한 내용은 <a href="../building-journeys/journey-ui.md#journeys-calendar">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 디자이너의 다크 모드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 이메일 디자이너에서 다크모드 보기로 전환할 수 있는 기능을 제공합니다. 이 기능에서는 다크모드에서 이메일을 읽는 수신자에게만 표시되는 특정 사용자 지정 설정을 추가로 정의할 수 있습니다.</p>
<p>다음 사항에 유의하십시오.</p>
<ul>
<li>다크모드 최종 렌더링은 수신자의 이메일 클라이언트에 따라 다를 수 있습니다.</li>
<li>모든 이메일 클라이언트가 사용자 정의 다크모드를 지원하지는 않습니다. 또한 일부 이메일 클라이언트는 수신되는 모든 이메일에 대해 자신의 기본 다크모드만 적용합니다. 두 경우 모두 이메일 디자이너에서 정의한 사용자 지정 설정을 렌더링할 수 없습니다.</li>
</ul>
<P>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>자세한 내용은 <a href="../email/dark-mode.md">세부 설명서</a>를 참조하십시오. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>캠페인의 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer는 캠페인 대상에 개인화되고 최적화된 콘텐츠를 전달할 수 있는 도구를 제공함으로써 콘텐츠 실험을 실행하고, 규칙 기반 타기팅을 만들고, 두 방법의 고급 조합을 사용하여 캠페인의 효과를 극대화할 수 있습니다.</p>
<p>최적화를 사용하면 다음을 할 수 있습니다.</p>
<ul>
<li>여러 콘텐츠 변형을 테스트하여 가장 효과적인 메시징을 식별합니다.</li>
<li>사용자 특성 및 컨텍스트 데이터를 기반으로 개인화된 콘텐츠를 제공합니다.</li>
<li>고급 캠페인 전략에 대한 타겟팅과 실험을 결합합니다.</li>
<li>변형 기준과 일치하지 않는 사용자를 필터링합니다.</li>
<li>사용자 참여를 유지하기 위한 대체 메커니즘을 확인하십시오.</li>
</ul>
<P>캠페인이 라이브되면 정의된 기준에 따라 프로필이 평가되고, 일치하는 기준을 기반으로 캠페인의 적절한 경험 또는 콘텐츠와 함께 전달됩니다.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#Aug-25-8-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.