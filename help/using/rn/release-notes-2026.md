---
solution: Journey Optimizer
product: journey optimizer
title: 2026년 릴리스 정보
description: Journey Optimizer 2026년 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: ht
source-wordcount: 6058
ht-degree: 100%

---

# 2026년 릴리스 정보 {#release-notes-2026}

이 페이지에서는 2026년에 릴리스된 [!DNL Journey Optimizer]의 모든 기능과 개선 사항 목록을 확인할 수 있습니다.

## 26년 4월 릴리스 정보 {#april-26-rn}


**릴리스 날짜**: 2026년 4월 28~29일

### 새로운 기능 {#april-26-features}

다음 기능은 2026년 4월에 출시되었습니다.

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 증분 쿼리 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>오케스트레이션된 캠페인</strong>이 이제 마지막 실행 이후 새로 자격을 얻은 프로필 또는 이벤트만 타기팅하는 <strong>증분 쿼리</strong> 활동을 지원합니다.

이 기능으로 쿼리 워크로드를 줄이고 시간이 지남에 따라 중복 전송이 발생하는 것을 방지하면서 반복 캠페인이 계속 순 신규 대상자(신규 등록 사용자, 새로 자격을 얻은 충성도 멤버, 유사한 세그먼트)에 집중되도록 할 수 있습니다.</p>
<p>자세한 내용은 <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 30일</p>
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
<p>이제 Journey Optimizer로 전송 엔터티(발신자)와 작성 엔터티(보내는 사람)가 다른 이메일을 보낼 수 있습니다. 이를 지원하는 이메일 클라이언트는 일반적으로 해당 이메일을 '발신자가 보내는 사람 대신 발신' 형태로 전달하거나 '경유' 표시자를 표시합니다. 이메일 채널 설정에서 선택에 따라 사용할 수 있는 <strong>발신자 헤더</strong> 필드에 값을 입력하면 이 기능을 구성할 수 있습니다.</p>
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>자세한 내용은 <a href="../email/header-parameters.md#sender-header">세부 설명서</a>를 참조하십시오.</p>
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
<p>이제 원하는 경우 이메일 채널 설정에서 CC(참조) 필드를 구성할 수 있습니다. BCC와 달리 CC 수신자는 1차 수신자가 볼 수 있어 투명한 의사소통이 가능하고 소유권이 명확해집니다.</p>
<p>관계 관리자나 계정 소유자 등 각 메시지에 적합한 이해 당사자를 자동으로 복사하는 동시에 고객에게 후속 조치를 위해 연락할 사람을 알릴 수 있습니다.</p>
<p>CC 필드는 개인화를 지원하여 단일 구성이 프로필 데이터를 기반으로 복사본을 동적으로 라우팅하므로 추가 설정 없이 여러 사용 사례로 확장 가능합니다.</p>
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>자세한 내용은 <a href="../configuration/cc-email-field.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>샌드박스 간 오케스트레이션 캠페인 복사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 샌드박스 도구가 오케스트레이션된 캠페인을 한 샌드박스에서 패키지화해 다른 샌드박스로 복사할 수 있도록 지원합니다. 각 환경에서 캠페인을 수동으로 재작성할 필요가 없습니다. 캠페인이 패키지화되면 병합 정책, 메시지와 같은 핵심 종속 오브젝트가 자동으로 포함되므로, 가져온 캠페인은 구성 및 유효성 검사를 수행할 준비가 된 상태로 도착합니다. 프로덕션 환경을 보호하기 위해 가져온 모든 캠페인은 대상 샌드박스에서 초안 상태로 전환되므로, 캠페인이 라이브로 전환되기 전에 팀에서 검토 및 승인하는 단계를 거치게 됩니다.</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>자세한 내용은 <a href="../configuration/copy-objects-to-sandbox.md">세부 설명서</a>를 참조하십시오.</p>
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
<p>이제 Adobe Journey Optimizer가 <strong>MCP(Model Context Protocol) 서버</strong>를 제공합니다. 이 서버는 모든 MCP 호환 애플리케이션 내에 직접 캠페인, 채널 구성, 샌드박스 작업을 표시합니다. 이 통합을 통해 다양한 페르소나가 동일한 오케스트레이션 데이터를 기반으로 공동 작업할 수 있습니다. Adobe Journey Optimizer REST API에 대해 쿼리를 작성하거나 여러 UI 화면을 탐색하는 대신, 사용자의 의도를 대화식으로 설명하여 LLM이 적절한 MCP 도구를 호출하도록 할 수 있습니다. 이 기능은 현재 Claude 웹 및 데스크탑에서 사용할 수 있습니다.</p>
<p>이 기능은 공개 Beta로 모든 고객이 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../integrations/ajo-mcp.md">세부 설명서</a>를 참조하십시오.</p>
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
<p>이제 순위 공식에서 <strong>AI 모델</strong>을 사용하여 고객 프로필 속성 및 컨텍스트 요인에 따라 여정 우선순위 점수를 자동으로 높임으로써 고객이 가장 관련성이 높은 여정에 입장하도록 할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>자세한 내용은 <a href="../conflict-prioritization/journey-ai-models.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Express 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer의 <b>Adobe Express 통합</b>을 사용하면 콘텐츠 제작 시 Adobe Express의 편집 도구를 직접 사용하여 에셋의 크기를 조정하고 배경을 제거하고 자르고 JPEG 또는 PNG로 변환할 수 있습니다.
</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>자세한 내용은 <a href="../integrations/express.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 4월 23일</p>
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
<p>이제 Adobe Journey Optimizer가 이메일을 Apple Intelligence와 Gmail의 Google Gemini 등 AI 기반 받은 편지함에 최적화하여 구성하는 새로운 기능을 제공합니다.</p>
<p>수신자가 이메일을 읽고 행동하는 방식에 대한 AI 어시스턴트의 영향이 점점 커지고 있는 상황에서 이 기능은 요약, 분류, 우선순위 지정, 의도 추출을 비롯한 다운스트림 AI 작업에서 좋은 성과를 내는 콘텐츠를 생성, 작성하는 데 도움이 됩니다.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>자세한 내용은 <a href="../email/llm-email-optimizer.md">AI 받은 편지함에 대한 이메일 최적화</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 4월 17일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>개인화 표현식에 AI 어시스턴트 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 이제 개인화 편집기와 이메일 디자이너에 <strong>AI 어시스턴트</strong>가 직접 포함되어 있어 자연어 프롬프트를 유효한 개인화 표현식과 조건부 논리로 변환하므로 구문 전문 지식이 필요하지 않습니다. 구현하려는 개인화에 대해 설명하면 AI가 바로 사용할 수 있는 코드를 생성하며, 이를 즉시 적용하거나 후속 프롬프트를 통해 다듬을 수 있습니다.</p>
<p>어시스턴트를 반대 방향으로도 사용할 수 있습니다. 원하는 기존 표현식을 선택하고 어시스턴트에게 논리를 설명하거나 문제를 식별하거나 개선 사항을 제안하도록 요청니다. 따라서 새 표현식을 작성하는 데 그치지 않고 팀 전체에서 기존 표현식을 검토하고 디버깅하는 데에도 유용합니다.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>자세한 내용은 <a href="../content-management/generative-personalization-expressions.md">개인화 표현식에 AI 어시스턴트 사용</a>을 참조하세요.</p>
<p>가용성 일자: 2026년 4월 13일</p>
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
<p>새로운 <strong>최적화</strong> 노드를 사용하여 A/B 테스트 또는 다중 암 밴딧 실험을 실행하고 비즈니스 중심 KPI를 달성하는 최적의 경로를 결정합니다. 이 도구를 사용하면 고객에게 가장 효과적으로 도달할 수 있도록 커뮤니케이션, 순서 및 타이밍을 테스트, 변경 및 맞춤 설정할 수 있습니다.
</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>이번 일반 출시에는 <strong>실험 유형</strong> 선택(A/B 또는 멀티암 밴딧) 및 단일 여정에 대한 <strong>성과 극대화</strong> 기능이 도입되었습니다.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/path-experimentation.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 7일</p>
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
<p><strong>받은 편지함</strong>은 콘텐츠 카드와 함께 사용할 수 있는 모바일 기능으로, 고객이 앱이나 웹 사이트 내에 사용자에게 전송된 메시지를 표시하는 중앙 집중식 위치를 만들 수 있도록 지원합니다. 이를 통해 메시지를 닫은 후에도 계속 액세스할 수 있도록 하여 마케팅 커뮤니케이션의 수명을 연장할 수 있습니다.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>자세한 내용은 <a href="../inbox/inbox-gs.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 7일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 채널에서 의사 결정 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>의사 결정</strong>을 사용하여 이메일 메시지 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선순위 점수, 공식 또는 AI 모델을 활용하여 각 수신자에게 가장 관련성이 높은 오퍼와 콘텐츠를 표시하세요.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). 이번 일반 출시를 통해 미러 페이지가 지원됩니다.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision-policy.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 6일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#april-26-improv}

다음 개선 사항도 2026년 4월에 출시되었습니다.

#### AI

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **프롬프트 어시스턴트 개선** - 프롬프트 어시스턴트는 사용자의 프롬프트를 실시간으로 분석하고 명확성, 완전성 및 맥락의 부족한 부분을 파악하여 AI 콘텐츠 생성을 개선합니다. 개선된 재작성을 제안하고 대상자, 톤 및 의도와 같은 주요 세부 정보를 추가하여 프롬프트를 풍부하게 만드는 데 도움이 되는 실행 가능한 지침을 제공합니다. 또한 이 기능은 사용자가 생성 전에 입력 내용을 다듬을 수 있도록 구체적인 질문을 제시합니다. 이를 통해 더 적은 반복 작업으로 더 정확하고 고품질의 결과물을 얻을 수 있습니다. [자세히 알아보기](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  사용 가능한 날짜: 2026년 5월 5일

#### 푸시

* **채널 설정에서 앱 ID 개인화** - 푸시 채널 구성 설정에서 이제 **앱 ID** 필드를 개인화하여 각 수신자가 프로필 정보에 따라 적절한 브랜드로부터 푸시 알림을 받을 수 있습니다. [자세히 보기](../push/push-configuration.md#app-id-personalization)

#### 결정

* **의사 결정 마이그레이션 워크플로 API** - 종속성 분석 및 마이그레이션 워크플로 생성을 위한 API 계약이 업데이트되었습니다. 요청 URL(`sandbox`, `offer` 또는 `decision`)에 **쿼리 매개변수**&#x200B;로 **`request-level`**&#x200B;을(를) 전달합니다. 요청 수준은 더 이상 JSON 본문에 전송해서는 안 됩니다. [자세히 보기](../experience-decisioning/decisioning-migration-api.md)

  사용 가능한 날짜: 2026년 5월 6일

* **결정 항목에 조각 첨부** - Journey Optimizer는 이제 결정 정책을 통해 코드 기반 경험 및 이메일 캠페인에서 활용할 수 있는 결정 항목에 조각을 첨부하는 기능을 제공합니다. [자세히 보기](../experience-decisioning/fragments-decision-policies.md)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

* **일시적으로 사용할 수 없는 조각 건너뛰기** - 결정 항목에서 조각을 사용할 때 Edge에서 조각을 일시적으로 사용할 수 없는 경우 해당 조각은 건너뛰어지고 여정 또는 캠페인 렌더링이 실패하지 않고 계속됩니다. [자세히 보기](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  사용 가능한 날짜: 2026년 4월 14일

#### Adobe Experience Manager 통합

* **Adobe Experience Manager 콘텐츠 조각 베리에이션 지원** - Adobe Experience Manager 콘텐츠 조각을 삽입할 때 **콘텐츠 조각 베리에이션**(예: 언어 또는 채널 베리에이션)을 선택할 수 있으며, 로케일 및 다국어 시나리오에 대한 처리가 향상되었습니다. [자세히 보기](../integrations/aem-fragments.md#aem-variations)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

* **작성 중 Adobe Experience Manager 콘텐츠 조각 컨텍스트** - 텍스트 필드와 콘텐츠 블록 사이를 이동할 때 콘텐츠 조각 선택이 활성 상태로 유지되므로 매번 **AEM 콘텐츠 어드바이저 열기**&#x200B;를 다시 열지 않고도 더 많은 조각 필드를 추가할 수 있습니다. [자세히 보기](../integrations/aem-fragments.md)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

#### 이메일 디자인

* **이메일 콘텐츠용 고급 HTML 편집기** - 고급 HTML 모드를 사용하면 이메일 디자이너에서 콘텐츠의 HTML 소스를 편집하고, 소스에 고급 표현식(예: 조건)을 추가하고, 변경 내용을 잃지 않고 HTML 보기와 데스크톱 보기 간에 전환할 수 있습니다.

  이전에는 이메일 콘텐츠 템플릿에서만 사용할 수 있었던 이 기능이 이제 이메일 콘텐츠 템플릿뿐만 아니라 이메일 디자이너의 **이메일** 콘텐츠(예: 여정 및 캠페인에서 작성된 이메일)에도 적용됩니다. 현재 제한된 가용성 상태이므로, 사용 권한을 얻으려면 Adobe 담당자에게 문의하세요. [자세히 보기](../email/email-expert-mode.md)

  사용 가능한 날짜: 2026년 4월 9일

#### 여정

* **여정 속성에서 현재 여정 페이로드 크기 확인 가능** - 이제 여정 속성 패널에 구성된 제한과 비교한 여정 페이로드의 현재 크기가 표시됩니다. 예를 들어 *1.5MB(총 4MB 중)* 식으로 표시됩니다. 이 읽기 전용 표시기를 사용하여 게시 전에 여정 복잡성을 모니터링하고 페이로드 크기 제한 초과로 인한 오류를 방지할 수 있습니다. [자세히 보기](../building-journeys/journey-properties.md#journey-payload-size)

  사용 가능한 날짜: 2026년 4월 30일

#### 여정 경로 최적화

* **실험 유형** - 이제 경로 실험을 구성할 때 A/B 실험(시작 시 고정 분할) 또는 멀티암 밴딧(매주 가중치 업데이트를 통한 자동 분할) 중에서 선택할 수 있습니다. [자세히 보기](../building-journeys/path-experimentation.md)

  사용 가능한 날짜: 2026년 4월 7일

* **경로 실험: 성과 극대화** - 이제 실험에서 가장 효과적인 경로를 전체 사용자에게 자동으로 또는 수동으로 롤아웃할 수 있습니다. 최적의 경로가 결정되면 실험을 지속적으로 모니터링하지 않고도 도달 범위와 효과를 확대할 수 있습니다. [자세히 보기](../building-journeys/path-experimentation.md#scale-winner)

  이 기능은 단일 여정(이벤트 기반 및 대상자 자격 기반)에서만 사용 가능합니다. 대상자 읽기 여정에는 사용할 수 없습니다.

  사용 가능한 날짜: 2026년 4월 7일

* **조건** - [최적화](../building-journeys/optimize.md) 활동은 여정에서 조건부 경로를 생성하기 위한 새로운 도구입니다. 이 활동은 UI에서 제거된 이전 **조건** 활동을 대체합니다. 모든 조건부 로직은 그대로 유지되며 이제 **최적화** 활동의 조건을 통해 처리됩니다. [자세히 보기](../building-journeys/conditions.md)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 4월 7일

#### 오케스트레이션된 캠페인

* **오케스트레이션된 캠페인의 전역 변수** - 오케스트레이션된 캠페인은 이제 워크플로 내의 모든 활동에서 한 번 정의하고 재사용할 수 있는 전역 변수를 지원하여 구성을 간소화하고 동적 값, 표현식 및 콘텐츠 개인화의 일관성을 보장합니다. [자세히 보기](../orchestrated/global-variables.md)
* **데이터 모델러 개선 사항** - 이제 오케스트레이션된 관계형 스키마에서 여러 필드에 걸쳐 있는 복합 키를 지원합니다. DDL 파일에서 스키마를 로드하면 열거형도 함께 로드되며, DDL 또는 Excel 파일에서 로드하면 테이블 간에 복합 관계가 자동으로 생성됩니다. 엔티티 관계 보기에서 파일 업로드 후 복합 링크에 테이블 간의 전체 필드 쌍이 표시됩니다. [자세히 보기](../orchestrated/gs-schemas.md)


## 2026년 3월 릴리스 정보 {#march-26-rn}

[새로운 기능](#march-26-features) 및 [개선 사항](#march-26-improv) 섹션에서는 이미 사용 가능한 기능에 대해 다룹니다. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**출시일**: 2026년 3월 24~25일

### 새로운 기능 {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL 매개변수 암호화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이메일 메시지에 추가된 추적 및 랜딩 페이지 링크의 URL 매개변수를 이제 암호화할 수 있어 민감한 매개변수 데이터에 대한 보안을 강화할 수 있습니다.</p>
<ul>
<li>전용 <strong>관리</strong> 레지스트리에서 암호화 키를 등록하고 관리하세요.</li>
<li>표현식에서 새로운 `Encrypt` 도우미 함수를 사용하여 렌더링 시 보호하려는 쿼리 매개변수의 URL에 있는 민감한 데이터를 암호화할 수 있습니다.</li>
</ul>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>자세한 내용은 <a href="../personalization/url-parameter-encryption.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 31일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이미지를 이메일 콘텐츠 템플릿으로 변환</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 직접 이미지를 이메일 콘텐츠 템플릿으로 변환할 수 있습니다. AI 기반 분석을 사용하여 시각적 참조 자료를 기반으로 구조화된 HTML 템플릿을 자동으로 생성함으로써 이메일을 디자인하는 시간을 크게 단축할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>자세한 내용은 <a href="../content-management/image-to-html.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 31일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>랜딩 페이지 사용자 정의 양식</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Journey Optimizer]에서 랜딩 페이지를 통해 프로필 속성을 캡처할 수 있습니다.</p>
<p>특정 데이터 세트를 기반으로 필요에 맞는 사용자 정의 양식을 만들고 디자인하고 관리합니다. 그런 다음 랜딩 페이지에서 이 양식을 활용하여 선택한 프로필 속성을 각 양식별로 정의한 데이터 세트에 추가할 수 있습니다.</p>
<p>이전에 미국과 호주에 있는 고객에게 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>자세한 내용은 <a href="../landing-pages/lp-forms.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 26일.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 테스트 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에서 새로운 <strong>테스트</strong> 활동을 사용할 수 있습니다. 이 활동은 정의된 조건에 따라 워크플로 실행을 다른 분기로 라우팅하므로 라이브 게재를 활성화하기 전에 캠페인 논리 및 구성을 확인할 수 있습니다.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>자세한 내용은 <a href="../orchestrated/activities/test.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 데이터 세트 조회 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정에 새로 추가된 <strong>데이터 세트 조회</strong> 활동을 사용하면 런타임 시 Adobe Experience Platform 레코드 데이터 세트에서 데이터를 동적으로 검색하여 프로필 또는 이벤트 페이로드의 일부가 아닌 정보에 액세스함으로써 지속적으로 적시에 적절한 고객 상호 작용을 수행할 수 있습니다.</p>
<p>이전에는 일부 조직에만 제한된 가용성으로 릴리스되었던 여정의 데이터 세트 조회 활동은 여전히 제한된 가용성 단계이지만 이제 [데이터 세트 조회](../data/lookup-aep-data.md) 권한이 있는 모든 고객이 사용할 수 있습니다.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>자세한 내용은 <a href="../building-journeys/dataset-lookup.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>채널별 여정 활동 대신 액션 활동 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>2026년 2월에 <strong>액션 활동</strong>이 일반 가용성으로 공개됨에 따라 여정 캔버스에서 레거시 기본 채널 활동(이메일, 푸시, SMS, 인앱, 웹, 코드 기반 경험, 콘텐츠 카드)의 사용이 종료될 예정입니다.</p>
<p>이제 별도의 채널별 노드를 만들 필요 없이 단일 액션 활동을 사용하여 모든 채널 액션을 구성해야 합니다.</p>
<p>레거시 채널 활동을 사용 기존 여정은 수정이나 마이그레이션을 수행할 필요 없이 계속 정상적으로 작동합니다.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/journey-action.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 템플릿용 고급 HTML 편집기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이메일 콘텐츠 템플릿용 고급 HTML 모드를 사용하면 이메일 디자이너에서 콘텐츠의 HTML 소스를 편집하고, 소스에 고급 표현식(조건 등)을 추가하고, 변경 내용을 유지하면서 HTML 보기와 데스크탑 보기를 전환할 수 있습니다.</p>
<p>이 기능은 이메일 채널의 콘텐츠 템플릿에서만 사용할 수 있습니다. 현재 제한된 가용성 단계이므로 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>자세한 내용은 <a href="../email/email-expert-mode.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 10일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 정의 Firefly 모델과 서드파티 이미지 생성 모델 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>승인된 서드파티 이미지 모델과 함께 표준 및 사용자 정의 Firefly 모델의 원활한 통합을 활성화하여 이미지 생성 시 더 큰 유연성, 컨트롤 및 브랜드 정렬을 제공합니다.</p>
<p>필요에 따라 적합한 모델을 선택하십시오.</p>
<ul><li> 추가 설정 없이 즉각적으로 이미지를 생성하려는 경우 <strong>Adobe 모델</strong>(Firefly Image Model 4 기반)</li><li> 특수 기능이 필요한 경우 <strong>파트너 모델</strong>(Gemini 2.5 Flash 지원)</li><li>브랜드 정체성, 스타일, 비주얼 가이드라인을 정확하게 준수하여 브랜드에 맞는 이미지를 생성하려는 경우 <strong>사용자 정의 모델</strong>(사용자 고유의 에셋으로 학습한 브랜드별 모델).</li></ul>
<p>자세한 내용은 <a href="../content-management/generative-models.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 2일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>iOS 라이브 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer에서 <strong>iOS 라이브 활동</strong>을 통해 고객의 잠금 화면 및 Dynamic Island에 직접 실시간 경험을 보낼 수 있습니다. 사용자가 앱을 열지 않아도 주문 추적 및 항공편 상태부터 이벤트 카운트다운, 라이브 점수, 배송 진행 상황에 이르기까지 실시간 업데이트를 제공할 수 있습니다. 바로 그 순간에 대상자가 있는 바로 그 자리로 정보를 제공하고 참여를 유도합니다.</p>
<p>이전에 Beta로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../mobile-live/get-started-mobile-live.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 : 2026년 3월 3일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey 에이전트: 채널 콘텐츠 작성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Adobe Experience Platform Agent Orchestrator</strong>에서 제공하는 <strong>Journey 에이전트</strong>를 Journey Optimizer에서 사용하여 자연어 인터페이스를 통해 여정을 분석할 수 있습니다. 이제 Journey 에이전트에서 직접 채널별 콘텐츠를 생성 및 관리하고, 이메일 및 푸시와 같은 채널을 위한 콘텐츠를 작성하고, 템플릿을 적용하고 미리 보고, 프롬프트를 통해 톤과 스타일을 개선하고, <strong>콘텐츠 디자이너</strong>에서 콘텐츠를 열어 컨텍스트를 확인하며 편집할 수도 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=ko" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>: 2026년 3월 4일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 모델 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 의사 결정 AI 모델의 상태, 학습 진행 상황, 성과를 모니터링할 수 있습니다. 이를 통해 모델의 학습 성공을 확인하고 실패를 해결하며 결과에 미치는 영향을 파악하여 AI로 각 고객을 위한 최상의 오퍼를 선택할 수 있습니다. 이 기능은 <strong>의사 결정</strong>에만 사용할 수 있습니다(레거시 의사 결정 관리 모델에는 사용 불가).</p>
<p>이 기능은 현재 <strong>개인화된 최적화</strong> 모델에만 사용할 수 있습니다(자동 최적화에는 사용 불가).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>자세한 내용은 <a href="../experience-decisioning/ranking/ai-model-observability.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 3월 9일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>신호를 사용하여 오케스트레이션된 캠페인 트리거</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>API 신호</strong>를 통해 오케스트레이션된 캠페인을 트리거할 수 있습니다. 대상 캠페인을 <strong>신호에 의해 트리거됨</strong>으로 구성하고 게시한 다음 API 호출을 사용하여 실행하면 됩니다. API 호출에 포함된 모든 매개 변수는 실행하는 캠페인 내에서 변수로 사용할 수 있습니다. 신호에 의해 트리거되는 오케스트레이션된 캠페인은 <strong>배치</strong> 캠페인으로 유지되며 API 트리거 캠페인과는 다릅니다.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>자세한 내용은 <a href="../orchestrated/trigger-orchestrated-campaign.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 트랜잭션 범주</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에서 채널 활동을 <strong>트랜잭션</strong> 범주로 설정할 수 있습니다. 이렇게 하면 해당 활동에 트랜잭션 채널 구성이 적용되며, 비즈니스 규칙을 적용하면 안 되거나 고객의 옵트인이 필요하지 않은 경우에 유용합니다.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>자세한 내용은 <a href="../orchestrated/activities/channels.md#add">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 향후 며칠 동안 모든 지역에 점진적으로 롤아웃될 예정입니다.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#march-26-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### 개인화

* **전체/기본 URL 개인화** - 프로필 속성(예: 도메인 또는 경로)을 사용하여 대상 URL을 개인화할 수 있습니다. 이 기능을 활성화하려면 Adobe에 허용할 도메인 목록을 제공해 주십시오. [자세히 보기](../personalization/personalization-build-expressions.md#where)

  이전에 여정에서 사용할 수 있도록 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 4월 1일

#### 보고

* **전송 시간 최적화: 컨트롤 위치 업데이트 및 새로운 상승도 보고서 추가** - 전송 시간 최적화(STO) 컨트롤이 액션 구성 메뉴로 재배치되었습니다. 또한 이제 여정 보고서에서 새로운 상승도 보고서를 사용하여 STO가 캠페인 성과 지표에 미치는 영향을 측정할 수 있습니다. [자세히 보기](../reports/channel-report-cja.md#optimization-models)

  가용성 일자: 2026년 3월 27일

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### 구성

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **AJO 도메인 인증서 갱신 실패** - 이제 구독을 통해 이메일 게재에 사용되는 도메인 인증서가 곧 만료되거나 이미 만료된 경우 이메일 또는 Journey Optimizer 알림 센터를 통해 시스템 경고를 수신할 수 있습니다. [자세히 보기](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  가용성 일자: 2026년 3월 26일

* **AJO 보조 수신자 피드백 이벤트 데이터 세트 이름 변경** - `AJO Email BCC Feedback Event` 데이터 세트의 이름이 `AJO Secondary Recipient Feedback Event` 데이터 세트로 바뀌었습니다. 영향은 상황에 따라 다릅니다.

   * **기존 사용자**: 표시 이름만 업데이트됩니다. 기본 테이블 이름은 변경되지 않습니다.
   * **신규 사용자 및 샌드박스**: 표시 이름과 테이블 이름에 모두 새로운 이름이 반영됩니다.
   * **새 샌드박스를 보유한 기존 사용자**: 표시 이름과 테이블 이름이 모두 새로운 이름으로 업데이트됩니다.

  >[!NOTE]
  >
  >새 데이터 세트에는 즉시 새로운 이름이 표시됩니다. 이전 데이터 세트 이름의 경우 채우기 및 조정 작업이 점진적으로 진행되며 완료되는 데 몇 주 정도 걸릴 수 있습니다.

  가용성 일자: 2026년 3월 2일


#### 여정

* **프로필 업데이트 액션: 여러 프로필 속성 지원** - **프로필 업데이트** 액션 활동이 이제 단일 노드에서 최대 5개의 프로필 속성 업데이트를 지원합니다. 이전에는 각 액션별로 한 번에 하나의 속성만 업데이트할 수 있어 여러 속성을 업데이트하려면 여러 노드에서 작업해야 했습니다. 새로운 **다른 필드 업데이트** 버튼을 사용하여 필드/값 쌍을 추가하면 캔버스의 복잡성을 줄이고 성능을 개선할 수 있습니다. [자세히 알아보기](../building-journeys/update-profiles.md)

* **여정의 아웃바운드 메시지 웨이브 전송** - 이제 Journey Optimizer 여정에서 메시지를 시간에 따라 제어되는 배치 단위로 게재하는 작업을 예약할 수 있습니다. [자세히 알아보기](../building-journeys/send-using-waves.md)

  이전에 여정에서 사용할 수 있도록 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  가용성 일자: 2026년 3월 16일

* **여정 기술 세부 정보의 일시 중지 및 다시 시작 세부 정보** - 이제 여정의 **기술 세부 정보**&#x200B;에 추가적인 일시 중지 및 다시 시작 정보가 포함됩니다. 여기에는 마지막으로 일시 중지 및 다시 시작한 날짜 및 시간, 각 액션을 수행한 사용자의 표시 이름 및 내부 식별자, 일시 중지된 여정 설정의 전체 집합(예: 일시 중지 동작, 최대 일시 중지 기간, 자동 다시 시작 상태)이 포함됩니다. [자세히 알아보기](../building-journeys/journey-properties.md)

  가용성 일자: 2026년 3월 2일

#### 결정

* **의사 결정 마이그레이션 — 오퍼 및 컨텍스트 속성** - 이제 마이그레이션 API 엔터티 매핑에 **오퍼 속성**(개인화된 오퍼 항목 스키마의 `migratedofferattributes`) 및 **컨텍스트 속성**(마이그레이션 데이터 세트 스키마의 `migratedcontextattributes`)이 표시됩니다. [자세히 보기](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  가용성 일자: 2026년 3월 31일

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->


## 26년 2월 릴리스 정보 {#feb-26-01-rn}

### 새로운 기능 {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>여정 중재</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>순위 공식</strong>을 사용하여 고객 프로필 속성 및 컨텍스트 요인에 따라 여정 우선순위 점수를 자동으로 높임으로써 고객이 가장 관련성이 높은 여정에 입장하도록 할 수 있습니다.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../conflict-prioritization/journey-ranking-formulas.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 24일</p>
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
<p>Journey Optimizer가 단일 액션과 여러 액션이 있는 인바운드 액션 그룹을 모두 구성할 수 있는 포괄적 <strong>액션 활동</strong>을 새롭게 지원하여 여정 캔버스 내 액션 구성을 간소화할 수 있습니다. 특히 이 새로운 기능에는 다음과 같은 이점이 있습니다.</p>
<ul>
<li>여정 캔버스 내 기본 액션 구성 간소화.</li>
<li>다중 액션 인바운드 액션 그룹을 만들 수 있는 용량.</li>
<li>모든 기본 제공 채널 액션에 최적화를 더하는 기능.</li>
<li>모든 액션에 실험과 다국어 옵션을 모두 추가하는 기능.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../building-journeys/journey-action.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 20일</p>
<p><strong>참고:</strong> 이제 액션 여정 활동을 통해 모든 기본 채널에 액세스할 수 있습니다. 레거시 기본 채널 활동은 3월 릴리스부터 사용이 중지될 예정입니다. 레거시 액션을 포함한 기존 여정은 마이그레이션할 필요 없이 계속 정상적으로 작동합니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>아웃바운드 메시지의 웨이브 전송</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 캠페인 또는 여정에서 메시지를 시간에 따라 제어되는 배치 단위로 게재하는 작업을 예약할 수 있습니다.</p>
<p>웨이브 전송은 다음과 같은 이점을 제공합니다.</p>
<ul>
<li>전달성 향상 - 전송을 시간에 따라 나누어 보냄으로써 강력한 발신자 평판을 유지하고 스팸으로 플래그가 지정될 위험을 줄이는 데 도움이 됩니다.</li>
<li>부하 제어 - 한 번에 전송되는 메시지 수를 제한하여 다운스트림 시스템(예: 콜센터, 랜딩 페이지)에 과부하가 걸리는 것을 방지합니다.</li>
<li>시간이 중요한 대량 발송 사용 사례 - 대상자의 규모가 크거나 시간 조절이 필요한 경우(예: 콜센터 용량, 점진적 게재량 증가 또는 시간 제한이 있는 오퍼)에 적합합니다.</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p><strong>캠페인</strong>의 경우 이 기능을 모든 환경에서 사용할 수 있습니다(일반 가용성). 자세한 내용은 <a href="../campaigns/send-using-waves.md">세부 설명서</a>를 참조하십시오.</p>

<p><strong>여정</strong>의 경우 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오. 자세한 내용은 <a href="../building-journeys/send-using-waves.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 19일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>하위 도메인을 사용자 정의 위임으로 마이그레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 CNAME 위임 모드를 사용하여 하위 도메인을 인터페이스에서 직접 사용자 정의 위임으로 마이그레이션함으로써 채널 구성을 다시 작성하지 않고도 회사의 지침에 따라 더 엄격한 보안 정책을 충족할 수 있습니다.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../configuration/custom-subdomain-migration.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 19일</p>
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
<p>Adobe Journey Optimizer가 이제 <strong>웹 푸시 알림</strong>을 지원하여 푸시 채널을 모바일 밖까지 확장합니다. <strong>모바일 브라우저와 데스크탑 브라우저</strong> 모두에 알림을 원활하게 전달할 수 있으므로 앱 설치를 요청할 필요 없이 고객의 디바이스에서 직접 고객에게 연락할 수 있습니다. 이 향상된 기능을 통해 이미 모바일 푸시에서 사용 가능한 것과 동일한 작성 워크플로 및 타기팅 기능을 활용하여 사용자에게 적시에 개인화된 메시지를 실시간으로 보낼 수 있습니다.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>이전에 Beta로 릴리스된 이 기능을 모든 환경에서 사용할 수 있게 됩니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../push/push-configuration-web.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 13일</p>
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
<p>이제 여정 캔버스에서 새로운 <strong>콘텐츠 결정 활동</strong>을 사용하여 개인화된 오퍼를 고객 여정에 직접 통합할 수 있습니다. 이 활동을 사용하면 의사 결정 기반 콘텐츠를 제공하고 여정 전체에 걸쳐 이러한 오퍼를 참조하여 자격 기반 분기를 만들기 위한 조건, 외부 시스템에 오퍼 데이터를 전달하기 위한 사용자 정의 액션, 완전히 개인화된 고객 경험을 구축하기 위한 기타 활동에 활용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/content-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 10일</p>
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
<p>마이그레이션 도구 API를 사용하여 <strong>의사 결정 관리</strong> 엔터티를 프로그래밍 방식으로 <strong>Decisioning</strong>으로 마이그레이션할 수 있습니다. 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>유연한 마이그레이션 범위(샌드박스, 오퍼 또는 의사 결정 수준)</li>
<li>자동화된 종속성 분석 및 유효성 검사</li>
<li>완료된 마이그레이션에 대한 롤백 지원</li>
<li>오브젝트 매핑이 포함된 자세한 마이그레이션 보고서</li>
</ul>
<p>자세한 내용은 <a href="../experience-decisioning/decisioning-migration-api.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 3일</p>
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
<p>새로운 모니터링 대시보드와 보강된 여정 단계 이벤트 데이터로 사용자 정의 액션 엔드포인트의 상태와 성능에 대한 심층 인사이트를 얻을 수 있습니다. 성공한 호출, 오류, 처리량, 응답 시간, 대기열 대기 시간을 추적하여 예외 항목이 발생하는 시점, 위치, 이유를 신속하게 파악합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../action/reporting.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 3일</p>
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
<p>이제 Decisioning을 통해 SMS 메시지의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선순위 점수, 공식 또는 AI 모델을 사용하여 고객에게 최상의 콘텐츠를 표시합니다.</p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 2일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#feb-26-01-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### 구성

* **여정 표현식에서 경험 이벤트 사용** - 2026년 4월 1일부터 지난 90일 동안 이 기능을 사용하지 않은 조직의 경우 여정 표현식에서 경험 이벤트 속성 사용이 더 이상 지원되지 않습니다. 이 기능은 2025년 7월 8일부터 신규 고객사에는 제공되지 않고 있습니다. 대안은 [여정에서 경험 이벤트 조회](../building-journeys/exp-event-lookup.md)를 참조하세요.

#### 콘텐츠 관리

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **테마를 사용하여 이미지를 이메일 템플릿으로 변환** - Journey Optimizer에서 이미지를 이메일 템플릿으로 변환할 때 이제 테마를 입력으로 사용하여 생성된 HTML이 브랜드 매개변수를 따르도록 할 수 있습니다. 배경색, 버튼 색상, 글꼴, 줄 간격, 여백 및 채우기와 같은 스타일이 자동으로 적용되어 수동 디자인 작업이 줄어들고 최소한의 편집으로 바로 사용할 수 있는 템플릿이 제공됩니다. [자세히 보기](../content-management/image-to-html.md)

  사용 가능한 날짜: 2026년 2월 17일

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### 이메일 디자이너

* **텍스트 들여쓰기** - 이제 속성 패널에서 텍스트 구성 요소의 단락 첫 줄에 사용자 정의 가능한 왼쪽 들여쓰기를 직접 적용할 수 있습니다. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->따라서 사설이나 기사와 같은 장문의 콘텐츠 가독성이 향상됩니다. [자세히 보기](../email/get-started-email-style.md)

  사용 가능한 날짜: 2026년 2월 18일

#### 결정

* **의사 결정에서 Adobe Experience Platform 데이터를 사용하기 위한 Edge 인바운드 지원** - 이제 의사 결정에서 Adobe Experience Platform 데이터를 사용하면 여정의 이메일 및 사용자 정의 액션 외에도 Edge 인바운드 사용 사례를 지원합니다. [자세히 보기](../experience-decisioning/aep-data-exd.md)

  이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

* **코드 기반 경험 채널에서 의사 결정 미리 보기** - 이제 코드 기반 경험 채널로 의사 결정을 구성할 때 의사 결정 항목을 미리 볼 수 있습니다. 미리 보기는 실제 서비스 시작 전에 저작 인터페이스에서 바로 사용할 수 있습니다. [자세히 보기](../code-based/test-code-based.md#preview-code-based)

  사용 가능한 날짜: 2026년 2월 18일

<!--
THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.
-->

#### 개인화

* **실행 메타데이터 도우미** - `executionMetadata` 도우미 함수를 이제 모든 Journey Optimizer 고객이 사용할 수 있습니다. 이 기능을 사용하면 모든 기본 액션에 컨텍스트 정보를 동적으로 추가하고 해당 정보를 데이터 세트에 캡처하여 외부 시스템으로 내보낼 수 있습니다. [자세히 보기](../personalization/functions/helpers.md#execution-metadata)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 2월 20일.

#### SMS

* **SMS 웹훅** - 이제 모든 SMS 제공업체에서 웹훅이 지원됩니다. 각 웹훅을 의도한 목적에 따라 수신 메시지를 캡처하기 위한 인바운드 웹훅과 게재 수신, 상태 업데이트, 기타 메시지 관련 이벤트를 수신하기 위한 피드백 웹훅으로 구성할 수 있습니다. [자세히 보기](../mobile/mobile-webhook.md)

  사용 가능한 날짜: 2026년 2월 2일.



## 26년 1월 릴리스 정보 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### 새로운 기능 {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>푸시 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>의사 결정</strong>을 사용하여 <strong>푸시 알림</strong>의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선순위 점수, 공식 또는 AI 모델을 사용하여 고객에게 최상의 콘텐츠를 표시합니다.</p>
<p>푸시 알림에서 경험 결정을 사용하려면 특정 버전의 Mobile SDK가 필요합니다. 이 기능을 구현하기 전에 <a href="https://developer.adobe.com/client-sdks/home/release-notes" target="_blank">릴리스 정보</a>에서 필요한 버전을 확인하고 그에 따라 업그레이드했는지 확인하세요. 또한 <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions" target="_blank">이 섹션</a>에서 플랫폼에 사용 가능한 모든 SDK 버전을 확인할 수 있습니다.</p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 1월 30일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 다이렉트 메일 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>전에는 캠페인에서만 사용할 수 있던 <strong>다이렉트 메일</strong> 채널을 이제 여정 캔버스에서 사용하여 DM을 여정에 통합할 수 있습니다. 이제 파일 추출 구성 및 시간 기반 빈도 설정 지원이 추가되어 DM을 <strong>배치 및 1:1 여정 시나리오</strong> 모두에서 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>자세한 내용은 <a href="../direct-mail/get-started-direct-mail.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 1월 29일 금요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>방해 금지 시간(시간 기반 제외)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>방해 금지 시간</strong> 기능으로 이메일, SMS, 푸시, WhatsApp 채널에 대한 시간 기반 제외를 정의할 수 있습니다. 특정 시간 동안 메시지가 전송되지 않도록 하여 고객 환경 설정과 및 규정 요건을 준수할 수 있습니다. <strong>규칙 세트</strong>를 통해 방해 금지 시간을 적용할 수 있으며, 정확한 제어를 위해 이 규칙 세트를 캠페인이나 여정의 개별 액션에 할당할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 일반 가용성 릴리스에서는 고객이 방해 금지 시간이 끝날 때까지 캠페인 액션을 대기열에 추가할 수 있는 기능과 활성화된 방해 금지 시간 규칙을 미리 볼 수 있는 기능이 제공됩니다.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>자세한 내용은 <a href="../conflict-prioritization/quiet-hours.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 1월 29일 금요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>메시지 내보내기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 및 SMS 채널에서 새로운 <strong>메시지 내보내기</strong> 기능을 사용할 수 있습니다. 이 기능을 사용하면 보낸 메시지 콘텐츠를 전용 Experience Platform 데이터 세트로 자동으로 내보내 다음과 같은 작업을 수행할 수 있습니다.</p>
<ul>
<li>규정 준수 요건 충족(예: HIPAA)</li>
<li>법률 소송 및 고객 지원 센터 문의 메시지 보관</li>
<li>개인에게 전송된 개인화된 콘텐츠의 사본 유지</li>
</ul>
<p>레코드는 수집 후 7일 동안 AJO 메시지 내보내기 데이터 세트에 보존됩니다. 이 보존 기간 동안 Experience Platform 대상을 통해 자체 스토리지로 내보낼 수 있습니다. 이 기능은 채널 구성 수준에서 활성화되므로 내보낼 메시지를 <strong>세밀하게 제어</strong>할 수 있습니다.</p>
<p>이 기능은 메시지 내보내기 추가 기능 서비스를 구입한 조직의 이메일 및 SMS 채널에서만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>자세한 내용은 <a href="../configuration/message-export.md#message-export">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 1월 28일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 다이렉트 메일 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션 캠페인에서 다이렉트 메일 채널을 사용할 수 있습니다. <strong>다이렉트 메일 활동</strong>은 오케스트레이션된 캠페인 내에서 다이렉트 메일 전송 과정을 원활하게 하며 일회성 메시지와 되풀이 메시지에 모두 적용됩니다. 이는 다이렉트 메일 제공업체에 필요한 <strong>추출 파일</strong> 생성 프로세스를 자동화하는 역할을 합니다. 채널 활동을 오케스트레이션된 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>자세한 내용은 <a href="../orchestrated/activities/channels.md#channel">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 1월 28일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey 에이전트 - 여정 만들기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey 에이전트가 생성 기능을 제공하므로 Journey Optimizer 사용자는 <strong>자연어 인터페이스</strong>를 통해 마케팅 여정을 작성하고 구성할 수 있습니다. 이 새로운 기술 덕분에 실무자가 <strong>대화 프롬프트</strong>로 요구 사항을 설명하기만 하면 여정을 빠르게 만들 수 있습니다. 이러한 혁신은 여정을 만드는 프로세스를 간소화하여 마케터가 기술 구성보다 전략에 집중할 수 있도록 지원합니다.</p>
<p>자세한 내용은 <a href="../start/ai-features.md#journey-agent">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 1월 12일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>액션 캠페인 검색 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 Journey Optimizer API를 사용하여 캠페인의 세부 정보, 버전, 구성 등 <strong>캠페인 관련 데이터</strong>를 프로그램 방식으로 검색하고 확인할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 11월 24일</p>
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
<p>이제 <strong>사전 승인된 테마</strong>를 빠르게 적용하여 모든 이메일에 대한 <strong>브랜드 일관성</strong>을 보장하고, 캠페인을 만드는 프로세스의 속도를 높이고, 디자인 팀에 대한 의존도를 줄이면서 고품질 이메일을 독립적으로 만들 수 있습니다.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>이전에 Beta 버전으로 릴리스된 이 기능을 이제 일부 조직에서 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../email/apply-email-themes.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 11월 5일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-26-01-improv}

#### AI

* **AI 어시스턴트 콘텐츠 품질 검사** - 이제 브랜드 일관성 외에도 전체 <strong>콘텐츠 품질</strong>을 평가하여 브랜드 가이드라인과 별개로 <strong>가독성</strong>, 일치도, 효과성 관련 잠재적인 문제를 찾을 수 있습니다. 이 자동화된 검사는 명확하지 않은 메시지, 일관되지 않은 톤 또는 구조적으로 빠진 부분을 식별하는 데 도움이 됩니다. [자세히 보기](../content-management/brands-score.md#validate-quality).

  [비디오에서 이 기능을 살펴보십시오](https://video.tv.adobe.com/v/3470553/?captions=kor&learn=on).

#### 여정

* **기본 및 Adobe Campaign 메시지 액션 결합** - 이제 Journey Optimizer에서 <strong>Adobe Campaign v7/v8</strong> 메시지 액션을 <strong>기본 채널 액션</strong>과 같은 여정에서 결합할 수 있습니다. [자세히 보기](../building-journeys/using-adobe-campaign-v7-v8.md)

  사용 가능한 날짜: 2026년 1월 27일 수요일.

* **사용자 정의 액션 오류 응답 페이로드** - 이제 사용자 정의 액션에 대해 선택적으로 <strong>오류 응답 페이로드</strong>를 정의할 수 있습니다. 호출이 실패하면 오류 페이로드가 여정 컨텍스트(액션의 errorResponse 노드 아래)에 노출되며 <strong>시간 초과/오류 분기</strong>에서 `jo_status_code`와(과) 함께 사용할 수 있어 보다 풍부한 대체 논리 및 디버깅을 지원합니다. [자세히 보기](../action/about-custom-action-configuration.md#define-the-message-parameters)

  사용 가능한 날짜: 2026년 1월 27일 수요일.

* **여정의 여정 페이로드 크기 유효성 검사** - 이제 Journey Optimizer에서 최적의 성능과 시스템 안정성을 보장하기 위해 <strong>페이로드 크기</strong>에 대해 유효성 검사를 수행합니다. 여정을 작성하거나 게시할 때 페이로드 크기가 권장 한도에 근접하거나 이를 초과하는 경우 명확한 <strong>경고 및 오류</strong>가 표시되고, 실행 가능한 여정 구성 최적화 지침이 제공됩니다. 이 사전 유효성 검사는 잠재적 문제를 조기에 식별하고 여정 성능을 유지하는 데 도움이 됩니다. [자세히 보기](../start/guardrails.md#journey-payload-size)

  사용 가능한 날짜: 2026년 1월 27일 수요일.


* **여정 경고** - 여정에 대해 새로운 <strong>사전 구성 경고</strong>를 사용할 수 있습니다.
   * <strong>프로필 삭제율 초과</strong> - 지난 5분 동안 입장한 프로필에 대한 프로필 삭제율이 임계값 초과
   * <strong>사용자 정의 액션 오류율 초과</strong> - 지난 5분 동안 성공적인 HTTP 호출에 대한 사용자 정의 액션 오류율이 임계값 초과
   * <strong>프로필 오류율 초과</strong> -지난 5분 동안 입장한 프로필 대비 오류가 발생한 프로필 비율이 임계값 초과

  자세한 내용은 [세부 설명서](../reports/alerts.md)를 참조하십시오.

  사용 가능한 날짜: 2025년 10월 14일.

#### 오케스트레이션된 캠페인

* **대상자에 대한 데이터 사용 레이블 상속** - 이제 오케스트레이션된 캠페인에 <strong>대상자</strong>를 저장할 때 Adobe Experience Platform에 적용된 레이블이 자동으로 이전되어 수동 <strong>DULE 태그 지정</strong> 작업이 줄어듭니다. [자세히 보기](../orchestrated/activities/save-audience.md)

* **매개 변수가 있는 미리 정의된 필터** - 이제 오케스트레이션된 캠페인에서 재사용과 편집이 가능한 규칙에 대해 <strong>매개 변수</strong>가 있는 <strong>미리 정의된 필터</strong>를 만들 수 있습니다. [자세히 보기](../orchestrated/predefined-filters.md)

* **속성 선택 및 분포 값 복사** - 이제 오케스트레이션 캠페인의 <strong>값 분포</strong> 보기에서 직접 <strong>값을 선택하거나 복사</strong>할 수 있습니다. [자세히 보기](../orchestrated/build-query.md)

* **보내기 전 메시지 확인** - 이제 실수로 오케스트레이션된 캠페인을 잘못 보내는 상황을 줄이기 위해 보내기 전에 <strong>확인 단계</strong>가 기본적으로 활성화됩니다. [자세히 보기](../orchestrated/activities/channels.md#confirm-message-sending)

* **사전 정의된 리타기팅 필터** - 오케스트레이션된 캠페인 사용 사례에 대해 더 쉬운 리타기팅을 지원하기 위해 이번 릴리스에서는 새로운 <strong>캠페인 피드백 필터</strong>를 도입했습니다. 이 필터를 사용하면 보냄, 열림만, 열림 또는 클릭됨, 열림 및 클릭됨 등 <strong>메시지 참여</strong>를 기반으로 대상자를 직접 타기팅하고 리타기팅할 특정 캠페인 또는 전환 중 캠페인을 선택할 수 있습니다. [자세히 보기](../orchestrated/retarget.md)

* **속도 제어 지원** - 이제 오케스트레이션된 캠페인이 <strong>속도 제어</strong>를 지원하여 게재 속도를 조정하고 <strong>볼륨 제한</strong>에 맞추는 데 도움이 됩니다. [자세히 보기](../orchestrated/activities/channels.md#rate-control)

* **다시 시작 버튼** - 오케스트레이션된 캠페인에 이제 <strong>다시 시작 버튼</strong>이 포함되어 있으므로 캠페인을 게시하기 전에 필요한 경우 <strong>실행을 빠르게 다시 시작</strong>할 수 있습니다. [자세히 보기](../orchestrated/start-monitor-campaigns.md)

* **사용자 생성 메타데이터 지원** - 이제 오케스트레이션된 캠페인용 개인화 편집기에서 <strong>executionMetadata 도우미 함수</strong>가 제공되어 모든 기본 액션에 상황별 정보를 첨부하고 데이터 세트에 저장하여 외부 시스템으로 내보낼 수 있습니다. [자세히 보기](../personalization/functions/helpers.md#execution-metadata)

  사용 가능한 날짜: 2026년 1월 27일 수요일.

* **실행 중인 캠페인을 초안 상태로 되돌리기** - 이제 실행 오류가 발생하거나 실행 시작 전에 예약된 캠페인을 수정해야 하는 경우 실행 중인 오케스트레이션된 캠페인을 초안 상태로 되돌릴 수 있습니다. 이 옵션은 첫 번째 메시지가 전송되기 전까지 사용할 수 있습니다. [자세히 보기](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### 캠페인

* **프로필 시간대를 사용한 캠페인 예약** - 이제 Campaign 예약 시 각 프로필의 <strong>시간대</strong>를 사용하여 의도한 현지 시간에 메시지를 게재할 수 있습니다. [자세히 보기](../campaigns/campaign-schedule.md)

  **참고**: 이 개선 사항은 일부 조직에서만 사용할 수 있습니다(제한적 가용성).

  사용 가능한 날짜: 2026년 1월 27일 수요일.

#### 권한

* **여정 및 캠페인에 대한 자체 승인 방지** - <strong>승인 정책</strong>을 만들거나 설정할 때 여정 또는 캠페인 작성자가 <strong>자신의 오브젝트를 직접 승인</strong>하지 못하도록 하는 옵션을 추가했습니다. [자세히 보기](../test-approve/approval-policies.md)

  사용 가능한 날짜: 2026년 1월 27일 수요일.
