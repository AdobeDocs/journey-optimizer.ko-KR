---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c00d5a97e7bedf6f1a22a59cc3bd7588eb9ad32e
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 61%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 여기 있는 릴리스 정보에 통합됩니다. [!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하십시오.


## 2025년 6월 초기 릴리스 정보 {#25-6-rn}


**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면 및 업데이트된 설명서는 릴리스 날짜에 게시됩니다.

**릴리스 날짜**: 2025년 6월 17~18일

[Adobe Experience Platform 시험판 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하세요.

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

* **캠페인** - 액션 캠페인에 대한 새로운 탭 탐색. 이 새로운 탐색 패턴을 통해 콘텐츠 작성에 보다 빠르게 액세스하고 캠페인 간 설정을 더욱 확장할 수 있습니다.

* **Decisioning** - 사용 가능한 날짜: 2025년 6월 3일

  이제 결정 오브젝트를 샌드박스 간에 복사할 수 있어 테스트 및 배포 워크플로가 간소화됩니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md#decisioning)

* **의사 결정 규칙에 대한 의사 결정 항목 특성 지원** - 사용 가능한 날짜: 2025년 6월 4일

  이제 의사 결정 항목 속성을 활용하여 의사 결정 규칙을 만들 수 있습니다. [자세히 보기](../experience-decisioning/rules.md#create)

* **대화형 메시지 실행 API 업데이트** - 사용 가능한 날짜: 2025년 6월 6일

  이제 대화형 메시지 실행 API를 사용하여 예정된 캠페인 실행 일정을 삭제할 수 있습니다. [자세히 보기](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

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
<p>이 변경 사항은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 액세스 권한을 요청하려면 <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">이 양식</a>을 사용하세요.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>자세한 내용은 다음 섹션을 참조하십시오. <a href="../building-journeys/journey-ui.md">여정 검색 및 필터링</a>, <a href="../campaigns/modify-stop-campaign.md">캠페인 액세스</a>.</p>
<p>사용 가능한 날짜: 2025년 5월 28일 목요일</p>
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
<p>이전에는 제한된 조직 세트(LA)에서 사용할 수 있었지만, 이제 다음과 같은 향상된 기능을 통해 GA됩니다. 이제 편집기 모드를 사용하여 조각 서명 내에서 자리 표시자를 정의하고 개인화 값을 매핑할 수 있습니다.</p>
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
<p>사용 가능한 날짜: 2025년 5월 20일 수요일</p>
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
<p>사용 가능한 날짜: 2025년 5월 20일 수요일</p>
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
<p>자세한 내용은 <a href="../experience-decisioning/exd-ranking-formulas.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 5월 14일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#25-05-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.


* **샌드박스 복사본에 대한 새 캠페인 개체 지원** - 사용 가능한 날짜: 2025년 5월 15일

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

* 웹 채널에서 **&#39;URL로 리디렉션&#39; 지원** - 사용 가능한 날짜: 2025년 5월 20일

  이제 시각적 편집기에서 새로운 베리에이션을 작성하는 대신 Journey Optimizer 웹 채널을 통해 방문자를 다른 기존 URL로 리디렉션할 수 있습니다. 이 기능을 사용하면 페이지 내 몇 가지 요소만 변경하는 것이 아니라, 완전히 다른 두 페이지를 비교하는 실험을 할 수 있습니다. [자세히 보기](../web/create-web.md#web-redirect-to-url)

* **템플릿 및 조각용 폴더** - 사용 가능한 날짜: 2025년 5월 20일

  폴더를 사용하면 오브젝트를 구조화된 계층으로 보다 쉽고 효과적으로 정리할 수 있습니다. 이전에는 일부 조직에서만 사용할 수 있던(LA) 폴더 기능을 이제 모든 사용자가 사용하여(GA) 콘텐츠 템플릿과 조각을 관리할 수 있습니다. [콘텐츠 템플릿](../content-management/access-content-templates.md#folders) 및 [조각](../content-management/manage-fragments.md#folders) 섹션에서 자세히 알아보십시오.

* **전자 메일 템플릿의 클릭 추적** - 사용 가능한 날짜: 2025년 5월 20일

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

