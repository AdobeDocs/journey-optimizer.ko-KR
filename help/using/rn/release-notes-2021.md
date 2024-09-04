---
solution: Journey Optimizer
product: journey optimizer
title: 이전 릴리스 정보(2021)
description: Journey Optimizer 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: ht
source-wordcount: '2035'
ht-degree: 100%

---

# 2021년 릴리스 정보 {#release-notes-2021}

이 페이지에서는 2021년에 릴리스된 [!DNL Journey Optimizer]의 기능과 개선 사항 목록을 확인할 수 있습니다.

## 2021년 11월 릴리스 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME 하위 도메인 위임</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 CNAME을 지원합니다. CNAME 또는 Canonical Name 레코드는 IP 주소가 아닌 다른 도메인 주소를 가리키는 레코드입니다. CNAME 하위 도메인을 위임하면 하위 도메인을 만들고 CNAME을 사용하여 Adobe 특정 레코드를 가리키도록 설정할 수 있습니다. 이 구성을 사용하면 사용자와 Adobe가 이메일을 보내고 렌더링 및 추적하기 위한 환경을 설정하기 위한 DNS 유지 관리를 공동으로 수행합니다.</p>
<p>조직의 정책이 전체 하위 도메인 위임 방법을 제한하는 경우 이 방법을 사용하는 것이 좋습니다.</p>
<p><a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">자세한 설명서</a>에서 CNAME 하위 도메인 위임에 대해 자세히 알아보세요.</p>
</td>
</tr>
</tbody>
</table>


## 2021년 10월 릴리스 {#oct-2021-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>의사 결정 관리 - 오퍼 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer UI에서 주어진 배치에 대해 테스트 프로필에 게재할 오퍼를 시뮬레이션할 수 있습니다. 이를 통해 자격 제한 및 등급 알고리즘 등 의사 결정 논리를 프로덕션에 적용하기 전에 쉽게 확인할 수 있습니다. 이 기능을 통해 기술 전문가 및 비전문가 사용자가 의사 결정 관리를 신속하게 테스트하고 잠재적 문제를 해결할 수 있습니다.</p>
<p>자세한 내용은 <a href="../offers/offer-activities/simulation.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>의사 결정 관리 - 오퍼 개인화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Experience Platform 프로필 속성 및 대상자를 사용하여 오퍼의 콘텐츠를 개인화할 수 있습니다. Journey Optimizer UI 전체에서 찾을 수 있는 동일한 표현식 편집기 구성 요소를 사용하여 간단하게 작업이 가능합니다. </p>
<p>자세한 내용은 <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">세부 설명서</a>를 참고하십시오.</p>
</td>
</tr>
</tbody>
</table>


더 많은 변화에 대해 알아보려면 [Adobe Experience Platform 10월 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=ko){target="_blank"}도 참조하십시오.

### 개선 사항

**여정**

* **표현식 편집기** - 이제 고급 사용자는 여정 지도 작업에 함수를 사용할 수 있습니다. 이 기능은 구독 목록에 활용할 수 있습니다. 예를 들어 이제 대상자의 구독 목록에서 이메일 주소를 가져올 수 있습니다. [이 샘플에서 자세히 알아보기](../building-journeys/message-to-subscribers-uc.md)

* **모니터링** - 실시간 여정 및 테스트 모드에 대한 단계 이벤트를 개선했습니다. 프로필 내보내기 작업과 관련하여 [새 필드](../reports/sharing-field-list.md#serviceevents)를 추가했습니다. 더 나은 사용자 경험을 위해 단계 이벤트 필드를 이제 다른 카테고리로 정리합니다. 이전 단계 이벤트 필드는 [stepEvents](../reports/sharing-legacy-fields.md) 카테고리에서 계속 사용할 수 있습니다.
* **접근성** - 여정의 접근성을 개선했습니다.
* **컬렉션** - 이제 하위 개체가 포함된 개체 배열이 지원됩니다. [자세히 보기](../building-journeys/collections.md)
* **목록** - 여정, 이벤트, 작업, 데이터 소스의 목록 화면을 개선했습니다.

**보고**

* **글로벌 보기의 데이터 형식** - 이제 **글로벌 보기**(**실행** 탭 내)에서 숫자와 백분율 간을 전환할 수 있습니다.


**관리**

* **메시지 사전 설정 편집** - 이제 메시지 사전 설정을 편집하고 업데이트 상태를 모니터링할 수 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md#edit-channel-surface)
* **PTR 레코드 편집** - 이제 PTR 레코드를 편집하고 업데이트 상태를 모니터링할 수 있습니다. [자세히 알아보기](../configuration/ptr-records.md#edit-ptr-record)

**개인화**

* **날짜 형식에 대한 새 도우미 함수** - 이제 날짜 문자열을 표시하는 방식을 지정할 수 있습니다. [자세히 알아보기](../personalization/functions/dates.md#format-date)


**의사 결정 관리**

* **평가 순서 지정** - 새롭고 개선된 의사 결정 만들기 플로우를 통해 의사 결정 객체 간을 보다 원활하게 탐색할 수 있을 뿐만 아니라 의사 결정 엔진에서 오퍼 컬렉션을 평가하는 방식을 완벽하게 제어할 수 있습니다. 제어할 수 있는 옵션에는 함께 평가할 컬렉션, 별도로 평가할 컬렉션, 컬렉션을 평가할 순서 등이 있습니다. [자세히 알아보기](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 문제 해결

* 브라우저 언어가 영어가 아닐 때 [여정 목록], [메시지 목록] 및 [이메일 디자이너]가 표시되지 않는 문제를 해결했습니다.
* [이메일 디자이너]에서 표현식을 사용하여 개인화를 추가할 때 발생하는, 문자가 잘못 이스케이프 처리되는 구문 오류를 수정했습니다.
* **관리** 메뉴를 탐색할 때 404 오류가 발생하는 문제를 해결했습니다.
* 비즈니스 이벤트를 사용하여 여정을 테스트할 때 다른 라이브 여정을 트리거하는 문제를 해결했습니다.


## 2021년 9월 릴리스 {#september-2021-release}

### 새로운 기능

<table>
<thead>
<tr>

<th><strong>보고 - 타겟팅한 대상자에 대한 인사이트 개선</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>보고에서 새 지표를 사용할 수 있습니다. 이메일 및 푸시 메시지에 대한 [타겟팅] 및 [제외]가 실시간 보고서와 글로벌 보고서 모두에 표시됩니다. </br> 최신 지표에 액세스하려면 각 채널 및 보고 유형에 대해 서로 다른 보고 대시보드를 재설정해야 합니다. 대시보드 사용자 지정에 대한 자세한 내용은 <a href="../reports/live-report.md">자세한 설명서</a>를 참조하세요.</p>
<p>각 메시지 실행에 대해 타겟팅한 프로필 수가 표시되는 열이 메시지 실행 목록에 새로 생겼습니다. </p>
<p>자세한 내용은 <a href="../reports/global-report.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>사용자 지정 작업으로 데이터 목록을 동적으로 보내기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 지정 작업 매개 변수에 컬렉션이나 데이터 목록을 전달할 수 있으며 그 내용은 실시간으로, 동적으로 채워집니다. 지원되는 컬렉션은 단순 컬렉션과 개체 컬렉션, 두 가지입니다. 이전에 만든 사용자 지정 작업은 계속 작동합니다. </p>
<p>컬렉션에 대한 자세한 내용은 <a href="../building-journeys/collections.md">자세한 설명서</a>를 참조하세요. </p>
<p>고급 표현식 편집기에서 사용할 수 있는 함수 목록에 필터링 및 교차 함수가 추가되었습니다. 이 함수를 통해 컬렉션을 더욱 다양하게 필터링 및 비교할 수 있습니다.</p>
<p><a href="../building-journeys/functions/functionfilter.md">필터링</a> 및 <a href="../building-journeys/functions/functionintersect.md">교차</a> 함수에 대한 설명서를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 단계 이벤트를 프로비전하는 동안 시스템에서 생성한 스키마 및 데이터 세트가 이제 읽기 전용 모드로 변경됩니다. 이를 통해 중요한 스키마를 실수로 수정하는 것을 방지할 수 있습니다. [자세히 알아보기](../reports/sharing-overview.md)
* **대기** 활동에 레이블을 지정하면 캔버스에 명확하게 표시됩니다. 이 레이블은 보고 및 테스트 모드 로그에서 수행할 작업을 정확하게 확인하는 데에도 사용됩니다. [자세히 알아보기](../building-journeys/about-journey-activities.md#best-practices)
* 검색 사용 시 **이벤트** 및 **작업** 카테고리로 요소를 필터링하여 이벤트 및 작업을 보다 신속하게 찾을 수 있습니다. 오케스트레이션 활동은 더 이상 필터링되지 않습니다. [자세히 알아보기](../building-journeys/using-the-journey-designer.md)
* 이제 규칙 기반 또는 비즈니스 이벤트에서 이벤트 ID 조건을 정의할 때 문자열 유형 필드에 &quot;포함&quot; 연산자를 사용할 수 있습니다. [자세히 알아보기](../event/about-creating.md)

**이메일 구성**

* 이제 IP 풀이 메시지 사전 설정과 연결되어 편집할 수 있습니다. 업데이트는 실시간 동기화되지 않습니다. 각 IP 풀의 업데이트 상태를 확인할 수도 있습니다. [자세히 알아보기](../configuration/ip-pools.md#edit-ip-pool)


## 2021년 8월 릴리스 {#august-2021-release}

### 새로운 기능

<table>
<thead>
<tr>

<th><strong>최적의 시간에 메시지 보내기 - 전송 시간 최적화</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer를 사용하여 모든 고객에게 최적의 시간에 푸시 또는 이메일을 자동으로 보냅니다. Adobe의 AI 서비스를 기반으로 하는 [전송 시간 최적화]는 기존의 오픈 및 클릭률 기록을 기반으로 참여를 극대화하기 위해 이메일 또는 푸시 메시지를 보내기 가장 적합한 시간을 예측합니다.</p>
<p>이 기능은 현재 beta 버전으로 beta 고객에게만 제공됩니다. beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주세요.</p>
<p>자세한 내용은 <a href="../building-journeys/journeys-message.md#send-time-optimization">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>비즈니스 이벤트에 스키마 관계 활용 - 룩업 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 비즈니스 이벤트를 구성할 때 스키마 간의 관계를 활용할 수 있습니다. 이는 단일 이벤트를 구성할 때, 여정에 조건을 사용할 때, 메시지 개인화 시, 사용자 지정 작업 개인화 시 연결된 테이블의 필드를 활용하는 기능도 함께 추가됩니다.</p>
<p>자세한 내용은 <a href="../event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>개인화된 URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>개인화된 URL은 프로필 속성에 따라 수신자를 웹사이트의 특정 페이지 또는 개인화된 마이크로사이트로 이동합니다. 이제 Adobe Journey Optimizer에서 메시지 콘텐츠의 URL에 개인화를 추가할 수 있습니다. URL 개인화는 텍스트 및 이미지에 적용할 수 있으며, 프로필 데이터 또는 컨텍스트 데이터를 사용합니다.</p>
<p>자세한 내용은 <a href="../personalization/personalization-syntax.md#perso-urls">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일이 사용자에게 전달되도록 - 이메일 다시 시도</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>더 이상 필요하지 않을 때 다시 시도가 더 이상 수행되지 않도록 이제 각 사전 설정을 기준으로 다시 시도 기간을 정의할 수 있습니다. 예를 들어, 하루 동안만 유효한 링크가 포함된 암호 재설정 트랜잭션 메시지에 대해 다시 시도 기간을 24시간으로 설정할 수 있습니다. 다시 시도 설정은 이메일 채널에만 적용됩니다.</p>
<p>자세한 내용은 <a href="../configuration/retries.md#retry-duration">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>전송에서 제외할 주소 정의 - 금지 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 인터페이스에서 하나씩 또는 CSV 파일 업로드를 통해 일괄 모드로 이메일 주소와 도메인을 금지 목록에 추가할 수 있습니다.</p>
<p>자세한 내용은 <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


### 개선 사항

**여정**

* **동적 헤더** - 이제 HTTP 헤더 매개 변수에서 동적 데이터를 전달할 수 있습니다. 이러한 매개 변수는 여정 작업 HTTP 호출(예: 타임스탬프 또는 추적 ID)을 수신하는 통합 시스템에서 사용할 수 있습니다. [자세히 알아보기](../action/about-custom-action-configuration.md#url-configuration)
* **동적 URL 경로** - 이제 사용자 지정 작업에 대해 동적 URL 경로를 설정할 수 있습니다. [자세히 알아보기](../action/about-custom-action-configuration.md#url-configuration)
* 대상자 읽기의 전체 스로틀링 수가 초당 메시지 17,000개에서 20,000개로 변경되었습니다. [자세히 알아보기](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**사용자 인터페이스**

* **검색** - 이제 모든 페이지에서 통합 Experience Cloud 검색 필드를 통해 직접 비즈니스 개체 및 도움말을 검색할 수 있습니다. [자세히 알아보기](../start/user-interface.md#unified-search)
* **최근 항목** - 이제 Adobe Journey Optimizer 홈페이지에서 최근 항목 요소에 표시할 대상에 비즈니스 개체를 추가하여 확장했습니다. 이 업데이트 이후에는 최근 액세스 항목에 [메시지], [여정], [대상자], [스키마], [데이터세트], [데이터 소스], [이벤트], [작업], [소스], [대상]이 포함됩니다. [자세히 알아보기](../action/about-custom-action-configuration.md#passing-collection)

**콘텐츠 디자인**

* **배경** - 이제 배경 이미지가 실시간 미리 보기에서 지원됩니다. [자세히 알아보기](../content-management/preview-test.md)
  <!--* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)-->

**개인화**

* **표현식 편집기** - 이제 개인화를 정의할 때 대체 값을 쉽게 추가할 수 있습니다. 프로필에 대한 개인화 필드가 비어 있으면 대체 값이 표시됩니다. [자세히 알아보기](../personalization/functions/helpers.md)

**이메일 구성**

* **허용 목록** - 이제 API 호출을 통해 비프로덕션 샌드박스에서 허용 목록을 활성화 및 비활성화할 수 있습니다. [자세히 알아보기](../configuration/allow-list.md#enable-allow-list)
* **탐색** - **관리 > 채널 > 이메일 설정 > 일반** 메뉴 아래에서 액세스할 수 있었던 금지 목록이 이제 새로운 **금지 목록** 하위 메뉴로 옮겨졌습니다. 해당 하위 메뉴 아래에 모든 관련 기능을 모아 두어 보다 쉽게 액세스할 수 있습니다. [자세히 알아보기](../configuration/manage-suppression-list.md#access-suppression-list)

**의사 결정 관리**

* 사용자 경험 개선을 위해 오퍼를 만들 때 표를 추가 및 구성하는 방식을 업데이트했습니다. 특히 [자산] 라이브러리는 이제 표에 대한 이미지 유형 컨텐츠를 정의할 때만 표시됩니다. [자세히 알아보기](../offers/offer-library/creating-personalized-offers.md#representations)

### 문제 해결

* 메시지 탭 탐색에서 접근성 문제를 해결했습니다.
* 이메일 디자이너 레이블의 현지화 문제를 해결했습니다.
* 여정에서 두 개 이상의 노드를 선택하고 속성 창에서 [삭제]를 클릭할 때 발생하는 문제를 해결했습니다.
* 여정에 사용한 작업에 새 헤더를 추가할 수 없는 문제를 해결했습니다.
* 이제 사용자 인터페이스에서 보다 명확한 경고를 통해 메시지 사전 설정을 만들지 못한 이유를 확인할 수 있습니다.


## 2021년 7월 릴리스 {#july-2021-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>메시지에 메타데이터 사용하기 - 룩업 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에 로드한 참조 데이터를 사용하여 경험을 강화할 수 있습니다. 예를 들면 경험 이벤트에서 예약 ID의 메타데이터를 조회하거나, 캔버스에서 사용할 경험 이벤트에서 sku의 제품 정보를 찾는 작업이 있습니다. </p>
<p>이제 스키마 간의 관계를 활용하여 하나의 데이터 세트를 다른 데이터 세트에 대한 룩업 테이블로 사용할 수 있습니다. 그런 다음 단일 이벤트를 구성할 때, 여정에 조건을 사용할 때, 메시지 개인화 시, 사용자 지정 작업 개인화 시 연결된 테이블의 필드를 활용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>허용 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 테스트 목적으로 안전한 환경을 갖도록 샌드박스 수준에서 특정 전송 안전 목록을 정의할 수 있습니다. 실수가 발생할 수 있는 비프로덕션 인스턴스에서 허용 목록을 사용하면 고객에게 원치 않는 메시지를 보낼 위험이 없습니다. 이 기능은 제외 API를 통해 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../configuration/allow-list.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 동일한 샌드박스에서 동시에 실행하는 모든 대상자 읽기의 전체 스로틀링 수는 초당 17,000개의 메시지로 제한됩니다. [자세히 보기](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* **캐시 기간** 필드가 데이터 소스 구성 창에서 제거되었습니다. [자세히 보기](../datasource/about-data-sources.md)
* 이제 외부 데이터 소스의 경우 초당 최대 15회 호출할 수 있는 가용량 규칙이 자동으로 정의됩니다. [자세히 보기](../configuration/external-systems.md#capping)
* 이제 실시간 여정의 여정 속성 화면에 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다. [자세히 보기](../building-journeys/journey-gs.md#change-properties)
* 여정 목록 화면에 여정 유형 필터를 추가했습니다. [자세히 보기](../start/user-interface.md#filter-lists)
* [대상자 읽기] 활동에 **[!UICONTROL 스로틀링 수]** 매개변수를 추가했습니다. [자세히 보기](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**미리 보기 및 테스트**

* 이제 신원과 네임스페이스가 **[!UICONTROL 미리보기]** 화면에 표시됩니다. [자세히 보기](../content-management/preview-test.md#preview-your-messages)
* 이제 교정용 테스트 이메일 수가 10개로 제한됩니다.
* 교정을 보낼 때 **제목 줄 접두사**&#x200B;에 사용할 수 있는 문자가 제한됩니다. [자세히 보기](../content-management/preview-test.md#send-proofs)

**개인화 표현식 편집기**

* 도우미 드롭다운 목록의 이름과 순서를 변경했습니다.

### 문제 해결

* 일괄 이메일 게재 시 중복 메시지를 게재하는 문제를 해결했습니다.
* 이제 다시 시도 기간이 끝나고 이메일 전송을 수행하지 않을 때 그에 따라 이벤트가 생성됩니다.
* [PTR 레코드] 화면에서 IP 정보가 누락되는 문제를 해결했습니다.
* 이제 [표현식 편집기] 내 오퍼 레일의 지역화가 구현되었습니다.
* 정보 팝업의 간격이 잘못 설정된 문제를 해결했습니다.
* [이메일 디자이너]에서 HTML 파일을 업로드할 때 `background-image` 속성이 있는 내부 스타일 시트를 지원하지 않는 문제를 해결했습니다.
