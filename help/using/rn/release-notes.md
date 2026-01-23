---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9ddf79c9542ad10907b25b2db4415130faec5d8d
workflow-type: tm+mt
source-wordcount: '2027'
ht-degree: 29%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적 제공 모델을 따르므로 Adobe에서 새로운 기능, 개선 사항, 버그 해결 업데이트를 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다.

이 모델로 인해 릴리스 노트는 월별 릴리스 사이에 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 2026년 1월 프리릴리스 정보 {#latest-rn}

**릴리스 일자**: 2026년 1월 27일 수요일

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

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
<p><strong>참고</strong>: 오케스트레이션된 캠페인에서는 자동 시간이 지원되지 않습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 고객이 방해 금지 모드가 완료될 때까지 캠페인 작업을 대기열에 추가할 수 있는 기능과 활성화된 방해 금지 모드 규칙을 미리 볼 수 있는 기능이 제공됩니다.</p>
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
<p><strong>참고</strong>: 웹 푸시 알림에 대해서는 자동 알림이 아직 지원되지 않습니다.</p>
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
<p>레코드는 <strong>7일 동안 수집 후 </strong>에 AJO 메시지 내보내기 데이터 세트에 보관됩니다. 이 보존 기간 동안 Experience Platform 대상을 통해 데이터를 고유한 저장소로 내보낼 수 있습니다. 이 기능은 채널 구성 수준에서 활성화되므로 내보낼 메시지를 세부적으로 제어할 수 있습니다.</p>
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
<p>여정 만들기 에이전트를 사용하면 Journey Optimizer 사용자는 자연어 인터페이스를 사용하여 마케팅 여정을 빌드하고 구성할 수 있습니다. 여정 만들기 에이전트를 사용하면 전문가가 대화 프롬프트에서 요구 사항을 설명하여 여정을 빠르게 만들 수 있습니다. 에이전트는 여정 생성을 간소화하므로 마케터는 기술 구성보다 전략에 집중할 수 있습니다.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">자세히 알아보기</a></p>
<p>가용성 일자: 2026년 1월 12일 화요일</p>
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
<p>가용성 일자: 2025년 11월 5일 목요일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-26-01-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### AI

* **AI 길잡이 콘텐츠 품질 검사** - 이제 브랜드 정렬 외에도 브랜드 지침과 관계없이 가독성, 응집성 및 효과성으로 잠재적인 문제를 발견하기 위해 전체 <strong>콘텐츠 품질</strong>을 평가할 수 있습니다. 이러한 자동화된 검사는 명확하지 않은 메시지, 일관되지 않은 말투 또는 구조적 차이를 식별하는 데 도움이 됩니다.

* **새 색상 탭으로 브랜드 업데이트** - 브랜드 지침은 모든 접점에서 브랜드가 일관되게 표시되도록 하는 데 도움이 됩니다. 새 <strong>색상 섹션</strong>은 브랜드 색상 시스템에 대한 표준을 정의하며 여러 경험에서 색상을 선택, 구성 및 적용하는 방법에 대해 대략적으로 설명합니다. 기본, 보조, 악센트 및 중립 색상을 일관되게 사용하여 통합적이고, 액세스가 가능하고, 인식 가능한 브랜드 이미지를 지원합니다.

#### 캠페인

* **프로필 시간대를 사용하여 캠페인 예약** - 이제 Campaign 예약에서 각 프로필의 <strong>시간대</strong>를 사용하여 원하는 현지 시간에 메시지를 배달할 수 있습니다. 이메일, 푸시, SMS, WhatsApp 및 LINE 채널에 프로필 시간대를 사용하여 예약할 수 있습니다.

  **참고**: 이 개선 사항은 조직 집합(제한된 가용성)에서만 사용할 수 있습니다.


#### 경험 의사 결정

* **셀프 서비스 마이그레이션 도구 API** - 새로운 <strong>마이그레이션 도구 API</strong> 집합을 사용하여 오퍼 관리 엔터티를 Experience Decisioning으로 마이그레이션할 수 있습니다. 이 도구를 사용하면 종속성 해결 및 롤백 기능을 통해 샌드박스 간에 원활하게 마이그레이션할 수 있습니다.

* **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서는 의사 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있는 의사 결정 항목에 <strong>조각</strong>을(를) 첨부할 수 있는 기능을 제공합니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이후에는 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).

#### 여정

* **여정 사용자 지정 작업에서 오류 응답 페이로드를 활용합니다** - 이제 사용자 지정 작업에 대해 선택적 <strong>오류 응답 페이로드</strong>를 정의할 수 있습니다. 호출이 실패하면 오류 페이로드가 여정 컨텍스트에 노출되며, 보다 풍부한 대체 논리 및 디버깅을 지원하기 위해 시간 초과/오류 분기에서 사용할 수 있습니다.

* **기본 및 Adobe Campaign 메시지 동작 결합** - 이제 Journey Optimizer을 사용하여 Adobe Campaign v7/v8 메시지 동작을 동일한 여정의 기본 채널 동작과 결합할 수 있습니다.

* **여정의 여정 페이로드 크기 유효성 검사** - 이제 Journey Optimizer에서 최적의 성능과 시스템 안정성을 보장하기 위해 <strong>페이로드 크기 유효성 검사</strong>를 제공합니다. 여정을 작성하거나 게시할 때 페이로드 크기가 권장 한도에 근접하거나 초과하는 경우 명확한 경고 및 오류가 표시되고, 여정 구성을 최적화하는 실행 가능한 지침이 제공됩니다. 이 사전 유효성 검사는 잠재적 문제를 조기에 식별하고 여정 성능을 유지하는 데 도움이 됩니다.

* **여정의 여러 인바운드 작업** - 이제 여정 오케스트레이션을 단순화하기 위해 단일 여정에서 <strong>여러 인바운드 작업</strong>을(를) 정의할 수 있습니다. 이전에 캠페인에서 사용할 수 있었던 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며 각 작업에는 특정 콘텐츠가 포함되어 있습니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이후에는 모든 환경에서 이 개선 사항을 사용할 수 있습니다(일반 가용성).

#### 오케스트레이션된 캠페인

* **특성 선택 및 배포 값 복사** - 이제 조정된 캠페인의 값 보기에서 직접 값을 선택하거나 복사할 수 있습니다.

* **대상에 대한 데이터 사용 레이블 상속** - 이제 오케스트레이션된 캠페인에 대상을 저장할 때 Adobe Experience Platform에 적용된 <strong>데이터 사용 레이블</strong>이 자동으로 이전되므로 수동 DULE 태그 지정이 줄어듭니다.

* **사전 정의된 리타겟팅 필터** - 오케스트레이션된 캠페인 사용 사례에 대해 더 쉬운 리타겟팅을 지원하기 위해 이 릴리스에서는 새로운 <strong>리타겟팅 필터</strong>을 도입했습니다. 이러한 필터를 사용하면 보냄, 열기만, 열림 또는 클릭됨, 열림 및 클릭됨 등의 메시지 참여를 기반으로 대상을 직접 타기팅하고 다시 타기팅할 특정 캠페인 또는 전환 중 캠페인을 선택할 수 있습니다.

* **매개 변수가 있는 사전 정의된 필터** - 이제 재사용 가능한 편집 가능한 규칙에 대해 조정된 캠페인에서 <strong>매개 변수가 있는 필터</strong>를 만들 수 있습니다.

* **보내기 전 메시지 확인** - 이제 우발적 전송을 줄이기 위해 오케스트레이션된 캠페인을 보내기 전에 <strong>확인 단계</strong>이(가) 기본적으로 활성화됩니다.

* **사용자 생성 메타데이터 지원** - 이제 오케스트레이션된 캠페인용 개인화 편집기에서 <strong>executionMetadata 도우미 함수</strong>를 사용할 수 있으므로 컨텍스트 정보를 기본 작업에 첨부하고 데이터 집합에 저장하여 외부 시스템으로 내보낼 수 있습니다.

* **다시 시작 단추** - 오케스트레이션된 캠페인에는 이제 <strong>다시 시작 단추</strong>가 포함되어 있으므로 필요할 때 실행을 빠르게 다시 시작한 후 캠페인을 게시할 수 있습니다.

* **속도 제어 지원** - 이제 오케스트레이션된 캠페인이 <strong>속도 제어</strong>를 지원하므로 게재 속도를 높이고 볼륨 제한에 맞출 수 있습니다.

#### 권한

* **여정 및 캠페인에 대한 자체 승인 방지** - 이제 작성자가 자신의 여정 또는 캠페인을 승인할 수 없도록 요구하여 승인 워크플로의 <strong>직무 분리</strong>을 개선할 수 있습니다.

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
<p>이 기능은 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p>가용성 일자: 2026년 2월 3일 수요일</p>
</td>
</tr>
</tbody>
</table>
