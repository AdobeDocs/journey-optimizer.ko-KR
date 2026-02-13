---
solution: Journey Optimizer
product: journey optimizer
title: 2026년 릴리스 정보
description: Journey Optimizer 2026 릴리스 노트
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: b53c28405e453be3767f05e2c7a7a1b2e69d0416
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 86%

---

# 2026년 릴리스 정보 {#release-notes-2026}

이 페이지에는 2026년에 릴리스된 [!DNL Journey Optimizer]의 모든 기능과 개선 사항이 나와 있습니다.

## 26년 1월 릴리스 정보 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

[기능](#jan-26-01-features) 및 [개선 사항](#jan-26-01-improv) 섹션은 이미 사용 가능한 기능을 다루고 [곧 출시 예정](#jan-26-01-coming-soon)에는 이후에 사용 가능한 날짜가 예약된 항목의 목록이 있습니다.

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
<p>이제 <strong>Decisioning</strong>을 통해 <strong>푸시 알림</strong>의 콘텐츠를 개인화하고 최적화할 수 있습니다. 우선순위 점수, 공식 또는 AI 모델을 사용하여 고객에게 최상의 콘텐츠를 표시합니다.</p>
<p>푸시 알림을 사용하는 Experience Decisioning에는 모바일 SDK의 특정 버전이 필요합니다. 이 기능을 구현하기 전에 <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">릴리스 정보</a>를 확인하여 필요한 버전을 식별하고 그에 따라 업그레이드했는지 확인하십시오. <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">이 섹션</a>에서 사용 가능한 플랫폼에 대한 모든 SDK 버전을 볼 수도 있습니다.</p>
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
<p><strong>방해 금지 시간</strong> 기능으로 이메일, SMS, 푸시, WhatsApp 채널에 대한 시간 기반 제외를 정의할 수 있습니다. 특정 시간 동안 메시지가 전송되지 않도록 하여 고객 환경 설정과 규정 요건을 준수할 수 있습니다. <strong>규칙 세트</strong>를 통해 방해 금지 시간을 적용할 수 있으며, 정확한 제어를 위해 이 규칙 세트를 캠페인이나 여정의 개별 액션에 할당할 수 있습니다.</p>
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
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">세부 설명서</a>를 참조하십시오.</p>
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

* **실시간 캠페인을 초안 상태로 되돌리기** - 이제 실행 오류가 발생하거나 실행을 시작하기 전에 예약된 캠페인을 수정해야 하는 경우 실시간 오케스트레이션된 캠페인을 초안 상태로 되돌릴 수 있습니다. 이 옵션은 첫 번째 메시지가 전송될 때까지 사용할 수 있습니다. [자세히 보기](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### 캠페인

* **프로필 시간대를 사용하여 캠페인 예약** - 이제 Campaign 예약에서 각 프로필의 <strong>시간대</strong>를 사용하여 원하는 현지 시간에 메시지를 배달할 수 있습니다. [자세히 보기](../campaigns/campaign-schedule.md)

  **참고**: 이 개선 사항은 조직 집합(제한된 가용성)에서만 사용할 수 있습니다.

  사용 가능한 날짜: 2026년 1월 27일 수요일.

#### 권한

* **여정 및 캠페인에 대한 자체 승인 방지** - <strong>승인 정책</strong>을 만들거나 설정할 때 여정 또는 캠페인 작성자가 <strong>자신의 오브젝트를 직접 승인</strong>하지 못하도록 하는 옵션을 추가했습니다. [자세히 보기](../test-approve/approval-policies.md)

  사용 가능한 날짜: 2026년 1월 27일 수요일.
