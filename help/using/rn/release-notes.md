---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 89b884cf1feb7af9fe52b14b4ae706013ed70247
workflow-type: tm+mt
source-wordcount: '3965'
ht-degree: 17%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 해결을 지원합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적인 게재 모델을 따르므로 Adobe은 새로운 기능, 개선 사항 및 수정 사항을 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다.

이 모델로 인해 월별 릴리스 사이에 릴리스 정보가 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 2026년 4월 프리릴리스 정보 {#april-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

4월 초에 출시된 새로운 기능 및 개선 사항은 출시 일자와 함께 발표됩니다.

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
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
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
<p>이제 Adobe Journey Optimizer은 MCP 호환 애플리케이션 내에서 직접 캠페인, 충성도, 채널 구성 및 샌드박스 작업을 표시하는 <strong>MCP(Model Context Protocol) 서버</strong>를 제공합니다. 이 통합을 통해 다양한 가상 사용자가 동일한 오케스트레이션 데이터를 기반으로 공동 작업할 수 있습니다. Adobe Journey Optimizer REST API에 대해 쿼리를 작성하거나 여러 UI 화면을 탐색하는 대신, 사용자의 의도를 대화식으로 설명하고 LLM이 적절한 MCP 도구를 호출하도록 할 수 있습니다. 이 기능은 현재 클라우드 웹 및 데스크탑에서 사용할 수 있습니다.</p>
<p>이 기능은 공용 Beta의 모든 고객이 사용할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>샌드박스 간 조정된 캠페인 복사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 샌드박스 도구 는 한 샌드박스에서 다른 샌드박스로 오케스트레이션된 캠페인을 패키징 및 복사할 수 있도록 지원합니다. 따라서 각 환경에서 캠페인을 수동으로 재구축할 필요가 없습니다. 캠페인이 패키지화되면 병합 정책, 메시지와 같은 핵심 종속 오브젝트가 자동으로 포함되므로, 가져온 캠페인이 구성 및 유효성 검사를 수행할 준비가 된 상태로 도착합니다. 프로덕션 환경을 보호하기 위해 가져온 모든 캠페인은 대상 샌드박스에 초안 상태로 전환되므로, 캠페인이 실행되기 전에 팀에서 검토 및 승인 단계를 거치게 됩니다.</p>
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
<p><strong>오케스트레이션된 캠페인</strong>은(는) 이제 마지막 실행 이후 새로 적격한 프로필 또는 이벤트만 타겟팅하는 <strong>증분 쿼리</strong> 활동을 지원합니다.

이렇게 하면 쿼리 워크로드를 줄이고 시간이 지남에 따라 중복 전송을 방지하면서 순 신규 대상자(새 등록, 새로 자격을 얻은 충성도 멤버 및 유사한 세그먼트)에 초점을 맞춘 반복 캠페인을 유지할 수 있습니다.</p>
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
<p>Adobe Journey Optimizer의 <b>Adobe Express 통합</b>을(를) 사용하면 콘텐츠를 만드는 동안 Adobe Express의 편집 도구를 직접 사용할 수 있으므로 에셋의 크기를 조정하고, 배경을 제거하고, 자르고, JPEG 또는 PNG로 변환할 수 있습니다.
</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>자세한 내용은 <a href="../integrations/express.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 23일</p>
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
<p>이제 Adobe Journey Optimizer에는 Gmail의 Apple Intelligence 및 Google Gemini와 같은 AI 기반 받은 편지함에 대해 이메일이 최적으로 구성되도록 하는 새로운 기능이 포함됩니다.</p>
<p>AI 어시스턴트가 수신자가 이메일을 읽고 행동하는 방법을 점점 더 제어하므로 이 기능은 요약, 등급, 우선 순위 지정 및 의도 추출을 비롯한 다운스트림 AI 작업에서 잘 수행되는 콘텐츠를 생성하고 작성하는 데 도움이 됩니다.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>자세한 내용은 <a href="../email/llm-email-optimizer.md">AI 받은 편지함에 대한 전자 메일 최적화</a>를 참조하세요.</p>
<p>사용 가능한 날짜: 2026년 4월 17일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalization 표현식을 위한 AI 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 이제 <strong>AI Assistant</strong>이(가) 자연어 프롬프트를 유효한 개인화 표현식 및 조건부 논리로 변환하는 개인화 편집기에 직접 포함되므로 구문 전문 지식이 필요하지 않습니다. 달성하고자 하는 개인화에 대해 설명하고, AI는 즉시 적용하거나 후속 프롬프트를 통해 구체화할 수 있는 사용 준비 코드를 생성합니다.</p>
<p>그 보조원은 또한 역순으로 일한다. 기존 표현식을 선택하고 논리를 설명하거나 문제를 식별하거나 개선 사항을 제안하도록 요청합니다. 이렇게 하면 새 표현식을 작성할 뿐만 아니라 팀 전체에서 기존 표현식을 검토하고 디버깅하는 데에도 유용합니다.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>자세한 내용은 <a href="../content-management/generative-personalization-expressions.md">Personalization 표현식 AI 지원</a>을 참조하세요.</p>
<p>사용 가능한 날짜: 2026년 4월 13일</p>
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
<p>새로운 <strong>최적화</strong> 노드를 사용하여 A/B 테스트 또는 multi-armed bandit 실험을 실행하여 비즈니스 중심 KPI를 충족하는 최상의 경로를 결정하십시오. 이 도구를 사용하여 테스트 및 변경을 수행하고 커뮤니케이션, 시퀀스, 타이밍을 사용자 정의하여 고객에게 가장 효과적으로 다가갈 수 있습니다.
</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>일반 가용성의 일부로 이 릴리스에서는 단일 여정에 대해 <strong>실험 유형</strong> 선택(A/B 또는 multi-armed bandit) 및 <strong>승자 크기 조정</strong>을 도입합니다.</p>
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
<p><strong>받은 편지함</strong>은(는) 콘텐츠 카드에서 사용할 수 있는 모바일 기능으로, 이를 통해 고객은 앱 또는 웹 사이트 내에서 중앙 위치를 만들어 사용자에게 보낸 메시지를 표시할 수 있습니다. 따라서 메시지가 종료된 후에도 계속 액세스할 수 있도록 보장함으로써 마케팅 커뮤니케이션의 수명을 연장할 수 있습니다.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>자세한 내용은 <a href="../inbox/inbox-gs.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 7일</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>이메일 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>의사 결정</strong>을 사용하여 전자 메일 메시지의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선 순위 점수, 공식 또는 AI 모델을 활용하여 각 수신자에게 가장 관련성이 높은 오퍼와 콘텐츠를 표시합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). 이번 GA 릴리스에서는 미러 페이지가 지원됩니다.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision-policy.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 4월 6일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#april-26-improv}

#### AI

* **Campaign 대시보드의 브랜드 정렬 점수** - 이제 Campaign 대시보드 내에서 직접 브랜드 정렬 점수를 평가하여 콘텐츠를 브랜드에 유지할 수 있습니다. 이렇게 하면 콘텐츠 디자이너를 열지 않고도 지침을 한 눈에 확인할 수 있습니다.

* **프롬프트 길잡이 개선** - 프롬프트 길잡이는 사용자 프롬프트를 실시간으로 분석하고 명확성, 완전성 및 컨텍스트의 차이를 식별하여 AI 콘텐츠 생성을 개선합니다. 향상된 재작성을 제안하고 대상, 색조 및 의도와 같은 주요 세부 사항으로 프롬프트를 보강하는 실행 가능한 지침을 제공합니다. 이 기능은 또한 사용자가 생성 전에 입력을 구체화하는 데 도움이 되는 타겟팅된 명확화 질문을 제공합니다. 따라서 반복이 적을수록 보다 정확하고 고품질의 출력이 생성됩니다. [자세히 알아보기](../content-management/ai-assistant-prompting-guide.md)

#### 결정

* **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서 의사 결정 정책을 통해 코드 기반 경험 및 이메일 캠페인에서 활용할 수 있는 의사 결정 항목에 조각을 첨부할 수 있는 기능을 제공합니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

* **일시적으로 사용할 수 없는 조각을 건너뜁니다** - 의사 결정 항목에서 조각을 사용할 때 Edge에서 조각을 일시적으로 사용할 수 없는 경우 해당 조각을 건너뛰고 여정 또는 캠페인이 실패하는 대신 렌더링을 계속합니다. [자세히 보기](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  사용 가능한 날짜: 2026년 4월 14일

#### 푸시

* **채널 설정에서 앱 ID 개인화** - 이제 푸시 채널 구성 설정에서 **앱 ID** 필드를 개인화할 수 있으므로 각 수신자는 프로필 정보를 기반으로 해당 브랜드에서 푸시 알림을 받을 수 있습니다.

#### SMS

* **문자 수** - 이제 Adobe Journey Optimizer에서 문자 수를 사용하여 SMS 메시지의 길이를 실시간으로 모니터링할 수 있습니다. 이렇게 하면 메시지를 여러 세그먼트로 분할하여 서식을 보다 효율적으로 관리하고 예기치 않은 전송 비용 증가를 방지할 수 있습니다. [자세히 보기](../sms/create-sms.md)

* **전화 번호 및 발신자에서의 옵트아웃 및 동의** - 이제 SMS의 경우 Journey Optimizer에서 프로필의 전화 번호와 짧은 코드 수준에서 마케팅 동의 및 옵트아웃을 기록합니다.

  이 기능은 현재 Sinch SMS 구성에만 사용할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

* **SMS에서 사용자 지정 데이터 집합으로 인바운드** - **SMS API 자격 증명**&#x200B;에서 **인바운드 SMS**&#x200B;를 **사용자 지정, 프로필 사용 경험 이벤트 데이터 집합으로 라우팅**&#x200B;합니다. 기본 추적 데이터 집합만 선택하는 것이 아니라 선택하는 것입니다. [자세히 보기](../sms/sms-webhook.md)

* **Webhook 인터페이스 개선 사항** - SMS Webhooks를 구성할 때 이제 사용자 인터페이스에 실제 예제가 포함된 기본 제공 설정 가이드가 포함되어 있으므로 구성 흐름을 종료하지 않고도 공급자 페이로드를 조정하고 문제를 해결할 수 있습니다. [자세히 보기](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp 대화형 단추 및 추적** - 이제 Journey Optimizer의 WhatsApp이 템플릿과 사용 사례에 필요한 대화형 단추 및 내장된 대화형 추적을 지원하므로 다른 채널 보고와 함께 참여를 측정하고 성능을 분석할 수 있습니다.

#### Adobe Experience Manager 통합

* **Adobe Experience Manager 콘텐츠 조각 변형 지원** - 로케일 및 다국어 시나리오에 대한 개선된 처리로 Adobe Experience Manager 콘텐츠 조각을 삽입할 때 **콘텐츠 조각 변형**(예: 언어 또는 채널 변형)을 선택할 수 있습니다. [자세히 보기](../integrations/aem-fragments.md#aem-variations)

  이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

  사용 가능한 날짜: 2026년 4월 3일

* **작성 중 Adobe Experience Manager 콘텐츠 조각 컨텍스트** - 콘텐츠 조각 선택 항목은 텍스트 필드와 콘텐츠 블록 사이를 이동할 때 활성 상태로 유지되므로 매번 **AEM 콘텐츠 관리자 열기**&#x200B;를 다시 열지 않고 조각 필드를 더 추가할 수 있습니다. [자세히 보기](../integrations/aem-fragments.md)

  이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

  사용 가능한 날짜: 2026년 4월 1일

#### 구성

* **URL 매개 변수 암호화 키에 대한 특정 권한** - URL 매개 변수 암호화에 대한 키에 액세스하고 관리하기 위해 새 권한을 만들었습니다. 이제 **키 레지스트리 보기** 및 **키 레지스트리 관리** 권한이 부여되어야 합니다.

#### 오케스트레이션된 캠페인

* **데이터 Modeler 개선 사항** - 이제 오케스트레이션된 관계형 스키마가 여러 필드에 걸친 복합 키를 지원합니다. DDL 파일에서 스키마를 로드하면 열거형이 발생하고 DDL 또는 Excel 파일에서 로드하면 자동으로 테이블 간에 복합 관계가 만들어집니다. 이제 엔티티 관계 보기에서 합성 링크는 파일을 업로드한 후 테이블 간의 전체 필드 연결 집합을 표시합니다.

* **오케스트레이션된 캠페인의 전역 변수** - 이제 오케스트레이션된 캠페인이 한 번 정의하여 워크플로우 내의 모든 활동에서 재사용할 수 있는 전역 변수를 지원하므로 구성을 단순화하고 동적 값, 표현식 및 콘텐츠 개인화의 일관성을 보장합니다.

#### 이메일 디자인

* **전자 메일 콘텐츠에 대한 고급 HTML 편집기** - 고급 HTML 모드를 사용하면 전자 메일 Designer에서 콘텐츠의 HTML 소스를 편집하고, 소스에 고급 표현식(예: 조건)을 추가하고, 변경 내용을 손실하지 않고 HTML 보기와 데스크톱 보기 간에 전환할 수 있습니다.

  이전에는 전자 메일 콘텐츠 템플릿에만 사용할 수 있었지만, 이제 이 기능은 전자 메일 콘텐츠 템플릿 외에 전자 메일 Designer의 **전자 메일** 콘텐츠(예: 여정 및 캠페인으로 작성된 전자 메일)에도 배포됩니다. 현재 제한된 가용성 상태입니다. Adobe 담당자에게 문의하여 액세스 권한을 받으십시오. [자세히 보기](../email/email-expert-mode.md)

  사용 가능한 날짜: 2026년 4월 9일

* **이메일 Designer의 개인화 표현식에 대한 AI 도우미** - 이메일 Designer에서 구성 요소를 선택하고 상황별 도구 모음의 **표현식 추가**&#x200B;를 사용하여 필요한 개인화를 일반 언어로 설명하고 생성된 표현식을 검토한 다음 디자이너를 떠나지 않고 삽입합니다. [자세히 알아보기](../content-management/generative-personalization-expressions.md#generate-email-designer)

  사용 가능한 날짜: 2026년 4월 15일

#### 여정 경로 최적화

* **실험 유형** - 이제 경로 실험을 구성할 때 A/B 실험(시작 시 고정 분할) 또는 Multi-armed bandit(주별 가중치 업데이트가 있는 자동 분할) 중에서 선택할 수 있습니다. [자세히 보기](../building-journeys/path-experimentation.md)

  사용 가능한 날짜: 2026년 4월 7일

* **경로 실험: 우승자 크기 조정** - 이제 실험의 성공 경로를 전체 대상자에게 자동 또는 수동으로 롤아웃할 수 있습니다. 일단 승자가 결정되면 실험을 지속적으로 모니터링하지 않고 그 도달 범위와 효과를 증폭시킬 수 있다. [자세히 보기](../building-journeys/path-experimentation.md#scale-winner)

  이 기능은 단일 여정(이벤트 트리거 및 대상 자격 조건)에서만 사용할 수 있습니다. 대상자 읽기 여정에 사용할 수 없습니다.

  사용 가능한 날짜: 2026년 4월 7일

* **조건** - [최적화](../building-journeys/optimize.md) 활동은 여정에서 조건부 경로를 만드는 새로운 수단입니다. UI에서 제거된 이전의 **조건** 활동을 대체합니다. 모든 조건부 논리는 유지되고 이제 **최적화** 활동의 조건을 통해 처리됩니다. [자세히 보기](../building-journeys/conditions.md)

  이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 4월 7일


## 2026년 3월 릴리스 정보 {#march-26-rn}

[새 기능](#march-26-features) 및 [개선 사항](#march-26-improv) 섹션에서는 이미 사용 가능한 기능을 다룹니다. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**릴리스 날짜**: 2026년 3월 24~25일

### 새로운 기능 {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL 매개 변수 암호화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 메시지에 추가된 추적 및 랜딩 페이지 링크의 URL 매개 변수를 암호화할 수 있으므로, 중요한 매개 변수 데이터에 대한 추가 보안 계층을 제공합니다.</p>
<ul>
<li>전용 <strong>관리</strong> 레지스트리에서 암호화 키를 등록 및 관리합니다.</li>
<li>표현식에 새로운 'Encrypt' 도우미 함수를 사용하여 렌더링 시 보호하려는 쿼리 매개변수에 대한 URL의 중요 데이터를 암호화합니다.</li>
</ul>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>자세한 내용은 <a href="../personalization/url-parameter-encryption.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 31일</p>
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
<p>이제 Journey Optimizer에서 직접 이미지를 이메일 콘텐츠 템플릿으로 변환할 수 있습니다. AI 기반 분석을 사용하여 시각적 참조에서 구조화된 HTML 템플릿을 자동으로 생성하여 이메일 디자인 시간을 크게 단축할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>자세한 내용은 <a href="../content-management/image-to-html.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 31일</p>
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
<p>[!DNL Journey Optimizer]을(를) 사용하면 랜딩 페이지를 통해 프로필 특성을 캡처할 수 있습니다.</p>
<p>특정 데이터 세트를 기반으로 필요에 맞는 사용자 정의 양식을 만들고 디자인하고 관리합니다. 그런 다음 랜딩 페이지에서 이 양식을 활용하여 선택한 프로필 속성을 각 양식별로 정의한 데이터 세트에 추가할 수 있습니다.</p>
<p>이전에 미국 및 오스트레일리아의 고객을 위한 제한된 가용성에 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>자세한 내용은 <a href="../landing-pages/lp-forms.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 26일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인에서 활동 테스트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에서 새 <strong>Test</strong> 활동을 사용할 수 있습니다. 이 활동은 정의된 조건에 따라 워크플로우 실행을 다른 분기로 라우팅하므로 라이브 게재를 활성화하기 전에 캠페인 논리 및 구성을 확인할 수 있습니다.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>자세한 내용은 <a href="../orchestrated/activities/test.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 데이터 세트 조회 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정의 새 <strong>데이터 세트 조회</strong> 활동을 사용하면 런타임 시 Adobe Experience Platform 레코드 데이터 세트에서 데이터를 동적으로 검색할 수 있으므로 프로필 또는 이벤트 페이로드의 일부가 아닌 정보에 액세스할 수 있으므로 고객 상호 작용이 적절하고 적시에 유지됩니다.</p>
<p>이전에는 제한된 조직 집합에 대해 제한된 가용성으로 릴리스되었지만 이제 제한된 가용성으로 남아 있으면서 [데이터 집합 조회](../data/lookup-aep-data.md)를 사용할 수 있는 모든 고객이 여정의 데이터 집합 조회 활동을 사용할 수 있습니다.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>자세한 내용은 <a href="../building-journeys/dataset-lookup.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>작업 활동은 채널별 여정 활동을 대체합니다</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>2026년 2월에 <strong>작업 활동</strong>이 일반 지원됨에 따라 여정 캔버스에서 레거시 기본 채널 활동(전자 메일, 푸시, SMS, 인앱, 웹, 코드 기반 경험 및 콘텐츠 카드)이 이제 더 이상 사용되지 않습니다.</p>
<p>이제 별도의 채널별 노드가 필요하므로 단일 작업 활동을 사용하여 모든 채널 작업을 구성해야 합니다.</p>
<p>기존 채널 활동을 사용하는 기존 여정은 변경 사항이나 마이그레이션이 필요 없이 계속 작동합니다.</p>
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
<p>이메일 콘텐츠 템플릿에 대한 고급 HTML 모드를 사용하면 이메일 Designer에서 콘텐츠의 HTML 소스를 편집하고, 소스에 고급 표현식(예: 조건)을 추가하고, 변경 내용을 유지한 채 HTML 보기와 데스크탑 보기 간에 전환할 수 있습니다.</p>
<p>이 기능은 이메일 채널의 콘텐츠 템플릿에서만 사용할 수 있습니다. 현재 제한된 가용성 상태입니다. Adobe 담당자에게 문의하여 액세스 권한을 받으십시오.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>자세한 내용은 <a href="../email/email-expert-mode.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 10일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 지정 Firefly 모델 및 타사 이미지 생성 모델 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>승인된 서드파티 이미지 모델과 함께 표준 및 사용자 정의 Firefly 모델의 원활한 통합을 활성화하여 이미지 생성 시 더 큰 유연성, 컨트롤 및 브랜드 정렬을 제공합니다.</p>
<p>요구 사항에 맞는 모델을 선택하십시오.</p>
<ul><li> 추가 설정 없이 즉각적인 이미지를 생성할 수 있도록 <strong>Adobe 모델</strong>(Firefly Image Model 4 제공)</li><li> 특수 기능을 위한 <strong>파트너 모델</strong>(Gemini 2.5 Flash 지원)</li><li>브랜드 정체성, 스타일 및 시각적 지침에 따라 정확하게 일치하는 온브랜드 생성을 위한 <strong>사용자 지정 모델</strong>(사용자 고유의 자산에 대해 교육된 브랜드별 모델).</li></ul>
<p>자세한 내용은 <a href="../content-management/generative-models.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 2일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>iOS에 대한 라이브 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer에서 <strong>iOS 라이브 활동</strong>을 통해 고객의 Screens 및 Dynamic Island 잠금에 직접 실시간 경험을 제공할 수 있습니다. 사용자가 앱을 열지 않고도 주문 추적 및 비행 상태부터 이벤트 처리, 라이브 점수 및 게재 진행률에 이르기까지 라이브 업데이트를 제공할 수 있습니다. 대상자가 있는 바로 그 순간에 정보를 얻고 참여하도록 하십시오.</p>
<p>이전에 베타 버전으로 출시된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p>자세한 내용은 <a href="../mobile-live/get-started-mobile-live.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 3일</p>
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
<p><strong>Adobe Experience Platform Agent Orchestrator</strong>에서 제공하는 <strong>Journey Agent</strong>은(는) Journey Optimizer에서 사용할 수 있으며 자연어 인터페이스를 통해 여정을 분석할 수 있도록 해줍니다. 이제 Journey Agent에서 직접 채널별 콘텐츠를 생성하고 관리할 수도 있습니다. 또한 이메일 및 푸시와 같은 채널용 콘텐츠를 만들고, 템플릿을 적용하고 미리 보고, 프롬프트를 통해 색조와 스타일을 개선하고, <strong>콘텐츠 Designer</strong>에서 콘텐츠를 열어 상황에 맞게 편집할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=ko" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 4일</p>
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
<p>이제 Journey Optimizer을 통해 Decisioning AI 모델의 상태, 교육 상태 및 성능을 모니터링할 수 있습니다. 이를 통해 교육 성공을 확인하고, 실패를 해결하며, 결과에 미치는 영향을 파악하여 AI를 사용하는 각 고객을 위한 최상의 오퍼를 선택할 수 있습니다. 이 기능은 <strong>Decisioning</strong>에만 사용할 수 있습니다(이전 의사 결정 관리 모델에는 사용할 수 없음).</p>
<p>이 기능은 현재 <strong>개인화된 최적화</strong> 모델에만 사용할 수 있습니다(자동 최적화는 아님).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>자세한 내용은 <a href="../experience-decisioning/ranking/ai-model-observability.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 3월 9일</p>
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
<p>이제 오케스트레이션된 캠페인을 <strong>API 신호</strong>를 통해 트리거할 수 있습니다. 이를 설정하려면 Target 캠페인을 <strong>신호에 의해 트리거됨</strong>(으)로 구성하고 게시한 다음 API 호출을 사용하여 실행합니다. API 호출에 포함된 모든 매개 변수는 실행 중인 캠페인 내에서 변수로 사용할 수 있습니다. 신호 트리거 오케스트레이션된 캠페인은 <strong>일괄</strong> 캠페인으로 유지되며 API 트리거 캠페인과 다릅니다.</p>
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
<p>오케스트레이션된 캠페인에서는 이제 채널 활동을 <strong>트랜잭션</strong> 범주로 설정할 수 있습니다. 이렇게 하면 해당 활동에 트랜잭션 채널 구성이 적용되며, 비즈니스 규칙이 적용되지 않거나 고객의 옵트인이 필요하지 않은 경우에 유용합니다.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>자세한 내용은 <a href="../orchestrated/activities/channels.md#add">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 앞으로 며칠 동안 모든 지역으로 점진적으로 배포될 예정입니다.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#march-26-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### 개인화

* **전체/기본 URL 개인화** - 프로필 특성(예: 도메인 또는 경로)을 사용하여 대상 URL을 개인화할 수 있습니다. 이 기능을 활성화하려면 Adobe에 허용된 도메인 목록을 제공하십시오. [자세히 보기](../personalization/personalization-build-expressions.md#where)

  이전에 여정에서 사용할 수 있도록 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 4월 1일

#### 보고

* **전송 시간 최적화: 컨트롤 위치 및 새 리프트 보고서를 업데이트했습니다** - STO(전송 시간 최적화) 컨트롤이 작업 구성 메뉴로 재배치되었습니다. 또한 이제 여정 보고서에서 STO가 캠페인 성과 지표에 미치는 영향을 측정하는 새로운 상승도 보고서를 사용할 수 있습니다. [자세히 보기](../reports/channel-report-cja.md#optimization-models)

  사용 가능한 날짜: 2026년 3월 27일

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### 구성

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **AJO 도메인 인증서 갱신 실패** - 이제 전자 메일 게재에 사용되는 도메인 인증서가 곧 만료되거나 이미 만료된 경우 전자 메일 또는 Journey Optimizer 알림 센터에서 시스템 경고를 수신하도록 구독할 수 있습니다. [자세히 보기](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  사용 가능한 날짜: 2026년 3월 26일

* **AJO 보조 받는 사람 피드백 이벤트 데이터 세트 이름 바꾸기** - `AJO Email BCC Feedback Event` 데이터 세트의 이름이 `AJO Secondary Recipient Feedback Event` 데이터 세트로 바뀌었습니다. 영향은 상황에 따라 다릅니다.

   * **기존 사용자**: 표시 이름만 업데이트됩니다. 기본 테이블 이름은 변경되지 않습니다.
   * **새 사용자 및 샌드박스**: 표시 이름과 테이블 이름이 모두 새 이름을 반영합니다.
   * **새 샌드박스를 가진 기존 사용자**: 표시 이름과 테이블 이름이 모두 새 이름으로 업데이트됩니다.

  >[!NOTE]
  >
  >새 데이터 세트에는 새 이름이 즉시 표시됩니다. 이전 데이터 세트 이름의 경우 채우기 및 조정은 점진적으로 진행되며 완료하는 데 몇 주가 걸릴 수 있습니다.

  사용 가능한 날짜: 2026년 3월 2일


#### 여정

* **프로필 업데이트 작업: 여러 프로필 특성 지원** - **프로필 업데이트** 작업 활동은 이제 단일 노드에서 최대 5개의 프로필 특성 업데이트를 지원합니다. 이전에는 각 작업이 한 번에 하나의 속성만 업데이트할 수 있으므로 여러 노드가 여러 속성을 업데이트해야 했습니다. 새 **다른 필드 업데이트** 단추를 사용하여 필드/값 쌍을 추가하여 캔버스 복잡성을 줄이고 성능을 개선합니다. [자세히 알아보기](../building-journeys/update-profiles.md)

* **여정에서 아웃바운드 메시지의 웨이브 전송** - 이제 Journey Optimizer 여정의 메시지를 시간에 따라 제어된 배치로 전달하도록 예약할 수 있습니다. [자세히 알아보기](../building-journeys/send-using-waves.md)

  이전에 여정에서 사용할 수 있도록 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 3월 16일

* **여정 기술 세부 정보의 일시 중지 및 다시 시작 세부 정보** - 이제 **기술 세부 정보** 여정에 마지막 일시 중지 및 다시 시작 날짜 및 시간, 각 작업을 수행한 사용자의 표시 이름 및 내부 식별자, 일시 중지 동작, 최대 일시 중지 기간 및 자동 다시 시작 상태와 같은 일시 중지된 여정 설정의 전체 집합과 같은 추가 일시 중지 및 다시 시작 정보가 포함됩니다. [자세히 알아보기](../building-journeys/journey-properties.md)

  사용 가능한 날짜: 2026년 3월 2일

#### 결정

* **Decisioning 마이그레이션 — 오퍼 및 컨텍스트 특성** - 이제 마이그레이션 API 엔터티 매핑에 **오퍼 특성**(`migratedofferattributes`은(는) 개인화된 오퍼 항목 스키마에 있음) 및 **컨텍스트 특성**(`migratedcontextattributes`은(는) 마이그레이션 데이터 세트 스키마에 있음)이 나열됩니다. [자세히 보기](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  사용 가능한 날짜: 2026년 3월 31일

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->
