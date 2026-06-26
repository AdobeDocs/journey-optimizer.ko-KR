---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 2df5d9db31e03d4548b8ccc32c2d25293d829f1d
workflow-type: tm+mt
source-wordcount: 3714
ht-degree: 86%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 해결을 지원합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적 제공 모델을 따르므로 Adobe에서 새로운 기능, 개선 사항, 버그 해결 업데이트를 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다. 이 모델로 인해 월별 릴리스 사이에 릴리스 정보가 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

>[!NOTE]
>
>이 릴리스 정보에 나열된 기능에는 각 변경 사항이 사용자 환경에서 사용 가능해지는 시점을 나타내는 **사용 가능한 날짜**&#x200B;가 포함되어 있습니다. **곧 출시 예정** 아코디언 항목은 향후 며칠 또는 몇 주 내에 제공될 예정입니다. 이 섹션의 정보는 변경될 수 있습니다.

## 2026년 6월 릴리스 정보 {#june-26-rn}

### 여정 {#june-26-journeys}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 여정에 추가되었습니다. 향후 며칠 또는 몇 주 내에 추가 변경 사항이 있을 예정입니다.


<table>
<thead>
<tr>
<th><strong>여정 시뮬레이션(일반 공급)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 시뮬레이션으로 설정할 수 있습니다. 이 모드를 사용하면 시뮬레이션된 사용자를 사용하여 논리의 유효성을 검사할 수 있습니다. 시뮬레이션된 사용자는 시뮬레이션을 위해 특별히 생성된 임시 프로필로, Adobe Experience Platform에서 영구 테스트 프로필을 관리할 필요 없이 자유롭게 테스트할 수 있습니다. </p>
<p>이전에 제한적으로 공급되었던 여정 시뮬레이션 기능이 이제 모든 환경에서 사용 가능합니다. 이번 일반 공급 릴리스를 통해 Journey 에이전트를 사용하여 시뮬레이션 메뉴에서 직접 시뮬레이션된 사용자와 이벤트를 생성할 수 있습니다.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/simulate-journey-gs.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 9일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 조각(일반 공급)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 <strong>여정 조각</strong>을 만들 수 있습니다. 여정 조각은 한 번 생성하여 샌드박스 내 모든 여정에 배치할 수 있는 재사용 가능한 여정 노드 세트입니다. 자격 확인, 선호 채널 라우팅 논리 또는 환영 시퀀스 등 어떤 논리든지 조각을 사용하면 매번 처음부터 다시 구축할 필요 없이 팀이 더 빠르게 일관성을 유지할 수 있습니다.</p>
<p>생성된 조각은 전용 <strong>조각 인벤토리</strong>에 저장되며 <strong>여정 조각</strong> 활동을 사용하여 모든 여정에 삽입할 수 있습니다.</p>
<p>이전에는 제한 공급으로만 사용 가능했던 이 기능이 이제 모든 고객에게 정식으로 제공됩니다. 여정 조각은 또한 <strong>샌드박스 도구</strong>를 지원하여 샌드박스 간에 조각을 패키징하고 내보낼 수 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/journey-fragments.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 9일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 경로 최적화 - 타겟팅(일반 공급)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>활동 최적화</strong>에서 <strong>타겟팅 규칙</strong>을 지원합니다. 이를 통해 대상자 세그먼트 또는 프로필 속성을 기반으로 고객이 특정 여정 경로를 이용하기 위해 충족해야 하는 특정 기준을 정의할 수 있습니다.</p>
<p>고객이 무작위로 경로에 배정되는 실험 방식과 달리 타겟팅은 확정적 논리를 사용하여 적절한 대상자 또는 고객 프로필이 의도한 경로로 안내되도록 합니다.</p>
<p>이전에 제한 공급 상태로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/path-targeting.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 8일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 표현식을 위한 AI 어시스턴트(공개 Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 어시스턴트가 이제 여정 고급 표현식 편집기에서 자연어 프롬프트를 유효한 표현식과 조건 논리로 변환합니다. 작성하려는 표현식을 설명하면 AI 어시스턴트가 즉시 적용하거나 후속 프롬프트를 통해 수정할 수 있는 바로 사용 가능한 코드를 생성합니다.</p>
<p>이 기능은 모든 고객에게 공개 Beta 버전으로 제공됩니다.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/expression/expression-agent.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 3일</p> 
</td>
</tr>
</tbody>
</table>


* [!BADGE 사용 중단]{type=Negative} **대상 자격 노드에서 사용되지 않는 일괄 처리 대상** - **2026년 8월**&#x200B;부터 Journey Optimizer은 **대상 자격** 노드에서 일괄 처리 대상을 사용하는 여정에 대한 게시를 차단합니다. 여정 캔버스에 유효성 검사 경고가 이미 표시되어 있습니다. 기존 라이브 여정은 영향을 받지 않습니다. 이 구성을 포함하는 신규, 초안 및 중복 여정은 2026년 8월 이전에 업데이트해야 합니다. 대상 자격 노드에서 스트리밍 대상을 사용하거나 **대상 읽기** 활동으로 전환합니다. [여정 마이그레이션 방법 알아보기](../building-journeys/aq-batch-audiences-migration.md)

* **일시 중지된 여정을 직접 중지** - 이제 **일시 중지됨** 상태에서 직접 여정을 중지할 수 있습니다. 이전에는 일시 중지된 여정을 중지하려면 **Live**(으)로 다시 시작해야 했습니다. [자세히 보기](../building-journeys/journey-pause.md#stop-close-paused)

  사용 가능한 날짜: 2026년 6월 18~22일

* **외부 대상자에 대한 보조 식별자 지원** - 이제 CSV 파일에서 가져온 대상자와 페더레이션된 대상자 컴포지션으로 만든 대상자를 포함한 외부 대상자에 대해 여정의 보조 식별자가 지원됩니다. 대상자의 ID가 아닌 속성 또는 개인 ID가 아닌 속성은 모두 보조 ID로 지정할 수 있으며, 스키마 레이블 지정은 필요하지 않습니다. [자세히 보기](../building-journeys/supplemental-identifier.md)

  사용 가능한 날짜: 2026년 6월 11일

* **일회성 대상자 읽기 여정의 자동 중지** - 일회성 **대상자 읽기** 여정은 마지막 활성 프로필이 종료되면 자동으로 **중지됨** 상태로 전환됩니다. 이전에는 이러한 여정이 91일의 전역 시간 초과가 만료될 때까지 프로필이 더 이상 이동하지 않더라도 **라이브** 상태로 유지되었습니다. 이번 개선으로 여정 상태는 완료되는 즉시 실제 실행 상태를 반영하여 수동 개입 없이도 여정 인벤토리를 정확하게 관리할 수 있게 되었습니다.

  참고로, 이 기능은 대기 노드, 반응 노드 또는 이벤트 트리거 전환과 같이 대기 기간이 발생하는 노드가 포함된 여정에는 적용되지 않습니다. 이러한 여정은 표준 91일 전역 시간 초과가 적용됩니다. [자세히 알아보기](../building-journeys/end-journey.md#auto-stop-non-recurring)

  사용 가능한 날짜: 2026년 6월 9일

* **사용자 정의 액션의 인증서 기반 사용자 정의 인증** - 사용자 정의 액션에서 이제 인증서 기반 사용자 정의 인증을 지원합니다. 사용자 정의 인증 구성에 `subType: "certificateCredential"`을(를) 추가하면 Journey Optimizer는 Adobe의 관리형 인증서를 사용하여 JWT 클라이언트 어설션에 서명한 후 액세스 토큰으로 교환합니다. 클라이언트 암호는 필요하지 않습니다. Microsoft Entra ID와 같이 인증서 기반 ID 확인을 적용하는 엔터프라이즈 API용으로 설계되었습니다. [자세히 알아보기](../datasource/external-data-sources.md#certificate-credential)

  사용 가능한 날짜: 2026년 6월 4일

* **활성 여정 제한 증가 및 새로운 가드레일** - 이제 최대 **200개의 활성 여정**&#x200B;을 생성할 수 있으며, 이전 제한인 100개에서 증가했습니다. [자세히 보기](../start/guardrails.md#journeys-guardrails-journeys)

  사용 가능한 날짜: 2026년 6월 18일 이 기능은 앞으로 며칠에 걸쳐 모든 지역으로 점진적으로 배포될 예정입니다.


+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

* **여정 헤더에 시작 및 종료 날짜 표시** - 활성 여정에 시작 및/또는 종료 날짜를 설정하면 이제 **여정 헤더**&#x200B;에서 활성 상태 배지 옆에 표시됩니다. 표시되는 레이블은 각 날짜가 다가오는지 또는 이미 지났는지에 따라 달라집니다.

+++

### 오케스트레이션된 캠페인 {#june-26-oc}

이번 릴리스에서는 오케스트레이션된 캠페인에 다음과 같은 기능 및 개선 사항이 추가됩니다.

* **관계형 데이터에 대한 루프 기반 개인화** - 이제 개인화 편집기에서 주문, 계정 또는 예약과 같은 관계형 컬렉션을 반복하고 단일 전자 메일 또는 SMS 내에서 레코드당 하나의 콘텐츠 블록을 렌더링하는 루프 블록을 지원합니다. 컬렉션은 개인화 토큰을 사용하여 데이터 선택기를 통해 구성되며 표현식을 작성할 필요가 없습니다. [자세히 보기](../orchestrated/add-personalization.md#enrichment-collections)

  사용 가능한 날짜: 2026년 6월 26일

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 파일 기반 타겟팅</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인은 파일을 Adobe Experience Platform으로 먼저 수집하지 않고도 <strong>CSV 또는 TXT 파일</strong>을 타깃팅 대상자로 캠페인 캔버스에 직접 로드할 수 있습니다. 파일 데이터는 실행 시 사용되며 Adobe Experience Platform 데이터 세트로 지속되지 않습니다. 파일 설정 중에 열 매핑, 데이터 유형, NULL 처리 및 열별 오류 정책을 정의할 수 있습니다. 유효성 검사에 실패한 행은 캠페인이 실행되기 전에 거부되고 기록되므로, 수동 사전 처리 없이 대상자를 깔끔하게 유지합니다. 이는 전체 수집 파이프라인을 구축하는 것이 실용적이지 않은 애드혹 전송 또는 파트너 목록 캠페인에 특히 적합합니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p> 사용 가능한 날짜: 2026년 6월 30일</p>
</td>
</tr>
</tbody>
</table>

+++

### 결정 {#june-26-decisioning}

이번 릴리스에서는 의사 결정에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>DM 채널에서 의사 결정 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 다이렉트 메일 여정 및 캠페인에 의사 결정 정책을 추가할 수 있습니다. 의사 결정 정책은 의사 결정 엔진을 활용하여 각 대상자 멤버에 대한 최상의 콘텐츠를 동적으로 반환하는 오퍼에 대한 컨테이너입니다. 다이렉트 메일 의사 결정은 배치 의사 결정 사용 사례를 지원하므로 특정 Adobe Experience Platform 대상자의 모든 프로필에 대해 해당하는 오퍼 항목을 내보낼 수 있습니다. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>자세한 내용은 <a href="../experience-decisioning/use-decision-policy.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 3일</p>
</td>
</tr>
</tbody>
</table>

* **의사 결정에서 Adobe Experience Manager 콘텐츠 조각 활용** - 이제 Adobe Experience Manager 콘텐츠 조각을 Decisioning의 의사 결정 항목에 매핑하고 의사 결정 정책 내에서 활용하여 적절한 시기에 적절한 고객에게 적절한 조각을 전달할 수 있습니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). [자세히 보기](../experience-decisioning/fragments-decision-policies.md)

  사용 가능한 날짜: 2026년 6월 18일

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

* **동적 항목 속성** - 이제 프로필, 컨텍스트 및 대상자 데이터를 사용하여 결정 항목의 사용자 정의 속성을 게재 시 개인화할 수 있습니다. 이렇게 하면 사소한 콘텐츠 변형에 대한 중복 오퍼를 관리할 필요가 없어지므로 마케터는 더 적고 유연한 결정 항목을 관리할 수 있습니다.

  사용 가능한 날짜: 2026년 6월 말

+++

### 콘텐츠 관리 {#june-26-content}

이 릴리스의 콘텐츠 관리에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>콘텐츠 변형 시뮬레이션 — 업데이트된 경험 및 AI 변형 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>콘텐츠 시뮬레이션</strong> 워크플로에서 다음과 같은 두 가지 업데이트를 사용할 수 있습니다.</p>
<ul>
<li><strong>새 기본 경로</strong> — <strong>콘텐츠 시뮬레이션</strong>을 클릭하면 기본적으로 <strong>콘텐츠 변형 시뮬레이션</strong> 경험이 열립니다. 단일 화면에서 샘플 입력을 수동으로 또는 CSV/JSON 파일에서 추가하고, 시뮬레이션된 사용자를 재사용하고, 렌더링을 미리 보고, 교정본을 보낼 수 있습니다. Adobe Experience Platform 테스트 프로필로 미리 보기, 테스트 프로필 데이터와 함께 교정본 전송, 이메일 받은 편지함 렌더링 및 스팸 보고서 확인을 하려면 <strong>콘텐츠 시뮬레이션</strong>을 클릭한 후 드롭다운에서 <strong>콘텐츠 시뮬레이션(AEP 프로필)</strong>을 선택합니다.</li>
<li><strong>AI 생성 콘텐츠 변형</strong> — <strong>콘텐츠 변형 시뮬레이션</strong> 경험에서 <strong>생성</strong>을 클릭하고 AI를 사용하여 콘텐츠 변형을 자동으로 만듭니다. 시스템이 메시지를 분석하고 개인화 필드와 조건 분기를 감지하여 실제 값을 채워 넣으면 모든 변형을 수동으로 만들지 않고도 렌더링의 유효성을 검사할 수 있습니다.</li>
</ul>
<p>자세한 내용은 <a href="../test-approve/simulate-sample-input.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 9일</p>
</td>
</tr>
</tbody>
</table>


+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

<table>
<thead>
<tr>
<th><strong>콘텐츠 변형 시뮬레이션 — 업데이트된 경험 및 AI 변형 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>콘텐츠 시뮬레이션</strong> 워크플로에서 다음과 같은 두 가지 업데이트를 사용할 수 있습니다.</p>
<ul>
<li><strong>새 기본 경로</strong> — <strong>콘텐츠 시뮬레이션</strong>을 클릭하면 기본적으로 <strong>콘텐츠 변형 시뮬레이션</strong> 경험이 열립니다. 단일 화면에서 샘플 입력을 수동으로 또는 CSV/JSON 파일에서 추가하고, 시뮬레이션된 사용자를 재사용하고, 렌더링을 미리 보고, 교정본을 보낼 수 있습니다. Adobe Experience Platform 테스트 프로필로 미리 보기, 테스트 프로필 데이터와 함께 교정본 전송, 이메일 받은 편지함 렌더링 및 스팸 보고서 확인을 하려면 <strong>콘텐츠 시뮬레이션</strong>을 클릭한 후 드롭다운에서 <strong>콘텐츠 시뮬레이션(AEP 프로필)</strong>을 선택합니다.</li>
<li><strong>AI 생성 콘텐츠 변형</strong> — <strong>콘텐츠 변형 시뮬레이션</strong> 경험에서 <strong>생성</strong>을 클릭하고 AI를 사용하여 콘텐츠 변형을 자동으로 만듭니다. 시스템이 메시지를 분석하고 개인화 필드와 조건 분기를 감지하여 실제 값을 채워 넣으면 모든 변형을 수동으로 만들지 않고도 렌더링의 유효성을 검사할 수 있습니다.</li>
</ul>
<p>자세한 내용은 <a href="../test-approve/simulate-sample-input.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 말</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer의 Adobe Experience Manager 콘텐츠 조각 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 Journey Optimizer 작성 워크플로 내에서 <strong>Adobe Experience Manager 콘텐츠 조각</strong>을 더욱 유용하고 관리하기 쉬우며 프로덕션 환경에 바로 적용할 수 있도록 여러 개선 사항이 적용됩니다.</p>
<ul>
<li>Journey Optimizer는 이제 작성, 게시 및 인증된 게시 계층을 포함한 여러 Adobe Experience Manager 구성에서 콘텐츠 조각을 가져오는 것을 지원합니다.</li>
<li>조각을 선택하면 해당 컨텍스트가 메시지 전체에 유지되므로 작성자는 다시 선택하지 않고도 콘텐츠 블록 간에 조각 필드를 재사용할 수 있습니다.</li>
<li>Journey Optimizer에 콘텐츠 조각 목록 페이지가 새롭게 추가되어 수명주기 관리가 향상되었습니다. 사용자는 동기화되지 않은 조각을 식별하고 수동으로 동기화하여 최신 상태를 유지할 수 있습니다.</li>
<li>마케터는 이제 로케일 및 변형 지원을 통해 동일한 콘텐츠 조각의 다른 버전을 더욱 신중하게 활용할 수 있습니다.</li>
<li>이제 Adobe Journey Optimizer에서 Adobe Experience Manager 콘텐츠에 액세스하는 방식을 유연하게 설정할 수 있습니다. 이번 릴리스에서는 여정과 캠페인에 사용되는 콘텐츠 조각의 <strong>소스 저장소를 전환</strong>할 수 있는 기능이 추가되었습니다.</li>
<li>이제 <b>Managed Services</b>와 호환되므로 Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 직접 보고 액세스하고 사용하여 개인화할 수 있습니다. 구성 설정에서 Adobe Experience Manager Managed Services 저장소 URL을 한 번만 추가하면 됩니다.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Asset Essentials와 AI 어시스턴트 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 AI 어시스턴트가 이메일, 웹 페이지 및 푸시 알림을 생성할 때 <b>브랜드 승인 이미지</b>를 Adobe Experience Manager Assets에서 자동으로 가져옵니다. 이렇게 하면 Assets을 수동으로 검색하거나 일반적인 AI 대체 기능을 사용할 필요가 없어 모든 시각적 요소가 완벽하게 정확하고 브랜드 규정을 준수할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>콘텐츠 생성을 위한 AI 어시스턴트 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 더욱 강력한 이미지 편집, 더욱 안정적인 브랜드 추출, 이미지 흐름에서의 콘텐츠 진위성 지원을 통해 <strong>AI 어시스턴트</strong> 콘텐츠 생성 환경이 개선되었습니다.</p>
<ul>
<li><strong>AI 이미지 편집</strong> 기능이 이제 이미지 생성 흐름에서 사용 가능하며, Firefly 타사 모델 지원도 포함되어 있어 어시스턴트를 종료하지 않고도 소스 이미지를 다듬을 수 있습니다.</li>
<li><strong>브랜드 신호 추출</strong> 기능은 더욱 높은 품질의 결과를 제공합니다. 선택한 페이지에 충분한 신호가 없는 경우, 개선된 대체 기능을 통해 색상, 타이포그래피, 글쓰기 가이드라인 및 기타 브랜드 속성이 자동으로 채워집니다.</li>
<li><strong>웹 기반 브랜드 추출</strong>이 더욱 안정적으로 개선되었습니다. 개선된 시간 초과 처리 기능을 통해 느린 페이지, 팝업 및 쿠키 배너로 인해 추출이 차단되는 것을 방지할 수 있습니다.</li>
<li><strong>콘텐츠 진위 확인(CAI)</strong> 기능이 이제 이미지 흐름에서 지원됩니다. 또한 이번 릴리스에서는 참조 이미지 업로드 문제를 수정하고 기존 C2PA 매니페스트가 없는 이미지 처리를 개선했습니다.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++


### 이메일 채널 {#june-26-email}

이 릴리스의 이메일 채널에 다음과 같은 개선 사항이 추가되었습니다.

* **URL 매개변수 암호화** - 이제 이메일 메시지에 추가하는 추적 및 랜딩 페이지 링크의 URL 매개변수를 암호화할 수 있습니다. 이를 통해 중요한 매개변수 데이터에 대한 추가 보안 계층을 제공합니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). [자세히 보기](../personalization/url-parameter-encryption.md)

  사용 가능한 날짜: 2026년 6월 1일

* **키 레지스트리에 대한 새 권한** - 이제 URL 매개변수 암호화에 필요한 키에 액세스하고 관리하는 데 두 가지 새로운 권한이 필요합니다. **키 레지스트리 관리** 및 **키 레지스트리 보기**&#x200B;입니다. [자세히 보기](../administration/high-low-permissions.md#administration-permissions)

  사용 가능한 날짜: 2026년 6월 1일

<table>
<thead>
<tr>
<th><strong>이메일 크기 축소 활성화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에는 이제 이메일 렌더링 방식에 영향을 주지 않고 불필요한 공백, 주석 및 중복 코드를 제거하여 이메일의 HTML 크기를 줄이는 옵션이 포함되어 있습니다.</p>
<p>이 옵션을 사용하면 일부 이메일 제공업체에서 메시지를 플래그 지정하거나 거부하는 데 사용하는 크기 임계값을 피하여 전달률을 높이고 수신자의 로드 시간을 단축할 수 있습니다.</p>
<p><img src="assets/do-not-localize/email-size-optimization.gif"></p>
<p>자세한 내용은 <a href="../email/create-email.md#optimize-html-size">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 26일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>조각의 편집 가능한 필드에 서식 있는 텍스트 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 콘텐츠에 사용되는 사용자 정의 가능한 조각에 서식 있는 텍스트를 추가할 수 있습니다.</p>
<p>예를 들어 이메일 디자이너에서 텍스트 구성 요소를 편집 가능한 필드로 사용하는 경우 콘텐츠 서식(예: 굵게 및 기울임꼴)을 직접 지정하고 하이퍼링크를 삽입할 수 있습니다.</p>
<p><img src="assets/do-not-localize/rich-text-editable-fields.gif"></p>
<p>자세한 내용은 <a href="../content-management/customizable-fragments.md#rich-text-visual">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 19일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 디자이너에서 콘텐츠 확인</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer는 이제 이메일 디자이너에 직접 자동화된 기술 유효성 검사 기능을 포함하여 전송 전에 HTML 및 CSS 문제를 감지할 수 있도록 지원합니다.</p>
<p>검사에는 <code>&lt;script&gt;</code> 및 <code>&lt;base&gt;</code> 태그와 같은 지원되지 않는 요소, Microsoft Outlook에서 레이아웃을 깨뜨릴 수 있는 빈 div, HTML Meta 새로 고침 태그, Gmail에서 렌더링 오류를 유발하는 CSS 또는 HTML 크기 임계값 등이 포함됩니다.</p>
<p>검사 결과는 작성 패널에 오류, 경고 또는 정보 알림으로 표시되며, 상황별 세부 정보와 가능한 경우 원클릭 수정 기능이 제공되므로 편집기를 종료하지 않고도 문제를 해결할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>자세한 내용은 <a href="../email/content-check.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 18일</p>
</td>
</tr>
</tbody>
</table>

* **향상된 이미지-HTML 변환기** - 이미지-HTML 변환기 기능의 새 버전이 출시되어 HTML 생성 정확도가 향상되었습니다. 이번 업데이트는 상위 계층 LLM 모델을 활용하여 이미지 입력에서 더욱 정확하고 안정적인 HTML 출력을 제공합니다.

  사용 가능한 날짜: 2026년 6월 18일

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

<table>
<thead>
<tr>
<th><strong>이메일 디자이너의 모듈</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 디자이너에 헤더, 제품 카드, 정보 블록, 바닥글과 같은 바로 사용할 수 있는 레이아웃 모듈 라이브러리가 포함되어 있어 이메일 캔버스에 직접 끌어다 놓을 수 있습니다.</p>
<p>각 모듈은 편집 가능한 속성(이미지, 제목, 텍스트, 버튼, 링크)으로 사전 구성되어 있으며 WYSIWYG 인터페이스를 통해 완벽하게 사용자 정의할 수 있으므로 처음부터 구조를 만들 필요 없이 이메일 작성 속도를 높일 수 있습니다.</p>
<p>사용 가능한 날짜: 2026년 6월 말</p>
</td>
</tr>
</tbody>
</table>

+++

### 콘텐츠 및 통합 {#june-26-integration}

이번 릴리스에서는 콘텐츠 관리 및 통합 기능에 다음과 같은 기능과 개선 사항이 추가될 예정입니다.

<table>
<thead>
<tr>
<th><strong>Journey Optimizer의 Adobe Experience Manager 콘텐츠 조각 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 Journey Optimizer 작성 워크플로 내에서 <strong>Adobe Experience Manager 콘텐츠 조각</strong>을 더욱 유용하고 관리하기 쉬우며 프로덕션 환경에 바로 적용할 수 있도록 여러 개선 사항이 적용됩니다.</p>
<ul>
<li>Journey Optimizer는 이제 작성, 게시 및 인증된 게시 계층을 포함한 여러 Adobe Experience Manager 구성에서 콘텐츠 조각을 가져오는 것을 지원합니다.</li>
<li>조각을 선택하면 해당 컨텍스트가 메시지 전체에 유지되므로 작성자는 다시 선택하지 않고도 콘텐츠 블록 간에 조각 필드를 재사용할 수 있습니다.</li>
<li>Journey Optimizer에 콘텐츠 조각 목록 페이지가 새롭게 추가되어 수명주기 관리가 향상되었습니다. 사용자는 동기화되지 않은 조각을 식별하고 수동으로 동기화하여 최신 상태를 유지할 수 있습니다.</li>
<li>마케터는 이제 로케일 및 변형 지원을 통해 동일한 콘텐츠 조각의 다른 버전을 더욱 신중하게 활용할 수 있습니다.</li>
<li>이제 Adobe Journey Optimizer에서 Adobe Experience Manager 콘텐츠에 액세스하는 방식을 유연하게 설정할 수 있습니다. 이번 릴리스에서는 여정과 캠페인에 사용되는 콘텐츠 조각의 <strong>소스 저장소를 전환</strong>할 수 있는 기능이 추가되었습니다.</li>
<li>이제 <b>Managed Services</b>와 호환되므로 Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 직접 보고 액세스하고 사용하여 개인화할 수 있습니다. 구성 설정에서 Adobe Experience Manager Managed Services 저장소 URL을 한 번만 추가하면 됩니다.</li>
</ul>
<p>자세한 내용은 <a href="../integrations/aem-fragments-gs.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 6월 18일</p>
</td>
</tr>
</tbody>
</table>

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Asset Essentials와 AI 어시스턴트 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 AI 어시스턴트가 이메일, 웹 페이지 및 푸시 알림을 생성할 때 <b>브랜드 승인 이미지</b>를 Adobe Experience Manager Assets에서 자동으로 가져옵니다. 이렇게 하면 Assets을 수동으로 검색하거나 일반적인 AI 대체 기능을 사용할 필요가 없어 모든 시각적 요소가 완벽하게 정확하고 브랜드 규정을 준수할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>콘텐츠 생성을 위한 AI 어시스턴트 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 더욱 강력한 이미지 편집, 더욱 안정적인 브랜드 추출, 이미지 흐름에서의 콘텐츠 진위성 지원을 통해 <strong>AI 어시스턴트</strong> 콘텐츠 생성 환경이 개선되었습니다.</p>
<ul>
<li><strong>AI 이미지 편집</strong> 기능이 이제 이미지 생성 흐름에서 사용 가능하며, Firefly 타사 모델 지원도 포함되어 있어 어시스턴트를 종료하지 않고도 소스 이미지를 다듬을 수 있습니다.</li>
<li><strong>브랜드 신호 추출</strong> 기능은 더욱 높은 품질의 결과를 제공합니다. 선택한 페이지에 충분한 신호가 없는 경우, 개선된 대체 기능을 통해 색상, 타이포그래피, 글쓰기 가이드라인 및 기타 브랜드 속성이 자동으로 채워집니다.</li>
<li><strong>웹 기반 브랜드 추출</strong>이 더욱 안정적으로 개선되었습니다. 개선된 시간 초과 처리 기능을 통해 느린 페이지, 팝업 및 쿠키 배너로 인해 추출이 차단되는 것을 방지할 수 있습니다.</li>
<li><strong>콘텐츠 진위 확인(CAI)</strong> 기능이 이제 이미지 흐름에서 지원됩니다. 또한 이번 릴리스에서는 참조 이미지 업로드 문제를 수정하고 기존 C2PA 매니페스트가 없는 이미지 처리를 개선했습니다.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### 보고 {#june-26-reporting}

이 릴리스의 보고에 다음과 같은 개선 사항이 추가되었습니다.

* **이메일 보고를 위한 새로운 예상 클릭 메트릭** - 실제 고객 참여를 보다 정확하게 볼 수 있도록 여정, 캠페인 및 채널 보고서에서 새로운 예상 메트릭을 사용할 수 있습니다.

   * **예상 CTR**(클릭스루 비율): 배달된 총 메시지 수에 상대적인 예상 클릭수로 계산됩니다.

   * **예상 CTOR**(Click-to-Open 비율): 총 예상 열람 수에 상대적인 예상 클릭수로 계산됩니다.

  사용 가능한 날짜: 2026년 6월 25일

### 관리 {#june-26-administration}

이 릴리스의 관리 및 데이터 관리에 다음과 같은 개선 사항이 추가되었습니다.

* [!BADGE 중요]{type=Informative} **AJO 메시지 피드백 이벤트 데이터 세트가 배치 수집으로 전환** - **AJO 메시지 피드백 이벤트 데이터 세트**&#x200B;가 스트리밍 수집에서 배치 수집으로 전환됩니다. 따라서 이 데이터 세트의 데이터 지연 시간이 최대 2시간까지 발생할 수 있습니다. Customer Journey Analytics에서 이 데이터 세트를 사용하여 보고서를 작성했거나 쿼리를 실행한 경우, 향후 지연 시간 증가를 고려해야 합니다. [자세히 보기](../data/datasets-query-examples.md#message-feedback-event-dataset)

  사용 가능한 날짜: 2026년 6월 10일

* **캠페인 라이프사이클 이벤트에 대한 고객 알림** - 이제 새로운 시스템 알림이 액션 및 API 트리거 캠페인에 대한 주요 라이프사이클 이벤트를 알려줍니다. 샌드박스 수준에서 구독할 수 있습니다. [자세히 보기](../reports/alerts.md)

  사용 가능한 날짜: 2026년 6월 1일


+++ 출시 예정 — **아래 정보는 변경될 수 있습니다**

* **웹 애플리케이션 방화벽(WAF) IP 화이트리스트** - Adobe Journey Optimizer는 이제 랜딩 페이지에 대한 웹 애플리케이션 방화벽(WAF) IP 화이트리스트를 지원하여 조직에서 모든 수신 요청이 구성된 WAF 인프라를 통해서만 라우팅되도록 할 수 있습니다. 고객은 이 개선 사항을 통해 WAF 계층을 우회하는 모든 직접 요청을 거부하도록 Journey Optimizer를 구성하여 Imperva와 같은 도구에 정의된 보안 정책을 일관되게 적용할 수 있습니다. 이 기능은 엄격한 네트워크 액세스 요구 사항이 있는 기업의 보안 태세를 강화하고 AJO에서 호스팅하는 랜딩 페이지로의 트래픽 흐름을 완벽하게 제어할 수 있도록 합니다.

  사용 가능한 날짜: 2026년 6월 말

+++


### 모바일 메시징(SMS, MMS, RCS 및 LINE) {#june-26-mobile}

이번 릴리스에서는 모바일 메시징에 다음과 같은 개선 사항이 적용됩니다.

* **SMS 보고서용 고유 클릭 수** - SMS 보고서에 새로운 **고유 클릭 수** 모듈이 추가되어 이메일 보고서에서 제공되는 것과 동일한 수준의 세부적인 성과 추적 기능을 SMS에도 제공합니다.

* **SMS - 사용량 지표 표시** - Adobe Journey Optimizer를 통해 SMS를 직접 구매하는 고객을 위해 새로운 **SMS 사용량 대시보드**&#x200B;가 추가되었습니다. 이제 모바일 발신(MO) 및 모바일 수신(MT) 메시지로 분류된 지난 90일간의 메시지 전송 지표를 확인하고 추적할 수 있습니다. 이 데이터는 CSV 파일로 다운로드할 수도 있으므로, SMS 비용을 더욱 효과적으로 관리하고 제어할 수 있습니다. [자세히 알아보기](../mobile/sms-usage-report.md)

* **SMS 보고서의 예상 클릭 수** - 이제 새로운 예상 클릭 수 지표를 여정, 캠페인 및 전자 메일 및 SMS의 채널 보고서에서 사용할 수 있습니다. 이 지표는 봇 및 비인간 상호 작용(NHI) 트래픽을 제외하여 실제 고객 참여를 더욱 명확하게 보여줍니다. 기존 클릭 수 지표는 계속 사용할 수 있으며 총 클릭 수를 보고합니다.

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

* **LINE 채널 - 작성 기능 변경** - LINE 채널 UI가 고급 메시지 작성 기능으로 업그레이드되었습니다. 이번 릴리스에서는 텍스트, 이미지, 이미지맵, 슬라이드, Flex(JSON 편집기)를 포함한 **다양한 메시지 형식**&#x200B;을 지원하며 실시간 디바이스 미리 보기 기능도 제공합니다. 이제 사용자는 최대 5개의 메시지로 구성된 그룹 메시지를 관리하고(추가, 제거 및 순서 변경 기능 포함) 통합된 개인화 편집기를 활용하여 검증된 동적 메시지를 보낼 수 있습니다.

+++

### 사용성 개선 사항 {#june-26-usability}

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다.**

* **여정 및 캠페인용 폴더** - 이제 여정과 캠페인을 **폴더**&#x200B;로 구성하여 인터페이스에서 탐색과 관리를 개선할 수 있습니다.

+++

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
