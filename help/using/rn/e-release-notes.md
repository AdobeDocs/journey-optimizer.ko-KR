---
solution: Journey Optimizer
product: journey optimizer
title: 초기 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 8188749c47be0a3d91b9857d170bceb4747a3400
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 33%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.


## 2025년 6월 초기 릴리스 정보 {#25-6-rn}


**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면 및 업데이트된 설명서는 릴리스 날짜에 게시됩니다.

**릴리스 일자**: 2025년 6월 18일 목요일


### 새로운 기능 {#25-06-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.




<table>
<thead>
<tr>
<th><strong>RCS 메시징</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 RCS(Rich Communication Services) 메시징이 지원되므로 공급자 및 통신사 지원에서 다음과 같은 향상된 메시징 기능을 사용할 수 있습니다.</p>
<ul>
<li>브랜드 및 인증된 발신자 지원: 브랜드 요소(로고, 발신자 이름 등)가 있는 인증된 비즈니스 프로필을 사용하여 메시지를 보냅니다.</li>
<li>메시지 게재 인사이트: 메시지 상태 업데이트(예: 보냄, 배달됨, 읽기)를 포함한 자세한 게재 보고서를 받습니다.</li>
<li>링크 추적: 참여 분석을 위해 RCS 메시지 내에 URL을 임베드하고 추적합니다.</li>
<li>SMS로 폴백: 프로필의 장치가 RCS를 지원하지 않거나 RCS를 통해 일시적으로 연결할 수 없는 경우 SMS로 자동 폴백합니다.</li>
<li>기본 메시지 구성: 공급업체 지원에 따라 선택적 미디어 및 리치 요소와 함께 텍스트 기반 RCS 메시지를 전송합니다.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>코드 기반 경험 콘텐츠의 양식 필드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 JSON 또는 HTML 콘텐츠 템플릿에서 편집 가능한 특정 필드를 정의할 수 있습니다. 이렇게 하면 기술 전문가가 아닌 사용자도 코드를 조작하지 않고도 코드 기반 경험 채널 작성 내에서 양식 보기로 콘텐츠를 쉽게 편집할 수 있습니다. 그 외에도 코드 기반 경험 콘텐츠 템플릿을 정의할 때 이제 템플릿에 의사 결정 정책을 삽입할 수 있으므로 재사용성과 사용 편의성을 높일 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>하위 도메인을 위한 사용자 지정 위임 방법</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 전체 위임과 CNAME 메서드 외에도 새로운 하위 도메인 구성 방법인 사용자 정의 위임 메서드를 사용할 수 있습니다. 이 방법을 사용하면 메시지 전달, 렌더링 및 추적에 필요한 DNS의 모든 측면을 완벽하게 제어하고 유지 관리할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정의 Content Decisioning 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 캔버스에서 전용 Content Decisioning 활동을 통해 개인화된 오퍼를 여정에 포함하고 조건 및 사용자 지정 작업을 포함한 여정 활동에서 사용할 수 있습니다.</p>
<p>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있으며 향후 릴리스에서 전역으로 롤아웃될 예정입니다.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>여정 시험 실행</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 Dry Run은 여정 제공자가 실제 고객에게 연락하거나 프로필 정보를 업데이트하지 않고도 실제 프로덕션 데이터를 사용하여 여정을 테스트할 수 있는 Adobe Journey Optimizer의 특수 여정 게시 모드입니다. 이 기능은 여정 제공자가 라이브로 게시하기 전에 여정 디자인 및 대상 타깃팅에 대한 자신감을 갖도록 도와줍니다.</p>
<p>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있으며 향후 릴리스에서 전역으로 롤아웃될 예정입니다.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>일시 중지 및 다시 시작 여정</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 일시 중지했다가 다시 시작할 수 있습니다. 이 기능을 사용하면 고객 경험을 중단하지 않고 라이브 여정을 일시적으로 중단할 수 있으므로 여정 실무자가 보다 강력하게 제어하고 유연화할 수 있습니다. 일시 중지되면 통신이 전송되지 않으며 프로필은 여정이 다시 시작될 때까지 일시 중지된 상태로 유지됩니다.</p>
<p>하나의 여정만 일시 중지했다가 다시 시작할 수 있으며, 일괄 일시 중지 및 다시 시작 작업을 수행하여 여정 그룹에 대한 작업을 다시 시작할 수 있습니다.</p>
<p>또한 일시 중지된 프로필에 전역 필터를 적용하여 여정의 속성에 따라 프로필을 제외할 수 있습니다.</p>
<p>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있으며 향후 릴리스에서 전역으로 롤아웃될 예정입니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>실험 우승자 적용 확대</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>실험 승자의 크기를 조정하면 실험의 가장 성과가 좋은 변형을 전체 대상자에게 자동 또는 수동으로 롤아웃할 수 있습니다. 이 기능을 사용하면 우승자가 식별된 후 지속적인 수동 감독 없이 도달 범위와 효과를 극대화할 수 있습니다.</p>
<p>자세한 내용은 <a href="../content-management/content-experiment.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 6월 2일</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>충돌 및 우선순위 지정</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에서 너무 많은 상호 작용으로 고객에게 부담 주는 상황을 피하려면 캠페인과 여정의 양과 타이밍을 관리하는 것이 필수적입니다. 이제 Journey Optimizer에서 충돌 관리 및 우선순위 지정을 위한 몇 가지 도구를 제공합니다. 이전에는 제한된 액세스(LA) 조직에서만 사용할 수 있었지만 현재는 일반 가용성(GA)으로 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 일반 가용성 릴리스에서는 다음과 같은 개선 사항이 도입되었습니다.</p>
<ul>
<li>지원 확대: 이제 충돌 관리 도구가 대상자 읽기 여정 외에도 단일 여정 및 대상자 선별 여정을 모두 지원합니다.</li>
<li>문제 해결 개선: 이제 쿼리 서비스에서 두 개의 새로운 단계 이벤트 필드를 사용하여 여정 또는 캠페인에서 프로필이 거부된 이유를 분석할 수 있습니다.</li>
<li>보고 기능 향상: 이제 보고서에 여정 또는 캠페인에서 특정 프로필을 제외한 규칙이 명시되어 투명도가 향상되고 실행 가능한 인사이트를 얻을 수 있습니다.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>자세한 내용은 <a href="../conflict-prioritization/gs-conflict-prioritization.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 6월 3일</p>
</td>
</tr>
</tbody>
</table>


### 개선 사항 {#25-06-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

* **채널 규칙 집합**

   * **시간 제한을 위한 사용자 지정 기간 창** - 이제 채널 규칙 집합 구성 화면에서 새 **반복 횟수** 필드를 사용할 수 있으므로 지정된 기간에 따라 여러 날, 주 또는 달에 걸쳐 빈도 제한 규칙을 적용할 수 있습니다.

   * **시간별 기간** - 이제 채널 규칙 집합에 대해 시간별로 상한을 적용할 수 있습니다.

* **코드 기반 경험**

  이제 코드 기반 경험 콘텐츠 템플릿 및 코드 편집기 오른쪽 레일에서 의사 결정 정책을 사용할 수 있습니다.

* **이메일 디자이너**

   * **사용자 지정 CSS 지원** - 이제 Journey Optimizer에서 사용자 지정 CSS를 이메일 디자이너 내에서 바로 이메일 콘텐츠에 추가할 수 있습니다.
   * **다크 모드 지원** - 이제 Journey Optimizer 이메일 디자이너가 특정 설정을 정의할 수 있는 다크 모드로 전환하는 기능을 제공합니다.


* **Decisioning** - 사용 가능한 날짜: 2025년 6월 3일

  이제 결정 오브젝트를 샌드박스 간에 복사할 수 있어 테스트 및 배포 워크플로가 간소화됩니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#decisioning)

* **의사 결정 규칙에 대한 의사 결정 항목 특성 지원** - 사용 가능한 날짜: 2025년 6월 4일

  이제 의사 결정 항목 속성을 활용하여 의사 결정 규칙을 만들 수 있습니다. [자세히 보기](../experience-decisioning/rules.md#create)

* **대화형 메시지 실행 API 업데이트** - 사용 가능한 날짜: 2025년 6월 6일

  이제 대화형 메시지 실행 API를 사용하여 예정된 캠페인 실행 일정을 삭제할 수 있습니다. [자세히 보기](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}