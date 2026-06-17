---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 46a540ec28ee184b3cb475f64c26d68f6c06d898
workflow-type: tm+mt
source-wordcount: 1822
ht-degree: 9%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer은 새로운 기능, 기존 기능 개선 사항 및 버그 수정 사항을 지속적으로 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 6월 프리릴리스 정보 {#june-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 제공되지만, 일부는 나중에 배포될 수 있습니다. 자세한 내용은 각 항목에 명시된 제공 예정일을 참조하세요.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 6월 16~17일

### 여정 {#june-26-journeys}

이 릴리스의 여정은 다음과 같은 기능 및 개선 사항을 제공합니다.

* **실시간 여정 제한 및 새 보호 기능 증가** - 이제 최대 **200개의 활성 여정을 사용할 수 있습니다**. 이전 제한인 100개에서 증가했습니다.

* **여정 헤더의 시작 및 종료 날짜** - 시작 및/또는 종료 날짜가 라이브 여정에 구성되면 이제 라이브 상태 배지 옆의 **여정 헤더**&#x200B;에 표시됩니다. 표시된 레이블은 각 날짜가 예정된 날짜인지 또는 이미 지난 날짜인지에 따라 조정됩니다.

* **일시 중지된 여정을 직접 중지하거나 닫을 수 있습니다** - 이제 **일시 중지됨** 상태에서 **여정을 중지하거나 새 출구로 닫을 수 있습니다**. 이전에는 일시 중지된 여정을 중단하거나 닫으려면 먼저 라이브로 다시 시작해야 했습니다.

### 오케스트레이션된 캠페인 {#june-26-oc}

이 릴리스의 오케스트레이션된 캠페인에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<!--
<table>
<thead>
<tr>
<th><strong>File-based targeting in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrated campaigns now support loading a <strong>CSV or TXT file</strong> directly into the campaign canvas as the targeting audience, without first ingesting the file into Adobe Experience Platform. The file data is consumed at execution time and is not persisted as an Adobe Experience Platform dataset. During file setup, you can define column mappings, data types, NULL handling, and per-column error policies. Rows that fail validation are rejected and logged before the campaign runs, keeping the audience clean without manual pre-processing. This is particularly suited for ad-hoc sends or partner list campaigns where building a full ingestion pipeline is not practical.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

* **오케스트레이션된 캠페인의 관계형 데이터에 대한 루프 기반 개인화** - 이제 개인화 편집기는 주문, 계정 또는 예약과 같은 관계형 컬렉션을 반복하고 단일 전자 메일 또는 SMS 내에서 레코드당 하나의 콘텐츠 블록을 렌더링하는 **루프 블록**&#x200B;을 지원합니다. 컬렉션은 표현식 쓰기가 필요하지 않고 개인화 토큰을 사용하여 데이터 선택기를 통해 구성됩니다. 빈 컬렉션 처리를 포함하여 캠페인이 실행되기 전에 루프가 있는 블록이 샘플 데이터에 대해 렌더링되는 방식을 미리 볼 수 있습니다.

* **받는 사람 및 캠페인별 전자 메일 보낸 사람 세부 정보 개인화** - 이제 오케스트레이션된 캠페인이 프로필 특성 또는 관계 데이터를 사용하여 보낸 사람 이름, 보낸 사람 주소 및 회신 주소를 포함한 **전자 메일 머리글 필드**&#x200B;의 개인화를 지원합니다. 이를 통해 보낸 사람의 세부 정보가 하나의 회사 주소를 통해 모든 전송을 라우팅하는 대신 각 받는 사람에 대한 관련 조언자, 위치 또는 분기를 반영할 수 있습니다. 헤더 값은 채널 수준에서 설정할 수 있으며 보다 정밀한 제어를 위해 컨텍스트 데이터를 사용하여 캠페인별로 재정의할 수 있습니다.

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

### 결정 {#june-26-decisioning}

이 릴리스에서는 다음 기능이 의사 결정 기능으로 제공됩니다.

<table>
<thead>
<tr>
<th><strong>Decisioning에서 Adobe Experience Manager 콘텐츠 조각 활용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Decisioning의 <strong>결정 항목</strong>에 <strong>Adobe Experience Manager 콘텐츠 조각</strong>을(를) 매핑하고 결정 정책 내에서 활용하여 적절한 시기에 적절한 고객에게 적절한 조각을 전달할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
</td>
</tr>
</tbody>
</table>

* **동적 항목 특성** - 이제 프로필, 컨텍스트 및 대상 데이터를 사용하여 게재 시 의사 결정 항목 사용자 지정 특성을 개인화할 수 있습니다. 이를 통해 사소한 콘텐츠 변형에 대해 중복 오퍼를 유지할 필요가 없으므로 마케터는 보다 적고 유연한 결정 항목을 관리할 수 있습니다.

### 이메일 {#june-26-email}

이 릴리스의 이메일 채널에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<table>
<thead>
<tr>
<th><strong>이메일 Designer의 콘텐츠 품질 검사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에는 이메일 Designer에 직접 자동화된 기술 유효성 검사가 포함되어 있으므로 보내기 전에 HTML 및 CSS 문제를 catch할 수 있습니다.</p>
<p>이 검사에서는 <code>&lt;script&gt;</code> 및 <code>&lt;base&gt;</code> 태그, Microsoft Outlook의 레이아웃을 나눌 수 있는 빈 div, HTML 메타 새로 고침 태그, Gmail에서 렌더링 오류를 트리거하는 CSS 또는 HTML 크기 임계값과 같은 지원되지 않는 요소를 다룹니다.</p>
<p>결과는 상황별 세부 정보와 원클릭 수정 사항(사용 가능한 경우)으로 작성 패널에 직접 오류, 경고 또는 정보 알림으로 표시되므로 편집기를 종료하지 않고도 문제를 해결할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 크기 감소 활성화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에는 이메일 렌더링 방식에 영향을 주지 않고 불필요한 공백, 댓글 및 중복 코드를 제거하여 이메일 HTML의 크기를 줄이는 옵션이 포함됩니다.</p>
<p>이렇게 하면 일부 이메일 공급자가 메시지를 플래그 지정하거나 거부하는 데 사용하는 크기 임계값을 방지하여 게재 능력을 향상시킬 수 있으며, 수신자의 로드 시간을 줄일 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>조각에 대해 편집 가능한 필드의 리치 텍스트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 콘텐츠에 사용되는 사용자 지정 가능한 조각에 서식 있는 텍스트를 추가할 수 있습니다.</p>
<p>예를 들어 텍스트 구성 요소를 이메일 Designer에서 편집 가능한 필드로 사용하는 경우 콘텐츠의 형식(예: 굵은 글꼴 및 기울임꼴)을 직접 지정하고 하이퍼링크를 삽입할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

* **HTML으로 향상된 이미지 변환기** - 이제 HTML으로 이미지 변환기 기능의 새 버전을 사용할 수 있으므로 HTML 생성의 정확도가 향상되었습니다. 이 업데이트는 상위 계층의 LLM 모델을 활용하여 이미지 입력에서 보다 정확하고 안정적인 HTML 출력을 제공합니다.

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다**

<table>
<thead>
<tr>
<th><strong>이메일 Designer의 모듈</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 Designer에 머리글, 제품 카드, 정보 블록 및 바닥글과 같이 이메일 캔버스로 바로 드래그하여 놓을 수 있는 즉시 사용 가능한 레이아웃 모듈 라이브러리가 포함됩니다.</p>
<p>각 모듈은 편집 가능한 속성(이미지, 제목, 텍스트, 버튼, 링크)으로 사전 구성되어 있으며 WYSIWYG 인터페이스를 통해 완전히 맞춤화할 수 있으므로 처음부터 구조를 빌드하지 않고도 이메일 작성 시간을 단축할 수 있습니다.</p>
<p>사용 가능한 날짜: 2026년 6월 22일</p>
</td>
</tr>
</tbody>
</table>

+++

### 모바일 메시징(SMS, MMS, RCS 및 LINE) {#june-26-mobile}

이 릴리스의 모바일 메시징에는 다음과 같은 개선 사항이 적용되었습니다.

* **SMS 보고서에 대한 고유 클릭 수** - 새로운 **고유 클릭 수** 모듈이 SMS 보고서에 도입되어 현재 이메일 보고서에 사용할 수 있는 SMS에 동일한 수준의 세분화된 성능 추적을 제공합니다.

* **LINE 채널 - 변경 내용 작성** - LINE 채널 UI가 고급 메시지 작성 기능으로 업그레이드되었습니다. 이 릴리스에서는 실시간 장치 미리 보기와 함께 텍스트, 이미지, 이미지 맵, 회전판 및 Flex(JSON 편집기)를 비롯한 **여러 메시지 형식**&#x200B;을 지원합니다. 이제 사용자는 최대 5개의 순서가 지정된 메시지로 구성된 그룹화된 메시지를 관리하고(추가, 제거 및 순서 조정 컨트롤 포함), 검증된 다이내믹 메시징을 위해 통합 개인화 편집기를 활용할 수 있습니다.

* **SMS - 사용 지표 표시** - Adobe Journey Optimizer을 통해 SMS를 직접 구매하는 고객의 경우 새 **SMS 사용 대시보드**&#x200B;가 도입되었습니다. 이제 MO(Mobile Originated) 및 MT(Mobile Terminated) 메시지로 분류된 최근 90일 간의 메시지 전송 지표를 보고 추적할 수 있습니다. 이 데이터는 CSV를 통해서도 다운로드할 수 있으므로 SMS 소비에 대한 가시성과 제어 능력이 향상됩니다.

### 콘텐츠 및 통합 {#june-26-content}

이 릴리스의 콘텐츠 관리 및 통합에 대해 다음과 같은 기능 및 개선 사항이 적용되었습니다.

<table>
<thead>
<tr>
<th><strong>Journey Optimizer의 Adobe Experience Manager 콘텐츠 조각 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 Adobe Experience Manager 작성 워크플로 내에서 <strong>Journey Optimizer 콘텐츠 조각</strong>을(를) 더 사용 가능하고, 더 관리 가능하며, 더 프로덕션 환경에서 사용할 수 있도록 하는 몇 가지 개선 사항이 제공됩니다.</p>
<ul>
<li>Journey Optimizer은 이제 작성자, 게시 및 인증된 게시 계층을 포함하여 여러 Adobe Experience Manager 구성에서 콘텐츠 조각 가져오기를 지원합니다.</li>
<li>조각을 선택하면 해당 컨텍스트가 메시지 전체에 유지되므로 작성자가 다시 선택하지 않고도 콘텐츠 블록 간 조각 필드를 재사용할 수 있습니다.</li>
<li>라이프사이클 관리를 개선하기 위해 새로운 전용 콘텐츠 조각 목록 페이지가 Journey Optimizer에 도입되었습니다. 사용자는 동기화 중단 조각을 식별하고 수동 동기화를 트리거하여 최신 상태를 유지할 수 있습니다.</li>
<li>이제 로케일 및 변형 지원을 통해 마케터는 보다 의도적으로 동일한 콘텐츠 조각의 대체 버전을 사용하여 작업할 수 있습니다.</li>
<li>이제 Adobe Journey Optimizer에서 Adobe Experience Manager 콘텐츠에 액세스하는 방법을 유연하게 사용할 수 있습니다. 이 릴리스에서는 여정 및 캠페인에 사용된 콘텐츠 조각에 대해 <strong>소스 리포지토리를 전환</strong>하는 기능을 도입했습니다.</li>
<li>이제 <b>Managed Services</b>과(와) 호환되므로 개인화를 위해 Journey Optimizer에서 직접 Adobe Experience Manager 콘텐츠 조각을 보고 액세스하고 사용할 수 있습니다. 구성 설정에 Adobe Experience Manager Managed Services 저장소 URL을 1회 설정으로 추가하기만 하면 됩니다.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Asset Essentials와 AI Assistant 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일, 웹 페이지 및 푸시 알림을 생성할 때 AI 도우미가 Adobe Experience Manager Assets에서 직접 <b>브랜드 승인 이미지</b>를 자동으로 가져옵니다. 이렇게 하면 Assets을 수동으로 검색하거나 일반 AI 폴백에 의존할 필요가 없어 모든 시각적 요소가 완벽하게 정확하고 브랜드 규정을 준수하도록 할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>콘텐츠 생성 향상을 위한 AI Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이 릴리스는 이미지 흐름에서 강력한 이미지 편집, 보다 안정적인 브랜드 추출 및 콘텐츠 신뢰성 지원을 통해 <strong>AI Assistant</strong> 콘텐츠 생성 경험을 개선합니다.</p>
<ul>
<li><strong>AI 이미지 편집</strong>을(를) 이제 Firefly 타사 모델 지원을 포함한 이미지 생성 흐름에서 사용할 수 있으므로 도우미를 종료하지 않고도 소스 이미지를 개선할 수 있습니다.</li>
<li><strong>브랜드 신호 추출</strong>은(는) 더 높은 품질의 결과를 제공합니다. 선택한 페이지에 충분한 신호가 없으면 향상된 폴백이 색상, 타이포그래피, 작성 지침 및 기타 브랜드 속성을 채웁니다.</li>
<li><strong>웹 기반 브랜드 추출</strong>이 더 안정적입니다. 향상된 시간 제한 처리는 느린 페이지, 팝업 및 쿠키 배너가 추출을 차단하는 것을 방지하는 데 도움이 됩니다.</li>
<li><strong>CAI(콘텐츠 정품 인증)</strong>이(가) 이제 이미지 흐름에서 지원됩니다. 또한 이 릴리스에서는 참조 이미지 업로드 문제를 수정하고 기존 C2PA 매니페스트가 없는 이미지에 대한 처리를 개선합니다.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### 보고 {#june-26-reporting}

이번 릴리스에서는 다음과 같은 개선 사항이 보고되었습니다.

* **이메일 및 SMS 보고에 대한 예상 클릭 수** — 이제 새로운 **예상 클릭 수** 지표를 여정, 캠페인 및 채널 보고서에서 이메일 및 SMS에 대한 사용 가능합니다. 이 지표는 식별된 봇 및 비사람 상호 작용(NHI) 트래픽을 제외하여 실제 고객 참여를 보다 명확하게 파악할 수 있도록 합니다. 기존 클릭 수 지표는 계속 사용할 수 있으며 총 클릭 수를 계속 보고합니다.

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다**

* **이메일 및 SMS 보고에 대한 새로운 예상 클릭 메트릭** - 실제 고객 참여를 보다 정확하게 볼 수 있도록 여정, 캠페인 및 채널 보고서에서 새로운 예상 메트릭을 사용할 수 있습니다. 이러한 지표는 보고 데이터에서 비인적 상호 작용(NHI) 및 보트 클릭을 필터링하는 데 도움이 됩니다.

   * 예상 CTR: 총 게재와 관련된 예상 클릭 수입니다.
   * 이메일에 대한 예상 CTOR 전용: 예상 열람에 대한 예상 클릭수.

  사용 가능한 날짜: 2026년 6월 말

+++

### 구성 {#june-26-configuration}

이 릴리스의 구성 및 관리에는 다음과 같은 개선 사항이 적용됩니다.

* **스트리밍에서 일괄 처리 모드로 데이터 세트 이동** - AJO 메시지 피드백 이벤트 데이터 세트가 스트리밍에서 **일괄 처리 수집 모드**(으)로 전환됩니다. 이 변경을 통해 데이터 수집이 스트리밍 수집 제한을 초과하는 것을 방지할 수 있습니다. Customer Journey Analytics 보고서에서 이 데이터 세트를 사용하거나 이에 대한 쿼리를 실행하는 경우 앞으로는 최대 2시간의 데이터 지연 증가가 예상됩니다.

+++ 곧 출시 예정 — **아래 정보는 변경될 수 있습니다**

* **웹 응용 프로그램 방화벽(WAF) IP 화이트리스트** - 이제 Adobe Journey Optimizer에서 랜딩 페이지에 대한 웹 응용 프로그램 방화벽(WAF) IP 화이트리스트를 지원하므로 조직에서 구성된 WAF 인프라를 통해서만 모든 수신 요청이 라우팅되도록 할 수 있습니다. 이 향상된 기능을 통해 고객은 WAF 계층을 무시하는 직접 요청을 거부하도록 Journey Optimizer을 구성할 수 있으므로 Imperva와 같은 도구에 정의된 보안 정책이 일관되게 적용됩니다. 이 기능은 엄격한 네트워크 액세스 요구 사항을 가진 기업의 보안 태세를 강화하여 AJO이 호스팅하는 랜딩 페이지로의 트래픽 흐름을 완벽하게 제어합니다.

  사용 가능한 날짜: 2026년 6월 말

+++

### 사용성 개선 {#june-26-usability}

이번 릴리스에서는 다음과 같은 사용 편의성 개선 사항이 적용되었습니다.

* **여정 및 캠페인용 폴더** - 이제 인터페이스 탐색 및 관리를 개선하기 위해 여정 및 캠페인을 **폴더**&#x200B;로 구성할 수 있습니다.
