---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 72%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 여기 있는 릴리스 정보에 통합됩니다. [!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.


## 2025년 6월 릴리스 정보 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**릴리스 일자**: 2025년 6월 18일

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 새로운 기능 {#25-06-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.


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
<th><strong>여정의 컨텐츠 결정 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 캔버스에서 전용 콘텐츠 결정 활동을 통해 여정에 개인화된 오퍼를 포함하고 조건 및 사용자 지정 작업을 포함한 여정 활동에 사용할 수 있습니다.</p>
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


<table>
<thead>
<tr>
<th><strong>decisioning의 Adobe Experience Platform 데이터 세트(베타)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에는 개인화에 사용할 수 있었지만, 이제 Adobe Experience Platform 데이터 세트를 의사 결정에 활용할 수 있습니다. 이렇게 하면 속성을 한 번에 하나씩 수동으로 업데이트할 필요 없이 주기적으로 변경되는 벌크 업데이트에 대해 의사 결정 속성의 정의를 데이터 세트의 추가 데이터로 확장할 수 있습니다. 예: 가용성, 대기 시간 등</p>
<p>이 기능은 현재 모든 고객이 공개 Beta로 사용할 수 있습니다. 액세스하려면 계정 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../experience-decisioning/aep-data-exd.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 6월 20일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#25-06-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

* **채널 규칙 세트**

   * **시간 제한을 위한 사용자 지정 기간 창** - 이제 채널 규칙 집합 구성 화면에서 새 **간격** 필드를 사용할 수 있으므로 지정된 기간에 따라 여러 날, 주 또는 달에 걸쳐 빈도 제한 규칙을 적용할 수 있습니다.

   * **시간별 재설정 최대 가용량** - 이제 채널 규칙 집합에 시간별로 최대 가용량 설정을 적용할 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 고객 지원 센터에 문의하여 활성화하십시오.

   * **일별 기간** - 이전에는 제한된 가용성에서 사용할 수 있었지만, 이제 채널 규칙 세트의 &quot;일별&quot; 빈도 제한을 모든 고객이 사용할 수 있습니다.

  자세한 내용은 [세부 설명서](../conflict-prioritization/channel-capping.md)를 참조하십시오.

* **코드 기반 경험**

   * 이제 코드 기반 경험 콘텐츠 템플릿에서 의사 결정 정책을 추가할 수 있습니다. 이 템플릿을 사용하여 편집 가능한 양식 필드의 오퍼를 활용할 수 있습니다. [자세히 보기](../code-based/code-based-form-fields.md)

   * 이제 코드 기반 경험 여정 또는 캠페인 버전 화면에서 개인화 편집기를 열지 않고도 의사 결정 정책을 직접 추가할 수 있습니다. [자세히 보기](../code-based/create-code-based.md#edit-code)

* **이메일 디자이너의 사용자 정의 CSS 지원**

  이제 Journey Optimizer을 사용하여 이메일 Designer 내에서 바로 이메일 콘텐츠에 사용자 지정 CSS를 추가할 수 있습니다. [자세히 보기](../email/custom-css.md)

* **캠페인에 새로운 탭 탐색 적용**

  새로운 탐색 패턴을 통해 콘텐츠 작성에 보다 빠르게 액세스하고 캠페인 간 설정을 더욱 확장할 수 있습니다. [자세히 보기](../campaigns/create-campaign.md)

* **결정**

   * **샌드박스 복사 및 의사 결정**(사용 가능한 날짜: 2025년 6월 3일) - 이제 의사 결정 개체를 샌드박스 간에 복사할 수 있으므로 테스트 및 배포 워크플로를 간소화할 수 있습니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **의사 결정 규칙에 대한 의사 결정 항목 특성 지원**(사용 가능한 날짜: 2025년 6월 4일) - 이제 의사 결정 항목 특성을 활용하여 의사 결정 규칙을 만들 수 있습니다. [자세히 보기](../experience-decisioning/rules.md#create)

* **Interactive Message Execution API 업데이트** - 사용 가능한 날짜: 2025년 6월 6일

  이제 Interactive Message Execution API를 사용하여 예정된 캠페인 실행 일정을 삭제할 수 있습니다. [자세히 보기](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
