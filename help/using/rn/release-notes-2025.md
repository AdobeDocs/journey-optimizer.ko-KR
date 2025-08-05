---
solution: Journey Optimizer
product: journey optimizer
title: 2025년 릴리스 정보
description: Journey Optimizer 2025년 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '4203'
ht-degree: 99%

---

# 2025년 릴리스 정보 {#release-notes-2025}

이 페이지에서는 2025년에 릴리스된 [!DNL Journey Optimizer]의 모든 기능과 개선 사항 목록을 확인할 수 있습니다.


## 25년 6월 릴리스 정보 {#25-6-rn}

**릴리스 일자**: 2025년 6월 18일

### 새로운 기능 {#25-06-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>결정에 Adobe Experience Platform 데이터 세트 사용(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에 개인화에 사용할 수 있었던 Adobe Experience Platform 데이터 세트를 이제 결정에 활용할 수 있습니다. 그러면 주기적으로 변경되는 일괄 업데이트 시 속성을 일일이 수동으로 업데이트할 필요 없이 결정 속성의 정의를 데이터 세트의 추가 데이터로 확장할 수 있습니다. 예를 들면 가용성, 대기 시간 등이 있습니다.</p>
<p>이 기능은 현재 모든 고객이 공개 Beta로 사용할 수 있습니다. 액세스하려면 계정 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../experience-decisioning/aep-data-exd.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 6월 20일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS 메시지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 Rich Communication Services(RCS) 메시지가 지원되므로 공급자 및 통신사 지원이 필요한 다음의 향상된 메시지 기능을 사용할 수 있습니다.</p>
<ul>
<li>브랜디드 및 인증된 발신자 지원: 브랜딩 요소(로고, 발신자 이름 등)가 있는 인증된 비즈니스 프로필을 사용하여 메시지를 보냅니다.</li>
<li>메시지 게재 인사이트: 메시지 상태 업데이트(예: 보냄, 전달됨, 읽음)를 포함한 자세한 게재 보고서를 받습니다.</li>
<li>링크 추적: 참여 분석을 위해 RCS 메시지 내에 URL을 임베딩하고 추적합니다.</li>
<li>SMS로 대체: 프로필의 디바이스가 RCS를 지원하지 않거나 일시적으로 RCS를 통해 연결할 수 없는 경우 SMS로 자동 대체합니다.</li>
<li>기본 메시지 구성: 공급업체 지원에 따라 선택적으로 미디어 및 리치 요소를 포함할 수 있는 텍스트 기반 RCS 메시지를 전송합니다.</li>
</ul>
<p>자세한 내용은 <a href="../sms/sms-configuration.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>코드 기반 경험 콘텐츠의 양식 필드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 JSON 또는 HTML 콘텐츠 템플릿에서 편집 가능한 특정 필드를 정의할 수 있습니다. 이렇게 하면 기술 전문가가 아닌 사용자도 코드를 조작할 필요 없이 손쉽게 코드 기반 경험 채널 작성 내 양식 보기의 콘텐츠를 편집할 수 있습니다.<br />더 나아가 이제 코드 기반 경험 콘텐츠 템플릿을 정의할 때 템플릿에 결정 정책을 삽입하여 재사용성과 사용 편의성을 높일 수 있습니다.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>자세한 내용은 <a href="../code-based/code-based-form-fields.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>여정의 콘텐츠 결정 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 캔버스에서 전용 [콘텐츠 결정] 활동을 통해 개인화된 오퍼를 여정에 포함하고 조건 및 사용자 정의 액션을 포함한 여정 활동에 사용할 수 있습니다.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>이 기능은 일부 조직에서만 사용할 수 있으며(제한된 가용성) 향후 릴리스에서 전체 사용자를 대상으로 공개될 예정입니다.</p>
<p>자세한 내용은 <a href="../building-journeys/content-decision.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 시험 실행</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 시험 실행은 Adobe Journey Optimizer에서 제공되는 특별한 여정 게시 모드로, 여정 실무자가 실제 고객에게 연락하거나 프로필 정보를 업데이트하지 않고도 실제 프로덕션 데이터를 사용해 여정을 테스트할 수 있도록 합니다. 이 기능은 여정 실무자가 여정을 게시하기 전에 여정 설계와 대상자 타기팅에 대한 자신감을 얻는 데 도움이 됩니다.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>이 기능은 일부 조직에서만 사용할 수 있으며(제한된 가용성) 향후 릴리스에서 전체 사용자를 대상으로 공개될 예정입니다.</p>
<p>자세한 내용은 <a href="../building-journeys/journey-dry-run.md">세부 설명서</a>를 참조하십시오.</p>

</td>
</tr>
</tbody>
</table>

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
<p>이 기능은 일부 조직에서만 사용할 수 있으며(제한된 가용성) 향후 릴리스에서 전체 사용자를 대상으로 공개될 예정입니다.</p>
<p>자세한 내용은 <a href="../building-journeys/journey-pause.md">세부 설명서</a>를 참조하십시오.</p>
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
<p>[실험 우승자 적용 확대] 기능을 사용하면 실험에서 우승한 베리에이션을 전체 대상자에게 자동 또는 수동으로 롤아웃할 수 있습니다. 이 기능을 사용하면 우승자가 식별된 후 지속적인 수동 감독 없이 도달 범위와 효과를 극대화할 수 있습니다.</p>
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

* **채널 규칙 세트**

   * 캡핑의 **사용자 정의 기간** - 채널 규칙 세트 구성 화면에 새로 추가된 **모든**(반복 주기) 필드를 사용하여 지정된 기간에 따라 여러 날, 주 또는 달에 걸쳐 빈도 상한 규칙을 적용할 수 있습니다.

   * **시간 단위 캡핑 빈도 재설정** - 이제 채널 규칙 세트에 대해 시간 단위로 캡핑을 적용할 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 이 기능을 활성화하려면 고객 지원 센터에 문의하십시오.

   * **일별 기간** - 이전에는 제한된 가용성으로 사용할 수 있던 채널 규칙 세트의 “일별” 빈도 제한을 이제 모든 고객이 사용할 수 있습니다.

  자세한 내용은 [세부 설명서](../conflict-prioritization/channel-capping.md)를 참조하십시오.

* **코드 기반 경험**

   * 이제 코드 기반 경험 콘텐츠 템플릿에 결정 정책을 추가할 수 있습니다. 템플릿에서 이 결정 정책으로 편집 가능한 양식 필드의 오퍼를 활용할 수 있습니다. [자세히 보기](../code-based/code-based-form-fields.md)

   * 이제 코드 기반 경험 여정 또는 캠페인 편집 화면에서 개인화 편집기를 열지 않고도 결정 정책을 직접 추가할 수 있습니다. [자세히 보기](../code-based/create-code-based.md#edit-code)

* **이메일 디자이너의 사용자 정의 CSS 지원**

  이제 Journey Optimizer의 [이메일 디자이너] 내에서 바로 이메일 콘텐츠에 사용자 정의 CSS를 추가할 수 있습니다. [자세히 보기](../email/custom-css.md)

* **캠페인에 새로운 탭 탐색 적용**

  새로운 탐색 패턴을 통해 콘텐츠 작성에 보다 빠르게 액세스하고 여러 캠페인 간에 설정을 더욱 확장할 수 있습니다. [자세히 보기](../campaigns/create-campaign.md)

* **의사 결정**

   * **샌드박스 복사 및 결정**(사용 가능한 날짜: 2025년 6월 3일) - 이제 결정 오브젝트를 샌드박스 간에 복사할 수 있으므로 테스트 워크플로및 배포 워크플로가 간소화됩니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **의사 결정 규칙에 대한 의사 결정 항목 특성 지원**(사용 가능한 날짜: 2025년 6월 4일) * 이제 의사 결정 항목 특성을 활용하여 의사 결정 규칙을 만들 수 있습니다. [자세히 보기](../experience-decisioning/rules.md#create)

* **Interactive Message Execution API 업데이트** - 사용 가능한 날짜: 2025년 6월 6일

  이제 Interactive Message Execution API를 사용하여 예정된 캠페인 실행 일정을 삭제할 수 있습니다. [자세히 보기](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}


## 25년 5월 릴리스 정보 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### 새로운 기능 {#25-05-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>캠페인 및 여정 인벤토리에 대한 캘린더 보기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 및 캠페인 목록에서 캘린더 보기를 사용할 수 있습니다. 이를 통해 각 목록에 있는 모든 여정 및 캠페인의 활성화를 시각화할 수 있습니다.</p>
<p>이 변경은 현재 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 요청하려면 <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">이 양식</a>을 사용하십시오.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>자세한 내용은 <a href="../building-journeys/journey-ui.md">여정 찾아보기 및 필터링</a>, <a href="../campaigns/modify-stop-campaign.md">캠페인 액세스</a> 섹션을 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 28일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 콘텐츠 조각 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Manager와 Adobe Journey Optimizer의 통합을 통해 이제 Journey Optimizer 콘텐츠 내에서 Adobe Experience Manager 콘텐츠 조각을 손쉽게 사용할 수 있습니다. 이 원활한 연결을 통해 Journey Optimizer에서 직접 AEM 콘텐츠에 손쉽게 액세스하고 사용할 수 있습니다.</p>
<p>이전에는 제한된 일부 조직에서만 사용할 수 있었던(LA) 이 기능을 이제 다음 개선 사항과 더불어 GA로 사용할 수 있습니다. [편집기 모드]를 사용하여 조각 서명 내에서 자리 표시자를 정의하고 개인화 값을 매핑할 수 있습니다.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>자세한 내용은 <a href="../integrations/aem-fragments.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 23일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Dynamic Media 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 Dynamic Media 자산을 바로 사용 및 액세스할 수 있습니다. 이 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.</p>
<ul>
<li>자산을 중앙에서 관리하며 실시간 업데이트를 확인합니다.</li>
<li>너비 및 높이와 같은 자산 설정을 즉시 수정합니다.</li>
<li>콘텐츠를 업데이트하고 개인화 필드를 추가하여 Dynamic Media 템플릿을 사용자 정의합니다.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../integrations/aem-dynamic.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 23일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이벤트 트리거 여정에 대한 보조 ID</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 주문 ID, 구독 ID 또는 처방전 ID와 같은 다른 식별자와 함께 프로필 ID를 사용하여 여정을 트리거함으로써 동일한 프로필이 한 번에 여러 차례 동일한 여정에 있도록 할 수 있습니다. 이를 통해 각 인스턴스가 자체 여정 경로를 따르면서 여러 주문 또는 구독을 동시에 관리할 수도 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/supplemental-identifier.md">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 23일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>콘텐츠 베리에이션 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 일반 가용성 릴리스에서는 이 기능에 다국어 콘텐츠 및 콘텐츠 실험 지원이 추가되어 다양한 언어 및 처리 빙식으로 베리에이션을 테스트할 수 있습니다. 또한 이제 프로필 속성 외에도 상황별 속성을 지원하므로 보다 동적이고 상황에 맞는 콘텐츠 테스트가 가능합니다.</p>
<img src="assets/do-not-localize/variants.gif">
<p>자세한 내용은 <a href="../test-approve/simulate-sample-input.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 23일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>대상자 읽기 일정을 배치 세분화 작업과 동기화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>배치 세분화 완료 후 일일 여정 실행을 트리거할 수 있습니다. 이제 모든 고객이 일별로 예약된 여정에서 이 옵션을 사용할 수 있습니다. 이 옵션을 사용하면 배치 세분화 작업에서 대상자 데이터를 기다리는 최대 6시간의 대기 시간을 정하여 여정을 최신 데이터로 실행하고, 준비되지 않은 경우 건너뛰도록 할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>자세한 내용은 <a href="../building-journeys/read-audience.md#schedule">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 20일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 정의 SMS 공급자</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 Sinch, Infobip, Twilio와 같은 기본 옵션 외에 추가 SMS 공급자를 구성할 수 있습니다. 사용자 정의 SMS 공급자 구성을 통해 서드파티 공급자를 직접 통합하고, 동적 메시지를 위한 고급 페이로드 사용자 정의를 활용하고, 동의 환경 설정(옵트인/옵트아웃)을 관리하여 규정 준수를 보장할 수 있습니다.</p>
<p>자세한 내용은 <a href="../sms/sms-configuration-custom.md">세부 설명서</a>를 참조하십시오.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>사용 가능한 날짜: 2025년 5월 20일</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 디자이너 테마</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사전 승인된 테마를 빠르게 적용하여 모든 이메일에 대한 브랜드 일관성을 보장하고, 캠페인을 만드는 프로세스의 속도를 높이고, 디자인 팀에 대한 의존도를 줄이면서 고품질 이메일을 독립적으로 만들 수 있습니다.</p>
<p>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/themes.gif">
<p>자세한 내용은 <a href="../email/apply-email-themes.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 14일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>결정 - 새로운 AI 공식 빌더</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 개선된 새 인터페이스에서 기준을 정하고 결합하여 구체적인 결정 순위 공식을 만들 수 있습니다. 정적 오퍼 우선순위에만 의존하는 대신 안내형 인터페이스를 통해 AI 모델 점수, 오퍼 우선순위, 프로필 속성, 오퍼 속성, 상황별 신호를 결합하는 사용자 정의 순위 공식을 정의할 수 있습니다.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>자세한 내용은 <a href="../experience-decisioning/ranking/ranking-formulas.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 14일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#25-05-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.


* **샌드박스 복사본에 대한 새 캠페인 오브젝트 지원** - 사용 가능한 날짜: 2025년 5월 15일

  이제 패키지 내보내기 및 가져오기 기능을 사용하여 여러 샌드박스에서 캠페인을 복사할 때 채널 구성, 실험 변형 및 설정, 결정 정책 및 항목 종속성도 복사됩니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md)

* **랜딩 페이지 폴더** - 사용 가능한 날짜: 2025년 5월 9일

  이제 랜딩 페이지를 쉽게 관리하기 위해 폴더를 사용하여 구조화된 계층으로 보다 효과적으로 정리할 수 있습니다. [자세히 보기](../landing-pages/manage-lp.md)

* **다이렉트 메일: SFTP 연결에 대한 SSH 키 지원** - 사용 가능한 날짜: 2025년 5월 5일

  이제 DM 파일 라우팅 구성에서 암호 인증 유형이 있는 기존 SFTP 외에도 SSH 키 인증이 있는 SFTP 서버로 DM 파일을 내보낼 수 있습니다. [자세히 보기](../direct-mail/direct-mail-configuration.md)

* **개인화를 위한 필 활성화** - 사용 가능한 날짜: 2025년 5월 5일

  개인화 편집기에 새로운 &quot;필&quot; 버튼이 추가되었습니다. 활성화하면 프로필 및 상황별 속성이 필 형태로 표시되어 코드의 가독성이 향상됩니다. [자세히 보기](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >이 기능은 향후 30일 동안 모든 환경에 점진적으로 적용될 예정입니다.

* **웹 채널의 ‘URL로 리디렉션’ 지원** - 사용 가능한 날짜: 2025년 5월 20일

  이제 시각적 편집기에서 새로운 베리에이션을 작성하는 대신 Journey Optimizer 웹 채널을 통해 방문자를 다른 기존 URL로 리디렉션할 수 있습니다. 이 기능을 사용하면 페이지 내 몇 가지 요소만 변경하는 것이 아니라, 완전히 다른 두 페이지를 비교하는 실험을 할 수 있습니다. [자세히 보기](../web/create-web.md#web-redirect-to-url)

* **템플릿 및 조각용 폴더** - 사용 가능한 날짜: 2025년 5월 20일

  폴더를 사용하면 오브젝트를 구조화된 계층으로 보다 쉽고 효과적으로 정리할 수 있습니다. 이전에는 일부 조직에서만 사용할 수 있던(LA) 폴더 기능을 이제 모든 사용자가 사용하여(GA) 콘텐츠 템플릿과 조각을 관리할 수 있습니다. [콘텐츠 템플릿](../content-management/access-content-templates.md#folders) 및 [조각](../content-management/manage-fragments.md#folders) 섹션에서 자세히 알아보십시오.

* **이메일 템플릿의 클릭 추적** - 사용 가능한 날짜: 2025년 5월 20일

  이제 [!DNL Journey Optimizer]에서 이메일 콘텐츠의 이미지 맵 내에 있는 `<area>` 요소에 대한 클릭 추적이 기본적으로 지원됩니다. 이는 이미지 맵 영역이 표준 하이퍼링크와 동일한 추적 래핑, 추적 데이터, 추가 매개 변수를 받도록 하기 위한 것입니다. [메시지 추적에 대해 자세히 알아보기](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **캠페인 목록의 오른쪽 레일** - 사용 가능한 날짜: 2025년 5월 20일

  이제 캠페인 목록에서 캠페인을 선택하면 세부 정보가 표시되는 창이 열립니다.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## 25년 4월 릴리스 정보 {#25-4-rn}

**릴리스 날짜**: 2025년 4월 29~30일

### 새로운 기능 {#25-04-features}

다음은 이번 릴리스의 새로운 기능 목록입니다.

<table>
<thead>
<tr>
<th><strong>개인화 편집기 - 실습 기능</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 개인화 표현식을 실험할 수 있는 공간인 개인화 플레이그라운드를 사용할 수 있습니다. 샘플 템플릿 및 페이로드를 탐색하여 자신만의 개인화 표현식을 시작하고 사용해 볼 수 있습니다.</p>
<p>자세한 내용은 <a href="../personalization/personalize.md#playground">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2025년 4월 24일</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>LINE 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer는 LINE 채널에 대한 지원을 포함하도록 크로스 채널 기능을 확장했습니다. 이 향상된 기능을 통해 LINE 경험을 만들고 편집하고 미리 볼 수 있으므로 보다 개인화되고 매력적인 상호 작용을 제공할 수 있습니다. LINE을 사용하여 더 많은 고객과 소통하고 관련 콘텐츠를 전송하며 참여도를 개선할 수 있습니다.</p>
<p>Adobe Journey Optimizer 고객은 요청 시 LINE 채널을 활성화할 수 있습니다. 조직에서 해당 기능을 활성화하려면 Adobe 고객 지원 센터 또는 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../line/get-started-line.md">세부 설명서</a>를 참조하십시오.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>여정 지표</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 지표를 사용하면 비즈니스의 주요 지표 전반에 걸쳐 활동이 미치는 영향을 측정하고 성과에 대해 보다 명확한 인사이트를 제공할 수 있습니다.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>자세한 내용은 <a href="../building-journeys/success-metrics.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2025년 4월 9일</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Adobe Express 통합(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer가 Adobe Express와 통합되어 크리에이티브 자산을 여정 오케스트레이션과 원활하게 연결할 수 있습니다. 이 통합으로 개인화된 콘텐츠를 디자인하고 여러 캠페인에 걸쳐 배포하는 프로세스가 간소화됩니다. </p>
<p>이 통합은 현재 Healthcare Shield 또는 Privacy and Security Shield와 함께 사용할 수 없습니다.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>자세한 내용은 <a href="../integrations/express.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>배치 세분화 완료 후 일일 여정 실행 트리거(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>일일 예약 여정의 경우, 새로운 옵션을 사용하면 배치 세분화 작업에서 대상자 데이터를 기다리는 최대 6시간의 시간대를 정의하여 여정을 최신 데이터로 실행하고, 준비되지 않은 경우 건너뛰도록 할 수 있습니다. 배치 대상자 평가 후 트리거 옵션은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../building-journeys/read-audience.md#schedule">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>브랜드 정렬 점수(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[브랜드 정렬 점수] 기능은 [이메일 디자이너]에서 직접 명확한 피드백을 제공하여 콘텐츠가 브랜드의 톤, 스타일, 지침에 맞는지 여부를 확인하는 데 도움이 됩니다. 이 기능은 Beta로 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../content-management/brands-score.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### 개선 사항 {#25-04-improv}

**캠페인 미리 보기 API**

기존 증명 전송 기능 외에 새로운 API를 사용하여 캠페인을 미리 볼 수 있습니다. [자세히 보기](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**샌드박스 도구**

* **사용자 정의 액션에 샌드박스 도구 적용**

  이제 사용자 정의 액션이 샌드박스 도구 기능을 사용하여 복사할 수 있는 Adobe Journey Optimizer 오브젝트 목록에 포함되어 테스트 및 배포가 간소화됩니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md)

* **캠페인에 샌드박스 도구 적용** - 가용성 일자: 2025년 4월 3일

  이제 패키지 내보내기 및 가져오기 기능을 사용하여 여러 샌드박스 간에 캠페인을 복사할 수 있습니다. 캠페인은 프로필, 대상자, 스키마, 인라인 메시지, 종속 오브젝트와 관련된 모든 항목과 함께 복사됩니다. 결정 항목, 데이터 사용 레이블, 언어 설정과 같은 일부 항목은 복사되지 않습니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#custom-actions)

**개인화**

* **새로운 상황별 속성**

  이제 개인화 편집기에서 새로운 상황별 속성인 **메시지 프로필 ID**&#x200B;를 선택할 수 있습니다. 이 속성은 게재 시 각 타기팅된 프로필로 전송된 각 메시지를 고유하게 식별하는 메시지 지향 속성입니다. 이 고유 식별자는 예를 들어 수신자가 열거나 클릭한 각 링크를 구별하기 위한 URL 추적 매개 변수로 사용할 수 있습니다.

* **속성 창의 채워진 속성** - 가용성 일자: 2025년 4월 2일

  이제 개인화 편집기의 속성 창에 기본적으로 채워진 속성만 표시됩니다. 모든 속성을 보려면 설정 버튼을 사용하여 **[!UICONTROL 채워진 속성만 표시]** 옵션을 끕니다. [자세히 보기](../personalization/personalization-build-expressions.md)

**이메일 채널**

* **개인화된 URL 추적** - 가용성 일자: 2025년 4월 30일

  이메일 설정을 보다 유연하게 관리하고 세밀하게 제어하기 위해 이제 콘텐츠의 각 링크에 대해 [이메일 디자이너]에서 하나하나 작업을 수행할 필요 없이 이메일 채널 구성 수준에서 모든 URL 추적 매개 변수를 한 번에 개인화할 수 있습니다. [자세히 보기](../email/surface-personalization.md#personalize-url-tracking)

* **이메일 디자이너** - 가용성 일자: 2025년 4월 1일

  Journey Optimizer의 접근성을 높이기 위해 이제 이메일 디자이너에서 새 필드 두 가지를 사용할 수 있습니다. 이 두 필드는 이메일 콘텐츠의 `<title>` 요소와, `<html>` 요소의 `lang` 속성에 해당합니다. 이메일 **[!UICONTROL 본문]** 섹션에서 **[!UICONTROL 프리헤더]** 필드에 더해 이 설정을 정의할 수 있습니다. [자세히 보기](../email/email-metadata.md)

**사용 사례 플레이북**

* **플레이북 작성 및 공유(Private Beta)** - 이제 나만의 사용 사례 플레이북을 만들고 관리하고 공유할 수 있습니다. 이 기능은 현재 Private Beta로 일부 조직에서만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오. [자세히 보기](../start/playbooks.md)

**탐색**

* **콘텐츠 관리** - 가용성 일자: 2025년 4월 2일

  이제 콘텐츠 템플릿과 조각을 쉽게 관리하기 위해 폴더를 사용하여 구조화된 계층 구조로 보다 효과적으로 구성할 수 있습니다. [콘텐츠 템플릿](../content-management/access-content-templates.md#folders) 및 [조각](../content-management/manage-fragments.md#folders) 섹션에서 자세히 알아보십시오.

  >[!AVAILABILITY]
  >
  >이 개선 사항은 일부 조직에서만 사용할 수 있습니다(제한된 가용성).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## 25년 3월 릴리스 정보 {#25-3-rn}

### 새로운 기능 {#25-03-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Dynamic Media 통합(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 Dynamic Media 자산을 바로 사용 및 액세스할 수 있습니다. 이 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.
<ul>
<li>자산을 중앙에서 관리하며 실시간 업데이트 확인</li>
<li>너비 및 높이와 같은 자산 설정을 즉시 수정</li>
<li>Dynamic Media 템플릿의 콘텐츠를 업데이트하고 개인화 필드를 추가하여 사용자 정의</li>
</ul>
<p>
<p>이 통합은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../integrations/aem-dynamic.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Adobe GenStudio 통합(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 마케팅 효율을 높이고 브랜드 일관성을 유지하기 위해 GenStudio for Performance Marketing 경험을 Journey Optimizer와 원활하게 통합할 수 있습니다. 이를 통해 Journey Optimizer의 고급 오케스트레이션 기능과 함께 GenStudio의 AI 기반 콘텐츠 생성을 활용할 수 있습니다.<p>
<p>Journey Optimizer의 GenStudio 통합은 현재 Healthcare Shield 또는 Privacy and Security Shield와 함께 사용할 수 없습니다(제한된 가용성).</p>
<p>자세한 내용은 <a href="../integrations/genstudio.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>유연한 대상자 평가(GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 유연한 대상자 평가를 이제 모든 사용자가 사용할 수 있습니다(GA). 이 기능을 사용하면 선택한 대상자에 대해 온디맨드로 세분화 작업을 실행할 수 있어 대상자를 Journey Optimizer 여정 및 캠페인으로 타기팅하기 전에 항상 최신 대상자 데이터를 보유할 수 있습니다.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>자세한 내용은 <a href="../audience/creating-a-segment-definition.md#flexible">세부 설명서</a>를 참조하십시오.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### 개선 사항 {#25-03-improv}

**개인화 편집기**(사용 가능한 날짜: 3월 12일)

Journey Optimizer 개인화 편집기가 다음과 같은 새로운 기능으로 업데이트되었습니다.
* **코드 편집기 디자인 업데이트** - 유용성과 집중도 개선을 위한 깔끔하고 현대적인 인터페이스를 적용했습니다.
* **검색 및 바꾸기** - 편집기 내에서 콘텐츠를 빠르게 찾고 바꿀 수 있는 기능이 추가되었습니다.
* **실행 취소 및 다시 실행 지원** - 변경 내용을 쉽게 되돌리거나 다시 적용할 수 있습니다.
* **사용자 정의 가능한 글꼴 크기** - 편집기의 글꼴 크기를 조정하여 가독성을 높일 수 있습니다.
* **인라인 JSON 유효성 검사** - JSON 콘텐츠에 대한 실시간 클라이언트측 유효성 검사를 제공하여 오류 감지 속도를 높입니다.
* **프로필 및 컨텍스트 속성 자동 완성** - 콘텐츠 작성을 간소화하는 스마트 제안을 제공합니다.
* **향상된 구문 강조 표시** - 코드 구조를 보다 시각적으로 구분하기 쉽게 하여 가독성을 개선합니다.

![개인화 편집기의 새로운 기능을 보여 주는 비디오](assets/do-not-localize/personalization-editor.gif)

자세한 내용은 [세부 설명서](../personalization/personalization-build-expressions.md)를 참조하십시오.

**승인**

이제 승인 정책에 대한 조건을 정의할 때 [태그] 및/또는 [오브젝트 카테고리]별로 필터링할 수 있는 옵션이 제공됩니다.

자세한 내용은 [세부 설명서](../test-approve/approval-policies.md)를 참조하십시오.

**구성**

* 이제 채널 구성에 Adobe Experience Platform 통합 태그를 할당할 수 있습니다. 이 방법으로 항목을 쉽게 분류하고, 모든 목록에서 검색과 탐색을 개선할 수 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md#channel-config-tags)

* 이제 Journey Optimizer에서 이메일 하위 도메인을 설정하거나 편집할 때 연결된 DMARC 레코드를 상위 도메인에서 사용 가능한 경우 직접 관리하도록 선택할 수 있습니다. [자세히 알아보기](../configuration/dmarc-record.md#set-up-dmarc)

**비즈니스 규칙**

이제 배치 세분화를 통해 여정 및 캠페인에서 일일 빈도 상한 설정을 사용할 수 있습니다. 일일 빈도 상한 설정 규칙의 정확도를 보장하려면 캠페인이나 여정을 작성할 때 우선 순위가 가장 높은 네임스페이스를 선택해야 합니다. [플랫폼 ID 서비스 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}에서 네임스페이스 우선 순위에 대해 자세히 알아보십시오.

다시 말씀드리지만, 규칙 세트의 일일 빈도 상한 설정은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

비즈니스 규칙에 대한 자세한 내용은 [세부 설명서](../conflict-prioritization/rule-sets.md)를 참조하십시오.

**콘텐츠 템플릿**

HTML 유형 콘텐츠 템플릿은 이제 사용되지 않습니다. [!DNL Journey Optimizer]에서 이전에 만든 기존 HTML 콘텐츠 템플릿은 계속 사용할 수 있습니다. [콘텐츠 템플릿에 대해 자세히 알아보기](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## 2025년 2월 릴리스 정보 {#25-02-rn}

**릴리스 날짜**: 2026년 2월 18~19일


### 새로운 기능 {#25-02-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>비즈니스 규칙 만들기 및 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 규칙 세트를 사용하여 비즈니스 규칙을 만들 수 있습니다. 규칙 세트는 캠페인 내에서 보내는 메시지와 채널 간 여정 작업을 제한하고 프로필의 여정 진입을 제어하는 데 도움이 되는 규칙 그룹입니다.<p>
<p><ul><li>채널 규칙 세트를 만들어 한 채널 또는 여러 채널에서 전송되는 메시지 수를 제한합니다. 캠페인 또는 여정 작업에 적용하여 규칙 세트에 정의된 규칙을 시행합니다. 채널 규칙 세트를 사용하면 커뮤니케이션 유형에 따른 캡핑 규칙을 적용할 수 있습니다. 예를 들어 "프로모션 메시지"를 제한하는 규칙 세트를 설정하고 "뉴스레터"에 대해 또 다른 규칙 세트를 설정할 수 있습니다. 보내는 커뮤니케이션 유형에 따라 캠페인 또는 여정 작업에 적절한 규칙 세트를 적용합니다.</li>
<li> 프로필의 여정 진입을 제어하려면 여정 규칙 세트를 만듭니다. 프로필이 지정된 기간 내에 여정에 진입할 수 있는 빈도 또는 프로필을 동시에 등록할 수 있는 여정 수를 제한합니다. 여정 수준에서 이를 적용하여 적절한 진입 관리를 보장합니다.</li></ul></p>
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 비즈니스 규칙을 이제 모든 사용자가 사용할 수 있습니다(GA). 여정 도메인 비즈니스 규칙은 여전히 제한된 일부 조직에서만 사용할 수 있습니다(LA).</p>
<p>자세한 내용은 <a href="../conflict-prioritization/rule-sets.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 어시스턴트로 랜딩 페이지 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 AI 어시스턴트의 도움을 받아 전체 페이지 디자인, 개인화된 텍스트, 사용자 정의 시각 자료 등 랜딩 페이지에 사용할 매력적인 콘텐츠를 제작할 수 있습니다.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>자세한 내용은 <a href="../content-management/generative-lp.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>AI 어시스턴트를 통한 브랜드 작업(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 고유한 브랜드를 설정하여 브랜드의 시각적 및 언어적 정체성을 정의할 수 있습니다. </p>
<p>이 기능은 제한된 수의 고객을 위한 Private Beta로 출시됩니다. 향후 릴리스에서 점진적으로 사용 범위를 확대하여 모든 고객에게 제공할 예정입니다.</p>
<p>자세한 내용은 <a href="../content-management/brands.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 지정 작업 문제 해결</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 직접 실제 API 호출을 수행하여 사용자 정의 액션 구성의 유효성을 검사할 수 있습니다. 이 새로운 기능은 여정에서 사용자 정의 작업을 사용하기 전이나 후에 문제를 해결하는 데 도움이 됩니다. </p>
<p>자세한 내용은 <a href="../action/troubleshoot-custom-action.md">세부 설명서</a>를 참조하십시오.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>유연한 대상자 평가(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>유연한 대상자 평가를 사용하면 선택한 대상자에 대해 온디맨드로 세분화 작업을 실행할 수 있어 대상자를 Journey Optimizer 여정 및 캠페인으로 타기팅하기 전에 항상 최신 대상자 데이터를 보유할 수 있습니다.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>자세한 내용은 <a href="../audience/creating-a-segment-definition.md#flexible">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>사용 가능한 날짜: 2025년 1월 28일</p>
</tr>
</tbody>
</table>
</table>


### 개선 사항 {#25-02-improvements}

2월 업데이트에서는 아래의 개선 사항이 제공됩니다.

* **데이터 세트 TTL(Time-to-Live)** - 이번 달부터 새로운 샌드박스와 새로운 조직에서 Journey Optimizer 시스템 생성 데이터 세트에 TTL(Time-to-Live) 가드레일이 다음과 같이 롤아웃됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 데이터 레이크의 데이터에 대해 13개월

  이 변경 사항은 차후 기존 고객 샌드박스에 대해서도 롤아웃됩니다. 

  [해당 FAQ](../data/datasets-ttl.md#frequently-asked-questions)에서 이 업데이트에 대해 자세히 알아보세요.

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **다이렉트 메일** - 이제 다이렉트 메일 채널 구성에서 파일 라우팅에 대해 새로운 서버 유형인 데이터 랜딩 구역이 지원됩니다. [자세히 보기](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** - 이제 게재, 피드백, 인바운드 및 콜백 URL을 재정의하여 다중 지역 엔드포인트의 SMS 메시지 게재를 관리할 수 있습니다. 이를 지원하기 위해 새 필드인 재정의 URL이 API 자격 증명 구성에 추가되었습니다. 이 변경 사항은 Sinch 공급자에서만 사용할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

* **개인화**(사용 가능한 날짜: 2025년 1월 29일) - 새로운 날짜/시간 도우미 함수를 개인화 편집기에서 사용할 수 있습니다. [자세히 보기](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **이메일 구성** - Adobe 외부에서 동의를 관리하는 경우 이제 이메일 채널 구성 설정의 일부로 사용자 정의 구독 취소 이메일 주소와 사용자 정의 원클릭 구독 취소 URL을 설정할 수 있습니다. [자세히 보기](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **의사 결정**(사용 가능한 날짜: 2025년 1월 28일) - 이제 의사 결정에서 항목 카탈로그의 스키마를 편집할 때 오브젝트 데이터 형식을 지원합니다. [자세히 보기](../experience-decisioning/catalogs.md)
