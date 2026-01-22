---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3d9316e3a42696c4e944ec23b0300e56b07142c2
workflow-type: tm+mt
source-wordcount: '2342'
ht-degree: 21%

---

# 사전 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.


## 2026년 1월 프리릴리스 정보 {#jan-26-01-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 일자**: 2026년 1월 26일 화요일

### 새로운 기능 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>여정의 액션 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 단일 작업과 <strong>다중 작업 인바운드 작업 그룹</strong>을 모두 구성할 수 있는 새로운 일반 <strong>작업 활동</strong>을 지원하므로 여정 캔버스 내에서 간소화된 작업 구성을 사용할 수 있습니다. 특히 이 새로운 기능에는 다음과 같은 이점이 있습니다.</p>
<ul>
<li>여정 캔버스 내 기본 액션 구성 간소화.</li>
<li>다중 액션 인바운드 액션 그룹을 만들 수 있는 용량.</li>
<li>모든 기본 제공 채널 액션에 최적화를 더하는 기능.</li>
<li>모든 액션에 실험과 다국어 옵션을 모두 추가하는 기능.</li>
</ul>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 지정 작업 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 <strong>모니터링 대시보드</strong> 및 보강된 여정 단계 이벤트 데이터를 사용하여 사용자 지정 작업 끝점의 상태 및 성능에 대해 더 자세한 insight을 알아보세요. 성공한 호출, 오류, 처리량, 응답 시간 및 대기열 대기 시간을 추적하여 예외 항목이 발생하는 시기, 장소 및 이유를 신속하게 파악합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>방해 금지 시간/시간 기반 제외</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>자동 시간에서는 전자 메일, SMS, 푸시 및 WhatsApp 채널에 대해 <strong>시간 기반 제외</strong>를 정의할 수 있습니다. 특정 기간 동안 메시지가 전송되지 않도록 하여 고객 선호도 및 규정 준수 요구 사항을 준수할 수 있습니다. 정확한 제어를 위해 캠페인 또는 여정의 개별 작업에 할당할 수 있는 <strong>규칙 집합</strong>을 통해 방해 금지 시간을 적용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 고객이 방해 금지 모드가 완료될 때까지 캠페인 작업을 대기열에 추가할 수 있는 기능과 활성화된 방해 금지 모드 규칙을 미리 볼 수 있는 기능이 제공됩니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 DM 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에 캠페인으로 제한되었던 <strong>DM 채널</strong>을 이제 <strong>여정 캔버스</strong>에서 사용할 수 있으므로 DM을 여정에 통합할 수 있습니다. 이제 파일 추출 구성 및 시간 기반 빈도 설정을 지원하여 DM을 일괄 처리 및 1:1 여정 시나리오 모두에서 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">제품 JIRA 작업에 연결</a></p>
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
<p>Adobe Journey Optimizer은 이제 <strong>웹 푸시 알림</strong>을 지원하므로 푸시 채널을 모바일 이상으로 확장합니다. 모바일 브라우저와 데스크탑 브라우저 모두에 알림을 원활하게 전달할 수 있으므로 앱을 사용하지 않고도 고객의 디바이스에서 직접 고객에게 연락할 수 있습니다. 이 향상된 기능을 통해 이미 모바일 푸시에서 사용 가능한 것과 동일한 작성 워크플로 및 타기팅 기능을 활용하여 사용자에게 적시에 개인화된 메시지를 실시간으로 보낼 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>푸시 및 SMS 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 푸시 및 SMS 여정 및 캠페인에 <strong>의사 결정 정책</strong>을 추가할 수 있습니다. 의사 결정 정책은 의사 결정 엔진을 활용하여 각 대상 구성원에 대해 제공할 최상의 콘텐츠를 동적으로 반환하는 오퍼에 대한 컨테이너입니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">제품 JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 DM 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에서 DM 채널을 사용할 수 있습니다. <strong>DM 활동</strong>을 사용하면 오케스트레이션된 캠페인 내에서 일회성 메시지와 반복 메시지 모두에 대해 DM을 쉽게 보낼 수 있습니다. DM 공급자가 요구하는 <strong>추출 파일</strong>을(를) 생성하는 프로세스를 자동화하는 역할을 합니다. 채널 활동을 오케스트레이션된 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새로운 충성도 앱 소스 커넥터</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Experience Platform에서 Talon.One, Capillary 및 Kobie 로열티 앱용 <strong>소스 커넥터</strong>를 사용할 수 있습니다. 이 커넥터를 사용하면 충성도 데이터를 Adobe Experience Platform으로 원활하게 스트리밍하고 Journey Optimizer에서 이 데이터를 활용할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">DOCAC JIRA 작업에 대한 링크</a></p>
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
<p>이제 보관 및 규정 준수를 위해 특정 데이터 세트로 <strong>보낸 게재를 내보내기</strong>할 수 있습니다. 이 용량은 이메일뿐만 아니라 SMS와 같은 다른 채널에도 사용할 수 있습니다. 이제 메시지 내보내기 데이터 세트의 데이터 보존이 <strong>7일</strong>입니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">제품 JIRA 작업에 연결</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새로운 액션 캠페인 검색용 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 <strong>Journey Optimizer API</strong>를 사용할 수 있으므로 세부 정보, 버전 및 구성과 같은 캠페인 관련 데이터를 프로그래밍 방식으로 검색하고 검사할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">세부 설명서</a>를 참조하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">제품 JIRA 작업에 연결</a></p>
<p>가용성 일자: 2025년 11월 24일 화요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새로운 여정 경고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 라이프사이클 이벤트 및 사용자 지정 작업 성능을 모니터링하고 추적하는 데 도움이 되는 새로운 <strong>여정 경고</strong>를 세 개 사용할 수 있습니다.</p>
<ul>
<li><strong>여정 게시됨</strong>: 여정 캔버스에서 실무자가 여정을 게시할 때 알림을 받습니다.</li>
<li><strong>여정 완료됨</strong>: 여정이 완료되면 알림을 받습니다. 여정 유형(대상자 읽기 또는 이벤트 트리거)에 따라 구체적인 정의가 표시됩니다.</li>
<li><strong>사용자 정의 액션 캡핑 트리거됨</strong>: 사용자 정의 액션 엔드포인트에서 캡핑이 활성화될 때 알림을 받습니다.</li>
</ul>
<p>이 경고는 조직 수준에서 또는 특정 여정에 대해 구독할 수 있습니다.</p>
<p>자세한 내용은 <a href="../reports/alerts.md#journey-alerts">세부 설명서</a>를 참조하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">DOCAC JIRA 작업에 대한 링크</a></p>
<p>가용성 일자: 2025년 11월 5일 목요일</p>
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
<p>이제 <strong>사전 승인된 테마</strong>를 빠르게 적용하여 모든 이메일에 브랜드 일관성을 보장하고, 캠페인 생성 프로세스를 가속화하고, 디자인 팀에 대한 의존도를 줄이면서 독자적으로 고품질 이메일을 생성할 수 있습니다.</p>
<p>이전에 Beta 버전으로 릴리스된 이 기능을 이제 일부 조직에서 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/themes.gif">
<p>자세한 내용은 <a href="../email/apply-email-themes.md">세부 설명서</a>를 참조하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">제품 JIRA 작업에 연결</a></p>
<p>가용성 일자: 2025년 11월 5일 목요일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-26-01-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### AI

* **AI 길잡이 콘텐츠 품질 검사** - 이제 브랜드 정렬 외에도 브랜드 지침과 관계없이 가독성, 응집성 및 효과성으로 잠재적인 문제를 발견하기 위해 전체 <strong>콘텐츠 품질</strong>을 평가할 수 있습니다. 이러한 자동화된 검사는 명확하지 않은 메시지, 일관되지 않은 말투 또는 구조적 차이를 식별하는 데 도움이 됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">제품 JIRA 작업에 연결</a>
* **새 색상 탭으로 브랜드 업데이트** - 브랜드 지침은 모든 접점에서 브랜드가 일관되게 표시되도록 하는 데 도움이 됩니다. 새 <strong>색상 섹션</strong>은 브랜드 색상 시스템에 대한 표준을 정의하며 여러 경험에서 색상을 선택, 구성 및 적용하는 방법에 대해 대략적으로 설명합니다. 기본, 보조, 악센트 및 중립 색상을 일관되게 사용하여 통합적이고, 액세스가 가능하고, 인식 가능한 브랜드 이미지를 지원합니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">제품 JIRA 작업에 연결</a>

#### 캠페인

* **프로필 시간대를 사용하여 캠페인 예약** - 이제 Campaign 예약에서 각 프로필의 <strong>시간대</strong>를 사용하여 원하는 현지 시간에 메시지를 배달할 수 있습니다.

  **참고**: 이 개선 사항은 조직 집합(제한된 가용성)에서만 사용할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">제품 JIRA 작업에 연결</a>

#### 채널

* **SMS Webhooks: 단계 II** - 제공할 설명.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">제품 JIRA 작업에 연결</a>

* **WhatsApp 재판매 오퍼** - 제공할 설명.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13669">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-86420">제품 JIRA 작업에 연결</a>

#### 이메일 디자이너

* **전자 메일 디자이너에서 바로 수정** - <strong>AI 기반 자동 콘텐츠 제안</strong>은(는) 콘텐츠 유효성 검사 중에 위반이 감지되면 전자 메일 Designer에서 사용할 수 있습니다. 콘텐츠가 브랜드 가이드라인과 잘못 일치하거나 품질 기준에 실패하는 것으로 플래그가 지정된 경우, 시스템은 사전에 검토 및 인라인 적용할 수 있는 수정된 대체 요소를 생성하여 준수 여부를 개선하고 생산 시간을 단축합니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">제품 JIRA 작업에 연결</a>

#### 경험 의사 결정

* **여정 중재** - 이제 <strong>공식 및 AI 모델</strong>을 사용하여 고객 프로필 특성 및 컨텍스트 요인에 따라 여정 우선 순위 점수를 자동으로 높여 고객이 가장 관련성이 높은 여정을 입력하도록 할 수 있습니다.

  **참고**: 이 개선 사항은 조직 집합(제한된 가용성)에서만 사용할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13976">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-78932">제품 JIRA 작업에 연결</a>

* **exd 샌드박스 도구 설명서 - 업데이트** - 제공할 설명.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13596">DOCAC JIRA 작업에 연결</a>

* **셀프 서비스 마이그레이션 도구 API** - 새로운 <strong>마이그레이션 도구 API</strong> 집합을 사용하여 오퍼 관리 엔터티를 Experience Decisioning으로 마이그레이션할 수 있습니다. 이 도구를 사용하면 종속성 해결 및 롤백 기능을 통해 샌드박스 간에 원활하게 마이그레이션할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">제품 JIRA 작업에 연결</a>

* **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서는 의사 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있는 의사 결정 항목에 <strong>조각</strong>을(를) 첨부할 수 있는 기능을 제공합니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이후에는 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">제품 JIRA 작업에 연결</a>

#### 여정

* **여정 사용자 지정 작업에서 오류 응답 페이로드를 활용합니다** - 이제 사용자 지정 작업에 대해 선택적 <strong>오류 응답 페이로드</strong>를 정의할 수 있습니다. 호출이 실패하면 오류 페이로드가 여정 컨텍스트에 노출되며, 보다 풍부한 대체 논리 및 디버깅을 지원하기 위해 시간 초과/오류 분기에서 사용할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">제품 JIRA 작업에 연결</a>

* **기본 및 Adobe Campaign 메시지 동작 결합** - 이제 Journey Optimizer을 사용하여 Adobe Campaign v7/v8 메시지 동작을 동일한 여정의 기본 채널 동작과 결합할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">제품 JIRA 작업에 연결</a>

* **여정의 여정 페이로드 크기 유효성 검사** - 이제 Journey Optimizer에서 최적의 성능과 시스템 안정성을 보장하기 위해 <strong>페이로드 크기 유효성 검사</strong>를 제공합니다. 여정을 작성하거나 게시할 때 페이로드 크기가 권장 한도에 근접하거나 초과하는 경우 명확한 경고 및 오류가 표시되고, 여정 구성을 최적화하는 실행 가능한 지침이 제공됩니다. 이 사전 유효성 검사는 잠재적 문제를 조기에 식별하고 여정 성능을 유지하는 데 도움이 됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">제품 JIRA 작업에 연결</a>

* **여정의 여러 인바운드 작업** - 이제 여정 오케스트레이션을 단순화하기 위해 단일 여정에서 <strong>여러 인바운드 작업</strong>을(를) 정의할 수 있습니다. 이전에 캠페인에서 사용할 수 있었던 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며 각 작업에는 특정 콘텐츠가 포함되어 있습니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이후에는 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">제품 JIRA 작업에 연결</a>

#### 오케스트레이션된 캠페인

* **특성 선택 및 배포 값 복사** - 이제 조정된 캠페인의 값 보기에서 직접 값을 선택하거나 복사할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">제품 JIRA 작업에 연결</a>

* **대상에 대한 데이터 사용 레이블 상속** - 이제 오케스트레이션된 캠페인에 대상을 저장할 때 Adobe Experience Platform에 적용된 <strong>데이터 사용 레이블</strong>이 자동으로 이전되므로 수동 DULE 태그 지정이 줄어듭니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">제품 JIRA 작업에 연결</a>

* **사전 정의된 리타겟팅 필터** - 오케스트레이션된 캠페인 사용 사례에 대해 더 쉬운 리타겟팅을 지원하기 위해 이 릴리스에서는 새로운 <strong>리타겟팅 필터</strong>을 도입했습니다. 이러한 필터를 사용하면 보냄, 열기만, 열림 또는 클릭됨, 열림 및 클릭됨 등의 메시지 참여를 기반으로 대상을 직접 타기팅하고 다시 타기팅할 특정 캠페인 또는 전환 중 캠페인을 선택할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">제품 JIRA 작업에 연결</a>

* **매개 변수가 있는 사전 정의된 필터** - 이제 재사용 가능한 편집 가능한 규칙에 대해 조정된 캠페인에서 <strong>매개 변수가 있는 필터</strong>를 만들 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">제품 JIRA 작업에 연결</a>

* **보내기 전 메시지 확인** - 이제 우발적 전송을 줄이기 위해 오케스트레이션된 캠페인을 보내기 전에 <strong>확인 단계</strong>이(가) 기본적으로 활성화됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">제품 JIRA 작업에 연결</a>

* **사용자 생성 메타데이터 지원** - 이제 오케스트레이션된 캠페인용 개인화 편집기에서 <strong>executionMetadata 도우미 함수</strong>를 사용할 수 있으므로 컨텍스트 정보를 기본 작업에 첨부하고 데이터 집합에 저장하여 외부 시스템으로 내보낼 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">제품 JIRA 작업에 연결</a>

* **다시 시작 단추** - 오케스트레이션된 캠페인에는 이제 <strong>다시 시작 단추</strong>가 포함되어 있으므로 필요할 때 실행을 빠르게 다시 시작한 후 캠페인을 게시할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">제품 JIRA 작업에 연결</a>

* **속도 제어 지원** - 이제 오케스트레이션된 캠페인이 <strong>속도 제어</strong>를 지원하므로 게재 속도를 높이고 볼륨 제한에 맞출 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">제품 JIRA 작업에 연결</a>

#### 권한

* **여정 및 캠페인에 대한 자체 승인 방지** - 이제 작성자가 자신의 여정 또는 캠페인을 승인할 수 없도록 요구하여 승인 워크플로의 <strong>직무 분리</strong>을 개선할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">제품 JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">제품 JIRA 작업에 연결</a>

## 곧 출시 예정 {#jan-26-01-coming-soon}

조만간 다음 기능 및 개선 업데이트가 릴리스될 예정입니다. **이 정보는 변경될 수 있습니다**. 업데이트된 링크, 화면, 설명서는 업데이트가 프로덕션에서 제공될 때 공유 예정입니다.

<table>
<thead>
<tr>
<th><strong>Journey Agent 내 콘텐츠 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform Agent Orchestrator에서 제공하는 <strong>Journey Agent</strong>은(는) Journey Optimizer에서 사용할 수 있으며 자연어 인터페이스를 통해 여정을 분석할 수 있도록 합니다. 이제 Journey Agent에서 직접 채널별 컨텐츠를 생성 및 관리하고, 이메일 및 푸시와 같은 채널용 컨텐츠를 작성하고, 템플릿을 적용하고 미리 보고, 프롬프트를 통해 색조와 스타일을 개선하고, 컨텍스트 내 편집을 위해 컨텐츠 Designer에서 컨텐츠를 열 수도 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">제품 JIRA 작업에 연결</a></p>
<p>가용성 일자: 2026년 2월 2일 화요일</p>
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
<p>이제 여정 캔버스에서 전용 콘텐츠 결정 활동을 통해 여정에 <strong>개인화된 오퍼</strong>를 포함하고 조건 및 사용자 지정 작업을 포함한 여정 활동에 사용할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">DOCAC JIRA 작업에 연결</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">제품 JIRA 작업에 연결</a></p>
<p>가용성 일자: 2026년 2월 2일 화요일</p>
</td>
</tr>
</tbody>
</table>
