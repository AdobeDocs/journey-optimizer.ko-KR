---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: a9c74b396e24fec418f0556124a07d482b015825
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 41%

---

# 사전 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 2월 프리릴리스 정보 {#feb-26-01-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 일자**: 2026년 2월 17일 수요일

### 새로운 기능 {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>아웃바운드 메시지의 웨이브 전송</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>캠페인 또는 여정의 아웃바운드 메시지가 시간에 따라 제어된 배치로 전달되도록 예약할 수 있습니다.</p>
<p>웨이브 전송은 다음과 같은 이점을 제공합니다.</p>
<ul>
<li>전달성 향상 - Spread는 시간이 지남에 따라 전송을 수행하여 강력한 발신자 평판을 유지하고 스팸으로 플래그가 지정될 위험을 줄이는 데 도움이 됩니다.</li>
<li>로드 제어 - 한 번에 전송되는 메시지 수를 제한하여 압도적인 다운스트림 시스템(예: 콜 센터, 랜딩 페이지)을 방지합니다.</li>
<li>대량의 시간에 민감한 사용 사례 - 대규모 대상자에 적합하거나 시간 조절(예: 콜 센터 용량, 램프 업 또는 시간 제한 제안)이 필요한 경우.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11533">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일용 CC(참조)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 설정에서 선택적 CC(Carbon Copy) 필드를 구성할 수 있습니다. BCC와 달리 CC 수신자는 1차 수신자가 볼 수 있어 투명한 의사소통이 가능하고 소유권이 명확해진다.</p>
<p>이를 통해 관계 관리자나 계정 소유자와 같은 각 메시지에 적합한 이해 당사자를 자동으로 복사하는 동시에 고객이 후속 조치를 위해 연락할 사람을 알 수 있습니다.</p>
<p>CC 필드는 개인화를 지원하므로 단일 구성이 프로필 데이터를 기반으로 복사본을 동적으로 라우팅하여 추가 설정 없이 여러 사용 사례에서 확장 가능합니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14051">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 중재</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 수식 및 AI 모델을 사용하여 고객 프로필 속성 및 컨텍스트 요인에 따라 여정 우선 순위 점수를 자동으로 높여 고객이 가장 관련성이 높은 여정을 입력하도록 할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13976">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: 채널 컨텐츠 만들기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform Agent Orchestrator을 기반으로 하는 Journey Agent은 Journey Optimizer에서 사용할 수 있으며 자연어 인터페이스를 통해 여정을 분석할 수 있도록 합니다. 이제 Journey 에이전트에서 직접 채널별 콘텐츠를 생성 및 관리하고, 이메일 및 푸시와 같은 채널을 위한 콘텐츠를 작성하고, 템플릿을 적용하고 미리 보고, 프롬프트를 통해 톤과 스타일을 개선하고, 컨텍스트를 확인하며 편집하기 위해 콘텐츠 디자이너에서 콘텐츠를 열 수도 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>모바일 라이브 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>라이브 활동은 모바일 앱 내에서 실시간 업데이트와 대화형 경험을 제공하여 사용자가 디바이스의 화면에서 직접 진행 중인 이벤트 또는 작업에 대한 정보를 유지할 수 있도록 합니다. 이 기능은 사용자가 앱을 열지 않아도 진행 추적, 이벤트 업데이트 또는 대화형 콘텐츠와 같은 라이브 정보를 전달하여 참여도를 높입니다.</p>
<p>이전에 베타 버전으로 출시된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13588">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 액션 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer가 단일 액션과 여러 액션이 있는 인바운드 액션 그룹을 모두 구성할 수 있는 포괄적 액션 활동을 새롭게 지원하여 여정 캔버스 내 액션 구성을 간소화할 수 있습니다. 특히 이 새로운 기능에는 다음과 같은 이점이 있습니다.</p>
<ul>
<li>여정 캔버스 내 기본 액션 구성 간소화.</li>
<li>다중 액션 인바운드 액션 그룹을 만들 수 있는 용량.</li>
<li>모든 기본 제공 채널 액션에 최적화를 더하는 기능.</li>
<li>모든 작업에 실험과 다국어 옵션을 모두 추가하는 기능.</li>
</ul>
<p>이제 모든 환경에서 이 기능을 사용할 수 있습니다(일반 공급).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>웹 푸시 알림 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer가 이제 웹 푸시 알림을 지원하여 푸시 채널을 모바일 밖까지 확장합니다. 모바일 브라우저와 데스크탑 브라우저 모두에 알림을 원활하게 전달할 수 있으므로 앱 설치를 요청할 필요 없이 고객의 디바이스에서 직접 고객에게 연락할 수 있습니다. 이 향상된 기능을 통해 이미 모바일 푸시에서 사용 가능한 것과 동일한 작성 워크플로 및 타기팅 기능을 활용하여 사용자에게 적시에 개인화된 메시지를 실시간으로 보낼 수 있습니다.</p>
<p>이전에 베타 버전으로 출시된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p>사용 가능한 날짜: 2026년 2월 12일 금요일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>콘텐츠 결정 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 맞춤형 오퍼를 고객 여정에 직접 통합하기 위한 새로운 컨텐츠 의사 결정 활동을 여정 캔버스에서 사용할 수 있습니다. 이 활동을 사용하면 의사 결정 기반 콘텐츠를 제공하고 자격 기반 분기를 만들기 위한 조건, 외부 시스템에 오퍼 데이터를 전달하기 위한 사용자 지정 작업 및 완전히 개인화된 고객 경험을 구축하기 위한 기타 활동에서 여정 전체에서 이러한 오퍼를 참조할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/content-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 11일 목요일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>셀프서비스 마이그레이션 도구 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>마이그레이션 도구 API</strong>를 사용하여 의사 결정 관리 엔터티를 프로그래밍 방식으로 Decisioning으로 마이그레이션할 수 있습니다. 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>유연한 마이그레이션 범위(샌드박스, 오퍼 또는 의사 결정 수준)</li>
<li>자동화된 종속성 분석 및 유효성 검사</li>
<li>완료된 마이그레이션에 대한 롤백 지원</li>
<li>오브젝트 매핑이 포함된 자세한 마이그레이션 보고서</li>
</ul>
<p>자세한 내용은 <a href="../experience-decisioning/decisioning-migration-api.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 3일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13837">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 정의 액션 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 모니터링 대시보드와 보강된 여정 단계 이벤트 데이터로 <strong>사용자 정의 액션 엔드포인트</strong>의 상태와 성능에 대한 심층 인사이트를 얻을 수 있습니다. 성공한 호출, 오류, 처리량, 응답 시간, 대기열 대기 시간을 추적하여 예외 항목이 발생하는 시점, 위치, 이유를 신속하게 파악합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../action/reporting.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 3일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>Decisioning</strong>을(를) 사용하여 <strong>SMS 메시지</strong>의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선순위 점수, 공식 또는 AI 모델을 사용하여 고객에게 최상의 콘텐츠를 표시합니다.</p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 2일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#feb-26-01-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### 구성

* **경험 이벤트 조회 사용 중단** - 2026년 4월 1일부터 여정 조건 식 편집기의 경험 이벤트 조회가 지난 90일 동안 경험 이벤트 조회를 사용하지 않은 조직에 대해 사용되지 않습니다. 이 기능은 2025년 7월 8일 이후 신규 고객 조직에서 이미 사용할 수 없습니다. 대안은 [여정의 경험 이벤트 조회](../building-journeys/exp-event-lookup.md)를 참조하십시오.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14136">DOCAC JIRA 작업에 연결</a>

* **하위 도메인 위임 방법 전환** - 이제 하나의 하위 도메인 위임 방법에서 다른 하위 도메인 위임 방법으로 전환할 수 있습니다. 이렇게 하면 CNAME 위임 모드를 사용하여 도메인을 회사의 보안 정책을 준수하도록 사용자 지정 위임 방법으로 마이그레이션할 수 있습니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13610">DOCAC JIRA 작업에 연결</a>

#### 이메일 디자이너

* **브랜드 테마를 사용하여 이미지를 이메일 템플릿으로 변환** - Journey Optimizer에서 이미지를 이메일 템플릿으로 변환할 때 이제 테마를 입력으로 사용하여 생성된 HTML이 브랜드 매개 변수를 따르도록 할 수 있습니다. 배경색, 단추 색상, 글꼴, 줄 간격, 여백 및 패딩과 같은 스타일이 자동으로 적용되어 수동 디자인 작업이 줄어들고 최소한의 편집으로 사용할 준비가 된 템플릿을 제공합니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14105">DOCAC JIRA 작업에 연결</a>

* **새 색상 탭으로 브랜드 업데이트** - 브랜드 가이드라인은 모든 접점에서 브랜드가 일관되게 표시되도록 하는 데 도움이 됩니다. 새 색상 섹션은 브랜드 색상 시스템에 대한 표준을 정의하며 경험을 통해 색상을 선택, 구성 및 적용하는 방법에 대해 대략적으로 설명합니다. 기본, 보조, 강조, 중립 색상을 일관되게 사용하여 일치도와 접근성이 높으며 인식히기 쉬운 브랜드 아이덴티티를 만드는 작업을 지원합니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">DOCAC JIRA 작업에 연결</a>

#### AI

* **사용자 지정 Firefly 모델 및 타사 이미지 생성 모델의 통합** - 표준 및 사용자 지정 Firefly 모델과 승인된 타사 이미지 모델(예: NanoBanana)을 매끄럽게 통합하여 이미지를 생성할 때 더 큰 유연성, 제어 및 브랜드 정렬을 제공합니다. 이를 통해 일반적인 요구 사항을 위한 표준 Firefly, 브랜드 내 생성을 위한 사용자 지정 Firefly 또는 전문 또는 실험 시나리오를 위한 승인된 서드파티 모델 등 각 사용 사례에 가장 적합한 모델을 선택할 수 있습니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13918">DOCAC JIRA 작업에 연결</a>

#### 캠페인

* **여정 및 캠페인용 폴더** - 이제 인터페이스 탐색 및 관리를 개선하기 위해 여정 및 캠페인을 폴더로 구성할 수 있습니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC JIRA 작업에 연결</a>

#### 경험 결정

* **코드 기반 경험 채널에서 경험 의사 결정 미리 보기** - 이제 코드 기반 경험 채널에서 경험 의사 결정을 구성할 때 의사 결정 항목을 미리 볼 수 있습니다. 미리보기는 라이브로 전환되기 전에 작성 인터페이스에서 직접 사용할 수 있습니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14082">DOCAC JIRA 작업에 연결</a>

* **상위 AI 모델 가시성** - 이제 Journey Optimizer을 통해 Decisioning에서 AI 모델의 상태, 교육 상태 및 성능을 모니터링할 수 있으므로 교육 성공을 확인하고, 오류를 해결하며, 결과에 미치는 영향을 이해할 수 있습니다. 이 기능은 개인화된 최적화 모델(자동 최적화는 아님)에만 사용할 수 있습니다.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14040">DOCAC JIRA 작업에 연결</a>

* **결정 항목에 조각 첨부** - 이제 Journey Optimizer가 결정 항목에 조각을 첨부할 수 있는 기능을 제공합니다. 따라서 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있습니다.

  **참고**: 이제 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 2월 12일

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">DOCAC JIRA 작업에 연결</a>

#### 여정

* **여정의 여러 인바운드 액션** - 이제 여정 오케스트레이션을 단순화하기 위해 단일 여정에서 여러 인바운드 액션을 정의할 수 있습니다. 이전에 캠페인에서 사용할 수 있었던 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며 각 작업에는 특정 콘텐츠가 포함되어 있습니다.

  **참고**: 이제 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">DOCAC JIRA 작업에 연결</a>

* **SMS Webhooks** - 이제 모든 SMS 공급자에서 Webhooks가 지원됩니다. 각 웹후크의 의도된 목적, 수신 메시지를 캡처하기 위한 인바운드 웹후크 및 게재 확인, 상태 업데이트 및 기타 메시지 관련 이벤트를 수신하기 위한 피드백 웹후크를 구성할 수 있습니다. [자세히 보기](../sms/sms-webhook.md)

  사용 가능한 날짜: 2026년 2월 2일

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">DOCAC JIRA 작업에 연결</a>

<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13747">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">Link to DOCAC JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
