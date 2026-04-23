---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: dd17038e3bae77f9de2642d2578e5fa4cad54d43
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 14%

---

# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer은 새로운 기능, 기존 기능 개선 사항 및 버그 수정 사항을 지속적으로 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 4월 프리릴리스 정보 {#april-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 4월 28~29일

### 새로운 기능 {#april-26-features}


<table>
<thead>
<tr>
<th><strong>여정 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 <strong>시뮬레이션</strong>(으)로 설정할 수 있습니다. 이 모드를 사용하면 <strong>시뮬레이션된 사용자</strong>를 사용하여 논리의 유효성을 검사할 수 있습니다. 이러한 프로필은 시뮬레이션을 위해 특별히 생성된 임시 프로필로서, Adobe Experience Platform에서 지속적인 테스트 프로필을 관리할 필요 없이 자유롭게 테스트할 수 있습니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14050">DOCAC-14050</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 헤더의 발신자 매개 변수</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer을 사용하여 전송 엔티티(발신자)가 작성 엔티티(보낸 사람)와 다른 위치에 이메일을 보낼 수 있습니다. 이를 지원하는 이메일 클라이언트는 일반적으로 "보낸 사람을 대신하여 보낸 사람"으로 렌더링하거나 "경유" 표시기를 표시합니다. 이 기능을 구성하려면 전자 메일 채널 설정의 선택적 <strong>보낸 사람 헤더</strong> 필드를 입력하십시오.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14458">DOCAC-14458</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 채널 설정의 CC 필드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 설정에서 선택적 CC(Carbon Copy) 필드를 구성할 수 있습니다. BCC와 달리 CC 수신자는 1차 수신자가 볼 수 있어 투명한 의사소통이 가능하고 소유권이 명확해진다.</p>
<p>이를 통해 관계 관리자나 계정 소유자와 같은 각 메시지에 적합한 이해 당사자를 자동으로 복사하는 동시에 고객이 후속 조치를 위해 연락할 사람을 알 수 있습니다.</p>
<p>CC 필드는 개인화를 지원하므로 단일 구성이 프로필 데이터를 기반으로 복사본을 동적으로 라우팅하여 추가 설정 없이 여러 사용 사례에서 확장 가능합니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14581">DOCAC-14581</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 Designer의 딥링크</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 Designer의 전용 옵션을 통해 이메일 콘텐츠에 딥 링크를 추가할 수 있습니다. 이렇게 하면 사용자가 브라우저나 앱스토어로 리디렉션되지 않고 올바른 인앱 콘텐츠로 바로 이동하여 컨텍스트와 참여를 유지할 수 있습니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14582">DOCAC-14582</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 및 캠페인용 폴더</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 및 캠페인을 <strong>폴더</strong>(으)로 구성하여 인터페이스에서 탐색 및 관리를 개선할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC-14038</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>MCP를 통한 Journey Optimizer AI 에이전트 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer은 MCP 호환 애플리케이션 내에서 직접 캠페인, 충성도 및 샌드박스 작업을 표시하는 <strong>MCP(Model Context Protocol) 서버</strong>를 제공합니다. 이 통합을 통해 다양한 가상 사용자가 동일한 오케스트레이션 데이터를 기반으로 공동 작업할 수 있습니다. AJO REST API에 대해 쿼리를 작성하거나 여러 UI 화면을 탐색하는 대신, 사용자의 의도를 대화식으로 설명하고 LLM이 적절한 MCP 도구를 호출하도록 할 수 있습니다. 이 기능은 현재 클라우드 웹 및 데스크탑에서 사용할 수 있습니다.</p>
<p>이 기능은 공용 Beta의 모든 고객이 사용할 수 있습니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14509">DOCAC-14509</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인용 샌드박스 사본</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>샌드박스 도구</strong>에서 패키지를 통해 샌드박스 간 <strong>오케스트레이션된 캠페인</strong> 내보내기 및 가져오기를 지원합니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-13760">DOCAC-13760</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 증분 쿼리 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>오케스트레이션된 캠페인</strong>에서 <strong>증분 쿼리</strong> 활동을 사용할 수 있습니다. 이 타깃팅 활동은 캠페인이 실행될 때마다 쿼리를 실행하고 이전 실행에서 반환되지 않은 레코드만 반환합니다. 동일한 프로필을 다시 타겟팅하지 않고 새 등록, 새 골드 멤버 또는 기타 "마지막 실행 이후 신규" 세그먼트만 메시지나 내보낼 수 있습니다.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 중재 - AI 모델</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 등급 수식에서 <strong>AI 모델</strong>을 사용하여 고객 프로필 특성 및 컨텍스트 요인에 따라 여정 우선 순위 점수를 자동으로 높여 고객이 가장 관련성이 높은 여정을 입력하도록 할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>설명서 JIRA 작업: <a href="https://jira.corp.adobe.com/browse/DOCAC-14295">DOCAC-14295</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 받은 편지함에 대한 이메일 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에는 Gmail의 Apple Intelligence 및 Google Gemini와 같은 AI 기반 받은 편지함에 대해 이메일이 최적으로 구성되도록 하는 새로운 기능이 포함됩니다. AI 어시스턴트가 수신자가 이메일을 읽고 행동하는 방법을 점점 더 제어하므로 이 기능은 요약, 분류, 우선 순위 지정 및 의도 추출을 비롯한 다운스트림 AI 작업에서 잘 수행되는 콘텐츠를 작성하는 데 도움이 됩니다.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>자세한 내용은 <a href="../email/llm-email-optimizer.md">AI 받은 편지함에 대한 전자 메일 최적화</a>를 참조하세요.</p>
<p>가용성 일자: 2026년 4월 17일 토요일</p>
<!--
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14520">DOCAC-14520</a></p>
-->
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Journey fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey fragments</strong> are reusable sets of journey nodes that you can build once and drop into any journey across your sandbox. Whether it's an eligibility check, a preferred channel routing logic, or a welcome sequence, fragments help teams move faster and stay consistent — without rebuilding the same logic from scratch every time. Once created, fragments are stored in a dedicated <strong>Fragment inventory</strong> and can be inserted into any journey using the <strong>Journey fragments</strong> activity.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11529">DOCAC-11529</a></p>
<p>Availability date: May 4, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Personalization 표현식을 위한 AI 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에는 개인화 표현식을 위한 AI Assistant가 포함되어 있습니다. 이메일 콘텐츠를 디자인하는 동안 Personalization 편집기 및 이메일 Designer 도구 모음에서 열 수 있습니다. 개인화할 내용을 일반 언어로 설명하면 도우미가 그대로 사용하거나 짧은 후속 대화에서 세분화할 수 있는 개인화 표현식을 생성합니다.
기존 개인화 코드를 선택하고 도우미에게 설명하거나 수정하거나 개선 사항을 제안하도록 요청할 수도 있습니다. 표현식을 생성한 후 샘플 프로필에 대한 미리보기 표시 는 제한된 합성 샘플 프로필 세트에 대해 빠른 검사를 실행합니다.</p>
<p>자세한 내용은 <a href="../content-management/generative-personalization-expressions.md">Personalization 표현식 AI 지원</a>을 참조하세요.</p>
<p>가용성 일자: 2026년 4월 13일 화요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>받은 편지함</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>받은 편지함</strong>은(는) <strong>콘텐츠 카드</strong>에서 사용할 수 있는 모바일 기능으로, 이를 통해 고객은 앱 또는 웹 사이트에서 중앙 위치를 만들어 사용자에게 보낸 메시지를 표시할 수 있습니다. 따라서 메시지가 종료된 후에도 계속 액세스할 수 있도록 보장함으로써 마케팅 커뮤니케이션의 수명을 연장할 수 있습니다.</p>
<p>자세한 내용은 <a href="../inbox/inbox-gs.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 4월 7일 수요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 경로 실험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 <strong>최적화</strong> 노드를 사용하여 A/B 테스트 또는 multi-armed bandit 실험을 실행하여 비즈니스 중심 KPI를 충족하는 최상의 경로를 결정하십시오. 이 도구를 사용하면 고객에게 가장 잘 도달하기 위해 커뮤니케이션, 시퀀스 및 타이밍을 테스트하고 다양하게 지정할 수 있습니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../building-journeys/path-experimentation.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 4월 7일 수요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>의사 결정</strong>을 사용하여 전자 메일 메시지의 콘텐츠를 개인화하고 최적화할 수 있습니다. <strong>우선 순위 점수</strong>, <strong>수식</strong> 또는 <strong>AI 모델</strong>을 활용하여 각 수신자에게 가장 관련성이 높은 오퍼와 콘텐츠를 표시합니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). 이번 일반 공급 릴리스에서는 <strong>미러 페이지</strong>이(가) 지원됩니다.</p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision-policy.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 4월 6일 화요일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#april-26-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### AI

* **Campaign 대시보드의 브랜드 정렬 점수** - 이제 Campaign 대시보드 내에서 직접 브랜드 정렬 점수를 평가하여 콘텐츠를 브랜드에 유지할 수 있습니다. 이렇게 하면 콘텐츠 디자이너를 열지 않고도 지침을 한 눈에 확인할 수 있습니다.

  설명서 JIRA 작업: [DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)

#### 결정

* **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서 의사 결정 정책을 통해 코드 기반 경험 및 이메일 캠페인에서 활용할 수 있는 의사 결정 항목에 조각을 첨부할 수 있는 기능을 제공합니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  설명서 JIRA 작업: [DOCAC-14452](https://jira.corp.adobe.com/browse/DOCAC-14452)

* **일시적으로 사용할 수 없는 조각을 건너뜁니다** - 의사 결정 항목에서 조각을 사용할 때 Edge에서 조각을 일시적으로 사용할 수 없는 경우 해당 조각을 건너뛰고 여정 또는 캠페인이 실패하는 대신 렌더링을 계속합니다. [자세히 보기](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  가용성 일자: 2026년 4월 14일 수요일

#### 이메일 디자인

* **전자 메일 콘텐츠에 대한 고급 HTML 편집기** - 고급 HTML 모드를 사용하면 전자 메일 Designer에서 콘텐츠의 HTML 소스를 편집하고, 소스에 고급 표현식(예: 조건)을 추가하고, 변경 내용을 손실하지 않고 HTML 보기와 데스크톱 보기 간에 전환할 수 있습니다. 이전에는 전자 메일 콘텐츠 템플릿에만 사용할 수 있었지만, 이제 이 기능이 전자 메일 Designer의 **전자 메일** 콘텐츠에 배포되었습니다. 현재 제한된 가용성 상태입니다. Adobe 담당자에게 문의하여 액세스 권한을 받으십시오. [자세히 보기](../email/email-expert-mode.md)

  가용성 일자: 2026년 4월 9일 금요일

#### 푸시

* **채널 설정에서 앱 ID 개인화** - 이제 푸시 채널 구성 설정에서 **앱 ID** 필드를 개인화할 수 있으므로 각 수신자는 프로필 정보를 기반으로 해당 브랜드에서 푸시 알림을 받을 수 있습니다.

  설명서 JIRA 작업: [DOCAC-14592](https://jira.corp.adobe.com/browse/DOCAC-14592)

#### SMS

* **문자 수** - 이제 Adobe Journey Optimizer에서 문자 수를 사용하여 SMS 메시지의 길이를 실시간으로 모니터링할 수 있습니다. 이렇게 하면 메시지를 여러 세그먼트로 분할하여 서식을 보다 효율적으로 관리하고 예기치 않은 전송 비용 증가를 방지할 수 있습니다. [자세히 보기](../sms/create-sms.md)

  설명서 JIRA 작업: [DOCAC-14346](https://jira.corp.adobe.com/browse/DOCAC-14346)

* **전화 번호 및 발신자에서의 옵트아웃 및 동의** - 이제 SMS의 경우 Journey Optimizer에서 프로필의 전화 번호와 짧은 코드 수준에서 마케팅 동의 및 옵트아웃을 기록합니다. 프로필의 전화 번호가 변경되면 이전 번호에 연결된 동의가 새 번호로 전송되지 않습니다. 수신자는 모든 메시지가 특정 번호 및 발신자 수준에서 동의로 정렬되도록 다시 옵트인해야 합니다.

  이 기능은 현재 Sinch SMS 구성에만 사용할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

  설명서 JIRA 작업: [DOCAC-14344](https://jira.corp.adobe.com/browse/DOCAC-14344)

* **사용자 지정 데이터 세트 선택 지원** - 인바운드 SMS 이벤트를 사용자가 선택한 **사용자 지정 데이터 세트**&#x200B;에 쓸 수 있으므로 대상자와 여정이 기본 메시지 피드백 경로 및 스트리밍 대상 새로 고침을 기다리는 것보다 빨리 해당 데이터를 사용할 수 있습니다. 이는 **양방향 SMS**&#x200B;에 유용합니다. [자세히 보기](../sms/sms-webhook.md)

  설명서 JIRA 작업: [DOCAC-14356](https://jira.corp.adobe.com/browse/DOCAC-14356)

* **Webhook 인터페이스 개선 사항** - SMS Webhooks를 구성할 때 이제 사용자 인터페이스에 실제 예제가 포함된 기본 제공 설정 가이드가 포함되어 있으므로 구성 흐름을 종료하지 않고도 공급자 페이로드를 조정하고 문제를 해결할 수 있습니다. [자세히 보기](../sms/sms-webhook.md)

  설명서 JIRA 작업: [DOCAC-14589](https://jira.corp.adobe.com/browse/DOCAC-14589)

#### WhatsApp

* **WhatsApp 대화형 단추 및 추적** - 이제 Journey Optimizer의 WhatsApp이 템플릿과 사용 사례에 필요한 대화형 단추 및 내장된 대화형 추적을 지원하므로 다른 채널 보고와 함께 참여를 측정하고 성능을 분석할 수 있습니다.

  설명서 JIRA 작업: [DOCAC-14590](https://jira.corp.adobe.com/browse/DOCAC-14590)

#### 여정 경로 최적화

* **실험 유형** - 이제 경로 실험을 구성할 때 A/B 실험(시작 시 고정 분할) 또는 Multi-armed bandit(주별 가중치 업데이트가 있는 자동 분할) 중에서 선택할 수 있습니다. [자세히 보기](../building-journeys/path-experimentation.md)

  가용성 일자: 2026년 4월 7일 수요일

* **경로 실험: 우승자 크기 조정** - 이제 실험의 성공 경로를 전체 대상자에게 자동 또는 수동으로 롤아웃할 수 있습니다. 일단 승자가 결정되면 실험을 지속적으로 모니터링하지 않고 그 도달 범위와 효과를 증폭시킬 수 있다. 이 기능은 단일 여정(이벤트 트리거 및 대상 자격 조건)에서만 사용할 수 있습니다. [자세히 보기](../building-journeys/path-experimentation.md#scale-winner)

  가용성 일자: 2026년 4월 7일 수요일

* **조건** - [최적화](../building-journeys/optimize.md) 활동은 여정에서 조건부 경로를 만드는 새로운 수단입니다. 이는 이전의 **조건** 활동을 대체합니다. 모든 조건부 논리는 유지되고 이제 **최적화** 활동의 조건을 통해 처리됩니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). [자세히 보기](../building-journeys/conditions.md)

  가용성 일자: 2026년 4월 7일 수요일

#### Adobe Experience Manager 통합

* **콘텐츠 관리자 선택기** - 이제 Adobe Experience Manager Assets 및 콘텐츠 조각 선택기가 모든 AEM Assets 및 AEM 콘텐츠 조각을 검색, 검색, 필터링 및 액세스할 수 있는 통합 모달인 **콘텐츠 관리자 선택기**&#x200B;로 대체되었습니다. Dynamic Media 렌디션 지원도 포함되어 있으므로 Dynamic Media 에셋을 선택한 경우 UI에서 이미지 렌디션을 추가할 수 있습니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  설명서 JIRA 작업: [DOCAC-13802](https://jira.corp.adobe.com/browse/DOCAC-13802)

* **Dynamic Media를 사용하여 카운트다운 타이머가 있는 오픈 타임 개인화** - Journey Optimizer 및 Adobe Experience Manager Dynamic Media 통합을 통해 Dynamic Media 템플릿에 대한 오픈 타임 개인화를 활성화하여 초개인화된 사용 사례를 잠글 수 있습니다. 고객은 Adobe Experience Manager에서 개인화된 템플릿을 만들고 게시하며, 오픈타임에 렌더링되는 데이터를 사용하여 Journey Optimizer에서 사용할 수 있습니다.

  설명서 JIRA 작업: [DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)

* **Adobe Experience Manager 콘텐츠 조각 변형 지원** - 로케일 및 다국어 시나리오에 대한 개선된 처리로 Adobe Experience Manager 콘텐츠 조각을 삽입할 때 **콘텐츠 조각 변형**(예: 언어 또는 채널 변형)을 선택할 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오. [자세히 보기](../integrations/aem-fragments.md#aem-variations)

  가용성 일자: 2026년 4월 3일 토요일

* **작성 중 Adobe Experience Manager 콘텐츠 조각 컨텍스트** - 콘텐츠 조각 선택 항목은 텍스트 필드와 콘텐츠 블록 사이를 이동할 때 활성 상태로 유지되므로 매번 **AEM 콘텐츠 관리자 열기**&#x200B;를 다시 열지 않고 조각 필드를 더 추가할 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오. [자세히 보기](../integrations/aem-fragments.md)

  가용성 일자: 2026년 4월 1일 목요일

<!--
#### WhatsApp

* **WhatsApp Channel: Embedded Sign Up** - Adobe Journey Optimizer now supports Meta's <strong>Embedded Sign Up</strong> flow for WhatsApp channel configuration. This streamlined onboarding experience allows you to connect your <strong>WhatsApp Business Account</strong> and phone numbers directly within the AJO interface, without navigating to <strong>Meta Business Manager</strong>, reducing setup time significantly. It also serves as a migration tool to transfer existing phone numbers and <strong>WhatsApp Business Accounts (WABAs)</strong> to Adobe.

  Documentation JIRA task: [DOCAC-13386](https://jira.corp.adobe.com/browse/DOCAC-13386)
-->

#### 구성

* **URL 매개 변수 암호화 키에 대한 특정 권한** - URL 매개 변수 암호화에 대한 키에 액세스하고 관리하기 위해 새 권한을 만들었습니다. 이제 **키 레지스트리 보기** 및 **키 레지스트리 관리** 권한이 부여되어야 합니다.

  설명서 JIRA 작업: [DOCAC-14490](https://jira.corp.adobe.com/browse/DOCAC-14490)

#### 오케스트레이션된 캠페인

* **데이터 Modeler 개선 사항** - 이제 오케스트레이션된 관계형 스키마가 여러 필드에 걸친 복합 키를 지원합니다. DDL 파일에서 스키마를 로드하면 열거형이 발생하고 DDL 또는 Excel 파일에서 로드하면 자동으로 테이블 간에 복합 관계가 만들어집니다. 이제 엔티티 관계 보기에서 합성 링크는 파일을 업로드한 후 테이블 간의 전체 필드 연결 집합을 표시합니다.

  설명서 JIRA 작업: [DOCAC-14334](https://jira.corp.adobe.com/browse/DOCAC-14334)

* **오케스트레이션된 캠페인의 전역 변수** - 이제 오케스트레이션된 캠페인이 한 번 정의하여 워크플로우 내의 모든 활동에서 재사용할 수 있는 전역 변수를 지원하므로 구성을 단순화하고 동적 값, 표현식 및 콘텐츠 개인화의 일관성을 보장합니다.

  설명서 JIRA 작업: [DOCAC-14113](https://jira.corp.adobe.com/browse/DOCAC-14113)

<!--
## March '26 pre-release notes {#march-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: March 24-25, 2026

### New capabilities {#march-26-features}

<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14340">DOCAC-14340</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convert images to email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now convert images into email content templates directly in Journey Optimizer. Use AI-powered analysis to automatically generate structured HTML templates from visual references, significantly reducing email design time.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14324">DOCAC-14324</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Incremental query activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Incremental query</strong> activity is now available in Orchestrated Campaigns. This activity queries only new or updated records since the last workflow execution, significantly reducing processing time and improving efficiency for recurring campaigns targeting large datasets.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transactional category in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Orchestrated campaigns, you can now set a channel activity to the <strong>Transactional</strong> category using the <strong>Category</strong> field. This applies transactional channel configurations to that activity and bypasses business rules for it.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14233">DOCAC-14233</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Test</strong> activity is now available in Orchestrated Campaigns. This activity routes workflow execution to different branches based on defined conditions, enabling you to validate campaign logic and configurations before activating live deliveries.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14115">DOCAC-14115</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom forms in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create <strong>custom forms</strong> in landing pages to collect specific subscriber data beyond standard opt-in fields. Define your own form fields, validation rules, and submission behaviors to support a wider range of subscription and profile enrichment use cases.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13963">DOCAC-13963</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Create Orchestrated Campaign use case</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>, powered by Adobe Experience Platform Agent Orchestrator, can now create complete <strong>Orchestrated Campaign</strong> use cases through a natural language interface. Describe your campaign goal and requirements in plain language, and Journey Agent configures the campaign structure, activities, and targeting for you.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13768">DOCAC-13768</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New profile acquisition in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Landing pages now support <strong>new profile acquisition</strong> workflows, enabling you to capture and onboard new audience members directly from your landing page experiences. Configure acquisition forms to collect profile data and automatically provision new profiles in Adobe Experience Platform.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13757">DOCAC-13757</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey path optimization</strong> uses AI to analyze historical journey performance and automatically select the best path for each customer, maximizing conversion and engagement outcomes.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13492">DOCAC-13492</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>Decisioning</strong> to personalize and optimize the content of your email messages. Leverage Priority Scores, Formulas, or AI Models to display the most relevant offers and content to each recipient.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability). With this General Availability release, mirror pages are now supported.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13182">DOCAC-13182</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message inbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Inbox</strong> is now available in Adobe Journey Optimizer, providing a centralized view of received in-app, push, and SMS messages. Recipients can access and interact with all their messages in one place, enabling richer engagement and re-engagement scenarios.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11382">DOCAC-11382</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Native channel action activities deprecated</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Following the General Availability of the <strong>Action activity</strong> in February 2026, legacy native channel action activities (Email, SMS, Push, In-App, etc.) in the journey canvas are now deprecated. Existing journeys using legacy channel activities continue to function without any changes or migration required.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14144">DOCAC-14144</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dataset lookup support in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new activity in journeys, Dataset lookup, allows you to to dynamically retrieve data from Adobe Experience Platform record datasets during runtime. By leveraging this capability, you can access data that may not reside in the profile or event payload, ensuring your customer interactions are both relevant and timely. Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14351">DOCAC-14351</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trigger orchestrated campaigns using API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger an orchestrated campaign via API. Configure the target campaign as "Triggered by a signal" and publish it. Then use an API call to fire the campaign. The API call can include parameters that will be available as variables in the triggered campaign.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14030">DOCAC-14030</a></p>
</td>
</tr>
</tbody>
</table>

### Improvements {#march-26-improv}

Improvements coming with this release are listed below.

#### Journeys

* **Journey Arbitration - AI Models** - In addition to ranking formulas, AI models can now be used with Journey Arbitration to automatically rank and prioritize journey entry for customers, using machine learning to determine the most relevant journey for each profile based on historical behavior and contextual signals. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

  Documentation JIRA task: [DOCAC-14295](https://jira.corp.adobe.com/browse/DOCAC-14295)

#### Reporting

* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.
  Documentation JIRA task: [DOCAC-14354](https://jira.corp.adobe.com/browse/DOCAC-14354)

* **Send-Time Optimization: updated controls location and new lift report** - Send-Time Optimization (STO) controls have been relocated to the Action configuration menu. Additionally, a new lift report is now available in Journeys reports to measure the impact of STO on your campaign performance metrics.

  Documentation JIRA task: [DOCAC-14335](https://jira.corp.adobe.com/browse/DOCAC-14335)

#### Email Designer

* **Open-time personalization using Dynamic Media (Beta)** - You can now personalize email content at open time using Adobe Dynamic Media assets, enabling real-time, recipient-specific images and visuals that are generated dynamically based on each recipient's attributes at the moment of email opening. This capability is currently in Beta.
  Documentation JIRA task: [DOCAC-14353](https://jira.corp.adobe.com/browse/DOCAC-14353)

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.
  Documentation JIRA task: [DOCAC-14254](https://jira.corp.adobe.com/browse/DOCAC-14254)

* **Text mode support in fragments** - Fragments now support text mode editing, allowing you to create and manage plain text versions of your content fragments for use in text-based email workflows and multi-channel scenarios.
  Documentation JIRA task: [DOCAC-14204](https://jira.corp.adobe.com/browse/DOCAC-14204)

#### Decisioning

* **Expression Fragment Reference change feed support in Edge Decisioning** - This enhancement allows changes in fragment references to automatically be reflected in all items that reference fragments, without needing to refresh anything manually (republishing the campaign or decision policy).
  Documentation JIRA task: [DOCAC-14350](https://jira.corp.adobe.com/browse/DOCAC-14350)

* **Optional fragments in decision items** - Fragments attached to decision items can now be configured as optional, providing greater flexibility in content composition when not all decision item renderings require a specific fragment.
  Documentation JIRA task: [DOCAC-14309](https://jira.corp.adobe.com/browse/DOCAC-14309)

#### Configuration

* **URL parameters encryption** - URL parameters in tracking links and landing pages can now be encrypted, providing an additional layer of security for sensitive parameter data. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14349](https://jira.corp.adobe.com/browse/DOCAC-14349)

* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14038](https://jira.corp.adobe.com/browse/DOCAC-14038)

#### Orchestrated campaigns

* **Target dimension simplification in Orchestrated Campaigns** - You can now easily select or automatically deduce the right targeting and secondary dimensions in Orchestrated campaigns for accurate, efficient audience activation.
  Documentation JIRA task: [DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)
-->

<!--
## February '26 pre-release notes {#feb-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: February 17, 2026

### New capabilities {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Wave sending of outbound messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can schedule outbound messages from <strong>campaigns</strong> or <strong>journeys</strong> to be delivered in controlled <strong>batches</strong> over time.</p>
<p>Wave sending offers the following benefits:</p>
<ul>
<li>Better <strong>deliverability</strong> – Spread sends over time to help maintain a strong <strong>sender reputation</strong> and reduce the risk of being flagged as spam.</li>
<li><strong>Load control</strong> – Avoid overwhelming downstream systems (e.g. call centers, landing pages) by limiting how many messages go out at once.</li>
<li>High-volume and time-sensitive use cases – Suited to large audiences or when you need to control timing (e.g. call center capacity, ramp-up, or time-bound offers).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey arbitration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>formulas</strong> and <strong>AI models</strong> to automatically boost <strong>journey priority scores</strong> based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Channel Content Create</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a <strong>natural language interface</strong>. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in <strong>Content Designer</strong> for in-context editing.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide <strong>real-time updates</strong> and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the <strong>journey canvas</strong>. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add <strong>optimization</strong> to any built-in channel action.</li>
<li>The ability to add both <strong>experimentation</strong> and <strong>multilingual</strong> options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
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
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same <strong>authoring workflows</strong> and <strong>targeting capabilities</strong> already available for mobile push.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>Availability date: February 13, 2026</p>
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
<p>A new <strong>Content decision activity</strong> is now available in the <strong>journey canvas</strong> for integrating <strong>personalized offers</strong> directly into your customer journeys. This activity enables you to deliver decision-based content and reference those offers throughout your journey—in conditions for creating eligibility-based branching, in custom actions for passing offer data to external systems, and in other activities for building fully personalized customer experiences.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/content-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-service migration tooling APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migration tooling APIs</strong> are now available to programmatically migrate <strong>Decision management</strong> entities to <strong>Decisioning</strong>, featuring:</p>
<ul>
<li>Flexible migration scopes (<strong>sandbox</strong>, <strong>offer</strong>, or <strong>decision</strong> level)</li>
<li>Automated <strong>dependency analysis</strong> and validation</li>
<li><strong>Rollback support</strong> for completed migrations</li>
<li>Detailed migration reports with object mappings</li>
</ul>
<p>For more information, refer to the <a href="../experience-decisioning/decisioning-migration-api.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
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
<p>Gain deeper insight into the health and performance of your <strong>custom action endpoints</strong> with a new <strong>monitoring dashboard</strong> and enriched <strong>journey step event data</strong>. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>For more information, refer to the <a href="../action/reporting.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in SMS channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize and optimize the content of your <strong>SMS messages</strong> with <strong>Decisioning</strong>. Use <strong>Priority Scores</strong>, <strong>Formulas</strong>, or <strong>AI Models</strong> to display the best content to your customers.</p>
<p>For more information, refer to the <a href="../experience-decisioning/create-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#feb-26-01-improv}

Improvements coming with this release are listed below.

#### Configuration

* **Experience event usage in journey expressions** - Starting April 1, 2026, the use of experience event attributes in journey expressions will no longer be supported for organizations that have not used this capability in the last 90 days. This capability has already been unavailable for new customer organizations since July 8, 2025. For alternatives, see [Experience event lookup in journeys](../building-journeys/exp-event-lookup.md).


* **Subdomain delegation method switching** - You can now switch from one <strong>subdomain delegation</strong> method to another. This enables you to migrate domains using the <strong>CNAME delegation</strong> mode to the <strong>custom delegation</strong> method to adhere to your company's security policies.

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


#### Email Designer

* **Use a brand theme to convert an image to an email template** - When converting an image to an email template in Journey Optimizer, you can now use a <strong>theme</strong> as input so the generated HTML follows your <strong>brand parameters</strong>. Styling such as background color, button color, fonts, line spacing, margins, and padding is applied automatically, reducing manual design work and delivering a template that is ready to use with minimal edits.


* **Update brands with new color tab** - <strong>Brand guidelines</strong> help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.


#### AI

* **Integration of custom Firefly models and third-party image generation models** - Enable seamless integration of standard and custom <strong>Firefly models</strong>, along with approved <strong>third-party image models</strong> (e.g., NanoBanana), to provide greater flexibility, control, and brand alignment when generating images. This allows you to select the best model for each use case: standard Firefly for general needs, custom Firefly for on-brand generation, or approved third-party models for specialized or experimental scenarios.


#### Experience Decisioning

* **Edge inbound support for using Adobe Experience Platform data in Decisioning** - Decisioning support of <strong>Experience Platform data lookup</strong> now includes <strong>edge inbound</strong> channel use cases. The capability remains in Limited Availability; General Availability of the underlying data lookup feature is not yet announced (AEP/product dependency).

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


* **Experience Decisioning preview in Code-based Experience channel** - You can now preview <strong>decision items</strong> when configuring <strong>Experience Decisioning</strong> with the <strong>Code-based Experience</strong> channel. Preview is available directly in the authoring interface before going live.


* **Offer Ranking AI Model Observability** - Journey Optimizer now allows you to monitor the <strong>health</strong>, <strong>training status</strong>, and <strong>performance</strong> of your <strong>AI models</strong> in Decisioning—so you can verify training success, troubleshoot failures, and understand impact on your outcomes. This capability is available for personalized optimization models only (not auto-optimization).


* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through <strong>decision policies</strong>.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.


#### Journeys

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define several <strong>inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple <strong>code-based experiences</strong>, <strong>in-app messages</strong>, <strong>content cards</strong>, or <strong>web actions</strong> to different locations at the same time, each action containing specific content.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).


* **SMS Webhooks** - <strong>Webhooks</strong> are now supported across all SMS providers. You can configure each webhook based on its intended purpose: <strong>Inbound webhooks</strong> to capture incoming messages and <strong>Feedback webhooks</strong> to receive delivery receipts, status updates, and other message-related events. [Read more](../sms/sms-webhook.md)

  Availability date: February 2, 2026.
-->
<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

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
<p><a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
