---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f0f647467186e9a64994cc5ab44ea5d05193ab44
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 20%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적 제공 모델을 따르므로 Adobe에서 새로운 기능, 개선 사항, 버그 해결 업데이트를 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다.

이 모델로 인해 릴리스 노트는 월별 릴리스 사이에 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 2026년 1월 릴리스 정보 {#latest-rn}

**릴리스 날짜**: 2026년 1월 27~28일

[기능](#jan-26-01-features) 및 [개선 사항](#jan-26-01-improv) 섹션은 이미 사용 가능한 기능을 다루고 [곧](#jan-26-01-coming-soon)은(는) 나중에 사용 가능한 날짜에 예약된 항목을 나열합니다.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 새로운 기능 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>웹 푸시 알림 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer은 이제 <strong>웹 푸시 알림</strong>을 지원하므로 푸시 채널을 모바일 이상으로 확장합니다. <strong>모바일 및 데스크톱 브라우저</strong> 모두에 알림을 원활하게 전달할 수 있으므로 앱을 사용하지 않고도 고객의 디바이스에서 바로 고객에게 연락할 수 있습니다. 이 향상된 기능을 통해 이미 모바일 푸시에서 사용 가능한 것과 동일한 작성 워크플로 및 타기팅 기능을 활용하여 사용자에게 적시에 개인화된 메시지를 실시간으로 보낼 수 있습니다.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>이전에 Beta로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../push/push-configuration-web.md">세부 설명서</a>를 참조하십시오.</p>
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
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>자세한 내용은 <a href="../orchestrated/activities/channels.md#channel">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - 여정 만들기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Agent은 생성 기능을 제공하므로 Journey Optimizer 사용자는 <strong>자연어 인터페이스</strong>를 통해 마케팅 여정을 빌드하고 구성할 수 있습니다. 이러한 새로운 기술을 통해 의료인은 <strong>대화 프롬프트</strong>에서 요구 사항을 간단히 설명하여 여정을 신속하게 만들 수 있습니다. 이러한 혁신은 여정 생성 프로세스를 간소화하여 마케터가 기술 구성보다 전략에 집중할 수 있도록 합니다.</p>
<p>자세한 내용은 <a href="../start/ai-features.md#journey-agent">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2026년 1월 12일 화요일</p>
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
<p>이제 새로운 Journey Optimizer API를 사용할 수 있으므로 세부 정보, 버전 및 구성과 같은 <strong>캠페인 관련 데이터</strong>를 프로그래밍 방식으로 검색하고 검사할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2025년 11월 24일 화요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 Designer 테마</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>사전 승인된 테마</strong>를 빠르게 적용하여 모든 이메일에 <strong>브랜드 일관성</strong>을 보장하고, 캠페인 생성 프로세스를 가속화하고, 디자인 팀에 대한 의존도를 줄이면서 독자적으로 고품질 이메일을 생성할 수 있습니다.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>이전에 Beta 버전으로 릴리스된 이 기능을 이제 일부 조직에서 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../email/apply-email-themes.md">세부 설명서</a>를 참조하십시오.</p>
<p>가용성 일자: 2025년 11월 5일 목요일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-26-01-improv}

#### AI

* **AI 길잡이 콘텐츠 품질 검사** - 이제 브랜드 정렬 외에도 브랜드 지침과 관계없이 전체 <strong>콘텐츠 품질</strong>을 평가하여 <strong>가독성</strong>, 응집성 및 효과성의 잠재적 문제를 확인할 수 있습니다. 이러한 자동화된 검사는 명확하지 않은 메시지, 일관되지 않은 말투 또는 구조적 차이를 식별하는 데 도움이 됩니다. [자세한 내용](../content-management/brands-score.md#validate-quality). [비디오에서 이 기능을 살펴보세요](https://video.tv.adobe.com/v/3470553/?captions=kor&learn=on).

#### 경험 의사 결정

* **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서 의사 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있는 <strong>의사 결정 항목</strong>에 <strong>조각</strong>을(를) 첨부할 수 있는 기능을 제공합니다. [자세히 보기](../experience-decisioning/items.md)

  **참고**: 이전에 제한된 가용성으로 릴리스된 이후에는 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).

#### 여정

* **기본 및 Adobe Campaign 메시지 동작 결합** - 이제 Journey Optimizer을 사용하여 <strong>Adobe Campaign v7/v8</strong> 메시지 동작을 동일한 여정의 <strong>기본 채널 동작</strong>과 결합할 수 있습니다. [자세히 보기](../building-journeys/using-adobe-campaign-v7-v8.md)

* **사용자 지정 작업 오류 응답 페이로드** - 이제 사용자 지정 작업에 대해 선택적 <strong>오류 응답 페이로드</strong>를 정의할 수 있습니다. 호출이 실패하면 오류 페이로드가 여정 컨텍스트(작업의 errorResponse 노드 아래)에 노출되며 <strong>과(와) 함께 </strong>시간 초과/오류 분기`jo_status_code`에서 사용할 수 있으므로 더 풍부한 대체 논리 및 디버깅을 지원할 수 있습니다. [자세히 보기](../action/action-response.md)

* **여정의 여정 페이로드 크기 확인** - Journey Optimizer이 이제 <strong>페이로드 크기</strong>를 확인하여 최적의 성능과 시스템 안정성을 보장합니다. 여정을 작성하거나 게시할 때 페이로드 크기가 권장 한도에 근접하거나 초과하는 경우 명확한 <strong>경고 및 오류</strong>와 함께, 여정 구성을 최적화하는 실행 가능한 지침을 받게 됩니다. 이 사전 유효성 검사는 잠재적 문제를 조기에 식별하고 여정 성능을 유지하는 데 도움이 됩니다. [자세히 보기](../start/guardrails.md#journey-payload-size)

* **여정 경고** - 새 <strong>사전 구성된 경고</strong>를 여정에 사용할 수 있습니다.
   * <strong>프로필 삭제 비율 초과</strong> - 지난 5분 동안 입력한 프로필에 대한 프로필 삭제 비율 임계값 초과
   * <strong>사용자 지정 작업 오류율 초과</strong> - 지난 5분 동안 임계값에 대한 성공한 HTTP 호출에 대한 사용자 지정 작업 오류의 비율
   * <strong>프로필 오류율 초과</strong> - 지난 5분 동안 입력한 프로필 대비 오류가 발생한 프로필 비율이 임계값을 초과했습니다.

  자세한 내용은 [세부 설명서](../reports/alerts.md)를 참조하십시오.

  사용 가능한 날짜: 2025년 10월 14일

#### 오케스트레이션된 캠페인

* **대상에 대한 데이터 사용 레이블 상속** - 이제 오케스트레이션된 캠페인에 <strong>대상</strong>을(를) 저장할 때 Adobe Experience Platform에 적용된 레이블이 자동으로 이전되어 수동 <strong>DULE 태그 지정</strong>이 줄어듭니다. [자세히 보기](../orchestrated/activities/save-audience.md)

* **매개 변수가 있는 사전 정의된 필터** - 이제 재사용 가능한 편집 가능한 규칙에 대해 오케스트레이션된 캠페인에서 <strong>매개 변수</strong>를 사용하여 <strong>사전 정의된 필터</strong>을(를) 만들 수 있습니다. [자세히 보기](../orchestrated/predefined-filters.md)

* **특성 선택 및 배포 값 복사** - 이제 조정된 캠페인의 <strong>값 배포</strong> 보기에서 직접 <strong>값을 선택 또는 복사</strong>할 수 있습니다. [자세히 보기](../orchestrated/build-query.md)

* **보내기 전 메시지 확인** - 이제 우발적 전송을 줄이기 위해 오케스트레이션된 캠페인을 보내기 전에 <strong>확인 단계</strong>이(가) 기본적으로 활성화됩니다. [자세히 보기](../orchestrated/activities/channels.md#confirm-message-sending)

* **사전 정의된 리타겟팅 필터** - 오케스트레이션된 캠페인 사용 사례에 대해 더 쉬운 리타겟팅을 지원하기 위해 이 릴리스에서는 새로운 <strong>캠페인 피드백 필터</strong>를 도입했습니다. 이러한 필터를 사용하면 [전송], [열기만], [열기 또는 클릭], [열기 및 클릭]과 같은 <strong>메시지 참여</strong>에 따라 대상자를 직접 타깃팅하고, 다시 타깃팅할 특정 캠페인이나 전환 중 캠페인을 선택할 수 있습니다. [자세히 보기](../orchestrated/retarget.md)

* **속도 제어 지원** - 이제 오케스트레이션된 캠페인이 <strong>속도 제어</strong>를 지원하므로 게재 속도를 높이고 <strong>볼륨 제한</strong>에 맞출 수 있습니다. [자세히 보기](../orchestrated/activities/channels.md#rate-control)

* **다시 시작 단추** - 오케스트레이션된 캠페인에는 이제 <strong>다시 시작 단추</strong>가 포함되어 있으므로 필요할 때 <strong>다시 실행</strong>한 후 캠페인을 게시할 수 있습니다. [자세히 보기](../orchestrated/start-monitor-campaigns.md)

* **사용자 생성 메타데이터 지원** - 이제 오케스트레이션된 캠페인용 개인화 편집기에서 <strong>executionMetadata 도우미 함수</strong>를 사용할 수 있으므로 컨텍스트 정보를 기본 작업에 첨부하고 데이터 집합에 저장하여 외부 시스템으로 내보낼 수 있습니다. [자세히 보기](../personalization/functions/helpers.md#execution-metadata)

#### 캠페인

* **프로필 시간대를 사용하여 캠페인 예약** - 이제 Campaign 예약에서 각 프로필의 <strong>시간대</strong>를 사용하여 원하는 현지 시간에 메시지를 배달할 수 있습니다. [자세히 보기](../campaigns/campaign-schedule.md)

  **참고**: 이 개선 사항은 조직 집합(제한된 가용성)에서만 사용할 수 있습니다.

#### 권한

* **여정 및 캠페인에 대한 자체 승인 방지** - <strong>승인 정책</strong>을 만들거나 설정할 때 여정 또는 캠페인 작성자가 <strong>자신의 개체를 승인</strong>하지 못하도록 옵션을 추가했습니다. [자세히 보기](../test-approve/approval-policies.md)

## 곧 출시 예정 {#jan-26-01-coming-soon}

조만간 다음 기능 및 개선 업데이트가 릴리스될 예정입니다. **이 정보는 변경될 수 있습니다**. 업데이트된 링크, 화면, 설명서는 업데이트가 프로덕션에서 제공될 때 공유 예정입니다.

### 기능

<table>
<thead>
<tr>
<th><strong>여정의 DM 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에 캠페인으로 제한되었던 <strong>DM</strong> 채널을 이제 여정 캔버스에서 사용할 수 있으므로 DM을 여정에 통합할 수 있습니다. 이제 파일 추출 구성 및 시간 기반 빈도 설정을 지원하여 <strong>일괄 처리 및 1:1 여정 시나리오</strong>에서 DM을 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>가용성 일자: 2026년 1월 28일 목요일</p>
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
<p><strong>방해 금지 시간</strong>을(를) 사용하면 전자 메일, SMS, 푸시 및 WhatsApp 채널에 대한 시간 기반 제외를 정의할 수 있습니다. 특정 기간 동안 메시지가 전송되지 않도록 하여 고객 선호도 및 규정 준수 요구 사항을 준수할 수 있습니다. 정확한 제어를 위해 캠페인 또는 여정의 개별 작업에 할당할 수 있는 <strong>규칙 집합</strong>을 통해 방해 금지 시간을 적용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 고객이 방해 금지 모드가 완료될 때까지 캠페인 작업을 대기열에 추가할 수 있는 기능과 활성화된 방해 금지 모드 규칙을 미리 볼 수 있는 기능이 제공됩니다.</p>
<p>가용성 일자: 2026년 1월 28일 목요일</p>
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
<p><strong>마이그레이션 도구 API</strong>를 사용하여 의사 결정 관리 엔터티를 Decisioning으로 프로그래밍 방식으로 마이그레이션할 수 있습니다. 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>유연한 마이그레이션 범위(샌드박스, 오퍼 또는 의사 결정 수준)</li>
<li>자동화된 종속성 분석 및 유효성 검사</li>
<li>완료된 마이그레이션에 대한 롤백 지원</li>
<li>개체 매핑이 포함된 자세한 마이그레이션 보고서</li>
</ul>
<p>가용성 일자: 2026년 1월 28일 목요일</p>
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
<p>새로운 모니터링 대시보드와 보강된 여정 단계 이벤트 데이터를 사용하여 <strong>사용자 지정 작업 끝점</strong>의 상태와 성능에 대해 더 깊이 있는 insight을 얻을 수 있습니다. 성공한 호출, 오류, 처리량, 응답 시간 및 대기열 대기 시간을 추적하여 예외 항목이 발생하는 시기, 장소 및 이유를 신속하게 파악합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>가용성 일자: 2026년 1월 28일 목요일</p>
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
<p>이제 새 <strong>메시지 내보내기</strong> 기능을 전자 메일 및 SMS 채널에 사용할 수 있습니다. 이 기능을 사용하면 보낸 메시지 콘텐츠를 전용 Experience Platform 데이터 세트로 자동으로 내보내 다음과 같은 작업을 수행할 수 있습니다.</p>
<ul>
<li>규정 준수 요건 충족(예: HIPAA)</li>
<li>법적 청구 및 고객 지원 문의 메시지 보관</li>
<li>개인에게 전송된 개인화된 콘텐츠의 사본 유지</li>
</ul>
<p>레코드는 수집 후 7일 동안 AJO 메시지 내보내기 데이터 세트에 유지됩니다. 이 보존 기간 동안 Experience Platform 대상을 통해 데이터를 고유한 저장소로 내보낼 수 있습니다. 이 기능은 채널 구성 수준에서 활성화되어 메시지를 내보내는 <strong>세분화된 제어</strong>를 제공합니다.</p>
<p>이 기능은 메시지 내보내기 추가 기능 서비스를 구입한 조직의 이메일 및 SMS 채널에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<p>가용성 일자: 2026년 1월 30일 토요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent 내 콘텐츠 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform Agent Orchestrator에서 제공하는 <strong>Journey Agent</strong>은(는) Journey Optimizer에서 사용할 수 있으며 자연어 인터페이스를 통해 여정을 분석할 수 있도록 합니다. 이제 Journey Agent에서 직접 <strong>콘텐츠를 생성하고 관리</strong>할 수도 있습니다. 이메일 및 푸시 등의 채널을 위한 콘텐츠를 만들고, 템플릿을 적용하고 미리 보고, 프롬프트를 통해 색조와 스타일을 개선하고, 상황에 맞는 편집을 위해 Content Designer에서 콘텐츠를 열 수도 있습니다.</p>
<p>가용성 일자: 2026년 2월 2일 화요일</p>
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
<p>이제 <strong>의사 결정</strong>을 통해 <strong>푸시 및 SMS</strong> 메시지의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선 순위 점수, 공식 또는 AI 모델을 사용하여 고객에게 최상의 콘텐츠를 표시합니다.</p>
<p>가용성 일자: 2026년 2월 3일 수요일</p>
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
<p>이제 <strong>개인화된 오퍼</strong>를 고객 여정에 직접 통합하기 위해 여정 캔버스에서 새 <strong>콘텐츠 결정 활동</strong>을 사용할 수 있습니다. 이 활동을 사용하면 의사 결정 기반 콘텐츠를 제공하고 자격 기반 분기를 만들기 위한 조건, 외부 시스템에 오퍼 데이터를 전달하기 위한 사용자 지정 작업 및 완전히 개인화된 고객 경험을 구축하기 위한 기타 활동에서 여정 전체에서 이러한 오퍼를 참조할 수 있습니다.</p>
<p>이 기능은 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p>가용성 일자: 2026년 2월 3일 수요일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

* **SMS Webhooks** - <strong>Webhooks</strong>이(가) 이제 모든 SMS 공급자에서 지원됩니다. 각 웹후크의 의도된 목적, 수신 메시지를 캡처하기 위한 인바운드 웹후크 및 게재 확인, 상태 업데이트 및 기타 메시지 관련 이벤트를 수신하기 위한 피드백 웹후크를 구성할 수 있습니다.

  사용 가능한 날짜: 2026년 1월 28일
