---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5e93ccee2056814c25531fc13c3cd433a19077a6
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 16%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 [최신 설명서 업데이트](documentation-updates.md).

## 2021년 10월 릴리스 {#oct-2021-release}

<!--table>
<thead>
<tr>
<th><strong>Journeys - Target users in a subscription list</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger a journey targeting a subscription list. To perform this: add a Read segment activity followed by a message, and in the message email settings, define an expression that will fetch the subscriber email address from the profile, for the targeted subscription list. The expression editor has been enhanced to allow you to to select the first entry key of a map.</p>
<p>Learn more in the <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">detailed documentation</a>.</p>>
</td>
</tr>
</tbody>
</table-->



<!--table>
<thead>
<tr>
<th><strong>Journeys - Profile cap condition</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>When using a <strong>Condition</strong> activity in a journey, you can now define a <strong>Profile cap</strong> condition. This new condition type allows you set a maximum number of profiles for a journey path. When this limit is reached, the selected profiles take a second path. This allows you to optimize your IP ramp up. For example, you may want to ramp up your deliveries on a domain to 50 millions by splitting the execution: send 1000 messages on day 1, 2000 on day 2, etc.</p>
<p>For more information, refer to the <a href="building-journeys/condition-activity.md#profile_cap">detailed documentation</a> and related <a href="building-journeys/ramp-up-deliveries-uc.md">sample use case</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>의사 결정 관리 - 오퍼 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer UI에서 주어진 배치를 위해 테스트 프로필에 전달되는 오퍼를 시뮬레이션할 수 있습니다. 이를 통해 자격 제한 및 등급 알고리즘을 포함하여 의사 결정 논리를 프로덕션에 적용하기 전에 쉽게 확인할 수 있습니다. 이 기능을 통해 기술 및 기술 전문가가 아닌 사용자는 offer decisioning을 신속하게 테스트하고 잠재적 문제를 해결할 수 있습니다.</p>
<p>자세한 내용은 <a href="offers/offer-activities/simulation.md">자세한 설명서</a>를 참조하세요.</p>
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
<p>이제 Journey Optimizer UI 전체에서 발견되는 동일한 표현식 편집기 구성 요소를 사용하여 Adobe Experience Platform 프로필 속성 및 세그먼트를 사용하여 오퍼의 콘텐츠를 개인화할 수 있습니다. </p>
<p>자세한 내용은 <a href="offers/offer-library/creating-personalized-offers.md#custom-text">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


참조 - [Adobe Experience Platform 10월 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;} 을 참조하십시오.

### 개선 사항

**여정**

* **표현식 편집기** - 이제 고급 사용자로서 기능을 사용하여 지도를 사용할 수 있습니다. 이 기능은 구독 목록에서 활용할 수 있습니다. 예를 들어 세그먼트에서 이제 구독 목록에서 이메일 주소를 가져올 수 있습니다. [자세한 내용은 이 샘플을 참조하십시오](building-journeys/message-to-subscribers-uc.md)

   <!-- * **Delta on segments** - When using a **Read segment** activity, you can now target the individuals who entered or exited a specific segment since the last execution.  -->
* **모니터링** - 라이브 여정 및 테스트 모드에 대한 단계 이벤트가 향상되었습니다. [새 필드](reports/sharing-field-list.md#serviceevents) 프로필 내보내기 작업과 관련하여 가 추가되었습니다. 더 나은 사용자 경험을 위해 이제 단계 이벤트 필드를 다른 카테고리로 구성합니다. 이전 단계 이벤트 필드는 여전히 [stepEvents](reports/sharing-legacy-fields.md) 카테고리.
* **접근성** - 여정에서 액세스 가능성이 개선되었습니다.
* **컬렉션** - 이제 하위 개체가 포함된 개체 배열이 지원됩니다. [자세히 보기](building-journeys/collections.md)
* **목록** - 여정, 이벤트, 작업, 데이터 소스에 대해 목록 화면이 개선되었습니다.

**보고**

* **글로벌 보기의 데이터 형식** - 이제 에서 숫자와 백분율 간을 전환할 수 있습니다 **전역 보기** 의 **실행** 탭. [자세히 알아보기](message-monitoring.md)

<!--* **New metrics** - New metrics and widgets are now available in **Live** and **Global** reports to measure your offers' impact on recipients. [Learn more](reports/journey-global-report.md)-->

**관리**

* **메시지 사전 설정 편집** - 이제 메시지 사전 설정을 편집하고 업데이트 상태를 모니터링할 수 있습니다. [자세히 알아보기](configuration/message-presets.md#edit-message-preset)
* **PTR 레코드 편집** - 이제 PTR 레코드를 편집하고 업데이트 상태를 모니터링할 수 있습니다. [자세히 알아보기](configuration/ptr-records.md#edit-ptr-record)

**개인화**

* **날짜 형식에 대한 새 도우미 함수** - 이제 날짜 문자열을 표시하는 방법을 지정할 수 있습니다. [자세히 알아보기](personalization/functions/dates.md#format-date)

**의사 결정 관리**

* **평가 순서 지정** - 새롭고 향상된 의사 결정 생성 플로우를 통해 의사 결정 객체 간을 보다 원활하게 탐색할 수 있을 뿐만 아니라 의사 결정 엔진에서 오퍼 컬렉션을 평가하는 방법을 완벽하게 제어할 수 있습니다. 여기에는 함께 평가되는 컬렉션과 별도로 평가되는 컬렉션과, 컬렉션을 평가해야 하는 순서가 포함됩니다. [자세히 알아보기](offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 수정 사항

* 브라우저 언어가 영어가 아닐 때 여정 목록, 메시지 목록 및 이메일 디자이너가 표시되지 않는 문제를 수정했습니다.
* 이메일 디자이너에서 표현식을 사용하여 개인화를 추가할 때 발생하는 구문 오류를 수정했습니다. 등장인물들은 잘못 탈출했다.
* 에서 탐색할 때 404 오류가 발생하는 문제를 수정했습니다 **관리** 메뉴 아래의 제품에서 사용할 수 있습니다.
* 비즈니스 이벤트를 사용하여 여정을 테스트할 때 다른 라이브 여정을 트리거하는 문제를 수정했습니다.

## 2021년 9월 릴리스 {#september-2021-release}

### 새로운 기능

<table>
<thead>
<tr>

<th><strong>보고 - 타깃팅된 대상에 대한 통찰력 향상</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>새 지표는 보고에서 사용할 수 있습니다. 이메일 및 푸시 메시지에 대한 타깃팅됨 및 제외는 라이브 보고서와 글로벌 보고서 모두에 표시됩니다. </br> 최신 지표에 액세스하려면 각 채널 및 보고 유형에 대해 서로 다른 보고 대시보드를 재설정해야 합니다. 대시보드 사용자 지정에 대한 자세한 내용은 <a href="reports/live-report.md">자세한 설명서</a></p>
<p>메시지 실행 목록의 새 열에는 각 메시지 실행에 대한 타겟팅된 프로필 수가 표시됩니다. </p>
<p>자세한 내용은 <a href="message-monitoring.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>사용자 지정 작업을 사용하여 동적으로 데이터 목록 전달</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 런타임 시 동적으로 채워지는 사용자 지정 작업 매개 변수에 컬렉션이나 데이터 목록을 전달할 수 있습니다. 지원되는 컬렉션은 두 가지입니다. 간단한 컬렉션 및 개체 컬렉션. 이전에 만든 사용자 지정 작업은 계속 작동합니다. </p>
<p>컬렉션에 대한 자세한 내용은 <a href="building-journeys/collections.md">세부 설명서</a>. </p>
<p>필터 및 교차 함수가 고급 표현식 편집기에서 사용할 수 있는 함수 목록에 추가되었습니다. 이 기능은 컬렉션 필터링 및 비교에 대한 더 많은 가능성을 제공합니다.</p>
<p>다음 항목에 대한 설명서를 참조하십시오. <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">필터</a> 및 <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">교차</a> 함수 위에 있어야 합니다.</p>
</td>
</tr>
</tbody>
</table>



### 개선 사항

**여정**

* 단계 이벤트를 프로비전하는 동안 생성된 시스템 생성 스키마 및 데이터 세트가 이제 읽기 전용 모드로 되어 중요한 스키마를 실수로 수정하는 것을 방지할 수 있습니다. [자세히 알아보기](reports/sharing-overview.md)
* 완전히 레이블 지정 **대기** 캔버스에 표시할 레이블이 있는 활동. 이 레이블은 보고 및 테스트 모드 로그에서 수행할 작업을 명확하게 식별하는 데에도 사용됩니다. [자세히 알아보기](building-journeys/about-journey-activities.md#best-practices)
* 에서 요소를 필터링하여 이벤트 및 작업을 보다 신속하게 찾을 수 있습니다. **이벤트** 및 **작업** 검색을 사용하는 카테고리. 오케스트레이션 활동은 더 이상 필터링되지 않습니다. [자세히 알아보기](building-journeys/using-the-journey-designer.md)
* 규칙 기반 또는 비즈니스 이벤트에서 이벤트 ID 조건을 정의할 때 이제 문자열 유형 필드에 &quot;포함&quot; 연산자를 사용할 수 있습니다. [자세히 알아보기](event/about-creating.md)

**이메일 구성**

* 이제 IP 풀이 메시지 사전 설정과 연결되면 편집할 수 있으므로 비동기적으로 업데이트됩니다. 각 IP 풀 업데이트 상태를 확인할 수도 있습니다. [자세히 알아보기](configuration/ip-pools.md#edit-ip-pool)

## 2021년 8월 릴리스 {#august-2021-release}

### 새로운 기능

<table>
<thead>
<tr>

<th><strong>최적의 시간에 메시지 전송 - 전송 시간 최적화</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer를 사용하는 모든 고객에게 최적의 시간에 푸시 또는 이메일을 자동으로 보냅니다. Adobe의 AI 서비스를 기반으로 하는 전송 시간 최적화는 이메일 또는 푸시 메시지를 보내는 가장 적합한 시간을 예측하여 이메일 또는 푸시 메시지를 전송함으로써 기존의 공개 및 클릭률 기록을 기반으로 참여를 극대화할 수 있습니다.</p>
<p>이 기능은 현재 베타 버전이며 베타 고객에게만 제공됩니다. 베타 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의하십시오.</p>
<p>자세한 내용은 <a href="building-journeys/journeys-message.md#send-time-optimization">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>비즈니스 이벤트에서 스키마 관계 활용 - 조회 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 비즈니스 이벤트를 구성할 때 스키마 간의 관계를 활용할 수 있습니다. 이는 단일 이벤트를 구성할 때, 여정에서 조건을 사용할 때, 메시지 개인화에서, 사용자 지정 작업 개인화에서 연결된 테이블의 필드를 활용하는 기능 외에 있습니다.</p>
<p>자세한 내용은 <a href="event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
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
<p>개인화된 URL은 프로필 속성에 따라 수신자를 웹 사이트의 특정 페이지 또는 개인화된 마이크로 사이트로 가져옵니다. 이제 Adobe Journey Optimizer에서 메시지 콘텐츠의 URL에 개인화를 추가할 수 있습니다. URL 개인화는 텍스트 및 이미지에 적용하고 프로필 데이터 또는 컨텍스트 데이터를 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="personalization/personalization-syntax.md#perso-urls">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일이 사용자에게 전달되는지 확인합니다. - 이메일 다시 시도</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>더 이상 필요하지 않을 때 다시 시도가 더 이상 수행되지 않도록 이제 각 사전 설정을 기준으로 다시 시도 기간을 정의할 수 있습니다. 예를 들어, 하루 동안만 유효한 링크가 포함된 암호 재설정 트랜잭션 메시지에 대해 재시도 기간을 24시간으로 설정할 수 있습니다. 다시 시도 설정은 전자 메일 채널에만 적용됩니다.</p>
<p>자세한 내용은 <a href="configuration/retries.md#retry-duration">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>전송에서 제외할 주소 정의 - 제외 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 인터페이스에서 하나씩 또는 CSV 파일 업로드를 통해 일괄 모드로 이메일 주소와 도메인을 제외 목록에 추가할 수 있습니다.</p>
<p>자세한 내용은 <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### 개선 사항

**여정**

* **동적 머리글** - 이제 HTTP 헤더 매개 변수에 동적 데이터를 전달할 수 있습니다. 이러한 매개 변수는 여정 작업 HTTP 호출(예: 타임스탬프 또는 추적 ID)을 수신하는 통합 시스템에서 사용할 수 있습니다. [자세히 알아보기](action/about-custom-action-configuration.md#url-configuration)
* **동적 URL 경로** - 이제 사용자 지정 작업에 대한 동적 URL 경로를 설정할 수 있습니다. [자세히 알아보기](action/about-custom-action-configuration.md#url-configuration)
* 읽기 세그먼트의 전체 전송률이 초당 17,000개에서 20,000개로 변경되었습니다. [자세히 알아보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**사용자 인터페이스**

* **검색** - 이제 모든 페이지에서 통합 Experience Cloud 검색 필드에서 직접 비즈니스 개체를 검색하고 도움말을 제공할 수 있습니다. [자세히 알아보기](user-interface.md#unified-search)
* **최근 항목** - 이제 Adobe Journey Optimizer 홈페이지에서 최근 요소 표시가 추가 비즈니스 개체로 확장되었습니다. 이 업데이트를 사용하면 최근에 액세스한 항목에 메시지, 여정, 세그먼트, 스키마, 데이터 세트, 데이터 소스, 이벤트, 작업, 소스 및 대상이 포함됩니다. [자세히 알아보기](action/about-custom-action-configuration.md#passing-collection)

**컨텐츠 디자인**

* **배경** - 이제 배경 이미지가 라이브 미리 보기에서 지원됩니다. [자세히 알아보기](preview.md)
* **옵트아웃 링크를 한 번 클릭** - 이메일 콘텐츠에 새로운 유형의 링크를 삽입할 수 있습니다. a **옵트아웃** 링크를 사용하면 옵트아웃을 확인하기 위해 랜딩 페이지로 리디렉션되지 않고 한 번의 클릭으로 커뮤니케이션으로부터 구독을 취소할 수 있습니다. [자세히 알아보기](message-tracking.md#one-click-opt-out-link)

**개인화**

* **표현식 편집기** - 이제 개인화를 정의할 때 폴백 값을 쉽게 추가할 수 있습니다. 프로필에 대한 개인화 필드가 비어 있으면 폴백 값이 표시됩니다. [자세히 알아보기](personalization/functions/helpers.md)

**이메일 구성**

* **허용 목록** - 이제 API 호출을 통해 비프로덕션 샌드박스에서 허용 목록을 활성화하고 비활성화할 수 있습니다. [자세히 알아보기](allow-list.md#enable-allow-list)
* **탐색** - 아래에 액세스할 수 있었던 제외 목록 **관리 > 채널 > 이메일 구성 > 일반** 메뉴, 새 페이지로 이동되었습니다. **제외 목록** 하위 메뉴로서, 모든 관련 기능을 수집하여 보다 쉽게 액세스할 수 있습니다. [자세히 알아보기](configuration/manage-suppression-list.md#access-suppression-list)

**의사 결정 관리**

* 오퍼를 만들 때 표를 추가 및 구성하는 방법이 업데이트되어 사용자 경험이 향상되었습니다. 특히 이제 표에 대한 이미지 유형 컨텐츠를 정의할 때만 자산 라이브러리가 표시됩니다. [자세히 알아보기](offers/offer-library/creating-personalized-offers.md#representations)

### 수정 사항

* 메시지 탭 탐색에서 액세스 가능성 문제가 해결되었습니다.
* 이메일 디자이너 레이블의 현지화 문제를 수정했습니다.
* 여정에서 두 개 이상의 노드를 선택하고 속성 패널에서 &#39;삭제&#39;를 클릭할 때 발생하는 문제를 수정했습니다.
* 여정에 사용된 작업에 새 헤더를 추가할 수 없는 문제를 수정했습니다.
* 이제 사용자 인터페이스에서 보다 명시적 경고를 통해 메시지 사전 설정을 만들지 못한 이유를 확인할 수 있습니다.


## 2021년 7월 릴리스 {#july-2021-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>메시지에서 메타데이터 사용 - 조회 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에 로드한 참조 데이터를 사용하여 경험을 보강합니다. 예로는 경험 이벤트에서 예약 ID에서 메타데이터를 조회하거나, 캔버스에서 사용할 경험 이벤트에서 sku의 제품 정보를 찾는 작업이 있습니다. </p>
<p>이제 스키마 간의 관계를 활용하여 하나의 데이터 세트를 다른 데이터 세트에 대한 조회 테이블로 사용할 수 있습니다. 그런 다음 단일 이벤트를 구성할 때, 여정에서 조건을 사용할 때, 메시지 개인화에서, 사용자 지정 작업 개인화에서 연결된 테이블의 모든 필드를 활용할 수 있습니다.</p>
<p>자세한 내용은 <a href="event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
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
<p>이제 테스트 목적으로 안전한 환경을 갖도록 샌드박스 수준에서 특정 전송 안전 목록을 정의할 수 있습니다. 허용 목록이 실수가 발생할 수 있는 비프로덕션 인스턴스에서 고객에게 원치 않는 메시지를 보낼 위험이 없습니다. 이 기능은 억제 API를 활용하여 활성화됩니다.</p>
<p>자세한 내용은 <a href="allow-list.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 동일한 샌드박스에서 동시에 실행되는 모든 읽기 세그먼트의 전체 전송률은 초당 17,000개의 메시지로 제한됩니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 다음 **캐시 기간** 필드가 데이터 소스 구성 창에서 제거되었습니다. [자세히 보기](datasource/about-data-sources.md)
* 이제 외부 데이터 소스의 경우 초당 15개의 호출의 최대 가용량 규칙이 자동으로 정의됩니다. [자세히 보기](configuration/external-systems.md#capping)
* 이제 라이브 여정의 경우 여정 속성 화면에 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다. [자세히 보기](building-journeys/journey-gs.md#change-properties)
* 여정 목록 화면에서 여정 유형 필터가 추가되었습니다. [자세히 보기](user-interface.md#section_lgm_hpz_pgb)
* 다음 **[!UICONTROL Throttling rate]** 세그먼트 읽기 활동에 매개 변수가 추가되었습니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**메시지 미리 보기 및 테스트**

* 이제 ID와 네임스페이스가 **[!UICONTROL Preview]** 화면. [자세히 보기](preview.md#preview-your-messages)
* 이제 증명을 위한 테스트 전자 메일 수가 10개로 제한됩니다.
* 에 사용할 수 있는 문자 **제목 줄 접두사** 이제 증명을 사용할 수 없습니다. [자세히 보기](preview.md#send-proofs)

**개인화 표현식 편집기**

* 도우미 드롭다운 목록의 이름이 변경되고 순서가 변경되었습니다.

### 수정 사항

* 배치 이메일 게재에 대해 중복 메시지가 전달되는 문제를 해결했습니다.
* 이제 다시 시도 기간이 끝나면 이메일 전송이 수행되지 않을 때 그에 따라 이벤트가 생성됩니다.
* PTR Records 화면에서 IP 정보가 누락되는 문제를 해결했습니다.
* 이제 표현식 편집기 내의 오퍼 레일의 현지화가 구현되었습니다.
* 정보 팝업에서 잘못된 간격이 수정되었습니다.
* 내부 스타일 시트가 있는 HTML 파일을 업로드할 때 이메일 디자이너의 문제가 해결되었습니다. `background-image` 속성이 지원되지 않습니다.
