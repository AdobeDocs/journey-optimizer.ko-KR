---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 279fd366b14520daec1df7f843ed337348e145a5
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 39%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적 제공 모델을 따르므로 Adobe에서 새로운 기능, 개선 사항, 버그 해결 업데이트를 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다.

이 모델로 인해 월별 릴리스 사이에 릴리스 정보가 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 2026년 2월 프리릴리스 정보 {#feb-26-01-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 2월 17~18일

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
<p><strong>캠페인</strong> 또는 <strong>여정</strong>의 아웃바운드 메시지를 시간에 따라 제어된 <strong>일괄 처리</strong>로 전달하도록 예약할 수 있습니다.</p>
<p>웨이브 전송은 다음과 같은 이점을 제공합니다.</p>
<ul>
<li>더 나은 <strong>전달성</strong> - Spread는 보낸 사람의 신뢰도를 유지하고 스팸으로 표시될 위험을 줄이기 위해 시간이 지남에 따라 전송됩니다.</li>
<li><strong>로드 제어</strong> - 한 번에 나가는 메시지 수를 제한하여 너무 많은 다운스트림 시스템(예: 콜 센터, 랜딩 페이지)을 사용하지 마십시오.</li>
<li>대량의 시간에 민감한 사용 사례 - 대규모 대상자에 적합하거나 시간 조절(예: 콜 센터 용량, 램프 업 또는 시간 제한 제안)이 필요한 경우.</li>
</ul>
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
<p>이제 <strong>수식</strong> 및 <strong>AI 모델</strong>을 사용하여 고객 프로필 특성 및 컨텍스트 요소를 기반으로 여정 우선 순위 점수를 자동으로 높여 고객이 가장 관련성이 높은 여정을 입력하도록 할 수 있습니다.</p>
<p>이 기능은 조직 집합(<strong>제한된 가용성</strong>)에만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
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
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>여정의 액션 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 단일 작업과 다중 작업 인바운드 작업 그룹을 모두 구성할 수 있는 새로운 일반 <strong>작업 활동</strong>을 지원하므로 여정 캔버스 내에서 간소화된 작업 구성을 사용할 수 있습니다. 특히 이 새로운 기능에는 다음과 같은 이점이 있습니다.</p>
<ul>
<li>여정 캔버스 내 기본 액션 구성 간소화.</li>
<li>다중 액션 인바운드 액션 그룹을 만들 수 있는 용량.</li>
<li>기본 제공 채널 작업에 <strong>최적화</strong>을(를) 추가하는 기능입니다.</li>
<li>모든 작업에 <strong>실험</strong> 및 <strong>다국어</strong> 옵션을 모두 추가하는 기능.</li>
</ul>
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
<p>Adobe Journey Optimizer가 이제 <strong>웹 푸시 알림</strong>을 지원하여 푸시 채널을 모바일 밖까지 확장합니다. 모바일 브라우저와 데스크탑 브라우저 모두에 알림을 원활하게 전달할 수 있으므로 앱 설치를 요청할 필요 없이 고객의 디바이스에서 직접 고객에게 연락할 수 있습니다. 이 향상된 기능을 통해 이미 모바일 푸시에서 사용 가능한 것과 동일한 작성 워크플로 및 타기팅 기능을 활용하여 사용자에게 적시에 개인화된 메시지를 실시간으로 보낼 수 있습니다.</p>
<p>이전에 베타 버전으로 출시된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 공급).</p>
<p>사용 가능한 날짜: 2026년 2월 13일 토요일</p>
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
<p>이전에 Beta에서 릴리스된 이 기능은 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../push/push-configuration-web.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 11일 목요일</p>
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
<p>이제 개인 맞춤화된 오퍼를 고객 여정에 직접 통합하기 위해 여정 캔버스에서 새로운 <strong>콘텐츠 결정 활동</strong>을 사용할 수 있습니다. 이 활동을 사용하면 의사 결정 기반 콘텐츠를 제공하고 자격 기반 분기를 만들기 위한 조건, 외부 시스템에 오퍼 데이터를 전달하기 위한 사용자 지정 작업 및 완전히 개인화된 고객 경험을 구축하기 위한 기타 활동에서 여정 전체에서 이러한 오퍼를 참조할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/content-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 11일 목요일</p>
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
<p><strong>마이그레이션 도구 API</strong>을(를) 사용하여 <strong>의사 결정 관리</strong> 엔터티를 <strong>의사 결정</strong>(으)로 프로그래밍 방식으로 마이그레이션할 수 있습니다.</p>
<ul>
<li>유연한 마이그레이션 범위(<strong>샌드박스</strong>, <strong>오퍼</strong> 또는 <strong>결정</strong> 수준)</li>
<li>자동화된 <strong>종속성 분석</strong> 및 유효성 검사</li>
<li>완료된 마이그레이션에 대한 <strong>롤백 지원</strong></li>
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
<p>새로운 <strong>모니터링 대시보드</strong> 및 보강된 <strong>여정 단계 이벤트 데이터</strong>를 사용하여 <strong>사용자 지정 작업 엔드포인트</strong>의 상태 및 성능에 대해 더 자세한 insight을 사용하세요. 성공한 호출, 오류, 처리량, 응답 시간, 대기열 대기 시간을 추적하여 예외 항목이 발생하는 시점, 위치, 이유를 신속하게 파악합니다.</p>
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
<p>이제 <strong>Decisioning</strong>을(를) 사용하여 <strong>SMS 메시지</strong>의 콘텐츠를 개인화하고 최적화할 수 있습니다. <strong>우선 순위 점수</strong>, <strong>수식</strong> 또는 <strong>AI 모델</strong>을 사용하여 고객에게 최상의 콘텐츠를 표시하십시오.</p>
<p>자세한 내용은 <a href="../experience-decisioning/create-decision.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 2월 2일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#feb-26-01-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

#### 구성

* **여정 식의 경험 이벤트 사용** - 2026년 4월 1일부터 지난 90일 동안 이 기능을 사용하지 않은 조직에 대해 여정 식의 경험 이벤트 특성 사용이 더 이상 지원되지 않습니다. 이 기능은 2025년 7월 8일 이후 신규 고객 조직에서 이미 사용할 수 없습니다. 대안은 [여정의 경험 이벤트 조회](../building-journeys/exp-event-lookup.md)를 참조하십시오.


* **하위 도메인 위임 방법 전환** - 이제 하나의 하위 도메인 위임 방법에서 다른 하위 도메인 위임 방법으로 전환할 수 있습니다. 이렇게 하면 CNAME 위임 모드를 사용하여 도메인을 회사의 보안 정책을 준수하도록 사용자 지정 위임 방법으로 마이그레이션할 수 있습니다.

  **참고**: 이 기능은 조직 집합(<strong>제한된 가용성</strong>)에서만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.


#### 이메일 디자이너

* **브랜드 테마를 사용하여 이미지를 이메일 템플릿으로 변환** - Journey Optimizer에서 이미지를 이메일 템플릿으로 변환할 때 이제 테마를 입력으로 사용하여 생성된 HTML이 브랜드 매개 변수를 따르도록 할 수 있습니다. 배경색, 단추 색상, 글꼴, 줄 간격, 여백 및 패딩과 같은 스타일이 자동으로 적용되어 수동 디자인 작업이 줄어들고 최소한의 편집으로 사용할 준비가 된 템플릿을 제공합니다.


* **새 색상 탭으로 브랜드 업데이트** - 브랜드 가이드라인은 모든 접점에서 브랜드가 일관되게 표시되도록 하는 데 도움이 됩니다. 새 색상 섹션은 브랜드 색상 시스템에 대한 표준을 정의하며 경험을 통해 색상을 선택, 구성 및 적용하는 방법에 대해 대략적으로 설명합니다. 기본, 보조, 강조, 중립 색상을 일관되게 사용하여 일치도와 접근성이 높으며 인식히기 쉬운 브랜드 아이덴티티를 만드는 작업을 지원합니다.


#### AI

* **사용자 지정 Firefly 모델 및 타사 이미지 생성 모델의 통합** - 표준 및 사용자 지정 Firefly 모델과 승인된 타사 이미지 모델(예: NanoBanana)을 매끄럽게 통합하여 이미지를 생성할 때 더 큰 유연성, 제어 및 브랜드 정렬을 제공합니다. 이를 통해 일반적인 요구 사항을 위한 표준 Firefly, 브랜드 내 생성을 위한 사용자 지정 Firefly 또는 전문 또는 실험 시나리오를 위한 승인된 서드파티 모델 등 각 사용 사례에 가장 적합한 모델을 선택할 수 있습니다.


#### 경험 결정

* **Decisioning에서 Adobe Experience Platform 데이터 사용에 대한 Edge 인바운드 지원** - Decisioning에서 Adobe Experience Platform 데이터 사용은 이제 여정의 이메일 및 사용자 지정 작업 외에도 에지 인바운드 사용 사례를 지원합니다.

  **참고**: 이 기능은 조직 집합(<strong>제한된 가용성</strong>)에서만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.


* **코드 기반 경험 채널에서 경험 의사 결정 미리 보기** - 이제 코드 기반 경험 채널에서 경험 의사 결정을 구성할 때 의사 결정 항목을 미리 볼 수 있습니다. 미리보기는 라이브로 전환되기 전에 작성 인터페이스에서 직접 사용할 수 있습니다.


* **상위 AI 모델 가시성** - 이제 Journey Optimizer을 통해 Decisioning에서 AI 모델의 상태, 교육 상태 및 성능을 모니터링할 수 있으므로 교육 성공을 확인하고, 오류를 해결하며, 결과에 미치는 영향을 이해할 수 있습니다. 이 기능은 개인화된 최적화 모델(자동 최적화는 아님)에만 사용할 수 있습니다.


* **결정 항목에 조각 첨부** - 이제 Journey Optimizer가 결정 항목에 조각을 첨부할 수 있는 기능을 제공합니다. 따라서 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있습니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).

  사용 가능한 날짜: 2026년 2월 12일


#### 여정

* **여정의 여러 인바운드 액션** - 이제 여정 오케스트레이션을 단순화하기 위해 단일 여정에서 여러 인바운드 액션을 정의할 수 있습니다. 이전에 캠페인에서 사용할 수 있었던 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며 각 작업에는 특정 콘텐츠가 포함되어 있습니다.

  **참고**: 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).


* **SMS 웹훅** - <strong>웹훅</strong>이 이제 모든 SMS 공급자에서 지원됩니다. 의도한 목적에 따라 각 웹후크를 구성할 수 있습니다. <strong>수신 웹후크</strong>를 통해 들어오는 메시지를 캡처하고 <strong>피드백 웹후크</strong>를 통해 게재 확인, 상태 업데이트 및 기타 메시지 관련 이벤트를 받을 수 있습니다. [자세히 보기](../sms/sms-webhook.md)

  사용 가능한 날짜: 2026년 2월 2일